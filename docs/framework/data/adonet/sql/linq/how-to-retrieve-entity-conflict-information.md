---
title: "Procedura: recuperare informazioni sui conflitti di entità"
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
ms.assetid: 9a02b608-e7bb-4041-a452-a7fed26fd008
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 885c411491564244c26123a0dc8abcad47b31b62
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="how-to-retrieve-entity-conflict-information"></a><span data-ttu-id="60e53-102">Procedura: recuperare informazioni sui conflitti di entità</span><span class="sxs-lookup"><span data-stu-id="60e53-102">How to: Retrieve Entity Conflict Information</span></span>
<span data-ttu-id="60e53-103">È possibile usare oggetti della classe <xref:System.Data.Linq.ObjectChangeConflict> per fornire informazioni sui conflitti rivelati dalle eccezioni <xref:System.Data.Linq.ChangeConflictException>.</span><span class="sxs-lookup"><span data-stu-id="60e53-103">You can use objects of the <xref:System.Data.Linq.ObjectChangeConflict> class to provide information about conflicts revealed by <xref:System.Data.Linq.ChangeConflictException> exceptions.</span></span> <span data-ttu-id="60e53-104">Per ulteriori informazioni, vedere [la concorrenza ottimistica: Panoramica](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60e53-104">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="60e53-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="60e53-105">Example</span></span>  
 <span data-ttu-id="60e53-106">L'esempio riportato di seguito consente di scorrere un elenco di conflitti accumulati.</span><span class="sxs-lookup"><span data-stu-id="60e53-106">The following example iterates through a list of accumulated conflicts.</span></span>  
  
 [!code-csharp[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.objectchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.ObjectChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.objectchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="60e53-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="60e53-107">See Also</span></span>  
 [<span data-ttu-id="60e53-108">Procedura: gestire i conflitti di modifiche</span><span class="sxs-lookup"><span data-stu-id="60e53-108">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
