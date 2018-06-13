---
title: 'Procedura: Trovare elementi di pari livello precedenti (XPath-LINQ to XML) (C#)'
ms.date: 07/20/2015
ms.assetid: b281ff99-d08a-43d0-bea1-eff831b2f8ae
ms.openlocfilehash: 64c5bc35899f85e107ccc9d6b0bf93eefb5576ef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33316881"
---
# <a name="how-to-find-preceding-siblings-xpath-linq-to-xml-c"></a><span data-ttu-id="71877-102">Procedura: Trovare elementi di pari livello precedenti (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="71877-102">How to: Find Preceding Siblings (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="71877-103">Questo argomento confronta l'asse `preceding-sibling` XPath con l'asse <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> dell'elemento figlio di [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="71877-103">This topic compares the XPath `preceding-sibling` axis to the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] child <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> axis.</span></span>  
  
 <span data-ttu-id="71877-104">L'espressione XPath è:</span><span class="sxs-lookup"><span data-stu-id="71877-104">The XPath expression is:</span></span>  
  
 `preceding-sibling::*`  
  
 <span data-ttu-id="71877-105">Notare che i risultati di <xref:System.Xml.XPath.Extensions.XPathSelectElements%2A> e <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType>, sono espressi nell'ordine dei documenti.</span><span class="sxs-lookup"><span data-stu-id="71877-105">Note that the results of both <xref:System.Xml.XPath.Extensions.XPathSelectElements%2A> and <xref:System.Xml.Linq.XNode.ElementsBeforeSelf%2A?displayProperty=nameWithType> are in document order.</span></span>  
  
## <a name="example"></a><span data-ttu-id="71877-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="71877-106">Example</span></span>  
 <span data-ttu-id="71877-107">Nell'esempio seguente viene cercato l'elemento `FullAddress` e quindi vengono recuperati gli elementi precedenti usando l'asse `preceding-sibling`.</span><span class="sxs-lookup"><span data-stu-id="71877-107">The following example finds the `FullAddress` element, and then retrieves the previous elements using the `preceding-sibling` axis.</span></span>  
  
 <span data-ttu-id="71877-108">Nell'esempio viene usato il documento XML seguente: [File XML di esempio: Customers e Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml-2.md).</span><span class="sxs-lookup"><span data-stu-id="71877-108">This example uses the following XML document: [Sample XML File: Customers and Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-customers-and-orders-linq-to-xml-2.md).</span></span>  
  
```csharp  
XElement co = XElement.Load("CustomersOrders.xml");  
  
XElement add = co.Element("Customers").Element("Customer").Element("FullAddress");  
  
// LINQ to XML query  
IEnumerable<XElement> list1 = add.ElementsBeforeSelf();  
  
// XPath expression  
IEnumerable<XElement> list2 = add.XPathSelectElements("preceding-sibling::*");  
  
if (list1.Count() == list2.Count() &&  
        list1.Intersect(list2).Count() == list1.Count())  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
foreach (XElement el in list2)  
    Console.WriteLine(el);  
```  
  
 <span data-ttu-id="71877-109">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="71877-109">This example produces the following output:</span></span>  
  
```  
Results are identical  
<CompanyName>Great Lakes Food Market</CompanyName>  
<ContactName>Howard Snyder</ContactName>  
<ContactTitle>Marketing Manager</ContactTitle>  
<Phone>(503) 555-7555</Phone>  
```  
  
## <a name="see-also"></a><span data-ttu-id="71877-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="71877-110">See Also</span></span>  
 [<span data-ttu-id="71877-111">LINQ to XML per gli utenti di XPath (C#)</span><span class="sxs-lookup"><span data-stu-id="71877-111">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
