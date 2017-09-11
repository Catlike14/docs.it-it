---
title: 'Procedura: trovare la differenza dei Set tra due elenchi (LINQ) (Visual Basic) | Documenti di Microsoft'
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
ms.assetid: b5b25474-10a8-4df6-aab5-75621bb6b68e
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
ms.openlocfilehash: 9c00a66c79e080211c92457c0194462698fee98f
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="how-to-find-the-set-difference-between-two-lists-linq-visual-basic"></a><span data-ttu-id="be00d-102">Procedura: trovare la differenza dei Set tra due elenchi (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="be00d-102">How to: Find the Set Difference Between Two Lists (LINQ) (Visual Basic)</span></span>
<span data-ttu-id="be00d-103">In questo esempio viene illustrato come utilizzare LINQ per confrontare due elenchi di stringhe e restituire le righe presenti in names1. txt, ma non in names2.</span><span class="sxs-lookup"><span data-stu-id="be00d-103">This example shows how to use LINQ to compare two lists of strings and output those lines that are in names1.txt but not in names2.txt.</span></span>  
  
### <a name="to-create-the-data-files"></a><span data-ttu-id="be00d-104">Per creare i file di dati</span><span class="sxs-lookup"><span data-stu-id="be00d-104">To create the data files</span></span>  
  
1.  <span data-ttu-id="be00d-105">Copiare names1. txt e names2. txt nella cartella della soluzione come illustrato nella [procedura: combinare e confrontare stringhe raccolte (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-combine-and-compare-string-collections-linq.md).</span><span class="sxs-lookup"><span data-stu-id="be00d-105">Copy names1.txt and names2.txt to your solution folder as shown in [How to: Combine and Compare String Collections (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-combine-and-compare-string-collections-linq.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="be00d-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="be00d-106">Example</span></span>  
  
```vb  
Class CompareLists  
  
    Shared Sub Main()  
  
        ' Create the IEnumerable data sources.  
        Dim names1 As String() = System.IO.File.ReadAllLines("../../../names1.txt")  
        Dim names2 As String() = System.IO.File.ReadAllLines("../../../names2.txt")  
  
        ' Create the query. Note that method syntax must be used here.  
        Dim differenceQuery = names1.Except(names2)  
        Console.WriteLine("The following lines are in names1.txt but not names2.txt")  
  
        ' Execute the query.  
        For Each name As String In differenceQuery  
            Console.WriteLine(name)  
        Next  
  
        ' Keep console window open in debug mode.  
        Console.WriteLine("Press any key to exit.")  
        Console.ReadKey()  
    End Sub  
End Class  
' Output:  
' The following lines are in names1.txt but not names2.txt  
' Potra, Cristina  
' Noriega, Fabricio  
' Aw, Kam Foo  
' Toyoshima, Tim  
' Guy, Wey Yuan  
' Garcia, Debra  
```  
  
 <span data-ttu-id="be00d-107">Alcuni tipi di query operazioni in Visual Basic, ad esempio <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Union%2A>, e <xref:System.Linq.Enumerable.Concat%2A>, può essere espresso solo nella sintassi delle query basate su metodo.</xref:System.Linq.Enumerable.Concat%2A> </xref:System.Linq.Enumerable.Union%2A> </xref:System.Linq.Enumerable.Distinct%2A> </xref:System.Linq.Enumerable.Except%2A></span><span class="sxs-lookup"><span data-stu-id="be00d-107">Some types of query operations in Visual Basic, such as <xref:System.Linq.Enumerable.Except%2A>, <xref:System.Linq.Enumerable.Distinct%2A>, <xref:System.Linq.Enumerable.Union%2A>, and <xref:System.Linq.Enumerable.Concat%2A>, can only be expressed in method-based syntax.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="be00d-108">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="be00d-108">Compiling the Code</span></span>  
 <span data-ttu-id="be00d-109">Creare un progetto destinato a .NET Framework versione 3.5 o versione successiva con un riferimento a System.Core.dll e una `Imports` istruzione per lo spazio dei nomi System. Linq.</span><span class="sxs-lookup"><span data-stu-id="be00d-109">Create a project that targets the .NET Framework version 3.5 or higher with a reference to System.Core.dll and a `Imports` statement for the System.Linq namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="be00d-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="be00d-110">See Also</span></span>  
 [<span data-ttu-id="be00d-111">LINQ e stringhe (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="be00d-111">LINQ and Strings (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-and-strings.md)
