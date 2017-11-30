---
title: "Lettura delle dichiarazioni di entità e dei riferimenti a entità nel DOM"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 86dba977-5cc4-4567-964f-027ffabc47b2
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 6370db06cbe7ff8d46258b0315059f5c37587fea
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="reading-entity-declarations-and-entity-references-into-the-dom"></a><span data-ttu-id="c6fd7-102">Lettura delle dichiarazioni di entità e dei riferimenti a entità nel DOM</span><span class="sxs-lookup"><span data-stu-id="c6fd7-102">Reading Entity Declarations and Entity References into the DOM</span></span>
<span data-ttu-id="c6fd7-103">Un'entità è una dichiarazione che stabilisce il nome da usare in XML al posto del contenuto o del markup.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-103">An entity is a declaration that states a name to be used in the XML in place of content or markup.</span></span> <span data-ttu-id="c6fd7-104">Le entità sono composte da due parti.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-104">There are two parts to entities.</span></span> <span data-ttu-id="c6fd7-105">Innanzitutto, è necessario associare un nome al contenuto di sostituzione tramite una dichiarazione di entità.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-105">First, you must tie a name to the replacement content using an entity declaration.</span></span> <span data-ttu-id="c6fd7-106">La dichiarazione di entità viene creata mediante la sintassi `<!ENTITY name "value">` in una DTD (Document Type Definition) o in uno schema XML.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-106">An entity declaration is created by using the `<!ENTITY name "value">` syntax in a document type definition (DTD) or XML schema.</span></span> <span data-ttu-id="c6fd7-107">Successivamente, il nome definito nella dichiarazione di entità viene usato in XML</span><span class="sxs-lookup"><span data-stu-id="c6fd7-107">Secondly, the name defined in the entity declaration is subsequently used in the XML.</span></span> <span data-ttu-id="c6fd7-108">e, in questo caso, viene denominato riferimento all'entità.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-108">When used in the XML, it is called an entity reference.</span></span> <span data-ttu-id="c6fd7-109">Ad esempio, la dichiarazione di entità seguente dichiara un'entità il cui nome `publisher` viene associato al contenuto di "Microsoft Press".</span><span class="sxs-lookup"><span data-stu-id="c6fd7-109">For example, the following entity declaration declares an entity of the name `publisher` being associated with the content of "Microsoft Press".</span></span>  
  
```xml  
<!ENTITY publisher "Microsoft Press">  
```  
  
 <span data-ttu-id="c6fd7-110">Nel seguente esempio è illustrato l'uso di questa dichiarazione di entità in XML come riferimento all'entità.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-110">The following example shows the use of this entity declaration in XML as an entity reference.</span></span>  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by &publisher;</pubinfo>  
```  
  
 <span data-ttu-id="c6fd7-111">Alcuni parser consentono di espandere automaticamente le entità quando viene caricato un documento in memoria.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-111">Some parsers automatically expand entities when a document is loaded into memory.</span></span> <span data-ttu-id="c6fd7-112">Quindi, quando l'XML viene letto in memoria, le dichiarazioni di entità vengono memorizzate e salvate.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-112">Therefore, when the XML is being read into memory, entity declarations are remembered and saved.</span></span> <span data-ttu-id="c6fd7-113">Durante il successivo rilevamento dei caratteri `&;`, che identificano un riferimento a un'entità generale, il parser ricercherà quel determinato nome in una tabella delle dichiarazioni di entità.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-113">When the parser subsequently encounters `&;` characters, which identify a general entity reference, the parser looks up that name in an entity declaration table.</span></span> <span data-ttu-id="c6fd7-114">Il riferimento `&publisher;` verrà sostituito dal contenuto che rappresenta.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-114">The reference, `&publisher;` is replaced by the content that it represents.</span></span> <span data-ttu-id="c6fd7-115">Usando il seguente codice XML,</span><span class="sxs-lookup"><span data-stu-id="c6fd7-115">Using the following XML,</span></span>  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by &publisher;</pubinfo>  
```  
  
 <span data-ttu-id="c6fd7-116">espandendo il riferimento all'entità e sostituendo `&publisher;` con il contenuto di Microsoft Press viene fornito il seguente codice XML espanso.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-116">expanding the entity reference and replacing the `&publisher;` with the Microsoft Press content gives the following expanded XML.</span></span>  
  
 <span data-ttu-id="c6fd7-117">**Output**</span><span class="sxs-lookup"><span data-stu-id="c6fd7-117">**Output**</span></span>  
  
