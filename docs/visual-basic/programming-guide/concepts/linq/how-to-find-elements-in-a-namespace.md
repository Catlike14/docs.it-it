---
title: 'Procedura: trovare elementi in un Namespace (XPath-LINQ to XML) (Visual Basic) | Documenti di Microsoft'
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
ms.assetid: c7cb3b77-3424-4b54-9efa-4dc715948e41
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 9efa99c1b8cffa6d02a40ee8f302a6e1ad0b6b6e
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017


---
# <a name="how-to-find-elements-in-a-namespace-xpath-linq-to-xml-visual-basic"></a><span data-ttu-id="811f8-102">Procedura: trovare elementi in un Namespace (XPath-LINQ to XML) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="811f8-102">How to: Find Elements in a Namespace (XPath-LINQ to XML) (Visual Basic)</span></span>
<span data-ttu-id="811f8-103">Le espressioni XPath consentono di trovare nodi in un determinato spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="811f8-103">XPath expressions can find nodes in a particular namespace.</span></span> <span data-ttu-id="811f8-104">Per specificare gli spazi dei nomi, nelle espressioni XPath si usano prefissi di spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="811f8-104">XPath expressions use namespace prefixes for specifying namespaces.</span></span> <span data-ttu-id="811f8-105">Per analizzare un'espressione XPath che contiene i prefissi dello spazio dei nomi, è necessario passare un oggetto ai metodi XPath che implementa <xref:System.Xml.IXmlNamespaceResolver>.</xref:System.Xml.IXmlNamespaceResolver></span><span class="sxs-lookup"><span data-stu-id="811f8-105">To parse an XPath expression that contains namespace prefixes, you must pass an object to the XPath methods that implements <xref:System.Xml.IXmlNamespaceResolver>.</span></span> <span data-ttu-id="811f8-106">Questo esempio viene utilizzato <xref:System.Xml.XmlNamespaceManager>.</xref:System.Xml.XmlNamespaceManager></span><span class="sxs-lookup"><span data-stu-id="811f8-106">This example uses <xref:System.Xml.XmlNamespaceManager>.</span></span>  
  
 <span data-ttu-id="811f8-107">L'espressione XPath è:</span><span class="sxs-lookup"><span data-stu-id="811f8-107">The XPath expression is:</span></span>  
  
 `./aw:*`  
  
## <a name="example"></a><span data-ttu-id="811f8-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="811f8-108">Example</span></span>  
 <span data-ttu-id="811f8-109">Nell'esempio seguente viene letto un albero XML contenente due spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="811f8-109">The following example reads an XML tree that contains two namespaces.</span></span> <span data-ttu-id="811f8-110">Viene utilizzato un <xref:System.Xml.XmlReader>per leggere il documento XML.</xref:System.Xml.XmlReader></span><span class="sxs-lookup"><span data-stu-id="811f8-110">It uses an <xref:System.Xml.XmlReader> to read the XML document.</span></span> <span data-ttu-id="811f8-111">Ottiene quindi un <xref:System.Xml.XmlNameTable>dal <xref:System.Xml.XmlReader>e un <xref:System.Xml.XmlNamespaceManager>da <xref:System.Xml.XmlNameTable>.</xref:System.Xml.XmlNameTable> </xref:System.Xml.XmlNamespaceManager> </xref:System.Xml.XmlReader> </xref:System.Xml.XmlNameTable></span><span class="sxs-lookup"><span data-stu-id="811f8-111">It then gets an <xref:System.Xml.XmlNameTable> from the <xref:System.Xml.XmlReader>, and an <xref:System.Xml.XmlNamespaceManager> from the <xref:System.Xml.XmlNameTable>.</span></span> <span data-ttu-id="811f8-112">Usa il <xref:System.Xml.XmlNamespaceManager>quando si selezionano elementi.</xref:System.Xml.XmlNamespaceManager></span><span class="sxs-lookup"><span data-stu-id="811f8-112">It uses the <xref:System.Xml.XmlNamespaceManager> when selecting elements.</span></span>  
  
```vb  
Dim reader As XmlReader = _  
        XmlReader.Create("ConsolidatedPurchaseOrders.xml")  
Dim root As XElement = XElement.Load(reader)  
Dim nameTable As XmlNameTable = reader.NameTable  
Dim namespaceManager As XmlNamespaceManager = New XmlNamespaceManager(nameTable)  
namespaceManager.AddNamespace("aw", "http://www.adventure-works.com")  
  
Dim list1 As IEnumerable(Of XElement) = _  
        root.XPathSelectElements("./aw:*", namespaceManager)  
Dim list2 As IEnumerable(Of XElement) = _  
    From el In root.Elements() _  
    Where el.Name.Namespace = "http://www.adventure-works.com" _  
    Select el  
  
If list1.Count() = list2.Count() And _  
        list1.Intersect(list2).Count() = list1.Count() Then  
    Console.WriteLine("Results are identical")  
Else  
    Console.WriteLine("Results differ")  
End If  
For Each el As XElement In list2  
    Console.WriteLine(el)  
Next  
```  
  
 <span data-ttu-id="811f8-113">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="811f8-113">This example produces the following output:</span></span>  
  
```  
Results are identical  
<aw:PurchaseOrder PONumber="11223" Date="2000-01-15" xmlns:aw="http://www.adventure-works.com">  
    <aw:ShippingAddress>  
      <aw:Name>Chris Preston</aw:Name>  
      <aw:Street>123 Main St.</aw:Street>  
      <aw:City>Seattle</aw:City>  
      <aw:State>WA</aw:State>  
      <aw:Zip>98113</aw:Zip>  
      <aw:Country>USA</aw:Country>  
    </aw:ShippingAddress>  
    <aw:BillingAddress>  
      <aw:Name>Chris Preston</aw:Name>  
      <aw:Street>123 Main St.</aw:Street>  
      <aw:City>Seattle</aw:City>  
      <aw:State>WA</aw:State>  
      <aw:Zip>98113</aw:Zip>  
      <aw:Country>USA</aw:Country>  
    </aw:BillingAddress>  
    <aw:DeliveryInstructions>Ship only complete order.</aw:DeliveryInstructions>  
    <aw:Item PartNum="LIT-01">  
      <aw:ProductID>Litware Networking Card</aw:ProductID>  
      <aw:Qty>1</aw:Qty>  
      <aw:Price>20.99</aw:Price>  
    </aw:Item>  
    <aw:Item PartNum="LIT-25">  
      <aw:ProductID>Litware 17in LCD Monitor</aw:ProductID>  
      <aw:Qty>1</aw:Qty>  
      <aw:Price>199.99</aw:Price>  
    </aw:Item>  
  </aw:PurchaseOrder>  
```  
  
## <a name="see-also"></a><span data-ttu-id="811f8-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="811f8-114">See Also</span></span>  
 [<span data-ttu-id="811f8-115">LINQ to XML per gli utenti di XPath (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="811f8-115">LINQ to XML for XPath Users (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-for-xpath-users.md)
