---
title: Modifica di dati XML con XPathNavigator
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b1f91616-3115-4264-9821-c66589d11d11
caps.latest.revision: "2"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 488651181aaec34c52f368d8829b1c556e6e746e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="editing-xml-data-using-xpathnavigator"></a><span data-ttu-id="3e888-102">Modifica di dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-102">Editing XML Data using XPathNavigator</span></span>
<span data-ttu-id="3e888-103">La classe <xref:System.Xml.XPath.XPathNavigator> fornisce dei metodi per inserire, modificare e rimuovere nodi e valori da un documento XML contenuto in un oggetto <xref:System.Xml.XmlDocument>.</span><span class="sxs-lookup"><span data-stu-id="3e888-103">The <xref:System.Xml.XPath.XPathNavigator> class provides methods to insert, modify and remove nodes and values from an XML document contained in an <xref:System.Xml.XmlDocument> object.</span></span> <span data-ttu-id="3e888-104">Per usare tali metodi, è necessario che l'oggetto <xref:System.Xml.XPath.XPathNavigator> sia modificabile, ovvero che la relativa proprietà <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> sia impostata su true.</span><span class="sxs-lookup"><span data-stu-id="3e888-104">In order to use any of these methods to insert, modify, and remove nodes and values, the <xref:System.Xml.XPath.XPathNavigator> object must be editable, that is, its <xref:System.Xml.XPath.XPathNavigator.CanEdit%2A> property must be true.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="3e888-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3e888-105">In This Section</span></span>  
 [<span data-ttu-id="3e888-106">Inserire i dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-106">Insert XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/insert-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="3e888-107">Viene descritto come inserire valori e nodi Attribute, nodi figlio e nodi di pari livello in un oggetto <xref:System.Xml.XmlDocument> usando la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="3e888-107">Describes how to insert sibling, child, attribute nodes and values in to an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="3e888-108">Modifica dei dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-108">Modify XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/modify-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="3e888-109">Viene descritto come modificare nodi e valori in un oggetto <xref:System.Xml.XmlDocument> usando la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="3e888-109">Describes how to modify nodes and values in an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
 [<span data-ttu-id="3e888-110">Rimozione di dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-110">Remove XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/remove-xml-data-using-xpathnavigator.md)  
 <span data-ttu-id="3e888-111">Viene descritto come rimuovere nodi e valori da un oggetto <xref:System.Xml.XmlDocument> usando la classe <xref:System.Xml.XPath.XPathNavigator>.</span><span class="sxs-lookup"><span data-stu-id="3e888-111">Describes how to remove nodes and values from an <xref:System.Xml.XmlDocument> object using the <xref:System.Xml.XPath.XPathNavigator> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3e888-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3e888-112">See Also</span></span>  
 <xref:System.Xml.XmlDocument>  
 <xref:System.Xml.XPath.XPathDocument>  
 <xref:System.Xml.XPath.XPathNavigator>  
 [<span data-ttu-id="3e888-113">Elaborazione di dati XML con il modello di dati XPath</span><span class="sxs-lookup"><span data-stu-id="3e888-113">Process XML Data Using the XPath Data Model</span></span>](../../../../docs/standard/data/xml/process-xml-data-using-the-xpath-data-model.md)  
 [<span data-ttu-id="3e888-114">Lettura di dati XML con XPathDocument e XmlDocument</span><span class="sxs-lookup"><span data-stu-id="3e888-114">Reading XML Data using XPathDocument and XmlDocument</span></span>](../../../../docs/standard/data/xml/reading-xml-data-using-xpathdocument-and-xmldocument.md)  
 [<span data-ttu-id="3e888-115">Selezione, valutazione e corrispondenza di dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-115">Selecting, Evaluating and Matching XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/selecting-evaluating-and-matching-xml-data-using-xpathnavigator.md)  
 [<span data-ttu-id="3e888-116">Accesso ai dati XML con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-116">Accessing XML Data using XPathNavigator</span></span>](../../../../docs/standard/data/xml/accessing-xml-data-using-xpathnavigator.md)  
 [<span data-ttu-id="3e888-117">Convalida dello schema con XPathNavigator</span><span class="sxs-lookup"><span data-stu-id="3e888-117">Schema Validation using XPathNavigator</span></span>](../../../../docs/standard/data/xml/schema-validation-using-xpathnavigator.md)
