---
title: 'Procedura: recuperare informazioni sui conflitti di concorrenza'
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
ms.assetid: 7dd6829e-79a5-4480-9023-9e588cb0bf2e
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: a6766e40b842675cbe37ba1ebeb1a956c19e6318
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-retrieve-member-conflict-information"></a><span data-ttu-id="5489c-102">Procedura: recuperare informazioni sui conflitti di concorrenza</span><span class="sxs-lookup"><span data-stu-id="5489c-102">How to: Retrieve Member Conflict Information</span></span>
<span data-ttu-id="5489c-103">È possibile usare la classe <xref:System.Data.Linq.MemberChangeConflict> per recuperare informazioni sui singoli membri in conflitto.</span><span class="sxs-lookup"><span data-stu-id="5489c-103">You can use the <xref:System.Data.Linq.MemberChangeConflict> class to retrieve information about individual members in conflict.</span></span> <span data-ttu-id="5489c-104">In questo stesso contesto è possibile provvedere alla gestione personalizzata del conflitto per qualsiasi membro.</span><span class="sxs-lookup"><span data-stu-id="5489c-104">In this same context you can provide for custom handling of the conflict for any member.</span></span> <span data-ttu-id="5489c-105">Per ulteriori informazioni, vedere [la concorrenza ottimistica: Panoramica](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5489c-105">For more information, see [Optimistic Concurrency: Overview](../../../../../../docs/framework/data/adonet/sql/linq/optimistic-concurrency-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="5489c-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="5489c-106">Example</span></span>  
 <span data-ttu-id="5489c-107">Il codice riportato di seguito consente di scorrere gli oggetti <xref:System.Data.Linq.ObjectChangeConflict></span><span class="sxs-lookup"><span data-stu-id="5489c-107">The following code iterates through the <xref:System.Data.Linq.ObjectChangeConflict> objects.</span></span> <span data-ttu-id="5489c-108">quindi, per ogni oggetto, di scorrere gli oggetti <xref:System.Data.Linq.MemberChangeConflict>.</span><span class="sxs-lookup"><span data-stu-id="5489c-108">For each object, it then iterates through the <xref:System.Data.Linq.MemberChangeConflict> objects.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5489c-109">Includere <xref:System.Reflection> in modo da fornire informazioni su <xref:System.Data.Linq.MemberChangeConflict.Member%2A>.</span><span class="sxs-lookup"><span data-stu-id="5489c-109">Include <xref:System.Reflection> in order to provide <xref:System.Data.Linq.MemberChangeConflict.Member%2A> information.</span></span>  
  
 [!code-csharp[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.memberchangeconflict/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.MemberChangeConflict#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.memberchangeconflict/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5489c-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5489c-110">See Also</span></span>  
 [<span data-ttu-id="5489c-111">Procedura: gestire i conflitti di modifiche</span><span class="sxs-lookup"><span data-stu-id="5489c-111">How to: Manage Change Conflicts</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-manage-change-conflicts.md)
