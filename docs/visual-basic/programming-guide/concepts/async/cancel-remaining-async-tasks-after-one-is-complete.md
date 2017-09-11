---
title: "Annullare le attività asincrone rimanenti dopo che ne è completa (Visual Basic) | Documenti di Microsoft"
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
ms.assetid: c928b5a1-622f-4441-8baf-adca1dde197f
caps.latest.revision: 3
author: stevehoag
ms.author: shoag
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 1b70822edd972ac33614ab49faad6ff50b0e80b7
ms.contentlocale: it-it
ms.lasthandoff: 03/13/2017

---
# <a name="cancel-remaining-async-tasks-after-one-is-complete-visual-basic"></a><span data-ttu-id="0a971-102">Annullare le attività asincrone rimanenti dopo che ne è completa (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="0a971-102">Cancel Remaining Async Tasks after One Is Complete (Visual Basic)</span></span>
<span data-ttu-id="0a971-103">Tramite il <xref:System.Threading.Tasks.Task.WhenAny%2A?displayProperty=fullName>metodo insieme a un <xref:System.Threading.CancellationToken>, è possibile annullare tutte le attività rimanenti quando un'attività è stata completata.</xref:System.Threading.CancellationToken> </xref:System.Threading.Tasks.Task.WhenAny%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="0a971-103">By using the <xref:System.Threading.Tasks.Task.WhenAny%2A?displayProperty=fullName> method together with a <xref:System.Threading.CancellationToken>, you can cancel all remaining tasks when one task is complete.</span></span> <span data-ttu-id="0a971-104">Il `WhenAny` metodo accetta un argomento che rappresenta una raccolta di attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-104">The `WhenAny` method takes an argument that’s a collection of tasks.</span></span> <span data-ttu-id="0a971-105">Il metodo avvia tutte le attività e restituisce una singola attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-105">The method starts all the tasks and returns a single task.</span></span> <span data-ttu-id="0a971-106">La singola operazione è completa quando un'attività nella raccolta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0a971-106">The single task is complete when any task in the collection is complete.</span></span>  
  
 <span data-ttu-id="0a971-107">In questo esempio viene illustrato come utilizzare un token di annullamento in combinazione con `WhenAny` per detenere la prima attività per completare dalla raccolta di attività e per annullare le attività rimanenti.</span><span class="sxs-lookup"><span data-stu-id="0a971-107">This example demonstrates how to use a cancellation token in conjunction with `WhenAny` to hold onto the first task to finish from the collection of tasks and to cancel the remaining tasks.</span></span> <span data-ttu-id="0a971-108">Ogni attività Scarica il contenuto di un sito Web.</span><span class="sxs-lookup"><span data-stu-id="0a971-108">Each task downloads the contents of a website.</span></span> <span data-ttu-id="0a971-109">L'esempio visualizza la lunghezza del contenuto del download prima di completare e Annulla altri download.</span><span class="sxs-lookup"><span data-stu-id="0a971-109">The example displays the length of the contents of the first download to complete and cancels the other downloads.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="0a971-110">Per eseguire gli esempi, è necessario disporre di Visual Studio 2012 o versione successiva e .NET Framework 4.5 o versioni successive installato nel computer in uso.</span><span class="sxs-lookup"><span data-stu-id="0a971-110">To run the examples, you must have Visual Studio 2012 or newer and the .NET Framework 4.5 or newer installed on your computer.</span></span>  
  
