---
title: 'Esempi di sintassi di query basate sul metodo: ordinamento'
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
ms.assetid: 5d21b178-d731-471a-8534-1f8184a2ef06
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: de1b610bbc0462c4712c4dec397757ab5c3c9dc1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="method-based-query-syntax-examples-ordering"></a><span data-ttu-id="4b2ec-102">Esempi di sintassi di query basate sul metodo: ordinamento</span><span class="sxs-lookup"><span data-stu-id="4b2ec-102">Method-Based Query Syntax Examples: Ordering</span></span>
<span data-ttu-id="4b2ec-103">Negli esempi in questo argomento viene illustrato come utilizzare il <xref:System.Linq.Enumerable.ThenBy%2A> metodo per eseguire query di [modello Sales di AdventureWorks](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) utilizzando la sintassi di query basate su metodo.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-103">The examples in this topic demonstrate how to use the <xref:System.Linq.Enumerable.ThenBy%2A> method to query the [AdventureWorks Sales Model](http://msdn.microsoft.com/en-us/f16cd988-673f-4376-b034-129ca93c7832) using method-based query syntax.</span></span> <span data-ttu-id="4b2ec-104">Il modello Sales di AdventureWorks usato in questi esempi è compilato in base alle tabelle Contact, Address, Product, SalesOrderHeader e SalesOrderDetail del database di esempio AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-104">The AdventureWorks Sales Model used in these examples is built from the Contact, Address, Product, SalesOrderHeader, and SalesOrderDetail tables in the AdventureWorks sample database.</span></span>  
  
 <span data-ttu-id="4b2ec-105">Gli esempi in questo argomento usano seguenti `using` / `Imports` istruzioni:</span><span class="sxs-lookup"><span data-stu-id="4b2ec-105">The examples in this topic use the following `using`/`Imports` statements:</span></span>  
  
 [!code-csharp[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#importsusing)]
 [!code-vb[DP L2E Examples#ImportsUsing](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#importsusing)]  
  
## <a name="thenby"></a><span data-ttu-id="4b2ec-106">ThenBy</span><span class="sxs-lookup"><span data-stu-id="4b2ec-106">ThenBy</span></span>  
  
### <a name="example"></a><span data-ttu-id="4b2ec-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="4b2ec-107">Example</span></span>  
 <span data-ttu-id="4b2ec-108">Nell'esempio seguente nella sintassi delle query basate su metodo vengono usati gli oggetti <xref:System.Linq.Queryable.OrderBy%2A> e <xref:System.Linq.Queryable.ThenBy%2A> per restituire un elenco di contatti ordinati in base al cognome e quindi al nome.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-108">The following example in method-based query syntax uses <xref:System.Linq.Queryable.OrderBy%2A> and <xref:System.Linq.Queryable.ThenBy%2A> to return a list of contacts ordered by last name and then by first name.</span></span>  
  
 [!code-csharp[DP L2E Examples#OrderByThenBy_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#orderbythenby_mq)]
 [!code-vb[DP L2E Examples#OrderByThenBy_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#orderbythenby_mq)]  
  
## <a name="thenbydescending"></a><span data-ttu-id="4b2ec-109">ThenByDescending</span><span class="sxs-lookup"><span data-stu-id="4b2ec-109">ThenByDescending</span></span>  
  
### <a name="example"></a><span data-ttu-id="4b2ec-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="4b2ec-110">Example</span></span>  
 <span data-ttu-id="4b2ec-111">Nell'esempio seguente vengono usati i metodi <xref:System.Linq.Queryable.OrderBy%2A> e <xref:System.Linq.Queryable.ThenByDescending%2A> per eseguire prima l'ordinamento in base al prezzo di listino e quindi per applicare un ordinamento decrescente ai nomi di prodotto.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-111">The following example uses the <xref:System.Linq.Queryable.OrderBy%2A> and <xref:System.Linq.Queryable.ThenByDescending%2A> methods to first sort by list price, and then perform a descending sort of the product names.</span></span>  
  
 [!code-csharp[DP L2E Examples#ThenByDescending_MQ](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DP L2E Examples/CS/Program.cs#thenbydescending_mq)]
 [!code-vb[DP L2E Examples#ThenByDescending_MQ](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DP L2E Examples/VB/Module1.vb#thenbydescending_mq)]  
  
## <a name="see-also"></a><span data-ttu-id="4b2ec-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4b2ec-112">See Also</span></span>  
 [<span data-ttu-id="4b2ec-113">Query in LINQ to Entities</span><span class="sxs-lookup"><span data-stu-id="4b2ec-113">Queries in LINQ to Entities</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/queries-in-linq-to-entities.md)
