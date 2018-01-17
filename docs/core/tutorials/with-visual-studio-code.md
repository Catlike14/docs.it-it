---
title: Introduzione a C# e Visual Studio Code - Guida a C#
description: Informazioni su come creare la prima applicazione .NET Core in C# ed eseguirne il debug tramite Visual Studio Code.
keywords: C#, introduzione, acquisizione, installazione, Visual Studio Code, multipiattaforma
author: kendrahavens
ms.author: mairaw
ms.date: 09/27/2017
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.assetid: 76c23597-4cf9-467e-8a47-0c3703ce37e7
ms.workload: dotnetcore
ms.openlocfilehash: 95052da1688ec1026f11ff679dda6aad50a340fa
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/23/2017
---
# <a name="get-started-with-c-and-visual-studio-code"></a>Introduzione a C# e Visual Studio Code

.NET Core offre una piattaforma veloce e modulare per la creazione di applicazioni eseguibili in Windows, Linux e macOS. Usare Visual Studio Code con l'estensione C# per ottenere un'efficace esperienza di programmazione con il supporto completo per IntelliSense C# (completamento intelligente del codice) e debug.

## <a name="prerequisites"></a>Prerequisiti

1. Installare [Visual Studio Code](https://code.visualstudio.com/).
2. Installare [.NET Core SDK](https://www.microsoft.com/net/download/core).
3. Installare l'[estensione C#](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp) da Visual Studio Code Marketplace.

## <a name="hello-world"></a>Hello World

Si inizia con un semplice programma "Hello World" in .NET Core:

1. Aprire un progetto:

    * Aprire Visual Studio Code.
    * Fare clic sull'icona Esplora nel menu a sinistra e quindi fare clic su **Apri cartella**.
    * Selezionare **File** > **Apri cartella** dal menu principale per aprire la cartella in cui inserire il programma C# e fare clic su **Seleziona cartella**. Ai fini di questo esempio, viene creata una cartella per il progetto denominato *HelloWorld*.

      ![VSCodeOpenFolder](media/with-visual-studio-code/vscodeopenfolder.png)

2. Inizializzare un progetto C#:
    * Aprire il terminale integrato da Visual Studio Code scegliendo **Visualizza** > **Terminale integrato** dal menu principale.
    * Nella finestra del terminale digitare `dotnet new console`.
    * Questo comando crea un file `Program.cs` nella cartella con un semplice programma "Hello World" già scritto, oltre a un file di progetto C# denominato `HelloWorld.csproj`.

      ![Comando new di dotnet](media/with-visual-studio-code/dotnetnew.png)

3. Risolvere le risorse di compilazione:

    * Per **.NET Core 1.x** digitare `dotnet restore`. L'esecuzione di `dotnet restore` consente di accedere ai pacchetti .NET Core necessari per la compilazione del progetto.

      ![Comando restore di dotnet](media/with-visual-studio-code/dotnetrestore.png)

      [!INCLUDE[DotNet Restore Note](~/includes/dotnet-restore-note.md)]

4. Eseguire il programma "Hello World":

    * Digitare `dotnet run`. 

      ![Comando run di dotnet](media/with-visual-studio-code/dotnetrun.png)

Per altre informazioni sull'installazione in [Windows](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core), [macOS](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-using-CSharp-and-NET-Core-on-MacOS) o [Linux](https://channel9.msdn.com/Blogs/dotnet/Get-started-with-VS-Code-Csharp-dotnet-Core-Ubuntu), è anche possibile guardare una breve esercitazione video.

## <a name="debug"></a>Debug

1. Aprire il file *Program.cs* facendo clic su di esso. La prima volta che si apre un file C# in Visual Studio Code, [OmniSharp](http://www.omnisharp.net/) viene caricato nell'editor.

    ![Aprire il file Program.cs](media/with-visual-studio-code/opencs.png)

2. Visual Studio Code dovrebbe chiedere di aggiungere le risorse mancanti per compilare l'app ed eseguirne il debug. Selezionare **Sì**. 

    ![Richiesta delle risorse mancanti](media/with-visual-studio-code/missing-assets.png)

3. Per aprire la visualizzazione Debug, fare clic sull'icona Debug nel menu di sinistra.

    ![Aprire la scheda Debug](media/with-visual-studio-code/opendebug.png)

4. Individuare la freccia verde nella parte superiore del riquadro. Verificare che nel menu a discesa accanto alla freccia sia selezionato `.NET Core Launch (console)`.

    ![Selezione di .NET Core](media/with-visual-studio-code/selectcore.png)

5. Aggiungere un punto di interruzione al progetto facendo clic sul **margine dell'editor**, ovvero lo spazio a sinistra dei numeri riga nell'editor, accanto alla riga 9.

    ![Impostazione di un punto di interruzione](media/with-visual-studio-code/setbreakpoint.png)

6. Per avviare il debug, premere <kbd>F5</kbd> o fare clic sulla freccia verde. Il debugger interrompe l'esecuzione del programma quando raggiunge il punto di interruzione impostato nel passaggio precedente.
    * Durante il debug è possibile visualizzare le variabili locali nel riquadro superiore sinistro. In alternativa, usare la console di debug.

    ![Run e Debug](media/with-visual-studio-code/rundebug.png)

7. Selezionare la freccia verde in alto per continuare il debug oppure fare clic sul quadrato rosso per arrestarlo.

> [!TIP] 
> Per altre informazioni e per suggerimenti sul debug .NET Core con OmniSharp in Visual Studio Code, vedere [Instructions for setting up the .NET Core debugger](https://github.com/OmniSharp/omnisharp-vscode/blob/master/debugger.md) (Istruzioni per l'impostazione del debugger .NET Core).

## <a name="see-also"></a>Vedere anche
[Setting up Visual Studio Code](https://code.visualstudio.com/docs/setup/setup-overview)  (Impostazione di Visual Studio Code)  
[Debugging in Visual Studio Code](https://code.visualstudio.com/Docs/editor/debugging) (Debug in Visual Studio Code)
