---
title: "async (Riferimenti per C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
f1_keywords: 
  - "async_CSharpKeyword"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "async [C#]"
  - "async (parola chiave) [C#]"
  - "async (metodo) [C#]"
ms.assetid: 16f14f09-b2ce-42c7-a875-e4eca5d50674
caps.latest.revision: 52
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 52
---
# async (Riferimenti per C#)
Utilizzare il modificatore `async` per specificare che un metodo, un'[espressione lambda](../../../csharp/programming-guide/statements-expressions-operators/lambda-expressions.md) o un [metodo anonimo](../../../csharp/programming-guide/statements-expressions-operators/anonymous-methods.md) è asincrono.  Se questo modificatore viene utilizzato in un metodo o in un'espressione, viene indicato come metodo asincrono.  
  
```c#  
public async Task<int> ExampleMethodAsync()  
{  
    // . . . .  
}  
  
```  
  
 Se non si ha esperienza di programmazione asincrona o non si comprende in che modo un metodo asincrono utilizza la parola chiave `await` per eseguire attività potenzialmente prolungate senza bloccare il thread del chiamante, è consigliabile leggere l'introduzione in [Programmazione asincrona con Async e Await](../Topic/Asynchronous%20Programming%20with%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md).  
  
```  
string contents = await contentsTask;  
```  
  
 Il metodo viene eseguito in modo sincrono finché non raggiunge la prima espressione `await`, a quel punto il metodo viene sospeso fino al completamento dell'attività attesa.  Nel frattempo il controllo torna al chiamante del metodo, come illustrato nell'esempio della sezione successiva.  
  
 Il metodo modificato dalla parola chiave `async` viene eseguito in modo sincrono se non contiene un'espressione o un'istruzione `await`.  Un avviso del compilatore segnala eventuali metodi asincroni che non contengono `await` perché questa situazione potrebbe indicare un errore.  Vedere [Avviso del compilatore \(livello 1\) CS4014](../../../csharp/language-reference/compiler-messages/cs4014.md).  
  
 La parola chiave `async` è contestuale, in quanto è una parola chiave solo quando modifica un metodo, un'espressione lambda o un metodo anonimo.  In tutti gli altri contesti, viene interpretato come identificatore.  
  
## Esempio  
 Nell'esempio seguente vengono illustrati la struttura e il flusso di controllo tra un gestore eventi asincrono, `StartButton_Click`, e un metodo asincrono, `ExampleMethodAsync`.  Il risultato ottenuto dal metodo asincrono è la lunghezza di un sito Web scaricato.  Il codice è adatto per un'applicazione Windows Presentation Foundation \(WPF\) o un'app di Windows Store creata in [!INCLUDE[vs_dev12](../../../csharp/getting-started/includes/vs-dev12-md.md)]; vedere i commenti del codice per l'installazione dell'applicazione.  
  
