---
title: Eliminare elementi duplicati da una sequenza
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
ms.assetid: 2b224a84-bad5-4843-adcc-14e784d280f5
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 3f3196b07c84ac5c63d883eef35d29b450c3b285
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="eliminate-duplicate-elements-from-a-sequence"></a><span data-ttu-id="82f67-102">Eliminare elementi duplicati da una sequenza</span><span class="sxs-lookup"><span data-stu-id="82f67-102">Eliminate Duplicate Elements from a Sequence</span></span>
<span data-ttu-id="82f67-103">Per eliminare elementi duplicati da una sequenza, usare l'operatore <xref:System.Linq.Queryable.Distinct%2A>.</span><span class="sxs-lookup"><span data-stu-id="82f67-103">Use the <xref:System.Linq.Queryable.Distinct%2A> operator to eliminate duplicate elements from a sequence.</span></span>  
  
## <a name="example"></a><span data-ttu-id="82f67-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="82f67-104">Example</span></span>  
 <span data-ttu-id="82f67-105">Nell'esempio riportato di seguito viene usato <xref:System.Linq.Queryable.Distinct%2A> per selezionare una sequenza di città univoche in cui sono presenti clienti.</span><span class="sxs-lookup"><span data-stu-id="82f67-105">The following example uses <xref:System.Linq.Queryable.Distinct%2A> to select a sequence of the unique cities that have customers.</span></span>  
  
 [!code-csharp[DLinqQueryExamples#36](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryExamples/cs/Program.cs#36)]
 [!code-vb[DLinqQueryExamples#36](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryExamples/vb/Module1.vb#36)]  
  
## <a name="see-also"></a><span data-ttu-id="82f67-106">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="82f67-106">See Also</span></span>  
 [<span data-ttu-id="82f67-107">Esempi di query</span><span class="sxs-lookup"><span data-stu-id="82f67-107">Query Examples</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-examples.md)
