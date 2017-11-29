---
title: Clonazione e Collegamento (C#)
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
ms.assetid: 357c5efa-7b73-4f14-aa67-6bebdba4e7ea
caps.latest.revision: "3"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e58e9538c319c20f9e820ff1de1fb6f973a18bdc
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="cloning-vs-attaching-c"></a><span data-ttu-id="86fb0-102">Clonazione e Collegamento (C#)</span><span class="sxs-lookup"><span data-stu-id="86fb0-102">Cloning vs. Attaching (C#)</span></span>
<span data-ttu-id="86fb0-103">Se quando si aggiungono oggetti <xref:System.Xml.Linq.XNode> (incluso <xref:System.Xml.Linq.XElement>) o <xref:System.Xml.Linq.XAttribute> a un nuovo albero XML, il nuovo contenuto non ha elementi padre, gli oggetti vengono semplicemente collegati all'albero.</span><span class="sxs-lookup"><span data-stu-id="86fb0-103">When adding <xref:System.Xml.Linq.XNode> (including <xref:System.Xml.Linq.XElement>) or <xref:System.Xml.Linq.XAttribute> objects to a new tree, if the new content has no parent, the objects are simply attached to the XML tree.</span></span> <span data-ttu-id="86fb0-104">Se il nuovo contenuto include già elementi padre e fa parte di un altro albero XML viene duplicato.</span><span class="sxs-lookup"><span data-stu-id="86fb0-104">If the new content already is parented, and is part of another XML tree, the new content is cloned.</span></span> <span data-ttu-id="86fb0-105">Il nuovo contesto duplicato viene quindi collegato all'albero XML.</span><span class="sxs-lookup"><span data-stu-id="86fb0-105">The newly cloned content is then attached to the XML tree.</span></span>  
  
## <a name="example"></a><span data-ttu-id="86fb0-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="86fb0-106">Example</span></span>  
 <span data-ttu-id="86fb0-107">Nel codice seguente viene illustrato il diverso comportamento relativo all'aggiunta di un elemento con o senza elemento padre a una struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="86fb0-107">The following code demonstrates the behavior when you add a parented element to a tree, and when you add an element with no parent to a tree.</span></span>  
  
```csharp  
// Create a tree with a child element.  
XElement xmlTree1 = new XElement("Root",  
    new XElement("Child1", 1)  
);  
  
// Create an element that is not parented.  
XElement child2 = new XElement("Child2", 2);  
  
// Create a tree and add Child1 and Child2 to it.  
XElement xmlTree2 = new XElement("Root",  
    xmlTree1.Element("Child1"),  
    child2  
);  
  
// Compare Child1 identity.  
Console.WriteLine("Child1 was {0}",  
    xmlTree1.Element("Child1") == xmlTree2.Element("Child1") ?  
    "attached" : "cloned");  
  
// Compare Child2 identity.  
Console.WriteLine("Child2 was {0}",  
    child2 == xmlTree2.Element("Child2") ?  
    "attached" : "cloned");  
```  
  
 <span data-ttu-id="86fb0-108">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="86fb0-108">This example produces the following output:</span></span>  
  
```  
Child1 was cloned  
Child2 was attached  
```  
  
## <a name="see-also"></a><span data-ttu-id="86fb0-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="86fb0-109">See Also</span></span>  
 [<span data-ttu-id="86fb0-110">Creazione di alberi XML (C#)</span><span class="sxs-lookup"><span data-stu-id="86fb0-110">Creating XML Trees (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/creating-xml-trees.md)
