---
title: Assi integrati nel linguaggio in Visual Basic (LINQ to XML)
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d450a556-a134-4261-b011-44e399660894
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d648ba7c8710f73c4aeb8dad3983f219c5fe1815
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="language-integrated-axes-in-visual-basic-linq-to-xml"></a><span data-ttu-id="50ceb-102">Assi integrati nel linguaggio in Visual Basic (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="50ceb-102">Language-Integrated Axes in Visual Basic (LINQ to XML)</span></span>
<span data-ttu-id="50ceb-103">Questa sezione vengono descritte le funzionalità incorporate nel [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] linguaggio per semplificare l'accesso a XML.</span><span class="sxs-lookup"><span data-stu-id="50ceb-103">This section describes features built directly into the [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] language to make it easy to access XML.</span></span> <span data-ttu-id="50ceb-104">Questi assi [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] integrati vengono usati in molti degli esempi della documentazione relativa a LINQ to XML.</span><span class="sxs-lookup"><span data-stu-id="50ceb-104">Many of the examples in the LINQ to XML documentation use these integrated [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] axes.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="50ceb-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="50ceb-105">In This Section</span></span>  
  
|<span data-ttu-id="50ceb-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="50ceb-106">Topic</span></span>|<span data-ttu-id="50ceb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ceb-107">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="50ceb-108">Proprietà Child Axis XML</span><span class="sxs-lookup"><span data-stu-id="50ceb-108">XML Child Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-child-axis-property.md)|<span data-ttu-id="50ceb-109">Fornisce l'accesso agli elementi figlio di uno dei seguenti oggetti: <xref:System.Xml.Linq.XElement>, <xref:System.Xml.Linq.XDocument>, raccolta di <xref:System.Xml.Linq.XElement> o raccolta di <xref:System.Xml.Linq.XDocument>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-109">Provides access to the children of one of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, a collection of <xref:System.Xml.Linq.XElement> objects, or a collection of <xref:System.Xml.Linq.XDocument> objects.</span></span> <span data-ttu-id="50ceb-110">Questo asse è equivalente all'asse <xref:System.Xml.Linq.XContainer.Elements%2A>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-110">This axis is equivalent to the <xref:System.Xml.Linq.XContainer.Elements%2A> axis.</span></span>|  
|[<span data-ttu-id="50ceb-111">Proprietà axis descendant XML</span><span class="sxs-lookup"><span data-stu-id="50ceb-111">XML Descendant Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-descendant-axis-property.md)|<span data-ttu-id="50ceb-112">Fornisce l'accesso ai discendenti di uno dei seguenti oggetti: <xref:System.Xml.Linq.XElement>, <xref:System.Xml.Linq.XDocument> o raccolta di <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-112">Provides access to the descendants of the following: an <xref:System.Xml.Linq.XElement> object, an <xref:System.Xml.Linq.XDocument> object, or a collection of <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="50ceb-113">Questo asse è equivalente all'asse <xref:System.Xml.Linq.XContainer.Descendants%2A>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-113">This axis is equivalent to the <xref:System.Xml.Linq.XContainer.Descendants%2A> axis.</span></span>|  
|[<span data-ttu-id="50ceb-114">Proprietà axis dell'attributo XML</span><span class="sxs-lookup"><span data-stu-id="50ceb-114">XML Attribute Axis Property</span></span>](../../../../visual-basic/language-reference/xml-axis/xml-attribute-axis-property.md)|<span data-ttu-id="50ceb-115">Fornisce l'accesso a un attributo di un oggetto <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-115">Provides access to an attribute of an <xref:System.Xml.Linq.XElement> object.</span></span> <span data-ttu-id="50ceb-116">Questo asse è quasi equivalente all'asse <xref:System.Xml.Linq.XElement.Attribute%2A>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-116">This axis is roughly equivalent to the <xref:System.Xml.Linq.XElement.Attribute%2A> axis.</span></span> <span data-ttu-id="50ceb-117">Questo asse è diverso dall'asse <xref:System.Xml.Linq.XElement.Attribute%2A>, in quanto restituisce il valore dell'attributo, non un oggetto <xref:System.Xml.Linq.XAttribute>.</span><span class="sxs-lookup"><span data-stu-id="50ceb-117">This axis differs from the <xref:System.Xml.Linq.XElement.Attribute%2A> axis in that it returns the value of the attribute, not an <xref:System.Xml.Linq.XAttribute> object.</span></span>|  
|[<span data-ttu-id="50ceb-118">Proprietà dell'indicizzatore di estensione</span><span class="sxs-lookup"><span data-stu-id="50ceb-118">Extension Indexer Property</span></span>](../../../../visual-basic/language-reference/xml-axis/extension-indexer-property.md)|<span data-ttu-id="50ceb-119">Fornisce l'accesso ai singoli elementi di una raccolta.</span><span class="sxs-lookup"><span data-stu-id="50ceb-119">Provides access to individual elements in a collection.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="50ceb-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50ceb-120">See Also</span></span>  
 [<span data-ttu-id="50ceb-121">Assi LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="50ceb-121">LINQ to XML Axes (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml-axes.md)
