---
title: 'Procedura: Trovare l''elemento radice (XPath-LINQ to XML) (C#)'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 4fd824e0-4d39-429b-b092-f6a5c046ee6c
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 2731b773e436114bb2324ba1cea339cf9327adb9
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="how-to-find-the-root-element-xpath-linq-to-xml-c"></a><span data-ttu-id="32cbb-102">Procedura: Trovare l'elemento radice (XPath-LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="32cbb-102">How to: Find the Root Element (XPath-LINQ to XML) (C#)</span></span>
<span data-ttu-id="32cbb-103">In questo argomento viene illustrato come ottenere l'elemento radice con XPath e [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="32cbb-103">This topic shows how to get the root element with XPath and [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span></span>  
  
 <span data-ttu-id="32cbb-104">L'espressione XPath è:</span><span class="sxs-lookup"><span data-stu-id="32cbb-104">The XPath expression is:</span></span>  
  
 `/PurchaseOrders`  
  
## <a name="example"></a><span data-ttu-id="32cbb-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="32cbb-105">Example</span></span>  
 <span data-ttu-id="32cbb-106">In questo esempio viene trovato l'elemento radice.</span><span class="sxs-lookup"><span data-stu-id="32cbb-106">This example finds the root element.</span></span>  
  
 <span data-ttu-id="32cbb-107">Nell'esempio viene usato il documento XML seguente: [File XML di esempio: più ordini di acquisto (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span><span class="sxs-lookup"><span data-stu-id="32cbb-107">This example uses the following XML document: [Sample XML File: Multiple Purchase Orders (LINQ to XML)](../../../../csharp/programming-guide/concepts/linq/sample-xml-file-multiple-purchase-orders-linq-to-xml.md).</span></span>  
  
```csharp  
XDocument po = XDocument.Load("PurchaseOrders.xml");  
  
// LINQ to XML query  
XElement el1 = po.Root;  
  
// XPath expression  
XElement el2 = po.XPathSelectElement("/PurchaseOrders");  
  
if (el1 == el2)  
    Console.WriteLine("Results are identical");  
else  
    Console.WriteLine("Results differ");  
Console.WriteLine(el1.Name);  
```  
  
 <span data-ttu-id="32cbb-108">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="32cbb-108">This example produces the following output:</span></span>  
  
```  
Results are identical  
PurchaseOrders  
```  
  
## <a name="see-also"></a><span data-ttu-id="32cbb-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32cbb-109">See Also</span></span>  
 [<span data-ttu-id="32cbb-110">LINQ to XML per gli utenti di XPath (C#)</span><span class="sxs-lookup"><span data-stu-id="32cbb-110">LINQ to XML for XPath Users (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)