```c#  
// You can run this code in Visual Studio 2013 as a WPF app or a Windows Store app.  
// You need a button (StartButton) and a textbox (ResultsTextBox).  
// Remember to set the names and handler so that you have something like this:  
// <Button Content="Button" HorizontalAlignment="Left" Margin="88,77,0,0" VerticalAlignment="Top" Width="75"  
//         Click="StartButton_Click" Name="StartButton"/>  
// <TextBox HorizontalAlignment="Left" Height="137" Margin="88,140,0,0" TextWrapping="Wrap"   
//          Text="TextBox" VerticalAlignment="Top" Width="310" Name="ResultsTextBox"/>  
  
// To run the code as a WPF app:  
//    paste this code into the MainWindow class in MainWindow.xaml.cs,  
//    add a reference to System.Net.Http, and  
//    add a using directive for System.Net.Http.  
  
// To run the code as a Windows Store app:  
//    paste this code into the MainPage class in MainPage.xaml.cs, and  
//    add using directives for System.Net.Http and System.Threading.Tasks.  
  
private async void StartButton_Click(object sender, RoutedEventArgs e)  
{  
    // ExampleMethodAsync returns a Task<int>, which means that the method  
    // eventually produces an int result. However, ExampleMethodAsync returns  
    // the Task<int> value as soon as it reaches an await.  
    ResultsTextBox.Text += "\n";  
    try  
    {  
        int length = await ExampleMethodAsync();  
        // Note that you could put "await ExampleMethodAsync()" in the next line where  
        // "length" is, but due to when '+=' fetches the value of ResultsTextBox, you  
        // would not see the global side effect of ExampleMethodAsync setting the text.  
        ResultsTextBox.Text += String.Format("Length: {0}\n", length);  
    }  
    catch (Exception)  
    {  
        // Process the exception if one occurs.  
    }  
}  
  
public async Task<int> ExampleMethodAsync()  
{  
    var httpClient = new HttpClient();  
    int exampleInt = (await httpClient.GetStringAsync("http://msdn.microsoft.com")).Length;  
    ResultsTextBox.Text += "Preparing to finish ExampleMethodAsync.\n";  
    // After the following return statement, any method that's awaiting  
    // ExampleMethodAsync (in this case, StartButton_Click) can get the   
    // integer result.  
    return exampleInt;  
}  
// Output:  
// Preparing to finish ExampleMethodAsync.  
// Length: 53292  
  
```  
  
> [!IMPORTANT]
>  Per ulteriori informazioni sulle attività e sul codice eseguito in attesa di un'attività, vedere [Programmazione asincrona con Async e Await](../Topic/Asynchronous%20Programming%20with%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md).  Per un esempio completo di WPF in cui sono utilizzati elementi simili, vedere [Procedura dettagliata: accesso al Web tramite Async e Await](../Topic/Walkthrough:%20Accessing%20the%20Web%20by%20Using%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md).  È possibile scaricare il codice della procedura dettagliata dalla pagina degli [esempi di codice per gli sviluppatori](http://go.microsoft.com/fwlink/?LinkId=255191).  
  
## Tipi restituiti  
 Un metodo asincrono può avere un tipo restituito <xref:System.Threading.Tasks.Task>, <xref:System.Threading.Tasks.Task%601> o [void](../../../csharp/language-reference/keywords/void.md).  Il metodo non può dichiarare parametri [ref](../../../csharp/language-reference/keywords/ref.md) o [out](../../../csharp/language-reference/keywords/out.md), ma può chiamare metodi che hanno tali parametri.  
  
 Specificare `Task<TResult>` come tipo restituito di un metodo async se l'istruzione [return](../../../csharp/language-reference/keywords/return.md) del metodo specifica un operando di tipo `TResult`.  Utilizzare `Task` se non viene restituito alcun valore significativo al completamento del metodo.  Ciò significa che una chiamata al metodo restituisce `Task`, ma al completamento di `Task`, qualsiasi espressione `await` in attesa di `Task` restituisce `void`.  
  
 Utilizzare il tipo restituito `void` principalmente per definire gestori eventi, che richiedono tale tipo restituito.  Il chiamante di un metodo asincrono che restituisce `void` non può attendere il metodo e non può acquisire eccezioni generate dal metodo.  
  
 Per ulteriori informazioni ed esempi, vedere [Tipi restituiti asincroni](../Topic/Async%20Return%20Types%20\(C%23%20and%20Visual%20Basic\).md).  
  
## Vedere anche  
 <xref:System.Runtime.CompilerServices.AsyncStateMachineAttribute>   
 [await](../../../csharp/language-reference/keywords/await.md)   
 [Procedura dettagliata: accesso al Web tramite Async e Await](../Topic/Walkthrough:%20Accessing%20the%20Web%20by%20Using%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md)   
 [Programmazione asincrona con Async e Await](../Topic/Asynchronous%20Programming%20with%20Async%20and%20Await%20\(C%23%20and%20Visual%20Basic\).md)