---
title: Proiezioni e trasformazioni (LINQ to XML) (C#)
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
ms.assetid: bb0457ab-1823-47e6-9d2d-c93c958cc913
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 9dc3f97281f2cd13a44e52c441b537e9e2c640a6
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="projections-and-transformations-linq-to-xml-c"></a><span data-ttu-id="d04a2-102">Proiezioni e trasformazioni (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-102">Projections and Transformations (LINQ to XML) (C#)</span></span>
<span data-ttu-id="d04a2-103">Questa sezione riporta esempi di proiezioni e trasformazioni di [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d04a2-103">This section provides examples of [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] projections and transformations.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d04a2-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="d04a2-104">In This Section</span></span>  
  
|<span data-ttu-id="d04a2-105">Argomento</span><span class="sxs-lookup"><span data-stu-id="d04a2-105">Topic</span></span>|<span data-ttu-id="d04a2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d04a2-106">Description</span></span>|  
|-----------|-----------------|  
|[<span data-ttu-id="d04a2-107">Procedura: utilizzare dizionari tramite LINQ to XML (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-107">How to: Work with Dictionaries Using LINQ to XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-work-with-dictionaries-using-linq-to-xml.md)|<span data-ttu-id="d04a2-108">Viene illustrato come trasformare dizionari in codice XML e viceversa.</span><span class="sxs-lookup"><span data-stu-id="d04a2-108">Shows how to transform dictionaries to XML, and how to transform XML into dictionaries.</span></span>|  
|[<span data-ttu-id="d04a2-109">Procedura: trasformare la forma di una struttura ad albero XML (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-109">How to: Transform the Shape of an XML Tree (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-transform-the-shape-of-an-xml-tree.md)|<span data-ttu-id="d04a2-110">Viene illustrato come trasformare la forma di un documento XML.</span><span class="sxs-lookup"><span data-stu-id="d04a2-110">Shows how to transform the shape of an XML document.</span></span>|  
|[<span data-ttu-id="d04a2-111">Procedura: controllare il tipo di una proiezione (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-111">How to: Control the Type of a Projection (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-control-the-type-of-a-projection.md)|<span data-ttu-id="d04a2-112">Viene illustrato come controllare il tipo di una query [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d04a2-112">Shows how to control the type of a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] query.</span></span>|  
|[<span data-ttu-id="d04a2-113">Procedura: proiettare un nuovo tipo (LINQ to XML) (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-113">How to: Project a New Type (LINQ to XML) (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-project-a-new-type-linq-to-xml.md)|<span data-ttu-id="d04a2-114">Viene illustrato come proiettare una raccolta di tipo definito dall'utente da una query [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d04a2-114">Shows how to project a collection of a user-defined type from a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] query.</span></span>|  
|[<span data-ttu-id="d04a2-115">Procedura: proiettare un grafico di oggetti (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-115">How to: Project an Object Graph (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-project-an-object-graph.md)|<span data-ttu-id="d04a2-116">Viene illustrato come proiettare un oggetto grafico più complesso da una query [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d04a2-116">Shows how to project a more complex object graph from a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] query.</span></span>|  
|[<span data-ttu-id="d04a2-117">Procedura: proiettare un tipo anonimo (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-117">How to: Project an Anonymous Type (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-project-an-anonymous-type.md)|<span data-ttu-id="d04a2-118">Viene illustrato come proiettare una raccolta di oggetti anonimi da una query [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d04a2-118">Shows how to project a collection of anonymous objects from a [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] query.</span></span>|  
|[<span data-ttu-id="d04a2-119">Procedura: generare file di testo da XML (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-119">How to: Generate Text Files from XML (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-generate-text-files-from-xml.md)|<span data-ttu-id="d04a2-120">Viene illustrato come trasformare un file XML in un file di testo non XML.</span><span class="sxs-lookup"><span data-stu-id="d04a2-120">Shows how to transform an XML file to a non-XML text file.</span></span>|  
|[<span data-ttu-id="d04a2-121">Procedura: generare XML da file CSV (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-121">How to: Generate XML from CSV Files (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/how-to-generate-xml-from-csv-files.md)|<span data-ttu-id="d04a2-122">Viene spiegato come usare [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] per analizzare un file CSV e generare codice XML da esso.</span><span class="sxs-lookup"><span data-stu-id="d04a2-122">Shows how to use [!INCLUDE[vbteclinq](~/includes/vbteclinq-md.md)] to parse a CSV file and generate XML from it.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d04a2-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d04a2-123">See Also</span></span>  
 [<span data-ttu-id="d04a2-124">Esecuzione di query su strutture ad albero XML (C#)</span><span class="sxs-lookup"><span data-stu-id="d04a2-124">Querying XML Trees (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/querying-xml-trees.md)

