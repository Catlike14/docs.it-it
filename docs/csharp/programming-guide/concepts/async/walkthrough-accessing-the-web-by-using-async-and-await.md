---
title: 'Procedura dettagliata: accesso al Web con Async e Await (C#)'
ms.date: 07/20/2015
ms.assetid: c95d8d71-5a98-4bf0-aaf4-45fed2ebbacd
ms.openlocfilehash: 33145f6a7ececd85e6eeaebb80a81f3075878761
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33338130"
---
# <a name="walkthrough-accessing-the-web-by-using-async-and-await-c"></a><span data-ttu-id="02c81-102">Procedura dettagliata: accesso al Web con Async e Await (C#)</span><span class="sxs-lookup"><span data-stu-id="02c81-102">Walkthrough: Accessing the Web by Using async and await (C#)</span></span>
<span data-ttu-id="02c81-103">È possibile scrivere programmi asincroni in modo più semplice e intuitivo usando le funzionalità async/await.</span><span class="sxs-lookup"><span data-stu-id="02c81-103">You can write asynchronous programs more easily and intuitively by using async/await features.</span></span> <span data-ttu-id="02c81-104">È possibile scrivere codice asincrono simile al codice sincrono e consentire al compilatore di gestire le complesse funzioni di callback e continuazione tipiche del codice asincrono.</span><span class="sxs-lookup"><span data-stu-id="02c81-104">You can write asynchronous code that looks like synchronous code and let the compiler handle the difficult callback functions and continuations that asynchronous code usually entails.</span></span>  
  
 <span data-ttu-id="02c81-105">Per altre informazioni sulla funzionalità Async, vedere [Programmazione asincrona con Async e Await (C#)](../../../../csharp/programming-guide/concepts/async/index.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-105">For more information about the Async feature, see [Asynchronous Programming with async and await (C#)](../../../../csharp/programming-guide/concepts/async/index.md).</span></span>  
  
 <span data-ttu-id="02c81-106">Questa procedura dettagliata inizia con l'esecuzione di un'applicazione Windows Presentation Foundation (WPF) sincrona che somma il numero di byte in un elenco di siti Web.</span><span class="sxs-lookup"><span data-stu-id="02c81-106">This walkthrough starts with a synchronous Windows Presentation Foundation (WPF) application that sums the number of bytes in a list of websites.</span></span> <span data-ttu-id="02c81-107">La procedura dettagliata converte quindi l'applicazione in una soluzione asincrona usando le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="02c81-107">The walkthrough then converts the application to an asynchronous solution by using the new features.</span></span>  
  
 <span data-ttu-id="02c81-108">Se non si vogliono compilare manualmente le applicazioni, è possibile scaricare l'esempio disponibile in [Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f) (Esempio asincrono: accesso alla procedura dettagliata Web (C# e Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="02c81-108">If you don't want to build the applications yourself, you can download [Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f).</span></span>  
  
 <span data-ttu-id="02c81-109">Questa procedura dettagliata prevede l'esecuzione delle attività seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c81-109">In this walkthrough, you complete the following tasks:</span></span>  
  
-   [<span data-ttu-id="02c81-110">Per creare un'applicazione WPF</span><span class="sxs-lookup"><span data-stu-id="02c81-110">To create a WPF application</span></span>](#CreateWPFApp)  
  
-   [<span data-ttu-id="02c81-111">Per progettare una finestra WPF MainWindow semplice</span><span class="sxs-lookup"><span data-stu-id="02c81-111">To design a simple WPF MainWindow</span></span>](#MainWindow)  
  
-   [<span data-ttu-id="02c81-112">Per aggiungere un riferimento</span><span class="sxs-lookup"><span data-stu-id="02c81-112">To add a reference</span></span>](#AddRef)  
  
-   [<span data-ttu-id="02c81-113">Per aggiungere le direttive using necessarie</span><span class="sxs-lookup"><span data-stu-id="02c81-113">To add necessary using directives</span></span>](#usingDir)  
  
-   [<span data-ttu-id="02c81-114">Per creare un'applicazione sincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-114">To create a synchronous application</span></span>](#synchronous)  
  
-   [<span data-ttu-id="02c81-115">Per eseguire il test della soluzione sincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-115">To test the synchronous solution</span></span>](#testSynch)  
  
-   [<span data-ttu-id="02c81-116">Per convertire GetURLContents in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-116">To convert GetURLContents to an asynchronous method</span></span>](#GetURLContents)  
  
-   [<span data-ttu-id="02c81-117">Per Convertire SumPageSizes in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-117">To convert SumPageSizes to an asynchronous method</span></span>](#SumPageSizes)  
  
-   [<span data-ttu-id="02c81-118">Per convertire startButton_Click in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-118">To convert startButton_Click to an asynchronous method</span></span>](#startButton)  
  
-   [<span data-ttu-id="02c81-119">Per eseguire il test della soluzione asincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-119">To test the asynchronous solution</span></span>](#testAsynch)  
  
-   [<span data-ttu-id="02c81-120">Per sostituire GetURLContentsAsync con un metodo .NET Framework</span><span class="sxs-lookup"><span data-stu-id="02c81-120">To replace method GetURLContentsAsync with a .NET Framework method</span></span>](#GetURLContentsAsync)  
  
-   [<span data-ttu-id="02c81-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="02c81-121">Example</span></span>](#BKMK_CompleteCodeExamples)  
  
> [!NOTE]
>  <span data-ttu-id="02c81-122">Per eseguire gli esempi, è necessario avere installato Visual Studio 2012 o versioni successive e .NET Framework 4.5 o versioni successive nel computer.</span><span class="sxs-lookup"><span data-stu-id="02c81-122">To run the examples, you must have Visual Studio 2012 or newer and the .NET Framework 4.5 or newer installed on your computer.</span></span>  
  
###  <a name="CreateWPFApp"></a> <span data-ttu-id="02c81-123">Per creare un'applicazione WPF</span><span class="sxs-lookup"><span data-stu-id="02c81-123">To create a WPF application</span></span>  
  
1.  <span data-ttu-id="02c81-124">Avviare Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="02c81-124">Start Visual Studio.</span></span>  
  
2.  <span data-ttu-id="02c81-125">Nella barra dei menu scegliere **File**, **Nuovo**, **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="02c81-125">On the menu bar, choose **File**, **New**, **Project**.</span></span>  
  
     <span data-ttu-id="02c81-126">Verrà visualizzata la finestra di dialogo **Nuovo progetto** .</span><span class="sxs-lookup"><span data-stu-id="02c81-126">The **New Project** dialog box opens.</span></span>  
  
3.  <span data-ttu-id="02c81-127">Nel riquadro **Modelli installati**, scegliere Visual C# e quindi scegliere **Applicazione WPF** nell'elenco dei tipi di progetto.</span><span class="sxs-lookup"><span data-stu-id="02c81-127">In the **Installed Templates** pane, choose Visual C#, and then choose **WPF Application** from the list of project types.</span></span>  
  
4.  <span data-ttu-id="02c81-128">Nella casella di testo **Nome** immettere `AsyncExampleWPF` e quindi scegliere il pulsante **OK**.</span><span class="sxs-lookup"><span data-stu-id="02c81-128">In the **Name** text box, enter `AsyncExampleWPF`, and then choose the **OK** button.</span></span>  
  
     <span data-ttu-id="02c81-129">Il nuovo progetto verrà visualizzato in **Esplora soluzioni**.</span><span class="sxs-lookup"><span data-stu-id="02c81-129">The new project appears in **Solution Explorer**.</span></span>  
  
##  <a name="BKMK_DesignWPFMainWin"></a>   
###  <a name="MainWindow"></a> <span data-ttu-id="02c81-130">Per progettare una finestra WPF MainWindow semplice</span><span class="sxs-lookup"><span data-stu-id="02c81-130">To design a simple WPF MainWindow</span></span>  
  
1.  <span data-ttu-id="02c81-131">Nell'Editor di codice di Visual Studio scegliere la scheda **MainWindow.xaml** .</span><span class="sxs-lookup"><span data-stu-id="02c81-131">In the Visual Studio Code Editor, choose the **MainWindow.xaml** tab.</span></span>  
  
2.  <span data-ttu-id="02c81-132">Se la finestra **Casella degli strumenti** non è visibile, aprire il menu **Visualizza** e quindi scegliere **Casella degli strumenti**.</span><span class="sxs-lookup"><span data-stu-id="02c81-132">If the **Toolbox** window isn’t visible, open the **View** menu, and then choose **Toolbox**.</span></span>  
  
3.  <span data-ttu-id="02c81-133">Aggiungere un controllo **Button** e un controllo **TextBox** alla finestra **MainWindow**.</span><span class="sxs-lookup"><span data-stu-id="02c81-133">Add a **Button** control and a **TextBox** control to the **MainWindow** window.</span></span>  
  
4.  <span data-ttu-id="02c81-134">Evidenziare il controllo **TextBox** e nella finestra **Proprietà** impostare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c81-134">Highlight the **TextBox** control and, in the **Properties** window, set the following values:</span></span>  
  
    -   <span data-ttu-id="02c81-135">Impostare la proprietà **Nome** su `resultsTextBox`.</span><span class="sxs-lookup"><span data-stu-id="02c81-135">Set the **Name** property to `resultsTextBox`.</span></span>  
  
    -   <span data-ttu-id="02c81-136">Impostare la proprietà **Height** su 250.</span><span class="sxs-lookup"><span data-stu-id="02c81-136">Set the **Height** property to 250.</span></span>  
  
    -   <span data-ttu-id="02c81-137">Impostare la proprietà **Width** su 500.</span><span class="sxs-lookup"><span data-stu-id="02c81-137">Set the **Width** property to 500.</span></span>  
  
    -   <span data-ttu-id="02c81-138">Nel scheda **Testo** specificare un tipo di carattere a spaziatura fissa, ad esempio Lucida Console o Global Monospace.</span><span class="sxs-lookup"><span data-stu-id="02c81-138">On the **Text** tab, specify a monospaced font, such as Lucida Console or Global Monospace.</span></span>  
  
5.  <span data-ttu-id="02c81-139">Evidenziare il controllo **Button** e nella finestra **Proprietà** impostare i valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c81-139">Highlight the **Button** control and, in the **Properties** window, set the following values:</span></span>  
  
    -   <span data-ttu-id="02c81-140">Impostare la proprietà **Nome** su `startButton`.</span><span class="sxs-lookup"><span data-stu-id="02c81-140">Set the **Name** property to `startButton`.</span></span>  
  
    -   <span data-ttu-id="02c81-141">Modificare il valore della proprietà **Content** da **Button** in **Start**.</span><span class="sxs-lookup"><span data-stu-id="02c81-141">Change the value of the **Content** property from **Button** to **Start**.</span></span>  
  
6.  <span data-ttu-id="02c81-142">Posizionare la casella di testo e il pulsante in modo che entrambi siano visualizzati nella finestra **MainWindow**.</span><span class="sxs-lookup"><span data-stu-id="02c81-142">Position the text box and the button so that both appear in the **MainWindow** window.</span></span>  
  
     <span data-ttu-id="02c81-143">Per altre informazioni su WPF XAML Designer, vedere [Creazione di un'interfaccia utente tramite XAML Designer](/visualstudio/designers/creating-a-ui-by-using-xaml-designer-in-visual-studio).</span><span class="sxs-lookup"><span data-stu-id="02c81-143">For more information about the WPF XAML Designer, see [Creating a UI by using XAML Designer](/visualstudio/designers/creating-a-ui-by-using-xaml-designer-in-visual-studio).</span></span>  
  
##  <a name="BKMK_AddReference"></a>   
###  <a name="AddRef"></a> <span data-ttu-id="02c81-144">Per aggiungere un riferimento</span><span class="sxs-lookup"><span data-stu-id="02c81-144">To add a reference</span></span>  
  
1.  <span data-ttu-id="02c81-145">In **Esplora soluzioni** evidenziare il nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="02c81-145">In **Solution Explorer**, highlight your project's name.</span></span>  
  
2.  <span data-ttu-id="02c81-146">Nella barra dei menu scegliere **Progetto**, **Aggiungi riferimento**.</span><span class="sxs-lookup"><span data-stu-id="02c81-146">On the menu bar, choose **Project**, **Add Reference**.</span></span>  
  
     <span data-ttu-id="02c81-147">Verrà visualizzata la finestra di dialogo **Gestione riferimenti**.</span><span class="sxs-lookup"><span data-stu-id="02c81-147">The **Reference Manager** dialog box appears.</span></span>  
  
3.  <span data-ttu-id="02c81-148">Nella parte superiore della finestra di dialogo verificare che il progetto sia destinato a .NET Framework 4.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="02c81-148">At the top of the dialog box, verify that your project is targeting the .NET Framework 4.5 or higher.</span></span>  
  
4.  <span data-ttu-id="02c81-149">Nell'area **Assembly** scegliere **Framework** se non è già selezionato.</span><span class="sxs-lookup"><span data-stu-id="02c81-149">In the **Assemblies** area, choose **Framework** if it isn’t already chosen.</span></span>  
  
5.  <span data-ttu-id="02c81-150">Nell'elenco dei nomi selezionare la casella di controllo **System.Net.Http**.</span><span class="sxs-lookup"><span data-stu-id="02c81-150">In the list of names, select the **System.Net.Http** check box.</span></span>  
  
6.  <span data-ttu-id="02c81-151">Scegliere il pulsante **OK** per chiudere la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="02c81-151">Choose the **OK** button to close the dialog box.</span></span>  
  
##  <a name="BKMK_AddStatesandDirs"></a>   
###  <a name="usingDir"></a> <span data-ttu-id="02c81-152">Per aggiungere le direttive using necessarie</span><span class="sxs-lookup"><span data-stu-id="02c81-152">To add necessary using directives</span></span>  
  
1.  <span data-ttu-id="02c81-153">In **Esplora soluzioni** aprire il menu di scelta rapida per MainWindow.xaml.cs e quindi scegliere **Visualizza codice**.</span><span class="sxs-lookup"><span data-stu-id="02c81-153">In **Solution Explorer**, open the shortcut menu for MainWindow.xaml.cs, and then choose **View Code**.</span></span>  
  
2.  <span data-ttu-id="02c81-154">Aggiungere le seguenti direttive `using` all'inizio del file di codice, se non sono già presenti.</span><span class="sxs-lookup"><span data-stu-id="02c81-154">Add the following `using` directives at the top of the code file if they’re not already present.</span></span>  
  
    ```csharp  
    using System.Net.Http;  
    using System.Net;  
    using System.IO;  
    ```  
  
##  <a name="BKMK_CreatSynchApp"></a>   
###  <a name="synchronous"></a> <span data-ttu-id="02c81-155">Per creare un'applicazione sincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-155">To create a synchronous application</span></span>  
  
1.  <span data-ttu-id="02c81-156">Nella finestra di progettazione MainWindow.xaml fare doppio clic sul pulsante **Start** per creare il gestore eventi `startButton_Click` in MainWindow.xaml.cs.</span><span class="sxs-lookup"><span data-stu-id="02c81-156">In the design window, MainWindow.xaml, double-click the **Start** button to create the `startButton_Click` event handler in MainWindow.xaml.cs.</span></span>  
  
2.  <span data-ttu-id="02c81-157">In MainWindow.xaml.cs copiare il codice seguente nel corpo di `startButton_Click`:</span><span class="sxs-lookup"><span data-stu-id="02c81-157">In MainWindow.xaml.cs, copy the following code into the body of `startButton_Click`:</span></span>  
  
    ```csharp  
    resultsTextBox.Clear();  
    SumPageSizes();  
    resultsTextBox.Text += "\r\nControl returned to startButton_Click.";  
    ```  
  
     <span data-ttu-id="02c81-158">Il codice chiama il metodo che controlla l'applicazione `SumPageSizes` e visualizza un messaggio quando il controllo torna a `startButton_Click`.</span><span class="sxs-lookup"><span data-stu-id="02c81-158">The code calls the method that drives the application, `SumPageSizes`, and displays a message when control returns to `startButton_Click`.</span></span>  
  
3.  <span data-ttu-id="02c81-159">Il codice per la soluzione sincrona contiene i quattro metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c81-159">The code for the synchronous solution contains the following four methods:</span></span>  
  
    -   <span data-ttu-id="02c81-160">`SumPageSizes`, che ottiene un elenco di URL delle pagine Web da `SetUpURLList` e quindi chiama `GetURLContents` e `DisplayResults` per elaborare ogni URL.</span><span class="sxs-lookup"><span data-stu-id="02c81-160">`SumPageSizes`, which gets a list of webpage URLs from `SetUpURLList` and then calls `GetURLContents` and `DisplayResults` to process each URL.</span></span>  
  
    -   <span data-ttu-id="02c81-161">`SetUpURLList`, che crea e restituisce un elenco di indirizzi web.</span><span class="sxs-lookup"><span data-stu-id="02c81-161">`SetUpURLList`, which makes and returns a list of web addresses.</span></span>  
  
    -   <span data-ttu-id="02c81-162">`GetURLContents`, che scarica il contenuto di ogni sito Web e restituisce il contenuto come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="02c81-162">`GetURLContents`, which downloads the contents of each website and returns the contents as a byte array.</span></span>  
  
    -   <span data-ttu-id="02c81-163">`DisplayResults`, che visualizza il numero di byte nella matrice di byte per ogni URL.</span><span class="sxs-lookup"><span data-stu-id="02c81-163">`DisplayResults`, which displays  the number of bytes in the byte array for each URL.</span></span>  
  
     <span data-ttu-id="02c81-164">Copiare i quattro metodi seguenti e incollarli nel gestore eventi `startButton_Click` in MainWindow.xaml.cs:</span><span class="sxs-lookup"><span data-stu-id="02c81-164">Copy the following four methods, and then paste them under the `startButton_Click` event handler in MainWindow.xaml.cs:</span></span>  
  
    ```csharp  
    private void SumPageSizes()  
    {  
        // Make a list of web addresses.  
        List<string> urlList = SetUpURLList();   
  
        var total = 0;  
        foreach (var url in urlList)  
        {  
            // GetURLContents returns the contents of url as a byte array.  
            byte[] urlContents = GetURLContents(url);  
  
            DisplayResults(url, urlContents);  
  
            // Update the total.  
            total += urlContents.Length;  
        }  
  
        // Display the total count for all of the web addresses.  
        resultsTextBox.Text +=   
            string.Format("\r\n\r\nTotal bytes returned:  {0}\r\n", total);  
    }  
  
    private List<string> SetUpURLList()  
    {  
        var urls = new List<string>   
        {   
            "http://msdn.microsoft.com/library/windows/apps/br211380.aspx",  
            "http://msdn.microsoft.com",  
            "http://msdn.microsoft.com/library/hh290136.aspx",  
            "http://msdn.microsoft.com/library/ee256749.aspx",  
            "http://msdn.microsoft.com/library/hh290138.aspx",  
            "http://msdn.microsoft.com/library/hh290140.aspx",  
            "http://msdn.microsoft.com/library/dd470362.aspx",  
            "http://msdn.microsoft.com/library/aa578028.aspx",  
            "http://msdn.microsoft.com/library/ms404677.aspx",  
            "http://msdn.microsoft.com/library/ff730837.aspx"  
        };  
        return urls;  
    }  
  
    private byte[] GetURLContents(string url)  
    {  
        // The downloaded resource ends up in the variable named content.  
        var content = new MemoryStream();  
  
        // Initialize an HttpWebRequest for the current URL.  
        var webReq = (HttpWebRequest)WebRequest.Create(url);  
  
        // Send the request to the Internet resource and wait for  
        // the response.  
        // Note: you can't use HttpWebRequest.GetResponse in a Windows Store app.  
        using (WebResponse response = webReq.GetResponse())  
        {  
            // Get the data stream that is associated with the specified URL.  
            using (Stream responseStream = response.GetResponseStream())  
            {  
                // Read the bytes in responseStream and copy them to content.    
                responseStream.CopyTo(content);  
            }  
        }  
  
        // Return the result as a byte array.  
        return content.ToArray();  
    }  
  
    private void DisplayResults(string url, byte[] content)  
    {  
        // Display the length of each website. The string format   
        // is designed to be used with a monospaced font, such as  
        // Lucida Console or Global Monospace.  
        var bytes = content.Length;  
        // Strip off the "http://".  
        var displayURL = url.Replace("http://", "");  
        resultsTextBox.Text += string.Format("\n{0,-58} {1,8}", displayURL, bytes);  
    }  
    ```  
  
##  <a name="BKMK_TestSynchSol"></a>   
###  <a name="testSynch"></a> <span data-ttu-id="02c81-165">Per eseguire il test della soluzione sincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-165">To test the synchronous solution</span></span>  
  
1.  <span data-ttu-id="02c81-166">Premere il tasto F5 per eseguire il programma e quindi scegliere il pulsante **Start** .</span><span class="sxs-lookup"><span data-stu-id="02c81-166">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>  
  
     <span data-ttu-id="02c81-167">Verrà visualizzato un output simile all'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="02c81-167">Output that resembles the following list should appear.</span></span>  
  
    ```  
    msdn.microsoft.com/library/windows/apps/br211380.aspx        383832  
    msdn.microsoft.com                                            33964  
    msdn.microsoft.com/library/hh290136.aspx               225793  
    msdn.microsoft.com/library/ee256749.aspx               143577  
    msdn.microsoft.com/library/hh290138.aspx               237372  
    msdn.microsoft.com/library/hh290140.aspx               128279  
    msdn.microsoft.com/library/dd470362.aspx               157649  
    msdn.microsoft.com/library/aa578028.aspx               204457  
    msdn.microsoft.com/library/ms404677.aspx               176405  
    msdn.microsoft.com/library/ff730837.aspx               143474  
  
    Total bytes returned:  1834802  
  
    Control returned to startButton_Click.  
    ```  
  
     <span data-ttu-id="02c81-168">Si noti che sono necessari alcuni secondi per visualizzare i conteggi.</span><span class="sxs-lookup"><span data-stu-id="02c81-168">Notice that it takes a few seconds to display the counts.</span></span> <span data-ttu-id="02c81-169">Durante tale periodo, il thread dell'interfaccia utente viene bloccato mentre attende il download delle risorse richieste.</span><span class="sxs-lookup"><span data-stu-id="02c81-169">During that time, the UI thread is blocked while it waits for requested resources to download.</span></span> <span data-ttu-id="02c81-170">Di conseguenza, è possibile spostare, ingrandire, ridurre o chiudere la finestra di visualizzazione dopo aver scelto il  pulsante **Start**.</span><span class="sxs-lookup"><span data-stu-id="02c81-170">As a result, you can't move, maximize, minimize, or even close the display window after you choose the  **Start** button.</span></span> <span data-ttu-id="02c81-171">Queste operazioni hanno esito negativo finché non vengono visualizzati i conteggi dei byte.</span><span class="sxs-lookup"><span data-stu-id="02c81-171">These efforts fail until the byte counts start to appear.</span></span> <span data-ttu-id="02c81-172">Se un sito Web non risponde, non si ha alcuna indicazione relativa al sito con esito negativo.</span><span class="sxs-lookup"><span data-stu-id="02c81-172">If a website isn’t responding, you have no indication of which site failed.</span></span> <span data-ttu-id="02c81-173">È inoltre difficile interrompere l'attesa e chiudere il programma.</span><span class="sxs-lookup"><span data-stu-id="02c81-173">It is difficult even to stop waiting and close the program.</span></span>  
  
##  <a name="BKMK_ConvertGtBtArr"></a>   
###  <a name="GetURLContents"></a> <span data-ttu-id="02c81-174">Per convertire GetURLContents in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-174">To convert GetURLContents to an asynchronous method</span></span>  
  
1.  <span data-ttu-id="02c81-175">Per convertire la soluzione sincrona in una soluzione asincrona, il punto di partenza migliore è in `GetURLContents` perché le chiamate al metodo <xref:System.Net.HttpWebRequest><xref:System.Net.HttpWebRequest.GetResponse%2A> e al metodo <xref:System.IO.Stream><xref:System.IO.Stream.CopyTo%2A> sono i punti in cui l'applicazione accede al Web.</span><span class="sxs-lookup"><span data-stu-id="02c81-175">To convert the synchronous solution to an asynchronous solution, the best place to start is in `GetURLContents` because the calls to the <xref:System.Net.HttpWebRequest> method <xref:System.Net.HttpWebRequest.GetResponse%2A> and to the <xref:System.IO.Stream> method <xref:System.IO.Stream.CopyTo%2A> are where the application accesses the web.</span></span> <span data-ttu-id="02c81-176">.NET Framework semplifica la conversione fornendo versioni asincrone di entrambi i metodi.</span><span class="sxs-lookup"><span data-stu-id="02c81-176">The .NET Framework makes the conversion easy by supplying asynchronous versions of both methods.</span></span>  
  
     <span data-ttu-id="02c81-177">Per altre informazioni sui modelli usati in `GetURLContents`, vedere <xref:System.Net.WebRequest>.</span><span class="sxs-lookup"><span data-stu-id="02c81-177">For more information about the methods that are used in `GetURLContents`, see <xref:System.Net.WebRequest>.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="02c81-178">Mentre si esegue la procedura descritta in questa procedura dettagliata, vengono visualizzati diversi errori del compilatore.</span><span class="sxs-lookup"><span data-stu-id="02c81-178">As you follow the steps in this walkthrough, several compiler errors appear.</span></span> <span data-ttu-id="02c81-179">È possibile ignorarli e continuare con la procedura dettagliata.</span><span class="sxs-lookup"><span data-stu-id="02c81-179">You can ignore them and continue with the walkthrough.</span></span>  
  
     <span data-ttu-id="02c81-180">Modificare il metodo chiamato nella terza riga di `GetURLContents` da `GetResponse` nel metodo asincrono basato su attività <xref:System.Net.WebRequest.GetResponseAsync%2A>.</span><span class="sxs-lookup"><span data-stu-id="02c81-180">Change the method that's called in the third line of `GetURLContents` from `GetResponse` to the asynchronous, task-based <xref:System.Net.WebRequest.GetResponseAsync%2A> method.</span></span>  
  
    ```csharp  
    using (WebResponse response = webReq.GetResponseAsync())  
    ```  
  
2.  <span data-ttu-id="02c81-181">`GetResponseAsync` restituisce <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="02c81-181">`GetResponseAsync` returns a <xref:System.Threading.Tasks.Task%601>.</span></span> <span data-ttu-id="02c81-182">In questo caso, la *variabile di restituzione dell'attività*, `TResult`, è di tipo <xref:System.Net.WebResponse>.</span><span class="sxs-lookup"><span data-stu-id="02c81-182">In this case, the *task return variable*, `TResult`, has type <xref:System.Net.WebResponse>.</span></span> <span data-ttu-id="02c81-183">L'attività rappresenta una promessa di creazione di un oggetto `WebResponse` effettivo dopo il download dei dati richiesti e il completamento dell'esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="02c81-183">The task is a promise to produce an actual `WebResponse` object after the requested data has been downloaded and the task has run to completion.</span></span>  
  
     <span data-ttu-id="02c81-184">Per recuperare il valore `WebResponse` dall'attività, applicare un operatore [await](../../../../csharp/language-reference/keywords/await.md) alla chiamata di `GetResponseAsync`, come mostrato nel codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="02c81-184">To retrieve the `WebResponse` value from the task, apply an [await](../../../../csharp/language-reference/keywords/await.md) operator to the call to `GetResponseAsync`, as the following code shows.</span></span>  
  
    ```csharp  
    using (WebResponse response = await webReq.GetResponseAsync())  
    ```  
  
     <span data-ttu-id="02c81-185">L'operatore `GetURLContents` sospende l'esecuzione del metodo corrente `await` fino al completamento dell'attività attesa.</span><span class="sxs-lookup"><span data-stu-id="02c81-185">The `await` operator suspends the execution of the current method, `GetURLContents`, until the awaited task is complete.</span></span> <span data-ttu-id="02c81-186">Nel frattempo il controllo viene restituito al chiamante del metodo asincrono.</span><span class="sxs-lookup"><span data-stu-id="02c81-186">In the meantime, control returns to the caller of the current method.</span></span> <span data-ttu-id="02c81-187">In questo esempio, il metodo corrente è `GetURLContents` e il chiamante è `SumPageSizes`.</span><span class="sxs-lookup"><span data-stu-id="02c81-187">In this example, the current method is `GetURLContents`, and the caller is `SumPageSizes`.</span></span> <span data-ttu-id="02c81-188">Quando l'attività è terminata, l'oggetto promesso `WebResponse` viene generato come valore dell'attività attesa e assegnato alla variabile `response`.</span><span class="sxs-lookup"><span data-stu-id="02c81-188">When the task is finished, the promised `WebResponse` object is produced as the value of the awaited task and assigned to the variable `response`.</span></span>  
  
     <span data-ttu-id="02c81-189">L'istruzione precedente può essere suddivisa nelle due istruzioni seguenti per chiarire cosa accade.</span><span class="sxs-lookup"><span data-stu-id="02c81-189">The previous statement can be separated into the following two statements to clarify what happens.</span></span>  
  
    ```csharp  
    //Task<WebResponse> responseTask = webReq.GetResponseAsync();  
    //using (WebResponse response = await responseTask)  
    ```  
  
     <span data-ttu-id="02c81-190">La chiamata a `webReq.GetResponseAsync` restituisce `Task(Of WebResponse)` o `Task<WebResponse>`.</span><span class="sxs-lookup"><span data-stu-id="02c81-190">The call to `webReq.GetResponseAsync` returns a `Task(Of WebResponse)` or `Task<WebResponse>`.</span></span> <span data-ttu-id="02c81-191">Viene quindi applicato un operatore await all'attività per recuperare il valore `WebResponse`.</span><span class="sxs-lookup"><span data-stu-id="02c81-191">Then an await operator is applied to the task to retrieve the `WebResponse` value.</span></span>  
  
     <span data-ttu-id="02c81-192">Se il metodo asincrono ha operazioni da eseguire che non dipendono dal completamento dell'attività, il metodo può continuare l'esecuzione tra queste due istruzioni, dopo la chiamata al metodo asincrono e prima che venga applicato l'operatore `await`.</span><span class="sxs-lookup"><span data-stu-id="02c81-192">If your async method has work to do that doesn’t depend on the completion of the task, the method can continue with that work between these two statements, after the call to the async method and before the `await` operator is applied.</span></span> <span data-ttu-id="02c81-193">Per esempi, vedere [Procedura: Eseguire più richieste Web in parallelo tramite async e await (C#)](../../../../csharp/programming-guide/concepts/async/how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md) e [Procedura: Estendere la procedura dettagliata asincrona usando Task.WhenAll (C#)](../../../../csharp/programming-guide/concepts/async/how-to-extend-the-async-walkthrough-by-using-task-whenall.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-193">For examples, see [How to: Make Multiple Web Requests in Parallel by Using async and await (C#)](../../../../csharp/programming-guide/concepts/async/how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md) and [How to: Extend the async Walkthrough by Using Task.WhenAll (C#)](../../../../csharp/programming-guide/concepts/async/how-to-extend-the-async-walkthrough-by-using-task-whenall.md).</span></span>  
  
3.  <span data-ttu-id="02c81-194">Poiché è stato aggiunto l'operatore `await` nel passaggio precedente, verrà generato un errore del compilatore.</span><span class="sxs-lookup"><span data-stu-id="02c81-194">Because you added the `await` operator in the previous step, a compiler error occurs.</span></span> <span data-ttu-id="02c81-195">L'operatore può essere usato solo nei metodi contrassegnati con il modificatore [async](../../../../csharp/language-reference/keywords/async.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-195">The operator can be used only in methods that are marked with the [async](../../../../csharp/language-reference/keywords/async.md) modifier.</span></span> <span data-ttu-id="02c81-196">Ignorare l'errore mentre vengono ripetuti i passaggi di conversione per sostituire la chiamata a `CopyTo` con una chiamata a `CopyToAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-196">Ignore the error while you repeat the conversion steps to replace the call to `CopyTo` with a call to `CopyToAsync`.</span></span>  
  
    -   <span data-ttu-id="02c81-197">Modificare il nome del metodo chiamato in <xref:System.IO.Stream.CopyToAsync%2A>.</span><span class="sxs-lookup"><span data-stu-id="02c81-197">Change the name of the method that’s called to <xref:System.IO.Stream.CopyToAsync%2A>.</span></span>  
  
    -   <span data-ttu-id="02c81-198">Il metodo `CopyTo` o `CopyToAsync` copia i byte nel relativo argomento `content` e non restituisce un valore significativo.</span><span class="sxs-lookup"><span data-stu-id="02c81-198">The `CopyTo` or `CopyToAsync` method copies bytes to its argument, `content`, and doesn’t return a meaningful value.</span></span> <span data-ttu-id="02c81-199">Nella versione sincrona, la chiamata a `CopyTo` è un'istruzione semplice che non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="02c81-199">In the synchronous version, the call to `CopyTo` is a simple statement that doesn't return a value.</span></span> <span data-ttu-id="02c81-200">La versione asincrona `CopyToAsync` restituisce <xref:System.Threading.Tasks.Task>.</span><span class="sxs-lookup"><span data-stu-id="02c81-200">The asynchronous version, `CopyToAsync`, returns a <xref:System.Threading.Tasks.Task>.</span></span> <span data-ttu-id="02c81-201">L'attività è analoga a "Task(void)" e consente l'attesa del metodo.</span><span class="sxs-lookup"><span data-stu-id="02c81-201">The task functions like "Task(void)" and enables the method to be awaited.</span></span> <span data-ttu-id="02c81-202">Applicare `Await` o `await` alla chiamata a `CopyToAsync`, come mostrato nel codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="02c81-202">Apply `Await` or `await` to the call to `CopyToAsync`, as the following code shows.</span></span>  
  
        ```csharp  
        await responseStream.CopyToAsync(content);  
        ```  
  
         <span data-ttu-id="02c81-203">L'istruzione precedente abbrevia le due righe di codice riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="02c81-203">The previous statement abbreviates the following two lines of code.</span></span>  
  
        ```csharp  
        // CopyToAsync returns a Task, not a Task<T>.  
        //Task copyTask = responseStream.CopyToAsync(content);  
  
        // When copyTask is completed, content contains a copy of  
        // responseStream.  
        //await copyTask;  
        ```  
  
4.  <span data-ttu-id="02c81-204">A questo punto, non rimane che modificare la firma del metodo in `GetURLContents`.</span><span class="sxs-lookup"><span data-stu-id="02c81-204">All that remains to be done in `GetURLContents` is to adjust the method signature.</span></span> <span data-ttu-id="02c81-205">È possibile usare l'operatore `await` solo nei metodi contrassegnati con il modificatore [async](../../../../csharp/language-reference/keywords/async.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-205">You can use the `await` operator only in methods that are marked with the [async](../../../../csharp/language-reference/keywords/async.md) modifier.</span></span> <span data-ttu-id="02c81-206">Aggiungere il modificatore per contrassegnare il metodo come *metodo async*, come mostrato nel codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="02c81-206">Add the modifier to mark the method as an *async method*, as the following code shows.</span></span>  
  
    ```csharp  
    private async byte[] GetURLContents(string url)  
    ```  
  
5.  <span data-ttu-id="02c81-207">Il tipo restituito di un metodo asincrono può essere solo <xref:System.Threading.Tasks.Task>, <xref:System.Threading.Tasks.Task%601> o `void` in C#.</span><span class="sxs-lookup"><span data-stu-id="02c81-207">The return type of an async method can only be <xref:System.Threading.Tasks.Task>, <xref:System.Threading.Tasks.Task%601>, or `void` in C#.</span></span> <span data-ttu-id="02c81-208">In genere il tipo restituito `void` si usa solo in un gestore eventi asincrono, dove `void` è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="02c81-208">Typically, a return type of `void` is used only in an async event handler, where `void` is required.</span></span> <span data-ttu-id="02c81-209">In altri casi è possibile usare `Task(T)` se il metodo completato include un'istruzione [return](../../../../csharp/language-reference/keywords/return.md) che restituisce un valore di tipo T e si usa `Task` se il metodo completato non restituisce un valore significativo.</span><span class="sxs-lookup"><span data-stu-id="02c81-209">In other cases, you use `Task(T)` if the completed method has a [return](../../../../csharp/language-reference/keywords/return.md) statement that returns a value of type T, and you use `Task` if the completed method doesn’t return a meaningful value.</span></span> <span data-ttu-id="02c81-210">È possibile considerare il tipo restituito `Task` come avente lo stesso significato di "Task(void)".</span><span class="sxs-lookup"><span data-stu-id="02c81-210">You can think of the `Task` return type as meaning "Task(void)."</span></span>  
  
     <span data-ttu-id="02c81-211">Per altre informazioni, vedere [Tipi restituiti asincroni (C#)](../../../../csharp/programming-guide/concepts/async/async-return-types.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-211">For more information, see [Async Return Types (C#)](../../../../csharp/programming-guide/concepts/async/async-return-types.md).</span></span>  
  
     <span data-ttu-id="02c81-212">Il metodo `GetURLContents` dispone di un'istruzione return che restituisce una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="02c81-212">Method `GetURLContents` has a return statement, and the statement returns a byte array.</span></span> <span data-ttu-id="02c81-213">Pertanto, il tipo restituito della versione asincrona è Task(T), dove T è una matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="02c81-213">Therefore, the return type of the async version is Task(T), where T is a byte array.</span></span> <span data-ttu-id="02c81-214">Apportare le modifiche seguenti nella firma del metodo:</span><span class="sxs-lookup"><span data-stu-id="02c81-214">Make the following changes in the method signature:</span></span>  
  
    -   <span data-ttu-id="02c81-215">Cambiare il tipo restituito in `Task<byte[]>`.</span><span class="sxs-lookup"><span data-stu-id="02c81-215">Change the return type to `Task<byte[]>`.</span></span>  
  
    -   <span data-ttu-id="02c81-216">Per convenzione, i metodi asincroni presentano nomi che terminano in "Async". Rinominare pertanto il metodo `GetURLContentsAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-216">By convention, asynchronous methods have names that end in "Async," so rename the method `GetURLContentsAsync`.</span></span>  
  
     <span data-ttu-id="02c81-217">Nel codice seguente sono illustrate queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="02c81-217">The following code shows these changes.</span></span>  
  
    ```csharp  
    private async Task<byte[]> GetURLContentsAsync(string url)  
    ```  
  
     <span data-ttu-id="02c81-218">Dopo aver apportato queste modifiche, la conversione di `GetURLContents` in un metodo asincrono è completa.</span><span class="sxs-lookup"><span data-stu-id="02c81-218">With those few changes, the conversion of `GetURLContents` to an asynchronous method is complete.</span></span>  
  
##  <a name="BKMK_ConvertSumPagSzs"></a>   
###  <a name="SumPageSizes"></a> <span data-ttu-id="02c81-219">Per Convertire SumPageSizes in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-219">To convert SumPageSizes to an asynchronous method</span></span>  
  
1.  <span data-ttu-id="02c81-220">Ripetere i passaggi della procedura precedente per `SumPageSizes`.</span><span class="sxs-lookup"><span data-stu-id="02c81-220">Repeat the steps from the previous procedure for `SumPageSizes`.</span></span> <span data-ttu-id="02c81-221">In primo luogo, modificare la chiamata a `GetURLContents` in una chiamata asincrona.</span><span class="sxs-lookup"><span data-stu-id="02c81-221">First, change the call to `GetURLContents` to an asynchronous call.</span></span>  
  
    -   <span data-ttu-id="02c81-222">Modificare il nome del metodo chiamato da `GetURLContents` in `GetURLContentsAsync`, se non è ancora stato fatto.</span><span class="sxs-lookup"><span data-stu-id="02c81-222">Change the name of the method that’s called from `GetURLContents` to `GetURLContentsAsync`, if you haven't already done so.</span></span>  
  
    -   <span data-ttu-id="02c81-223">Applicare `await` all'attività restituita da `GetURLContentsAsync` per ottenere il valore della matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="02c81-223">Apply `await` to the task that `GetURLContentsAsync` returns to obtain the byte array value.</span></span>  
  
     <span data-ttu-id="02c81-224">Nel codice seguente sono illustrate queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="02c81-224">The following code shows these changes.</span></span>  
  
    ```csharp  
    byte[] urlContents = await GetURLContentsAsync(url);  
    ```  
  
     <span data-ttu-id="02c81-225">L'assegnazione precedente abbrevia le due righe di codice riportate di seguito.</span><span class="sxs-lookup"><span data-stu-id="02c81-225">The previous assignment abbreviates the following two lines of code.</span></span>  
  
    ```csharp  
    // GetURLContentsAsync returns a Task<T>. At completion, the task  
    // produces a byte array.  
    //Task<byte[]> getContentsTask = GetURLContentsAsync(url);  
    //byte[] urlContents = await getContentsTask;  
    ```  
  
2.  <span data-ttu-id="02c81-226">Apportare le modifiche seguenti nella firma del metodo:</span><span class="sxs-lookup"><span data-stu-id="02c81-226">Make the following changes in the method's signature:</span></span>  
  
    -   <span data-ttu-id="02c81-227">Contrassegnare il metodo con il modificatore `async`.</span><span class="sxs-lookup"><span data-stu-id="02c81-227">Mark the method with the `async` modifier.</span></span>  
  
    -   <span data-ttu-id="02c81-228">Aggiungere "Async" al nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="02c81-228">Add "Async" to the method name.</span></span>  
  
    -   <span data-ttu-id="02c81-229">In questo caso non esiste alcuna variabile di restituzione dell'attività, T, perché `SumPageSizesAsync` non restituisce un valore per T. Il metodo non ha alcuna istruzione `return`. Tuttavia, il metodo deve restituire `Task` per poter essere un metodo di tipo awaitable.</span><span class="sxs-lookup"><span data-stu-id="02c81-229">There is no task return variable, T, this time because `SumPageSizesAsync` doesn’t return a value for T. (The method has no `return` statement.) However, the method must return a `Task` to be awaitable.</span></span> <span data-ttu-id="02c81-230">Cambiare quindi il tipo restituito del metodo da `void` in `Task`.</span><span class="sxs-lookup"><span data-stu-id="02c81-230">Therefore, change the return type of the method from `void` to `Task`.</span></span>  
  
     <span data-ttu-id="02c81-231">Nel codice seguente sono illustrate queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="02c81-231">The following code shows these changes.</span></span>  
  
    ```csharp  
    private async Task SumPageSizesAsync()  
    ```  
  
     <span data-ttu-id="02c81-232">La conversione di `SumPageSizes` in `SumPageSizesAsync` è completa.</span><span class="sxs-lookup"><span data-stu-id="02c81-232">The conversion of `SumPageSizes` to `SumPageSizesAsync` is complete.</span></span>  
  
##  <a name="BKMK_Cnvrtbttn1"></a>   
###  <a name="startButton"></a> <span data-ttu-id="02c81-233">Per convertire startButton_Click in un metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="02c81-233">To convert startButton_Click to an asynchronous method</span></span>  
  
1.  <span data-ttu-id="02c81-234">Nel gestore eventi modificare il nome del metodo chiamato da `SumPageSizes` in `SumPageSizesAsync`, se non è ancora stato fatto.</span><span class="sxs-lookup"><span data-stu-id="02c81-234">In the event handler, change the name of the called method from `SumPageSizes` to `SumPageSizesAsync`, if you haven’t already done so.</span></span>  
  
2.  <span data-ttu-id="02c81-235">Poiché `SumPageSizesAsync` è un metodo asincrono, modificare il codice nel gestore eventi in modo che attenda il risultato.</span><span class="sxs-lookup"><span data-stu-id="02c81-235">Because `SumPageSizesAsync` is an async method, change the code in the event handler to await the result.</span></span>  
  
     <span data-ttu-id="02c81-236">La chiamata a `SumPageSizesAsync` rispecchia la chiamata a `CopyToAsync` in `GetURLContentsAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-236">The call to `SumPageSizesAsync` mirrors the call to `CopyToAsync` in `GetURLContentsAsync`.</span></span> <span data-ttu-id="02c81-237">La chiamata restituisce `Task` e non `Task(T)`.</span><span class="sxs-lookup"><span data-stu-id="02c81-237">The call returns a `Task`, not a `Task(T)`.</span></span>  
  
     <span data-ttu-id="02c81-238">Come nelle procedure precedenti, è possibile convertire la chiamata tramite una o due istruzioni.</span><span class="sxs-lookup"><span data-stu-id="02c81-238">As in previous procedures, you can convert the call by using one statement or two statements.</span></span> <span data-ttu-id="02c81-239">Nel codice seguente sono illustrate queste modifiche.</span><span class="sxs-lookup"><span data-stu-id="02c81-239">The following code shows these changes.</span></span>  
  
    ```csharp  
    // One-step async call.  
    await SumPageSizesAsync();  
  
    // Two-step async call.  
    //Task sumTask = SumPageSizesAsync();  
    //await sumTask;  
    ```  
  
3.  <span data-ttu-id="02c81-240">Per impedire la reentrancy accidentale dell'operazione, aggiungere l'istruzione seguente all'inizio di `startButton_Click` per disabilitare il pulsante **Start**.</span><span class="sxs-lookup"><span data-stu-id="02c81-240">To prevent accidentally reentering the operation, add the following statement at the top of `startButton_Click` to disable the **Start** button.</span></span>  
  
    ```csharp  
    // Disable the button until the operation is complete.  
    startButton.IsEnabled = false;  
    ```  
  
     <span data-ttu-id="02c81-241">È possibile riabilitare il pulsante alla fine del gestore eventi.</span><span class="sxs-lookup"><span data-stu-id="02c81-241">You can reenable the button at the end of the event handler.</span></span>  
  
    ```csharp  
    // Reenable the button in case you want to run the operation again.  
    startButton.IsEnabled = true;  
    ```  
  
     <span data-ttu-id="02c81-242">Per altre informazioni sulla reentrancy, vedere [Gestione della reentrancy nelle applicazioni asincrone (C#)](../../../../csharp/programming-guide/concepts/async/handling-reentrancy-in-async-apps.md).</span><span class="sxs-lookup"><span data-stu-id="02c81-242">For more information about reentrancy, see [Handling Reentrancy in Async Apps (C#)](../../../../csharp/programming-guide/concepts/async/handling-reentrancy-in-async-apps.md).</span></span>  
  
4.  <span data-ttu-id="02c81-243">Aggiungere infine il modificatore `async` alla dichiarazione, in modo che il gestore eventi possa attendere `SumPagSizesAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-243">Finally, add the `async` modifier to the declaration so that the event handler can await `SumPagSizesAsync`.</span></span>  
  
    ```csharp  
    private async void startButton_Click(object sender, RoutedEventArgs e)  
    ```  
  
     <span data-ttu-id="02c81-244">In genere, i nomi dei gestori eventi non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="02c81-244">Typically, the names of event handlers aren’t changed.</span></span> <span data-ttu-id="02c81-245">Il tipo restituito non viene modificato in `Task` perché i gestori evento devono restituire `void`.</span><span class="sxs-lookup"><span data-stu-id="02c81-245">The return type isn’t changed to `Task` because event handlers must return `void`.</span></span>  
  
     <span data-ttu-id="02c81-246">La conversione del progetto dall'elaborazione sincrona a quella asincrona è completa.</span><span class="sxs-lookup"><span data-stu-id="02c81-246">The conversion of the project from synchronous to asynchronous processing is complete.</span></span>  
  
##  <a name="BKMK_testAsynchSolution"></a>   
###  <a name="testAsynch"></a> <span data-ttu-id="02c81-247">Per eseguire il test della soluzione asincrona</span><span class="sxs-lookup"><span data-stu-id="02c81-247">To test the asynchronous solution</span></span>  
  
1.  <span data-ttu-id="02c81-248">Premere il tasto F5 per eseguire il programma e quindi scegliere il pulsante **Start** .</span><span class="sxs-lookup"><span data-stu-id="02c81-248">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>  
  
2.  <span data-ttu-id="02c81-249">Viene visualizzato un output simile all'output della soluzione sincrona.</span><span class="sxs-lookup"><span data-stu-id="02c81-249">Output that resembles the output of the synchronous solution should appear.</span></span> <span data-ttu-id="02c81-250">Esistono tuttavia le differenze seguenti:</span><span class="sxs-lookup"><span data-stu-id="02c81-250">However, notice the following differences.</span></span>  
  
    -   <span data-ttu-id="02c81-251">I risultati non vengono restituiti contemporaneamente, al termine dell'elaborazione.</span><span class="sxs-lookup"><span data-stu-id="02c81-251">The results don’t all occur at the same time, after the processing is complete.</span></span> <span data-ttu-id="02c81-252">Ad esempio, entrambi i programmi contengono una riga in `startButton_Click` che consente di cancellare la casella di testo.</span><span class="sxs-lookup"><span data-stu-id="02c81-252">For example, both programs contain a line in `startButton_Click` that clears the text box.</span></span> <span data-ttu-id="02c81-253">Lo scopo è quello di cancellare il contenuto della casella di testo tra le esecuzioni se si sceglie il pulsante **Start** per la seconda volta, dopo la visualizzazione di un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="02c81-253">The intent is to clear the text box between runs if you choose the **Start** button for a second time, after one set of results has appeared.</span></span> <span data-ttu-id="02c81-254">Nella versione sincrona la casella di testo viene cancellata prima della seconda visualizzazione dei conteggi, ovvero quando vengono completati i download e il thread dell'interfaccia utente è libero di eseguire altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="02c81-254">In the synchronous version, the text box is cleared just before the counts appear for the second time, when the downloads are completed and the UI thread is free to do other work.</span></span> <span data-ttu-id="02c81-255">Nella versione asincrona, la casella di testo viene cancellata subito dopo aver scelto il pulsante **Start**.</span><span class="sxs-lookup"><span data-stu-id="02c81-255">In the asynchronous version, the text box clears immediately after you choose the **Start** button.</span></span>  
  
    -   <span data-ttu-id="02c81-256">È importante notare che il thread dell'interfaccia utente non è bloccato durante il download.</span><span class="sxs-lookup"><span data-stu-id="02c81-256">Most importantly, the UI thread isn’t blocked during the downloads.</span></span> <span data-ttu-id="02c81-257">È possibile spostare o ridimensionare la finestra durante il download, il conteggio e la visualizzazione delle risorse Web.</span><span class="sxs-lookup"><span data-stu-id="02c81-257">You can move or resize the window while the web resources are being downloaded, counted, and displayed.</span></span> <span data-ttu-id="02c81-258">Se uno dei siti Web è lento o non risponde, è possibile annullare l'operazione scegliendo il pulsante **Chiudi** (il simbolo x su sfondo rosso nell'angolo superiore destro).</span><span class="sxs-lookup"><span data-stu-id="02c81-258">If one of the websites is slow or not responding, you can cancel the operation by choosing the **Close** button (the x in the red field in the upper-right corner).</span></span>  
  
##  <a name="BKMK_ReplaceGetByteArrayAsync"></a>   
###  <a name="GetURLContentsAsync"></a> <span data-ttu-id="02c81-259">Per sostituire GetURLContentsAsync con un metodo .NET Framework</span><span class="sxs-lookup"><span data-stu-id="02c81-259">To replace method GetURLContentsAsync with a .NET Framework method</span></span>  
  
1.  <span data-ttu-id="02c81-260">.NET Framework 4.5 fornisce molti metodi asincroni che è possibile usare.</span><span class="sxs-lookup"><span data-stu-id="02c81-260">The .NET Framework 4.5 provides many async methods that you can use.</span></span> <span data-ttu-id="02c81-261">Uno di essi, il <xref:System.Net.Http.HttpClient> metodo <xref:System.Net.Http.HttpClient.GetByteArrayAsync%28System.String%29>, risulta utile in modo specifico per questa procedura dettagliata.</span><span class="sxs-lookup"><span data-stu-id="02c81-261">One of them, the <xref:System.Net.Http.HttpClient> method <xref:System.Net.Http.HttpClient.GetByteArrayAsync%28System.String%29>, does just what you need for this walkthrough.</span></span> <span data-ttu-id="02c81-262">È possibile usarlo al posto del metodo `GetURLContentsAsync` creato in una procedura precedente.</span><span class="sxs-lookup"><span data-stu-id="02c81-262">You can use it instead of the `GetURLContentsAsync` method that you created in an earlier procedure.</span></span>  
  
     <span data-ttu-id="02c81-263">Il primo passaggio consiste nel creare un oggetto `HttpClient` nel metodo `SumPageSizesAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-263">The first step is to create an `HttpClient` object in method `SumPageSizesAsync`.</span></span> <span data-ttu-id="02c81-264">Aggiungere la dichiarazione seguente all'inizio del metodo.</span><span class="sxs-lookup"><span data-stu-id="02c81-264">Add the following declaration at the start of the method.</span></span>  
  
    ```csharp  
    // Declare an HttpClient object and increase the buffer size. The  
    // default buffer size is 65,536.  
    HttpClient client =  
        new HttpClient() { MaxResponseContentBufferSize = 1000000 };  
    ```  
  
2.  <span data-ttu-id="02c81-265">In `SumPageSizesAsync,` sostituire la chiamata al metodo `GetURLContentsAsync` con una chiamata al metodo `HttpClient`.</span><span class="sxs-lookup"><span data-stu-id="02c81-265">In `SumPageSizesAsync,` replace the call to your `GetURLContentsAsync` method with a call to the `HttpClient` method.</span></span>  
  
    ```csharp  
    byte[] urlContents = await client.GetByteArrayAsync(url);  
    ```  
  
3.  <span data-ttu-id="02c81-266">Rimuovere o impostare come commento il metodo `GetURLContentsAsync` precedentemente scritto.</span><span class="sxs-lookup"><span data-stu-id="02c81-266">Remove or comment out the `GetURLContentsAsync` method that you wrote.</span></span>  
  
4.  <span data-ttu-id="02c81-267">Premere il tasto F5 per eseguire il programma e quindi scegliere il pulsante **Start** .</span><span class="sxs-lookup"><span data-stu-id="02c81-267">Choose the F5 key to run the program, and then choose the **Start** button.</span></span>  
  
     <span data-ttu-id="02c81-268">Il comportamento di questa versione del progetto deve corrispondere al comportamento descritto nella procedura "Per eseguire il test della soluzione asincrona" ma con un intervento ridotto da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="02c81-268">The behavior of this version of the project should match the behavior that the "To test the asynchronous solution" procedure describes but with even less effort from you.</span></span>  
  
##  <a name="BKMK_CompleteCodeExamples"></a> <span data-ttu-id="02c81-269">Esempio</span><span class="sxs-lookup"><span data-stu-id="02c81-269">Example</span></span>  
 <span data-ttu-id="02c81-270">Il codice seguente contiene l'esempio completo della conversione da soluzione sincrona a soluzione asincrona usando il metodo `GetURLContentsAsync` asincrono precedentemente scritto.</span><span class="sxs-lookup"><span data-stu-id="02c81-270">The following code contains the full example of the conversion from a synchronous to an asynchronous solution by using the asynchronous `GetURLContentsAsync` method that you wrote.</span></span> <span data-ttu-id="02c81-271">Si noti che è molto simile alla soluzione sincrona originale.</span><span class="sxs-lookup"><span data-stu-id="02c81-271">Notice that it strongly resembles the original, synchronous solution.</span></span>  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Threading.Tasks;  
using System.Windows;  
using System.Windows.Controls;  
using System.Windows.Data;  
using System.Windows.Documents;  
using System.Windows.Input;  
using System.Windows.Media;  
using System.Windows.Media.Imaging;  
using System.Windows.Navigation;  
using System.Windows.Shapes;  
  
// Add the following using directives, and add a reference for System.Net.Http.  
using System.Net.Http;  
using System.IO;  
using System.Net;  
  
namespace AsyncExampleWPF  
{  
    public partial class MainWindow : Window  
    {  
        public MainWindow()  
        {  
            InitializeComponent();  
        }  
  
        private async void startButton_Click(object sender, RoutedEventArgs e)  
        {  
            // Disable the button until the operation is complete.  
            startButton.IsEnabled = false;  
  
            resultsTextBox.Clear();  
  
            // One-step async call.  
            await SumPageSizesAsync();  
  
            // Two-step async call.  
            //Task sumTask = SumPageSizesAsync();  
            //await sumTask;  
  
            resultsTextBox.Text += "\r\nControl returned to startButton_Click.\r\n";  
  
            // Reenable the button in case you want to run the operation again.  
            startButton.IsEnabled = true;  
        }  
  
        private async Task SumPageSizesAsync()  
        {  
            // Make a list of web addresses.  
            List<string> urlList = SetUpURLList();  
  
            var total = 0;  
  
            foreach (var url in urlList)  
            {  
                byte[] urlContents = await GetURLContentsAsync(url);  
  
                // The previous line abbreviates the following two assignment statements.  
  
                // GetURLContentsAsync returns a Task<T>. At completion, the task  
                // produces a byte array.  
                //Task<byte[]> getContentsTask = GetURLContentsAsync(url);  
                //byte[] urlContents = await getContentsTask;  
  
                DisplayResults(url, urlContents);  
  
                // Update the total.            
                total += urlContents.Length;  
            }  
            // Display the total count for all of the websites.  
            resultsTextBox.Text +=  
                string.Format("\r\n\r\nTotal bytes returned:  {0}\r\n", total);  
        }  
  
        private List<string> SetUpURLList()  
        {  
            List<string> urls = new List<string>   
            {   
                "http://msdn.microsoft.com/library/windows/apps/br211380.aspx",  
                "http://msdn.microsoft.com",  
                "http://msdn.microsoft.com/library/hh290136.aspx",  
                "http://msdn.microsoft.com/library/ee256749.aspx",  
                "http://msdn.microsoft.com/library/hh290138.aspx",  
                "http://msdn.microsoft.com/library/hh290140.aspx",  
                "http://msdn.microsoft.com/library/dd470362.aspx",  
                "http://msdn.microsoft.com/library/aa578028.aspx",  
                "http://msdn.microsoft.com/library/ms404677.aspx",  
                "http://msdn.microsoft.com/library/ff730837.aspx"  
            };  
            return urls;  
        }  
  
        private async Task<byte[]> GetURLContentsAsync(string url)  
        {  
            // The downloaded resource ends up in the variable named content.  
            var content = new MemoryStream();  
  
            // Initialize an HttpWebRequest for the current URL.  
            var webReq = (HttpWebRequest)WebRequest.Create(url);  
  
            // Send the request to the Internet resource and wait for  
            // the response.                  
            using (WebResponse response = await webReq.GetResponseAsync())  
  
            // The previous statement abbreviates the following two statements.  
  
            //Task<WebResponse> responseTask = webReq.GetResponseAsync();  
            //using (WebResponse response = await responseTask)  
            {  
                // Get the data stream that is associated with the specified url.  
                using (Stream responseStream = response.GetResponseStream())  
                {  
                    // Read the bytes in responseStream and copy them to content.   
                    await responseStream.CopyToAsync(content);  
  
                    // The previous statement abbreviates the following two statements.  
  
                    // CopyToAsync returns a Task, not a Task<T>.  
                    //Task copyTask = responseStream.CopyToAsync(content);  
  
                    // When copyTask is completed, content contains a copy of  
                    // responseStream.  
                    //await copyTask;  
                }  
            }  
            // Return the result as a byte array.  
            return content.ToArray();  
        }  
  
        private void DisplayResults(string url, byte[] content)  
        {  
            // Display the length of each website. The string format   
            // is designed to be used with a monospaced font, such as  
            // Lucida Console or Global Monospace.  
            var bytes = content.Length;  
            // Strip off the "http://".  
            var displayURL = url.Replace("http://", "");  
            resultsTextBox.Text += string.Format("\n{0,-58} {1,8}", displayURL, bytes);  
        }  
    }  
}  
```  
  
 <span data-ttu-id="02c81-272">Il codice seguente contiene l'esempio completo della soluzione che usa il metodo `HttpClient`, `GetByteArrayAsync`.</span><span class="sxs-lookup"><span data-stu-id="02c81-272">The following code contains the full example of the solution that uses the `HttpClient` method, `GetByteArrayAsync`.</span></span>  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using System.Text;  
using System.Threading.Tasks;  
using System.Windows;  
using System.Windows.Controls;  
using System.Windows.Data;  
using System.Windows.Documents;  
using System.Windows.Input;  
using System.Windows.Media;  
using System.Windows.Media.Imaging;  
using System.Windows.Navigation;  
using System.Windows.Shapes;  
  
// Add the following using directives, and add a reference for System.Net.Http.  
using System.Net.Http;  
using System.IO;  
using System.Net;  
  
namespace AsyncExampleWPF  
{  
    public partial class MainWindow : Window  
    {  
        public MainWindow()  
        {  
            InitializeComponent();  
        }  
  
        private async void startButton_Click(object sender, RoutedEventArgs e)  
        {  
            resultsTextBox.Clear();  
  
            // Disable the button until the operation is complete.  
            startButton.IsEnabled = false;  
  
            // One-step async call.  
            await SumPageSizesAsync();  
  
            //// Two-step async call.  
            //Task sumTask = SumPageSizesAsync();  
            //await sumTask;  
  
            resultsTextBox.Text += "\r\nControl returned to startButton_Click.\r\n";  
  
            // Reenable the button in case you want to run the operation again.  
            startButton.IsEnabled = true;  
        }  
  
        private async Task SumPageSizesAsync()  
        {  
            // Declare an HttpClient object and increase the buffer size. The  
            // default buffer size is 65,536.  
            HttpClient client =  
                new HttpClient() { MaxResponseContentBufferSize = 1000000 };  
  
            // Make a list of web addresses.  
            List<string> urlList = SetUpURLList();  
  
            var total = 0;  
  
            foreach (var url in urlList)  
            {  
                // GetByteArrayAsync returns a task. At completion, the task  
                // produces a byte array.  
                byte[] urlContents = await client.GetByteArrayAsync(url);                 
  
                // The following two lines can replace the previous assignment statement.  
                //Task<byte[]> getContentsTask = client.GetByteArrayAsync(url);  
                //byte[] urlContents = await getContentsTask;  
  
                DisplayResults(url, urlContents);  
  
                // Update the total.  
                total += urlContents.Length;  
            }  
  
            // Display the total count for all of the websites.  
            resultsTextBox.Text +=  
                string.Format("\r\n\r\nTotal bytes returned:  {0}\r\n", total);  
        }  
  
        private List<string> SetUpURLList()  
        {  
            List<string> urls = new List<string>   
            {   
                "http://msdn.microsoft.com/library/windows/apps/br211380.aspx",  
                "http://msdn.microsoft.com",  
                "http://msdn.microsoft.com/library/hh290136.aspx",  
                "http://msdn.microsoft.com/library/ee256749.aspx",  
                "http://msdn.microsoft.com/library/hh290138.aspx",  
                "http://msdn.microsoft.com/library/hh290140.aspx",  
                "http://msdn.microsoft.com/library/dd470362.aspx",  
                "http://msdn.microsoft.com/library/aa578028.aspx",  
                "http://msdn.microsoft.com/library/ms404677.aspx",  
                "http://msdn.microsoft.com/library/ff730837.aspx"  
            };  
            return urls;  
        }  
  
        private void DisplayResults(string url, byte[] content)  
        {  
            // Display the length of each website. The string format   
            // is designed to be used with a monospaced font, such as  
            // Lucida Console or Global Monospace.  
            var bytes = content.Length;  
            // Strip off the "http://".  
            var displayURL = url.Replace("http://", "");  
            resultsTextBox.Text += string.Format("\n{0,-58} {1,8}", displayURL, bytes);  
        }  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="02c81-273">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="02c81-273">See Also</span></span>  
 <span data-ttu-id="02c81-274">[Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f) (Esempio asincrono: accesso alla procedura dettagliata Web (C# e Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="02c81-274">[Async Sample: Accessing the Web Walkthrough (C# and Visual Basic)](https://code.msdn.microsoft.com/Async-Sample-Accessing-the-9c10497f)</span></span>  
 [<span data-ttu-id="02c81-275">async</span><span class="sxs-lookup"><span data-stu-id="02c81-275">async</span></span>](../../../../csharp/language-reference/keywords/async.md)  
 [<span data-ttu-id="02c81-276">await</span><span class="sxs-lookup"><span data-stu-id="02c81-276">await</span></span>](../../../../csharp/language-reference/keywords/await.md)  
 [<span data-ttu-id="02c81-277">Programmazione asincrona con Async e Await (C#)</span><span class="sxs-lookup"><span data-stu-id="02c81-277">Asynchronous Programming with async and await (C#)</span></span>](../../../../csharp/programming-guide/concepts/async/index.md)  
 [<span data-ttu-id="02c81-278">Tipi restituiti asincroni (C#)</span><span class="sxs-lookup"><span data-stu-id="02c81-278">Async Return Types (C#)</span></span>](../../../../csharp/programming-guide/concepts/async/async-return-types.md)  
 [<span data-ttu-id="02c81-279">Programmazione asincrona basata su attività</span><span class="sxs-lookup"><span data-stu-id="02c81-279">Task-based Asynchronous Programming (TAP)</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=19957)  
 [<span data-ttu-id="02c81-280">Procedura: Estendere la procedura dettagliata asincrona tramite Task.WhenAll (C#)</span><span class="sxs-lookup"><span data-stu-id="02c81-280">How to: Extend the async Walkthrough by Using Task.WhenAll (C#)</span></span>](../../../../csharp/programming-guide/concepts/async/how-to-extend-the-async-walkthrough-by-using-task-whenall.md)  
 [<span data-ttu-id="02c81-281">Procedura: Eseguire più richieste Web in parallelo tramite async e await (C#)</span><span class="sxs-lookup"><span data-stu-id="02c81-281">How to: Make Multiple Web Requests in Parallel by Using async and await (C#)</span></span>](../../../../csharp/programming-guide/concepts/async/how-to-make-multiple-web-requests-in-parallel-by-using-async-and-await.md)
