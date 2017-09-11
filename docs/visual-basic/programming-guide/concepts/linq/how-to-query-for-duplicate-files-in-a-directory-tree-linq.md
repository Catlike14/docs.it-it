---
title: 'Procedura: eseguire una Query per i file duplicati in una struttura di Directory (LINQ) (Visual Basic) | Documenti di Microsoft'
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
ms.assetid: 387d7c97-95dd-4a50-9761-7e9cf8ae9e6a
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 3f4ddab6129e7d05851553e544b9813951415a45
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="how-to-query-for-duplicate-files-in-a-directory-tree-linq-visual-basic"></a><span data-ttu-id="fcb7e-102">Procedura: eseguire una Query per i file duplicati in una struttura di Directory (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="fcb7e-102">How to: Query for Duplicate Files in a Directory Tree (LINQ) (Visual Basic)</span></span>
<span data-ttu-id="fcb7e-103">Talvolta i file con lo stesso nome possono trovarsi in più di una cartella.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-103">Sometimes files that have the same name may be located in more than one folder.</span></span> <span data-ttu-id="fcb7e-104">Ad esempio, nella cartella di installazione di Visual Studio, diverse cartelle dispongano di un file Readme. htm.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-104">For example, under the Visual Studio installation folder, several folders have a readme.htm file.</span></span> <span data-ttu-id="fcb7e-105">In questo esempio viene illustrato come eseguire una query per tali nomi file duplicati in una cartella radice specificata.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-105">This example shows how to query for such duplicate file names under a specified root folder.</span></span> <span data-ttu-id="fcb7e-106">Nel secondo esempio viene illustrato come eseguire una query per i file le cui dimensioni e ora di creazione uguali.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-106">The second example shows how to query for files whose size and creation times also match.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fcb7e-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="fcb7e-107">Example</span></span>  
  
```vb  
Module QueryDuplicateFileNames  
  
    Public Sub Main()  
  
        Dim path As String = "C:\Program Files\Microsoft Visual Studio 9.0\Common7"  
        QueryDuplicates1(path)  
        ' Uncomment to run this query instead  
        ' QueryDuplicates2(path)  
  
    End Sub  
    Sub QueryDuplicates1(ByVal root As String)  
        Dim dir As New System.IO.DirectoryInfo(root)  
        Dim duplicates = From aFile In dir.GetFiles("*.*", System.IO.SearchOption.AllDirectories) _  
                                 Order By aFile.Name _  
                                 Group aFile By aFile.Name Into newGroup = Group _  
                                 Where newGroup.Count() >= 2 _  
                                 Select newGroup  
  
        ' Page the display so that the results can be read.  
        Dim trimLength = root.Length  
        PageOutput(duplicates, trimLength)  
  
    End Sub  
    Sub QueryDuplicates2(ByVal root As String)  
  
        ' This time a composite key is used. This sub finds all files  
        ' that have been copied into multiple subfolders.  
        Dim dir As New System.IO.DirectoryInfo(root)  
  
        Dim duplicates = From aFile In Dir.GetFiles("*.*", System.IO.SearchOption.AllDirectories) _  
                                 Order By aFile.Name _  
                                 Group aFile By aFile.Name, aFile.CreationTime, aFile.Length Into newGroup = Group _  
                                 Where newGroup.Count() >= 2 _  
                                 Select newGroup  
  
        ' Page the display so that the results can be read.  
        Dim trimLength = root.Length  
        PageOutput(duplicates, trimLength)  
  
    End Sub  
    ' Pages console diplay for large query results. No more than one group per page.  
    ' This sub specifically works with group queries of FileInfo objects  
    ' but can be modified for any type.  
    Sub PageOutput(ByVal groupQuery, ByVal charsToSkip)  
  
        ' "3" = 1 line for extension key + 1 for "Press any key" + 1 for input cursor.  
        Dim numLines As Integer = Console.WindowHeight - 3  
        ' Flag to indicate whether there are more results to diplay  
        Dim goAgain As Boolean = True  
  
        For Each fg As IEnumerable(Of System.IO.FileInfo) In groupQuery  
            ' Start a new extension at the top of a page.  
            Dim currentLine As Integer = 0  
  
            Do While (currentLine < fg.Count())  
                Console.Clear()  
  
                ' Get the next page of results  
                ' No more than one filename per page  
                Dim resultPage = From file In fg _  
                                Skip currentLine Take numLines  
  
                ' Execute the query. Trim the paths in the output.  
                For Each line In resultPage  
                    Console.WriteLine(vbTab & line.FullName.Substring(charsToSkip))  
                Next  
  
                ' Advance the current position  
                currentLine = numLines + currentLine  
  
                ' Give the user a chance to break out of the loop  
                Console.WriteLine("Press any key for next page or the 'End' key to exit.")  
                Dim key As ConsoleKey = Console.ReadKey().Key  
                If key = ConsoleKey.End Then  
                    goAgain = False  
                    Exit For  
                End If  
            Loop  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="fcb7e-108">La prima query utilizza una chiave semplice per determinare una corrispondenza. Consente di trovare i file che hanno lo stesso nome ma il cui contenuto potrebbe essere diverso.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-108">The first query uses a simple key to determine a match; this finds files that have the same name but whose contents might be different.</span></span> <span data-ttu-id="fcb7e-109">La seconda query utilizza una chiave composta per la corrispondenza con tre proprietà del <xref:System.IO.FileInfo>oggetto.</xref:System.IO.FileInfo></span><span class="sxs-lookup"><span data-stu-id="fcb7e-109">The second query uses a compound key to match against three properties of the <xref:System.IO.FileInfo> object.</span></span> <span data-ttu-id="fcb7e-110">Questa query è molto più probabile trovare i file con lo stesso nome e un contenuto simile o identico.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-110">This query is much more likely to find files that have the same name and similar or identical content.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="fcb7e-111">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="fcb7e-111">Compiling the Code</span></span>  
 <span data-ttu-id="fcb7e-112">Creare un progetto destinato a .NET Framework versione 3.5 o versione successiva con un riferimento a System.Core.dll e una `Imports` istruzione per lo spazio dei nomi System. Linq.</span><span class="sxs-lookup"><span data-stu-id="fcb7e-112">Create a project that targets the .NET Framework version 3.5 or higher with a reference to System.Core.dll and a `Imports` statement for the System.Linq namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fcb7e-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fcb7e-113">See Also</span></span>  
 <span data-ttu-id="fcb7e-114">[LINQ to Objects (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md) </span><span class="sxs-lookup"><span data-stu-id="fcb7e-114">[LINQ to Objects (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md) </span></span>  
<span data-ttu-id="fcb7e-115"> [Directory di File (Visual Basic) e LINQ](../../../../visual-basic/programming-guide/concepts/linq/linq-and-file-directories.md)</span><span class="sxs-lookup"><span data-stu-id="fcb7e-115"> [LINQ and File Directories (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-and-file-directories.md)</span></span>