## <a name="downloading-the-example"></a><span data-ttu-id="0a971-111">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0a971-111">Downloading the Example</span></span>  
 <span data-ttu-id="0a971-112">È possibile scaricare il progetto completo di Windows Presentation Foundation (WPF) da [esempio asincrono: Fine ottimizzazione dell'applicazione](http://go.microsoft.com/fwlink/?LinkId=255046) e attenersi alla seguente procedura.</span><span class="sxs-lookup"><span data-stu-id="0a971-112">You can download the complete Windows Presentation Foundation (WPF) project from [Async Sample: Fine Tuning Your Application](http://go.microsoft.com/fwlink/?LinkId=255046) and then follow these steps.</span></span>  
  
1.  <span data-ttu-id="0a971-113">Decomprimere il file scaricato e quindi avviare Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0a971-113">Decompress the file that you downloaded, and then start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="0a971-114">Nella barra dei menu scegliere **File**, **Apri**, **Progetto/Soluzione**.</span><span class="sxs-lookup"><span data-stu-id="0a971-114">On the menu bar, choose **File**, **Open**, **Project/Solution**.</span></span>  
  
3.  <span data-ttu-id="0a971-115">Nel **Apri progetto** la finestra di dialogo, aprire la cartella che contiene il codice di esempio che è stato decompresso e quindi aprire il file di soluzione (sln) per AsyncFineTuningVB.</span><span class="sxs-lookup"><span data-stu-id="0a971-115">In the **Open Project** dialog box, open the folder that holds the sample code that you decompressed, and then open the solution (.sln) file for AsyncFineTuningVB.</span></span>  
  
4.  <span data-ttu-id="0a971-116">In **Esplora**, aprire il menu di scelta rapida per il **CancelAfterOneTask** del progetto, quindi fare clic **imposta come progetto di avvio**.</span><span class="sxs-lookup"><span data-stu-id="0a971-116">In **Solution Explorer**, open the shortcut menu for the **CancelAfterOneTask** project, and then choose **Set as StartUp Project**.</span></span>  
  
5.  <span data-ttu-id="0a971-117">Premere il tasto F5 per eseguire il progetto.</span><span class="sxs-lookup"><span data-stu-id="0a971-117">Choose the F5 key to run the project.</span></span>  
  
     <span data-ttu-id="0a971-118">Premere i tasti Ctrl + F5 per eseguire il progetto senza eseguirne il debug.</span><span class="sxs-lookup"><span data-stu-id="0a971-118">Choose the Ctrl+F5 keys to run the project without debugging it.</span></span>  
  
6.  <span data-ttu-id="0a971-119">Eseguire il programma più volte per verificare che il download diversi terminare prima.</span><span class="sxs-lookup"><span data-stu-id="0a971-119">Run the program several times to verify that different downloads finish first.</span></span>  
  
 <span data-ttu-id="0a971-120">Se non si desidera scaricare il progetto, è possibile esaminare il file MainWindow.xaml.vb alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0a971-120">If you don't want to download the project, you can review the MainWindow.xaml.vb file at the end of this topic.</span></span>  
  
## <a name="building-the-example"></a><span data-ttu-id="0a971-121">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0a971-121">Building the Example</span></span>  
 <span data-ttu-id="0a971-122">Nell'esempio riportato in questo argomento viene aggiunto al progetto che è stato sviluppato in [annullare un'attività asincrona o un elenco di attività](http://msdn.microsoft.com/library/d6e4e801-df64-4705-98fc-df725a577fb0) per annullare un elenco di attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-122">The example in this topic adds to the project that's developed in [Cancel an Async Task or a List of Tasks](http://msdn.microsoft.com/library/d6e4e801-df64-4705-98fc-df725a577fb0) to cancel a list of tasks.</span></span> <span data-ttu-id="0a971-123">Nell'esempio viene utilizzata la stessa interfaccia utente, anche se il **Annulla** pulsante non viene utilizzato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="0a971-123">The example uses the same UI, although the **Cancel** button isn’t used explicitly.</span></span>  
  
 <span data-ttu-id="0a971-124">Per compilare l'esempio è l'utente passo passo, seguire le istruzioni nella sezione "Download di esempio", ma scegliere **CancelAListOfTasks** come il **progetto di avvio**.</span><span class="sxs-lookup"><span data-stu-id="0a971-124">To build the example yourself, step by step, follow the instructions in the "Downloading the Example" section, but choose **CancelAListOfTasks** as the **StartUp Project**.</span></span> <span data-ttu-id="0a971-125">A tale progetto, aggiungere le modifiche in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="0a971-125">Add the changes in this topic to that project.</span></span>  
  
 <span data-ttu-id="0a971-126">Nel file MainWindow.xaml.vb del **CancelAListOfTasks** del progetto, avviare la transizione spostando le fasi di elaborazione per ogni sito Web del ciclo in `AccessTheWebAsync` per il seguente metodo async.</span><span class="sxs-lookup"><span data-stu-id="0a971-126">In the MainWindow.xaml.vb file of the **CancelAListOfTasks** project, start the transition by moving the processing steps for each website from the loop in `AccessTheWebAsync` to the following async method.</span></span>  
  
```vb  
' ***Bundle the processing steps for a website into one async method.  
Async Function ProcessURLAsync(url As String, client As HttpClient, ct As CancellationToken) As Task(Of Integer)  
  
    ' GetAsync returns a Task(Of HttpResponseMessage).   
    Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)  
  
    ' Retrieve the website contents from the HttpResponseMessage.  
    Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()  
  
    Return urlContents.Length  
End Function  
```  
  
 <span data-ttu-id="0a971-127">In `AccessTheWebAsync`, in questo esempio viene utilizzata una query, il <xref:System.Linq.Enumerable.ToArray%2A>(metodo) e `WhenAny` per creare e avviare attività di una matrice.</xref:System.Linq.Enumerable.ToArray%2A></span><span class="sxs-lookup"><span data-stu-id="0a971-127">In `AccessTheWebAsync`, this example uses a query, the  <xref:System.Linq.Enumerable.ToArray%2A> method, and the `WhenAny` method to create and start an array of tasks.</span></span> <span data-ttu-id="0a971-128">L'applicazione di `WhenAny` alla matrice viene restituita una singola attività che, quando atteso, restituisce la prima attività per raggiungere il completamento della matrice di attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-128">The application of `WhenAny` to the array returns a single task that, when awaited, evaluates to the first task to reach completion in the array of tasks.</span></span>  
  
 <span data-ttu-id="0a971-129">Apportare le modifiche seguenti in `AccessTheWebAsync`.</span><span class="sxs-lookup"><span data-stu-id="0a971-129">Make the following changes in `AccessTheWebAsync`.</span></span> <span data-ttu-id="0a971-130">Gli asterischi contrassegnare le modifiche nel file di codice.</span><span class="sxs-lookup"><span data-stu-id="0a971-130">Asterisks mark the changes in the code file.</span></span>  
  
1.  <span data-ttu-id="0a971-131">Impostare come commento o eliminare il ciclo.</span><span class="sxs-lookup"><span data-stu-id="0a971-131">Comment out or delete the loop.</span></span>  
  
2.  <span data-ttu-id="0a971-132">Creare una query che, quando eseguita, produce un insieme di attività generiche.</span><span class="sxs-lookup"><span data-stu-id="0a971-132">Create a query that, when executed, produces a collection of generic tasks.</span></span> <span data-ttu-id="0a971-133">Ogni chiamata a `ProcessURLAsync` restituisce un <xref:System.Threading.Tasks.Task%601>dove `TResult` è un numero intero.</xref:System.Threading.Tasks.Task%601></span><span class="sxs-lookup"><span data-stu-id="0a971-133">Each call to `ProcessURLAsync` returns a <xref:System.Threading.Tasks.Task%601> where `TResult` is an integer.</span></span>  
  
<span data-ttu-id="0a971-134"><CodeContentPlaceHolder>1</CodeContentPlaceHolder></span><span class="sxs-lookup"><span data-stu-id="0a971-134"><CodeContentPlaceHolder>1</CodeContentPlaceHolder></span></span>  
3.  <span data-ttu-id="0a971-135">Chiamare `ToArray` per eseguire la query e avviare le attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-135">Call `ToArray` to execute the query and start the tasks.</span></span> <span data-ttu-id="0a971-136">L'applicazione di `WhenAny` metodo nel passaggio successivo si esegue la query e avviare le attività senza utilizzare `ToArray`, ma non altri metodi.</span><span class="sxs-lookup"><span data-stu-id="0a971-136">The application of the `WhenAny` method in the next step would execute the query and start the tasks without using `ToArray`, but other methods might not.</span></span> <span data-ttu-id="0a971-137">La più sicura consiste nel forzare l'esecuzione della query in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="0a971-137">The safest practice is to force execution of the query explicitly.</span></span>  
  
<span data-ttu-id="0a971-138"><CodeContentPlaceHolder>2</CodeContentPlaceHolder></span><span class="sxs-lookup"><span data-stu-id="0a971-138"><CodeContentPlaceHolder>2</CodeContentPlaceHolder></span></span>  
4.  <span data-ttu-id="0a971-139">Chiamare `WhenAny` sulla raccolta di attività.</span><span class="sxs-lookup"><span data-stu-id="0a971-139">Call `WhenAny` on the collection of tasks.</span></span> <span data-ttu-id="0a971-140">`WhenAny`Restituisce un `Task(Of Task(Of Integer))` o `Task<Task<int>>`.</span><span class="sxs-lookup"><span data-stu-id="0a971-140">`WhenAny` returns a `Task(Of Task(Of Integer))` or `Task<Task<int>>`.</span></span>  <span data-ttu-id="0a971-141">Vale a dire `WhenAny` restituisce un'attività che valuta in un unico `Task(Of Integer)` o `Task<int>` quando si è atteso.</span><span class="sxs-lookup"><span data-stu-id="0a971-141">That is, `WhenAny` returns a task that evaluates to a single `Task(Of Integer)` or `Task<int>` when it’s awaited.</span></span> <span data-ttu-id="0a971-142">Singola attività è la prima attività da completare nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="0a971-142">That single task is the first task in the collection to finish.</span></span> <span data-ttu-id="0a971-143">Attività completata innanzitutto viene assegnato a `firstFinishedTask`.</span><span class="sxs-lookup"><span data-stu-id="0a971-143">The task that finished first is assigned to `firstFinishedTask`.</span></span> <span data-ttu-id="0a971-144">Il tipo di `firstFinishedTask` è <xref:System.Threading.Tasks.Task%601>dove `TResult` è un numero intero che corrisponde al tipo restituito di `ProcessURLAsync`.</xref:System.Threading.Tasks.Task%601></span><span class="sxs-lookup"><span data-stu-id="0a971-144">The type of `firstFinishedTask` is <xref:System.Threading.Tasks.Task%601> where `TResult` is an integer because that's the return type of `ProcessURLAsync`.</span></span>  
  
```vb  
' ***Call WhenAny and then await the result. The task that finishes   
' first is assigned to firstFinishedTask.  
Dim firstFinishedTask As Task(Of Integer) = Await Task.WhenAny(downloadTasks)  
```  
  
5.  <span data-ttu-id="0a971-145">In questo esempio, si è interessati solo l'attività che termina per prima.</span><span class="sxs-lookup"><span data-stu-id="0a971-145">In this example, you’re interested only in the task that finishes first.</span></span> <span data-ttu-id="0a971-146">Pertanto, utilizzare <xref:System.Threading.CancellationTokenSource.Cancel%2A?displayProperty=fullName>per annullare le attività rimanenti.</xref:System.Threading.CancellationTokenSource.Cancel%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="0a971-146">Therefore, use <xref:System.Threading.CancellationTokenSource.Cancel%2A?displayProperty=fullName> to cancel the remaining tasks.</span></span>  
  
```vb  
' ***Cancel the rest of the downloads. You just want the first one.  
cts.Cancel()  
```  
  
6.  <span data-ttu-id="0a971-147">Infine, await `firstFinishedTask` per recuperare la lunghezza del contenuto scaricato.</span><span class="sxs-lookup"><span data-stu-id="0a971-147">Finally, await `firstFinishedTask` to retrieve the length of the downloaded content.</span></span>  
  
```vb  
Dim length = Await firstFinishedTask  
resultsTextBox.Text &= String.Format(vbCrLf & "Length of the downloaded website:  {0}" & vbCrLf, length)  
```  
  
 <span data-ttu-id="0a971-148">Eseguire il programma più volte per verificare che il download diversi terminare prima.</span><span class="sxs-lookup"><span data-stu-id="0a971-148">Run the program several times to verify that different downloads finish first.</span></span>  
  
## <a name="complete-example"></a><span data-ttu-id="0a971-149">Esempio completo</span><span class="sxs-lookup"><span data-stu-id="0a971-149">Complete Example</span></span>  
 <span data-ttu-id="0a971-150">Il codice seguente è il file MainWindow.xaml.vb o MainWindow.xaml.cs completo per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0a971-150">The following code is the complete MainWindow.xaml.vb or MainWindow.xaml.cs file for the example.</span></span> <span data-ttu-id="0a971-151">Gli asterischi contrassegnare gli elementi che sono stati aggiunti per questo esempio.</span><span class="sxs-lookup"><span data-stu-id="0a971-151">Asterisks mark the elements that were added for this example.</span></span>  
  
 <span data-ttu-id="0a971-152">Si noti che è necessario aggiungere un riferimento per <xref:System.Net.Http>.</xref:System.Net.Http></span><span class="sxs-lookup"><span data-stu-id="0a971-152">Notice that you must add a reference for <xref:System.Net.Http>.</span></span>  
  
 <span data-ttu-id="0a971-153">È possibile scaricare il progetto da [esempio asincrono: Fine ottimizzazione dell'applicazione](http://go.microsoft.com/fwlink/?LinkId=255046).</span><span class="sxs-lookup"><span data-stu-id="0a971-153">You can download the project from [Async Sample: Fine Tuning Your Application](http://go.microsoft.com/fwlink/?LinkId=255046).</span></span>  
  
```vb  
' Add an Imports directive and a reference for System.Net.Http.  
Imports System.Net.Http  
  
' Add the following Imports directive for System.Threading.  
Imports System.Threading  
  
Class MainWindow  
  
    ' Declare a System.Threading.CancellationTokenSource.  
    Dim cts As CancellationTokenSource  
  
    Private Async Sub startButton_Click(sender As Object, e As RoutedEventArgs)  
  
        ' Instantiate the CancellationTokenSource.  
        cts = New CancellationTokenSource()  
  
        resultsTextBox.Clear()  
  
        Try  
            Await AccessTheWebAsync(cts.Token)  
            resultsTextBox.Text &= vbCrLf & "Download complete."  
  
        Catch ex As OperationCanceledException  
            resultsTextBox.Text &= vbCrLf & "Download canceled." & vbCrLf  
  
        Catch ex As Exception  
            resultsTextBox.Text &= vbCrLf & "Download failed." & vbCrLf  
        End Try  
  
        ' Set the CancellationTokenSource to Nothing when the download is complete.  
        cts = Nothing  
    End Sub  
  
    ' You can still include a Cancel button if you want to.  
    Private Sub cancelButton_Click(sender As Object, e As RoutedEventArgs)  
  
        If cts IsNot Nothing Then  
            cts.Cancel()  
        End If  
    End Sub  
  
    ' Provide a parameter for the CancellationToken.  
    ' Change the return type to Task because the method has no return statement.  
    Async Function AccessTheWebAsync(ct As CancellationToken) As Task  
  
        Dim client As HttpClient = New HttpClient()  
  
        ' Call SetUpURLList to make a list of web addresses.  
        Dim urlList As List(Of String) = SetUpURLList()  
  
        '' Comment out or delete the loop.  
        ''For Each url In urlList  
        ''    ' GetAsync returns a Task(Of HttpResponseMessage).   
        ''    ' Argument ct carries the message if the Cancel button is chosen.   
        ''    ' Note that the Cancel button can cancel all remaining downloads.  
        ''    Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)  
  
        ''    ' Retrieve the website contents from the HttpResponseMessage.  
        ''    Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()  
  
        ''    resultsTextBox.Text &=  
        ''        String.Format(vbCrLf & "Length of the downloaded string: {0}." & vbCrLf, urlContents.Length)  
        ''Next  
  
        ' ***Create a query that, when executed, returns a collection of tasks.  
        Dim downloadTasksQuery As IEnumerable(Of Task(Of Integer)) =  
            From url In urlList Select ProcessURLAsync(url, client, ct)  
  
        ' ***Use ToArray to execute the query and start the download tasks.   
        Dim downloadTasks As Task(Of Integer)() = downloadTasksQuery.ToArray()  
  
        ' ***Call WhenAny and then await the result. The task that finishes   
        ' first is assigned to firstFinishedTask.  
        Dim firstFinishedTask As Task(Of Integer) = Await Task.WhenAny(downloadTasks)  
  
        ' ***Cancel the rest of the downloads. You just want the first one.  
        cts.Cancel()  
  
        ' ***Await the first completed task and display the results  
        ' Run the program several times to demonstrate that different  
        ' websites can finish first.  
        Dim length = Await firstFinishedTask  
        resultsTextBox.Text &= String.Format(vbCrLf & "Length of the downloaded website:  {0}" & vbCrLf, length)  
    End Function  
  
    ' ***Bundle the processing steps for a website into one async method.  
    Async Function ProcessURLAsync(url As String, client As HttpClient, ct As CancellationToken) As Task(Of Integer)  
  
        ' GetAsync returns a Task(Of HttpResponseMessage).   
        Dim response As HttpResponseMessage = Await client.GetAsync(url, ct)  
  
        ' Retrieve the website contents from the HttpResponseMessage.  
        Dim urlContents As Byte() = Await response.Content.ReadAsByteArrayAsync()  
  
        Return urlContents.Length  
    End Function  
  
    ' Add a method that creates a list of web addresses.  
    Private Function SetUpURLList() As List(Of String)  
  
        Dim urls = New List(Of String) From  
            {  
                "http://msdn.microsoft.com",  
                "http://msdn.microsoft.com/library/hh290138.aspx",  
                "http://msdn.microsoft.com/library/hh290140.aspx",  
                "http://msdn.microsoft.com/library/dd470362.aspx",  
                "http://msdn.microsoft.com/library/aa578028.aspx",  
                "http://msdn.microsoft.com/library/ms404677.aspx",  
                "http://msdn.microsoft.com/library/ff730837.aspx"  
            }  
        Return urls  
    End Function  
  
End Class  
  
' Sample output:  
  
' Length of the downloaded website:  158856  
  
' Download complete.  
```  
  
## <a name="see-also"></a><span data-ttu-id="0a971-154">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0a971-154">See Also</span></span>  
 <span data-ttu-id="0a971-155"><xref:System.Threading.Tasks.Task.WhenAny%2A></xref:System.Threading.Tasks.Task.WhenAny%2A></span><span class="sxs-lookup"><span data-stu-id="0a971-155"><xref:System.Threading.Tasks.Task.WhenAny%2A></span></span>   
<span data-ttu-id="0a971-156"> [Ottimizzazione dell'applicazione Async (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/fine-tuning-your-async-application.md) </span><span class="sxs-lookup"><span data-stu-id="0a971-156"> [Fine-Tuning Your Async Application (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/fine-tuning-your-async-application.md) </span></span>  
<span data-ttu-id="0a971-157"> [Programmazione asincrona con Async e Await (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/index.md) </span><span class="sxs-lookup"><span data-stu-id="0a971-157"> [Asynchronous Programming with Async and Await (Visual Basic)](../../../../visual-basic/programming-guide/concepts/async/index.md) </span></span>  
<span data-ttu-id="0a971-158"> [Esempio asincrono: Ottimizzazione dell'applicazione](http://go.microsoft.com/fwlink/?LinkId=255046)</span><span class="sxs-lookup"><span data-stu-id="0a971-158"> [Async Sample: Fine Tuning Your Application](http://go.microsoft.com/fwlink/?LinkId=255046)</span></span>
