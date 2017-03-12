---
title: "Procedura: accedere agli oggetti di interoperabilit&#224; di Office usando le funzionalit&#224; di Visual C# (Guida per programmatori C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "dynamic [C#], programmazione Office"
  - "argomenti denominati e facoltativi [C#], programmazione Office"
  - "argomenti denominati [C#], programmazione Office"
  - "programmazione Office [C#]"
  - "argomenti facoltativi [C#], programmazione Office"
  - "parametri facoltativi [C#], programmazione Office"
ms.assetid: 041b25c2-3512-4e0f-a4ea-ceb2999e4d5e
caps.latest.revision: 33
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 33
---
# Procedura: accedere agli oggetti di interoperabilit&#224; di Office usando le funzionalit&#224; di Visual C# (Guida per programmatori C#)
Visual C\# 2010 introduce nuove funzionalità che semplificano l'accesso agli oggetti API di Office.  Le nuove funzionalità includono argomenti denominati e facoltativi, un nuovo tipo chiamato `dynamic` e la possibilità di passare argomenti a parametri di riferimento nei metodi COM come se fossero parametri di valore.  
  
 In questo argomento si useranno le nuove funzionalità per scrivere codice che consente di creare e visualizzare un foglio di lavoro di Microsoft Office Excel.  Quindi si scriverà il codice per aggiungere un documento di Office Word contenente un'icona che è collegata al foglio di lavoro di Excel.  
  
 Per completare questa procedura dettagliata, è necessario aver installato nel computer Microsoft Office Excel 2007 e Microsoft Office Word 2007 o versioni successive.  
  
 Se si usa un sistema operativo precedente a [!INCLUDE[windowsver](../../../csharp/programming-guide/interop/includes/windowsver-md.md)], assicurarsi che [!INCLUDE[dnprdnlong](../../../csharp/programming-guide/events/includes/dnprdnlong-md.md)] sia installato.  
  
 [!INCLUDE[note_settings_general](../../../csharp/language-reference/compiler-messages/includes/note-settings-general-md.md)]  
  
### Per creare un nuovo progetto di applicazione console  
  
1.  Avviare Visual Studio.  
  
2.  Scegliere **Nuovo** dal menu **File**, quindi fare clic su **Progetto**.  Verrà visualizzata la finestra di dialogo **Nuovo progetto**.  
  
3.  Nel riquadro **Modelli installati** espandere **Visual C\#**, quindi selezionare **Windows**.  
  
4.  Nella parte superiore della finestra di dialogo **Nuovo progetto** assicurarsi che **.NET Framework 4** \(o versione successiva\) sia selezionato come framework di destinazione.  
  
5.  Nel riquadro **Modelli** fare clic su **Applicazione console**.  
  
6.  Digitare un nome per l'applicazione nella casella di testo **Nome**.  
  
7.  Fare clic su **OK**.  
  
     Il nuovo progetto verrà visualizzato in **Esplora soluzioni**.  
  
### Per aggiungere riferimenti  
  
1.  In **Esplora soluzioni** fare clic con il pulsante destro del mouse sul nome del progetto, quindi scegliere **Aggiungi riferimento**.  Viene visualizzata la finestra di dialogo **Aggiungi riferimento**.  
  
2.  Nella pagina **Assembly** selezionare **Microsoft.Office.Interop.Word** nell'elenco **Nome componente**, quindi tenere premuto il tasto CTRL e selezionare **Microsoft.Office.Interop.Excel**.  Se gli assembly non sono visibili, può essere necessario assicurarsi che siano installati e visualizzati \(vedere [Procedura: installare assembly di interoperabilità primari di Office](../Topic/How%20to:%20Install%20Office%20Primary%20Interop%20Assemblies.md)\)  
  
3.  Fare clic su **OK**.  
  
### Per aggiungere le direttive using necessarie  
  
1.  In **Esplora soluzioni**, fare clic con il pulsante destro del mouse sul file **Program.cs** e quindi fare clic su **Visualizza codice**.  
  
2.  Aggiungere le seguenti direttive `using` all'inizio del file di codice.  
  
     [!code-cs[csProgGuideOfficeHowTo#1](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#1)]  
  
### Per creare un elenco di conti correnti bancari  
  
1.  Incollare la seguente definizione di classe in **Program.cs**, sotto la classe `Program`.  
  
     [!code-cs[csProgGuideOfficeHowTo#2](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#2)]  
  
2.  Aggiungere il seguente codice al metodo `Main` per creare un elenco `bankAccounts` contenente due conti.  
  
     [!code-cs[csProgGuideOfficeHowTo#3](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#3)]  
  
### Per dichiarare un metodo che consente di esportare informazioni sul conto in Excel  
  
1.  Aggiungere il seguente metodo alla classe `Program` per impostare un foglio di lavoro di Excel.  
  
     Il metodo [Add](http://go.microsoft.com/fwlink/?LinkId=210910) ha un parametro facoltativo per specificare un modello particolare.  I parametri facoltativi, una novità di [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], consentono di omettere l'argomento per il parametro se si vuole usare il valore predefinito del parametro.  Poiché nessun argomento viene inviato nel codice seguente, `Add` usa il modello predefinito e crea una nuova cartella di lavoro.  L'istruzione equivalente nelle precedenti versioni di C\# richiede un argomento segnaposto: `ExcelApp.Workbooks.Add(Type.Missing)`.  
  
     [!code-cs[csProgGuideOfficeHowTo#4](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#4)]  
  
2.  Aggiungere il codice seguente alla fine di `DisplayInExcel`.  Il codice consente di inserire valori nelle prime due colonne della prima riga del foglio di lavoro.  
  
     [!code-cs[csProgGuideOfficeHowTo#5](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#5)]  
  
3.  Aggiungere il codice seguente alla fine di `DisplayInExcel`.  Il ciclo `foreach` inserisce le informazioni dall'elenco dei conti nelle prime due colonne delle righe successive del foglio di lavoro.  
  
     [!code-cs[csProgGuideOfficeHowTo#7](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#7)]  
  
4.  Aggiungere il seguente codice alla fine di `DisplayInExcel` per regolare la larghezza delle colonne in modo da adattarle al contenuto.  
  
     [!code-cs[csProgGuideOfficeHowTo#13](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#13)]  
  
     Le versioni precedenti di C\# richiedono il cast esplicito per queste operazioni perché `ExcelApp.Columns[1]` restituisce un `Object`, e `AutoFit` è un metodo [Range](http://go.microsoft.com/fwlink/?LinkId=210911) di Excel.  Le righe seguenti indicano il cast.  
  
     [!code-cs[csProgGuideOfficeHowTo#14](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#14)]  
  
     [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], e versioni successive, converte automaticamente l'oggetto restituito `Object` in `dynamic` se si fa riferimento all'assembly con l'opzione del compilatore [\/link](../../../csharp/language-reference/compiler-options/link-compiler-option.md) o, allo stesso modo, se la proprietà **Incorpora tipi di interoperabilità** di Excel viene impostata su true.  True è il valore predefinito di questa proprietà.  
  
### Per eseguire il progetto  
  
1.  Aggiungere la riga seguente alla fine di `Main`.  
  
     [!code-cs[csProgGuideOfficeHowTo#8](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#8)]  
  
2.  Premere CTRL\+F5.  
  
     Viene visualizzato un foglio di lavoro di Excel che contiene i dati dei due conti.  
  
### Per aggiungere un documento di Word  
  
1.  Per illustrare altri modi in cui [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], e versioni successive, consente di migliorare la programmazione di Office, il codice seguente apre un'applicazione Word e crea un'icona di collegamento al foglio di lavoro di Excel.  
  
     Incollare il metodo `CreateIconInWordDoc`, fornito più avanti in questo passaggio, nella classe `Program`.  `CreateIconInWordDoc` usa argomenti denominati e facoltativi per ridurre la complessità delle chiamate di metodo a [Add](http://go.microsoft.com/fwlink/?LinkId=210937) e [PasteSpecial](http://go.microsoft.com/fwlink/?LinkId=147099).  Queste chiamate incorporano altre due nuove funzionalità introdotte in [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)] che semplificano le chiamate ai metodi COM con parametri di riferimento.  In primo luogo, è possibile inviare argomenti ai parametri di riferimento come se fossero parametri di valore.  In altre parole, è possibile inviare i valori direttamente, senza creare una variabile per ogni parametro referenziato.  Il compilatore genera variabili temporanee per conservare i valori degli argomenti ed elimina le variabili restituite dalla chiamata.  In secondo luogo, è possibile omettere la parola chiave `ref` nell'elenco di argomenti.  
  
     Il metodo `Add` ha quattro parametri di riferimento, tutti facoltativi.  In [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], o versioni successive, è possibile omettere gli argomenti per alcuni o tutti i parametri se si vogliono usare i valori predefiniti.  In [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp-orcas-long-md.md)] e versioni precedenti, è necessario fornire un argomento per ogni parametro e l'argomento deve essere una variabile perché i parametri sono di riferimento.  
  
     Il metodo `PasteSpecial` inserisce il contenuto degli Appunti.  Il metodo ha sette parametri di riferimento, tutti facoltativi.  Il codice seguente consente di specificare gli argomenti per due di essi: `Link`, per creare un collegamento all'origine del contenuto degli Appunti e `DisplayAsIcon`, per visualizzare il collegamento come icona.  In [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], è possibile usare argomenti denominati per questi due parametri e omettere gli altri.  Anche se si tratta di parametri di riferimento, non è necessario usare la parola chiave `ref` o creare variabili per inviarle come argomenti.  È possibile inviare direttamente i valori.  In [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp-orcas-long-md.md)] e versioni precedenti, è necessario inviare un argomento variabile per ogni parametro referenziato.  
  
     [!code-cs[csProgGuideOfficeHowTo#9](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#9)]  
  
     In [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp-orcas-long-md.md)] o versioni precedenti del linguaggio, è necessario il codice più complesso seguente.  
  
     [!code-cs[csProgGuideOfficeHowTo#10](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#10)]  
  
2.  Aggiungere la seguente istruzione dopo `Main`.  
  
     [!code-cs[csProgGuideOfficeHowTo#11](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#11)]  
  
3.  Aggiungere la seguente istruzione dopo `DisplayInExcel`.  Il metodo `Copy` aggiunge il foglio di lavoro negli Appunti.  
  
     [!code-cs[csProgGuideOfficeHowTo#12](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#12)]  
  
4.  Premere CTRL\+F5.  
  
     Verrà visualizzato un documento di Word contenente un'icona.  Fare doppio clic sull'icona per visualizzare il foglio di lavoro in primo piano.  
  
### Per impostare la proprietà Incorpora tipi di interoperabilità  
  
1.  Quando si chiama un tipo COM che non richiede un assembly di interoperabilità primario \(PIA\) in fase di esecuzione, sono possibili altri miglioramenti.  Eliminando la dipendenza dai risultati dei PIA produce l'indipendenza dalla versione e semplifica la distribuzione.  Per altre informazioni sui vantaggi della programmazione senza PIA, vedere [Procedura dettagliata: Incorporamento dei tipi da assembly gestiti](../Topic/Walkthrough:%20Embedding%20Types%20from%20Managed%20Assemblies%20\(C%23%20and%20Visual%20Basic\).md).  
  
     Inoltre, la programmazione è più semplice perché i tipi richiesti e restituiti dai metodi COM possono essere rappresentati usando il tipo `dynamic` anziché `Object`.  Le variabili di tipo `dynamic` non saranno valutate fino al runtime, eliminando la necessità del cast esplicito.  Per altre informazioni, vedere [Utilizzo del tipo dinamico](../../../csharp/programming-guide/types/using-type-dynamic.md).  
  
     In [!INCLUDE[csharp_dev10_long](../../../csharp/programming-guide/classes-and-structs/includes/csharp-dev10-long-md.md)], il comportamento predefinito consiste nell'incorporare le informazioni di tipo invece di usare i PIA.  A causa di tale impostazione predefinita, molti degli esempi precedenti vengono semplificati perché non è necessario eseguire il cast esplicito.  Ad esempio, la dichiarazione di `worksheet` in `DisplayInExcel` è scritta come `Excel._Worksheet workSheet = excelApp.ActiveSheet` piuttosto che `Excel._Worksheet workSheet = (Excel.Worksheet)excelApp.ActiveSheet`.  Anche le chiamate a `AutoFit` nello stesso metodo richiederebbero il cast esplicito senza valore predefinito, perché `ExcelApp.Columns[1]` restituisce un `Object` e `AutoFit` è un metodo Excel.  Nel codice seguente viene illustrato il cast.  
  
     [!code-cs[csProgGuideOfficeHowTo#14](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#14)]  
  
2.  Per modificare il valore predefinito e usare i PIA anziché incorporare le informazioni sul tipo, espandere il nodo **Riferimenti** in **Esplora soluzioni** e quindi selezionare **Microsoft.Office.Interop.Excel** o **Microsoft.Office.Interop.Word**.  
  
3.  Se non è possibile visualizzare la finestra **Proprietà**, premere **F4**.  
  
4.  Trovare **Incorpora tipi di interoperabilità** nell'elenco delle proprietà e modificarne il valore in **False**.  Allo stesso modo, è possibile compilare usando l'opzione del compilatore [\/reference](../../../csharp/language-reference/compiler-options/reference-compiler-option.md) invece di [\/link](../../../csharp/language-reference/compiler-options/link-compiler-option.md) in un prompt dei comandi.  
  
### Per aggiungere ulteriore formattazione alla tabella  
  
1.  Sostituire le due chiamate a `AutoFit` in `DisplayInExcel` con la seguente istruzione.  
  
     [!code-cs[csProgGuideOfficeHowTo#15](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#15)]  
  
     Il metodo [AutoFormat](http://go.microsoft.com/fwlink/?LinkId=210948) ha sette parametri di valore, tutti facoltativi.  Gli argomenti denominati e facoltativi consentono di specificare gli argomenti per nessuno, alcuni o tutti i parametri.  Nell'istruzione precedente, viene fornito un argomento per uno solo dei parametri, `Format`.  Poiché `Format` è il primo parametro nell'elenco, non è necessario fornire il nome del parametro.  Tuttavia, l'istruzione potrebbe essere più facile da comprendere se si include il nome del parametro, come illustrato nel codice seguente.  
  
     [!code-cs[csProgGuideOfficeHowTo#16](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#16)]  
  
2.  Premere CTRL \+ F5 per visualizzare il risultato.  Altri formati sono elencati nell'enumerazione [XlRangeAutoFormat](http://go.microsoft.com/fwlink/?LinkId=210967).  
  
3.  Confrontare l'istruzione nel passaggio 1 con il codice seguente, che illustra gli argomenti necessari in [!INCLUDE[csharp_orcas_long](../../../csharp/programming-guide/interop/includes/csharp-orcas-long-md.md)] o versioni precedenti.  
  
     [!code-cs[csProgGuideOfficeHowTo#17](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/program.cs#17)]  
  
## Esempio  
 Nel codice seguente viene illustrato l'esempio completo.  
  
 [!code-cs[csProgGuideOfficeHowTo#18](../../../csharp/programming-guide/interop/codesnippet/csharp/officeprogrammingwalkthrough/walkthrough.cs#18)]  
  
## Vedere anche  
 <xref:System.Type.Missing?displayProperty=fullName>   
 [dynamic](../../../csharp/language-reference/keywords/dynamic.md)   
 [Utilizzo del tipo dinamico](../../../csharp/programming-guide/types/using-type-dynamic.md)   
 [Argomenti denominati e facoltativi](../../../csharp/programming-guide/classes-and-structs/named-and-optional-arguments.md)   
 [Procedura: utilizzare argomenti denominati e facoltativi nella programmazione di Office](../../../csharp/programming-guide/classes-and-structs/how-to-use-named-and-optional-arguments-in-office-programming.md)