```xml  
<author>Fred</author>  
<pubinfo>Published by Microsoft Press</pubinfo>  
```  
  
 <span data-ttu-id="c6fd7-118">Esistono molti tipi di entità.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-118">There are many kinds of entities.</span></span> <span data-ttu-id="c6fd7-119">Nel diagramma seguente è riportata la suddivisione dei tipi di entità e della terminologia.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-119">The following diagram shows the breakdown of entity types and terminology.</span></span>  
  
 <span data-ttu-id="c6fd7-120">![diagramma di flusso della gerarchia dei tipi di entità](../../../../docs/standard/data/xml/media/entity-hierarchy.gif "Entity_hierarchy")</span><span class="sxs-lookup"><span data-stu-id="c6fd7-120">![flow chart of entity type hierarchy](../../../../docs/standard/data/xml/media/entity-hierarchy.gif "Entity_hierarchy")</span></span>  
  
 <span data-ttu-id="c6fd7-121">Il valore predefinito per l'implementazione di Microsoft .NET Framework dell'oggetto modello DOM (Document XML) è di preservare i riferimenti a entità e non le entità vengono espanse quando si carica il XML.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-121">The default for the Microsoft .NET Framework implementation of the XML Document Object Model (DOM) is to preserve the entities references and not expand the entities when the XML is loaded.</span></span> <span data-ttu-id="c6fd7-122">L'implicazione di ciò è che quando un documento viene caricato nel DOM, un **XmlEntityReference** nodo che contiene la variabile di riferimento `&publisher;` viene creato, i nodi figlio che rappresenta il contenuto dell'entità dichiarata nella DTD.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-122">The implication of this is that as a document is loaded in the DOM, an **XmlEntityReference** node containing the reference variable `&publisher;` is created, with child nodes representing the content in the entity declared in the DTD.</span></span>  
  
 <span data-ttu-id="c6fd7-123">Utilizzando il `<!ENTITY publisher "Microsoft Press">` dichiarazione di entità, il diagramma seguente mostra il **XmlEntity** e **XmlText** nodi creati da questa dichiarazione.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-123">Using the `<!ENTITY publisher "Microsoft Press">` entity declaration, the following diagram shows the **XmlEntity** and **XmlText** nodes created from this declaration.</span></span>  
  
 <span data-ttu-id="c6fd7-124">![nodi creati da dichiarazioni di entità](../../../../docs/standard/data/xml/media/xml-entitydeclaration-node2.png "xml_entitydeclaration_node2")</span><span class="sxs-lookup"><span data-stu-id="c6fd7-124">![nodes created from entity declaration](../../../../docs/standard/data/xml/media/xml-entitydeclaration-node2.png "xml_entitydeclaration_node2")</span></span>  
  
 <span data-ttu-id="c6fd7-125">Il fatto che i riferimenti alle entità vengano espansi o meno determina quali nodi vengono generati nell'albero DOM, in memoria.</span><span class="sxs-lookup"><span data-stu-id="c6fd7-125">The differences when entity references are expanded and when they are not makes a difference in what nodes are generated in the DOM tree, in memory.</span></span> <span data-ttu-id="c6fd7-126">La differenza tra i nodi generati è descritta negli argomenti [riferimenti alle entità conservati](../../../../docs/standard/data/xml/entity-references-are-preserved.md) e [i riferimenti alle entità vengono espansi e non conservati](../../../../docs/standard/data/xml/entity-references-are-expanded-and-not-preserved.md).</span><span class="sxs-lookup"><span data-stu-id="c6fd7-126">The difference in the nodes that are generated is explained in the topics [Entity References are Preserved](../../../../docs/standard/data/xml/entity-references-are-preserved.md) and [Entity References are Expanded and Not Preserved](../../../../docs/standard/data/xml/entity-references-are-expanded-and-not-preserved.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c6fd7-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c6fd7-127">See Also</span></span>  
 [<span data-ttu-id="c6fd7-128">XML Document Object Model (DOM)</span><span class="sxs-lookup"><span data-stu-id="c6fd7-128">XML Document Object Model (DOM)</span></span>](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
