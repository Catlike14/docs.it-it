---
title: 'Procedura: filtrare dati correlati'
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
ms.assetid: ec8b8f97-5d01-4f31-9b97-d1556df6a4bc
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: 9d51ac97611379cc6c47ef698bc635bbf46d1e5f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-filter-related-data"></a><span data-ttu-id="b93cc-102">Procedura: filtrare dati correlati</span><span class="sxs-lookup"><span data-stu-id="b93cc-102">How to: Filter Related Data</span></span>
<span data-ttu-id="b93cc-103">Usare il metodo <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> per specificare sottoquery che consentano di limitare la quantità di dati recuperati.</span><span class="sxs-lookup"><span data-stu-id="b93cc-103">Use the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method to specify sub-queries to limit the amount of retrieved data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b93cc-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="b93cc-104">Example</span></span>  
 <span data-ttu-id="b93cc-105">Nell'esempio seguente il metodo <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> limita il numero di `Orders` recuperati a quelli non spediti in data odierna.</span><span class="sxs-lookup"><span data-stu-id="b93cc-105">In the following example, the <xref:System.Data.Linq.DataLoadOptions.AssociateWith%2A> method limits the `Orders` retrieved to those that have not been shipped today.</span></span> <span data-ttu-id="b93cc-106">Senza questo approccio verrebbero recuperati tutti gli elementi in `Orders`, anche se è richiesto solo un subset.</span><span class="sxs-lookup"><span data-stu-id="b93cc-106">Without this approach, all `Orders` would have been retrieved even though only a subset is desired.</span></span>  
  
 [!code-csharp[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/system.data.linq.dataloadoptions/cs/program.cs#1)]
 [!code-vb[System.Data.Linq.DataLoadOptions#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/system.data.linq.dataloadoptions/vb/module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="b93cc-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b93cc-107">See Also</span></span>  
 [<span data-ttu-id="b93cc-108">Esecuzione di query sul database</span><span class="sxs-lookup"><span data-stu-id="b93cc-108">Querying the Database</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/querying-the-database.md)
