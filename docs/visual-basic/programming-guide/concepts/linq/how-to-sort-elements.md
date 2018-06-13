---
title: 'Procedura: ordinare elementi (Visual Basic)'
ms.date: 07/20/2015
ms.assetid: c2c09279-6c8a-482e-8e71-b1453a815052
ms.openlocfilehash: 868f3eb448393e5c06a37ab68431620638e9dc35
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33642090"
---
# <a name="how-to-sort-elements-visual-basic"></a><span data-ttu-id="eac11-102">Procedura: ordinare elementi (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="eac11-102">How to: Sort Elements (Visual Basic)</span></span>
<span data-ttu-id="eac11-103">In questo esempio viene illustrato come scrivere una query che ordina i relativi risultati.</span><span class="sxs-lookup"><span data-stu-id="eac11-103">This example shows how to write a query that sorts its results.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eac11-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="eac11-104">Example</span></span>  
 <span data-ttu-id="eac11-105">Questo esempio usa il documento XML seguente: [File XML di esempio: dati numerici (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="eac11-105">This example uses the following XML document: [Sample XML File: Numerical Data (LINQ to XML)](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-linq-to-xml.md).</span></span>  
  
```vb  
Dim root As XElement = XElement.Load("Data.xml")  
Dim prices As IEnumerable(Of Decimal) = _  
    From el In root.<Data> _  
    Let price = Convert.ToDecimal(el.<Price>.Value) _  
    Order By (price) _  
    Select price  
For Each el As Decimal In prices  
    Console.WriteLine(el)  
Next  
```  
  
 <span data-ttu-id="eac11-106">L'output del codice è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eac11-106">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="example"></a><span data-ttu-id="eac11-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="eac11-107">Example</span></span>  
 <span data-ttu-id="eac11-108">Nell'esempio seguente è illustrata la stessa query per XML in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="eac11-108">The following example shows the same query for XML that is in a namespace.</span></span> <span data-ttu-id="eac11-109">Per ulteriori informazioni, vedere [utilizzo di spazi dei nomi XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="eac11-109">For more information, see [Working with XML Namespaces (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md).</span></span>  
  
 <span data-ttu-id="eac11-110">Questo esempio usa il documento XML seguente: [File XML di esempio: dati numerici in uno spazio dei nomi](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="eac11-110">This example uses the following XML document: [Sample XML File: Numerical Data in a Namespace](../../../../visual-basic/programming-guide/concepts/linq/sample-xml-file-numerical-data-in-a-namespace.md).</span></span>  
  
```vb  
Imports <xmlns='http://www.adatum.com'>  
  
Module Module1  
    Sub Main()  
        Dim root As XElement = XElement.Load("DataInNamespace.xml")  
        Dim prices As IEnumerable(Of Decimal) = _  
            From el In root.<Data> _  
            Let price = Convert.ToDecimal(el.<Price>.Value) _  
            Order By (price) _  
            Select price  
        For Each el As Decimal In prices  
            Console.WriteLine(el)  
        Next  
    End Sub  
End Module  
```  
  
 <span data-ttu-id="eac11-111">L'output del codice è il seguente:</span><span class="sxs-lookup"><span data-stu-id="eac11-111">This code produces the following output:</span></span>  
  
```  
0.99  
4.95  
6.99  
24.50  
29.00  
66.00  
89.99  
```  
  
## <a name="see-also"></a><span data-ttu-id="eac11-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eac11-112">See Also</span></span>  
 [<span data-ttu-id="eac11-113">Ordinamento dei dati</span><span class="sxs-lookup"><span data-stu-id="eac11-113">Sorting Data</span></span>](../../../../visual-basic/programming-guide/concepts/linq/sorting-data.md)  
 [<span data-ttu-id="eac11-114">Le query di base (LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="eac11-114">Basic Queries (LINQ to XML) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/basic-queries-linq-to-xml.md)
