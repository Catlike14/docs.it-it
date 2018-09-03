---
title: 'File XML di esempio: tipico ordine di acquisto in uno spazio dei nomi1'
ms.date: 07/20/2015
ms.assetid: 84dc3339-ea32-4ccc-9af6-ab38ddfecced
ms.openlocfilehash: 0adee32a3ee4d2347bd2e0a84024fe478346987a
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/03/2018
ms.locfileid: "43404230"
---
# <a name="sample-xml-file-typical-purchase-order-in-a-namespace"></a><span data-ttu-id="0a016-102">File XML di esempio: tipico ordine di acquisto in uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0a016-102">Sample XML File: Typical Purchase Order in a Namespace</span></span>
<span data-ttu-id="0a016-103">Il file XML seguente viene usato in vari esempi nella documentazione di [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="0a016-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="0a016-104">Si tratta di un ordine di acquisto tipico.</span><span class="sxs-lookup"><span data-stu-id="0a016-104">This file is a typical purchase order.</span></span> <span data-ttu-id="0a016-105">L'XML si trova in uno spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0a016-105">The XML is in a namespace.</span></span>  
  
## <a name="purchaseorderinnamespacexml"></a><span data-ttu-id="0a016-106">PurchaseOrderInNamespace.xml</span><span class="sxs-lookup"><span data-stu-id="0a016-106">PurchaseOrderInNamespace.xml</span></span>  
  
```xml  
<?xml version="1.0"?>  
<aw:PurchaseOrder  
    aw:PurchaseOrderNumber="99503"  
    aw:OrderDate="1999-10-20"  
    xmlns:aw="http://www.adventure-works.com">  
  <aw:Address aw:Type="Shipping">  
    <aw:Name>Ellen Adams</aw:Name>  
    <aw:Street>123 Maple Street</aw:Street>  
    <aw:City>Mill Valley</aw:City>  
    <aw:State>CA</aw:State>  
    <aw:Zip>10999</aw:Zip>  
    <aw:Country>USA</aw:Country>  
  </aw:Address>  
  <aw:Address aw:Type="Billing">  
    <aw:Name>Tai Yee</aw:Name>  
    <aw:Street>8 Oak Avenue</aw:Street>  
    <aw:City>Old Town</aw:City>  
    <aw:State>PA</aw:State>  
    <aw:Zip>95819</aw:Zip>  
    <aw:Country>USA</aw:Country>  
  </aw:Address>  
  <aw:DeliveryNotes>Please leave packages in shed by driveway.</aw:DeliveryNotes>  
  <aw:Items>  
    <aw:Item aw:PartNumber="872-AA">  
      <aw:ProductName>Lawnmower</aw:ProductName>  
      <aw:Quantity>1</aw:Quantity>  
      <aw:USPrice>148.95</aw:USPrice>  
      <aw:Comment>Confirm this is electric</aw:Comment>  
    </aw:Item>  
    <aw:Item aw:PartNumber="926-AA">  
      <aw:ProductName>Baby Monitor</aw:ProductName>  
      <aw:Quantity>2</aw:Quantity>  
      <aw:USPrice>39.98</aw:USPrice>  
      <aw:ShipDate>1999-05-21</aw:ShipDate>  
    </aw:Item>  
  </aw:Items>  
</aw:PurchaseOrder>  
```  
  
## <a name="see-also"></a><span data-ttu-id="0a016-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0a016-107">See Also</span></span>  
 [<span data-ttu-id="0a016-108">Documenti XML di esempio (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="0a016-108">Sample XML Documents (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
