---
title: 'Procedura: gestire le chiavi composite nelle query'
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
ms.assetid: ce2f14fd-1038-458a-91e3-a078c61f0d10
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 168e721eee7f5253412438a2185934f01bf081c1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-handle-composite-keys-in-queries"></a><span data-ttu-id="c1374-102">Procedura: gestire le chiavi composite nelle query</span><span class="sxs-lookup"><span data-stu-id="c1374-102">How to: Handle Composite Keys in Queries</span></span>
<span data-ttu-id="c1374-103">Alcuni operatori possono accettare un solo argomento.</span><span class="sxs-lookup"><span data-stu-id="c1374-103">Some operators can take only one argument.</span></span> <span data-ttu-id="c1374-104">Se l'argomento deve includere più di una colonna del database, è necessario creare un tipo anonimo per rappresentare la combinazione.</span><span class="sxs-lookup"><span data-stu-id="c1374-104">If your argument must include more than one column from the database, you must create an anonymous type to represent the combination.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1374-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1374-105">Example</span></span>  
 <span data-ttu-id="c1374-106">Nell'esempio seguente viene illustrata una query che richiama l'operatore `GroupBy` che può accettare un solo argomento `key`.</span><span class="sxs-lookup"><span data-stu-id="c1374-106">The following example shows a query that invokes the `GroupBy` operator, which can take only one `key` argument.</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#1)]
 [!code-vb[DLinqCompositeKeys#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#1)]  
  
## <a name="example"></a><span data-ttu-id="c1374-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="c1374-107">Example</span></span>  
 <span data-ttu-id="c1374-108">La stessa situazione è applicabile ai join, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="c1374-108">The same situation pertains to joins, as in the following example:</span></span>  
  
 [!code-csharp[DLinqCompositeKeys#2](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCompositeKeys/cs/Program.cs#2)]
 [!code-vb[DLinqCompositeKeys#2](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCompositeKeys/vb/Module1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="c1374-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c1374-109">See Also</span></span>  
 [<span data-ttu-id="c1374-110">Concetti relativi alle query</span><span class="sxs-lookup"><span data-stu-id="c1374-110">Query Concepts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
