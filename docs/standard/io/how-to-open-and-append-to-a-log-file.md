---
title: 'Procedura: Aprire e accodare un file di log'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- log files, opening
- streams, opening and appending to log file
- log files, appending to
- I/O [.NET Framework], log files
ms.assetid: 74423362-1721-49cb-aa0a-e04005f72a06
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 60c31339231405a1cbbb98dae37d36ad3c3709c1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-open-and-append-to-a-log-file"></a><span data-ttu-id="13aed-102">Procedura: Aprire e accodare un file di log</span><span class="sxs-lookup"><span data-stu-id="13aed-102">How to: Open and Append to a Log File</span></span>
<span data-ttu-id="13aed-103"><xref:System.IO.StreamWriter>e <xref:System.IO.StreamReader> caratteri da scrivere e leggere i caratteri da flussi.</span><span class="sxs-lookup"><span data-stu-id="13aed-103"><xref:System.IO.StreamWriter> and <xref:System.IO.StreamReader> write characters to and read characters from streams.</span></span> <span data-ttu-id="13aed-104">Nell'esempio di codice viene aperto il `log.txt` del file di input o creare il file se non esiste già e aggiunge informazioni alla fine del file.</span><span class="sxs-lookup"><span data-stu-id="13aed-104">The following code example opens the `log.txt` file for input, or creates the file if it does not already exist, and appends information to the end of the file.</span></span> <span data-ttu-id="13aed-105">Il contenuto del file viene quindi scritti nell'output standard per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="13aed-105">The contents of the file are then written to standard output for display.</span></span> <span data-ttu-id="13aed-106">In alternativa a questo esempio, le informazioni può essere archiviate come un'unica stringa o matrice di stringhe e <xref:System.IO.File.WriteAllText%2A> o <xref:System.IO.File.WriteAllLines%2A> metodo può essere utilizzato per ottenere la stessa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="13aed-106">As an alternative to this example, the information could be stored as a single string or string array, and the <xref:System.IO.File.WriteAllText%2A> or <xref:System.IO.File.WriteAllLines%2A> method could be used to achieve the same functionality.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="13aed-107">Gli utenti di Visual Basic è possono scegliere di utilizzare i metodi e le proprietà forniti dal <xref:Microsoft.VisualBasic.Logging.Log> classe o <xref:Microsoft.VisualBasic.FileIO.FileSystem> classe per la creazione o la scrittura nei file di log.</span><span class="sxs-lookup"><span data-stu-id="13aed-107">Visual Basic users may choose to use the methods and properties provided by the <xref:Microsoft.VisualBasic.Logging.Log> class or <xref:Microsoft.VisualBasic.FileIO.FileSystem> class for creating or writing to log files.</span></span>  
  
## <a name="example"></a><span data-ttu-id="13aed-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="13aed-108">Example</span></span>  
 [!code-csharp[Conceptual.BasicIO.TextFiles#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source2.cs#2)]
 [!code-vb[Conceptual.BasicIO.TextFiles#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="13aed-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="13aed-109">See Also</span></span>  
 <xref:System.IO.StreamWriter>  
 <xref:System.IO.StreamReader>  
 <xref:System.IO.File.AppendText%2A?displayProperty=nameWithType>  
 <xref:System.IO.File.OpenText%2A?displayProperty=nameWithType>  
 <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="13aed-110">Procedura: Enumerare directory e file</span><span class="sxs-lookup"><span data-stu-id="13aed-110">How to: Enumerate Directories and Files</span></span>](../../../docs/standard/io/how-to-enumerate-directories-and-files.md)  
 [<span data-ttu-id="13aed-111">Procedura: Leggere e scrivere su un file di dati appena creato</span><span class="sxs-lookup"><span data-stu-id="13aed-111">How to: Read and Write to a Newly Created Data File</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
 [<span data-ttu-id="13aed-112">Procedura: Leggere testo da un file</span><span class="sxs-lookup"><span data-stu-id="13aed-112">How to: Read Text from a File</span></span>](../../../docs/standard/io/how-to-read-text-from-a-file.md)  
 [<span data-ttu-id="13aed-113">Procedura: Scrivere un testo in un file</span><span class="sxs-lookup"><span data-stu-id="13aed-113">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [<span data-ttu-id="13aed-114">Procedura: Leggere caratteri da una stringa</span><span class="sxs-lookup"><span data-stu-id="13aed-114">How to: Read Characters from a String</span></span>](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
 [<span data-ttu-id="13aed-115">Procedura: Scrivere caratteri in una stringa</span><span class="sxs-lookup"><span data-stu-id="13aed-115">How to: Write Characters to a String</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [<span data-ttu-id="13aed-116">I/O di file e di flussi</span><span class="sxs-lookup"><span data-stu-id="13aed-116">File and Stream I-O</span></span>](../../../docs/standard/io/index.md)
