---
title: 'Procedura: leggere testo da un file'
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
- streams, reading text from files
- reading text files
- reading data, text files
- data streams, reading text from files
- I/O [.NET Framework], reading text from files
ms.assetid: ed180baa-dfc6-4c69-a725-46e87edafb27
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: 6fbf9c910847986af1c02b5848c81266009e2e07
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-read-text-from-a-file"></a><span data-ttu-id="9e766-102">Procedura: leggere testo da un file</span><span class="sxs-lookup"><span data-stu-id="9e766-102">How to: Read Text from a File</span></span>
<span data-ttu-id="9e766-103">Negli esempi seguenti viene illustrato come leggere il testo in modo sincrono e in modo asincrono da un file di testo usando .NET per le applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="9e766-103">The following examples show how to read text synchronously and asynchronously from a text file using .NET for desktop apps.</span></span> <span data-ttu-id="9e766-104">In entrambi gli esempi, quando si crea l'istanza della classe <xref:System.IO.StreamReader>, si immette il percorso relativo o assoluto del file.</span><span class="sxs-lookup"><span data-stu-id="9e766-104">In both examples, when you create the instance of the <xref:System.IO.StreamReader> class, you provide the relative or absolute path to the file.</span></span> <span data-ttu-id="9e766-105">Negli esempi si presuppone che il file denominato TestFile.txt sia nella stessa cartella dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9e766-105">The following examples assume that the file named TestFile.txt is in the same folder as the application.</span></span>  
  
 <span data-ttu-id="9e766-106">Questi esempi di codice non sono applicabili allo sviluppo di applicazioni Windows Store poiché Windows Runtime offre diversi tipi di flussi che leggono e scrivono sui file.</span><span class="sxs-lookup"><span data-stu-id="9e766-106">These code examples do not apply developing for Windows Store Apps because the Windows Runtime provides different streams types reading and writing to files.</span></span> <span data-ttu-id="9e766-107">Per un esempio che illustra come leggere il testo da un file nel contesto di un'app di Windows Store, vedere [Quickstart: Reading and writing files](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx) (Guida introduttiva: Lettura e scrittura di file).</span><span class="sxs-lookup"><span data-stu-id="9e766-107">For an example that shows how to read text from a file within the context of a Windows Store app, see [Quickstart: Reading and writing files](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx).</span></span> <span data-ttu-id="9e766-108">Per esempi che illustrano come eseguire la conversione tra flussi di .NET Framework e flussi di Windows Runtime, vedere [Procedura: eseguire la conversione tra flussi di .NET Framework e flussi di Windows Runtime](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md).</span><span class="sxs-lookup"><span data-stu-id="9e766-108">For examples that show how to convert between .NET Framework streams and Windows runtime streams see [How to: Convert Between .NET Framework Streams and Windows Runtime Streams](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9e766-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e766-109">Example</span></span>  
 <span data-ttu-id="9e766-110">Il primo esempio illustra un'operazione di lettura sincrona in un'applicazione console.</span><span class="sxs-lookup"><span data-stu-id="9e766-110">The first example shows a synchronous read operation within a console application.</span></span> <span data-ttu-id="9e766-111">In questo esempio viene aperto il file di testo usando un lettore del flusso, il contenuto viene copiato in una stringa, che quindi viene data in output alla console.</span><span class="sxs-lookup"><span data-stu-id="9e766-111">In this example, the text file is opened using a stream reader, the contents are copied to a string and string is output to the console.</span></span>  
  
 [!code-csharp[Conceptual.BasicIO.TextFiles#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source3.cs#3)]
 [!code-vb[Conceptual.BasicIO.TextFiles#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source3.vb#3)]  
  
## <a name="example"></a><span data-ttu-id="9e766-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="9e766-112">Example</span></span>  
 <span data-ttu-id="9e766-113">Nel secondo esempio viene illustrata l'operazione di lettura asincrona in un'applicazione Windows Presentation Foundation (WPF).</span><span class="sxs-lookup"><span data-stu-id="9e766-113">The second example shows an asynchronous read operation within a Windows Presentation Foundation (WPF) application.</span></span>  
  
 [!code-csharp[Conceptual.BasicIO.TextFiles#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.basicio.textfiles/cs/source6.cs#6)]
 [!code-vb[Conceptual.BasicIO.TextFiles#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.basicio.textfiles/vb/source6.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="9e766-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9e766-114">See Also</span></span>  
 <xref:System.IO.StreamReader>  
 <xref:System.IO.File.OpenText%2A?displayProperty=nameWithType>  
 <xref:System.IO.StreamReader.ReadLine%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="9e766-115">I/O di file asincrono</span><span class="sxs-lookup"><span data-stu-id="9e766-115">Asynchronous File I/O</span></span>](../../../docs/standard/io/asynchronous-file-i-o.md)  
 [<span data-ttu-id="9e766-116">Procedura: creare una visualizzazione directory</span><span class="sxs-lookup"><span data-stu-id="9e766-116">NIB: How to: Create a Directory Listing</span></span>](http://msdn.microsoft.com/library/4d2772b1-b991-4532-a8a6-6ef733277e69)  
 [<span data-ttu-id="9e766-117">Quickstart: Reading and writing files (Guida introduttiva: Lettura e scrittura di file)</span><span class="sxs-lookup"><span data-stu-id="9e766-117">Quickstart: Reading and writing files</span></span>](http://msdn.microsoft.com/library/windows/apps/hh758325.aspx)  
 [<span data-ttu-id="9e766-118">Procedura: Eseguire la conversione tra flussi di .NET Framework e flussi di Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="9e766-118">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)  
 [<span data-ttu-id="9e766-119">Procedura: Leggere e scrivere su un file di dati appena creato</span><span class="sxs-lookup"><span data-stu-id="9e766-119">How to: Read and Write to a Newly Created Data File</span></span>](../../../docs/standard/io/how-to-read-and-write-to-a-newly-created-data-file.md)  
 [<span data-ttu-id="9e766-120">Procedura: Aprire e accodare un file di log</span><span class="sxs-lookup"><span data-stu-id="9e766-120">How to: Open and Append to a Log File</span></span>](../../../docs/standard/io/how-to-open-and-append-to-a-log-file.md)  
 [<span data-ttu-id="9e766-121">Procedura: Scrivere un testo in un file</span><span class="sxs-lookup"><span data-stu-id="9e766-121">How to: Write Text to a File</span></span>](../../../docs/standard/io/how-to-write-text-to-a-file.md)  
 [<span data-ttu-id="9e766-122">Procedura: Leggere caratteri da una stringa</span><span class="sxs-lookup"><span data-stu-id="9e766-122">How to: Read Characters from a String</span></span>](../../../docs/standard/io/how-to-read-characters-from-a-string.md)  
 [<span data-ttu-id="9e766-123">Procedura: Scrivere caratteri in una stringa</span><span class="sxs-lookup"><span data-stu-id="9e766-123">How to: Write Characters to a String</span></span>](../../../docs/standard/io/how-to-write-characters-to-a-string.md)  
 [<span data-ttu-id="9e766-124">I/O di file e di flussi</span><span class="sxs-lookup"><span data-stu-id="9e766-124">File and Stream I-O</span></span>](../../../docs/standard/io/index.md)
