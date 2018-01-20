---
title: 'Esempi di sintassi di espressione di query: operatori di aggregazione'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: d729120c-4c1b-4f34-bbe9-33694fca2dde
caps.latest.revision: "3"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 76af42681767b17fd69fac5bfd924e02b0f6b9b0
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="query-expression-syntax-examples-aggregate-operators"></a><span data-ttu-id="11b8c-102">Esempi di sintassi di espressione di query: operatori di aggregazione</span><span class="sxs-lookup"><span data-stu-id="11b8c-102">Query Expression Syntax Examples: Aggregate Operators</span></span>
<span data-ttu-id="11b8c-103">Negli esempi in questo argomento viene illustrato come utilizzare il <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A>, e <xref:System.Linq.Enumerable.Sum%2A> metodi per eseguire una query di [modello Sales di AdventureWorks](http://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) usando la sintassi di espressione di query.</span><span class="sxs-lookup"><span data-stu-id="11b8c-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.Average%2A>, <xref:System.Linq.Enumerable.Count%2A>, <xref:System.Linq.Enumerable.Max%2A>, <xref:System.Linq.Enumerable.Min%2A>, and <xref:System.Linq.Enumerable.Sum%2A> methods to query the [AdventureWorks Sales Model](http://msdn.microsoft.com/library/f16cd988-673f-4376-b034-129ca93c7832) using query expression syntax.</span></span> <span data-ttu-id="11b8c-104">Il modello Sales di AdventureWorks usato in questi esempi è compilato in base alle tabelle Contact, Address, Product, SalesOrderHeader e SalesOrderDetail del database di esempio AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="11b8c-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="11b8c-105">Gli esempi in questo argomento usano seguenti `using` / `Imports` istruzioni:</span><span class="sxs-lookup"><span data-stu-id="11b8c-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="average"></a><span data-ttu-id="11b8c-106">Media</span><span class="sxs-lookup"><span data-stu-id="11b8c-106">Average</span></span>  
  
### <a name="example"></a><span data-ttu-id="11b8c-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-107">Example</span></span>  
 <span data-ttu-id="11b8c-108">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Average%2A> per individuare il prezzo medio di listino dei prodotti per ogni stile.</span><span class="sxs-lookup"><span data-stu-id="11b8c-108">The following example uses the <xref:System.Linq.Enumerable.Average%2A> method to find the average list price of the products of each style.</span></span>  
  
 [!code-csharp[DP L2E Examples#Average2_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#average2_mq)]
 [!code-vb[DP L2E Examples#Average2_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#average2_mq)]  
  
### <a name="example"></a><span data-ttu-id="11b8c-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-109">Example</span></span>  
 <span data-ttu-id="11b8c-110">Nell'esempio seguente viene usato <xref:System.Linq.Enumerable.Average%2A> per ottenere il totale medio dovuto per ogni ID contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-110">The following example uses <xref:System.Linq.Enumerable.Average%2A> to get the average total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#AverageGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#averagegrouped_mq)]
 [!code-vb[DP L2E Examples#AverageGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#averagegrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="11b8c-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-111">Example</span></span>  
 <span data-ttu-id="11b8c-112">Nell'esempio seguente viene usato <xref:System.Linq.Enumerable.Average%2A> per ottenere gli ordini con il totale medio dovuto per ogni contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-112">The following example uses <xref:System.Linq.Enumerable.Average%2A> to get the orders with the average total due for each contact.</span></span>  
  
 [!code-csharp[DP L2E Examples#AverageElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#averageelements_mq)]
 [!code-vb[DP L2E Examples#AverageElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#averageelements_mq)]  
  
## <a name="count"></a><span data-ttu-id="11b8c-113">Conteggio</span><span class="sxs-lookup"><span data-stu-id="11b8c-113">Count</span></span>  
  
### <a name="example"></a><span data-ttu-id="11b8c-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-114">Example</span></span>  
 <span data-ttu-id="11b8c-115">Nell'esempio seguente viene usato <xref:System.Linq.Enumerable.Count%2A> per restituire un elenco di ID contatto e la quantità di ordini di ciascuno.</span><span class="sxs-lookup"><span data-stu-id="11b8c-115">The following example uses <xref:System.Linq.Enumerable.Count%2A> to return a list of contact IDs and how many orders each has.</span></span>  
  
 [!code-csharp[DP L2E Examples#CountNested](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#countnested)]
 [!code-vb[DP L2E Examples#CountNested](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#countnested)]  
  
### <a name="example"></a><span data-ttu-id="11b8c-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-116">Example</span></span>  
 <span data-ttu-id="11b8c-117">Nell'esempio seguente vengono raggruppati i prodotti in base al colore e viene usato <xref:System.Linq.Enumerable.Count%2A> per restituire il numero di prodotti inclusi in ciascun gruppo.</span><span class="sxs-lookup"><span data-stu-id="11b8c-117">The following example groups products by color and uses <xref:System.Linq.Enumerable.Count%2A> to return the number of products in each color group.</span></span>  
  
 [!code-csharp[DP L2E Examples#CountGrouped](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#countgrouped)]
 [!code-vb[DP L2E Examples#CountGrouped](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#countgrouped)]  
  
## <a name="max"></a><span data-ttu-id="11b8c-118">Max</span><span class="sxs-lookup"><span data-stu-id="11b8c-118">Max</span></span>  
  
### <a name="example"></a><span data-ttu-id="11b8c-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-119">Example</span></span>  
 <span data-ttu-id="11b8c-120">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Max%2A> per ottenere il totale massimo dovuto per ogni ID contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-120">The following example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the largest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MaxGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#maxgrouped_mq)]
 [!code-vb[DP L2E Examples#MaxGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#maxgrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="11b8c-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-121">Example</span></span>  
 <span data-ttu-id="11b8c-122">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Max%2A> per ottenere gli ordini con il totale massimo dovuto per ogni ID contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-122">The following example uses the <xref:System.Linq.Enumerable.Max%2A> method to get the orders with the largest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MaxElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#maxelements_mq)]
 [!code-vb[DP L2E Examples#MaxElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#maxelements_mq)]  
  
## <a name="min"></a><span data-ttu-id="11b8c-123">Min</span><span class="sxs-lookup"><span data-stu-id="11b8c-123">Min</span></span>  
  
### <a name="example"></a><span data-ttu-id="11b8c-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-124">Example</span></span>  
 <span data-ttu-id="11b8c-125">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Min%2A> per ottenere il totale minimo dovuto per ogni ID contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-125">The following example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the smallest total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#MinGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#mingrouped_mq)]
 [!code-vb[DP L2E Examples#MinGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#mingrouped_mq)]  
  
### <a name="example"></a><span data-ttu-id="11b8c-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-126">Example</span></span>  
 <span data-ttu-id="11b8c-127">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Min%2A> per ottenere gli ordini con il totale minimo dovuto per ogni contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-127">The following example uses the <xref:System.Linq.Enumerable.Min%2A> method to get the orders with the smallest total due for each contact.</span></span>  
  
 [!code-csharp[DP L2E Examples#MinElements_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#minelements_mq)]
 [!code-vb[DP L2E Examples#MinElements_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#minelements_mq)]  
  
## <a name="sum"></a><span data-ttu-id="11b8c-128">Sum</span><span class="sxs-lookup"><span data-stu-id="11b8c-128">Sum</span></span>  
  
### <a name="example"></a><span data-ttu-id="11b8c-129">Esempio</span><span class="sxs-lookup"><span data-stu-id="11b8c-129">Example</span></span>  
 <span data-ttu-id="11b8c-130">Nell'esempio seguente viene usato il metodo <xref:System.Linq.Enumerable.Sum%2A> per ottenere il totale dovuto per ogni ID contatto.</span><span class="sxs-lookup"><span data-stu-id="11b8c-130">The following example uses the <xref:System.Linq.Enumerable.Sum%2A> method to get the total due for each contact ID.</span></span>  
  
 [!code-csharp[DP L2E Examples#SumGrouped_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#sumgrouped_mq)]
 [!code-vb[DP L2E Examples#SumGrouped_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#sumgrouped_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="11b8c-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="11b8c-131">See Also</span></span>  
 [<span data-ttu-id="11b8c-132">Query in LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="11b8c-132">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
