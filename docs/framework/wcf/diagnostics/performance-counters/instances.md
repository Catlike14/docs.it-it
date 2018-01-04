---
title: Istanze
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c8cf3460-0ca1-4411-8262-e9ecaf7f0a31
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 7ed0c4a6f13ddcafdb3a9a773be9cd3f017474ec
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="instances"></a><span data-ttu-id="f83c3-102">Istanze</span><span class="sxs-lookup"><span data-stu-id="f83c3-102">Instances</span></span>
<span data-ttu-id="f83c3-103">Nome contatore: istanze.</span><span class="sxs-lookup"><span data-stu-id="f83c3-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="f83c3-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f83c3-104">Description</span></span>  
 <span data-ttu-id="f83c3-105">Numero di contesti di istanza attualmente contenuti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="f83c3-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="f83c3-106">In genere, il numero di contesti di istanza è identico al numero di istanze.</span><span class="sxs-lookup"><span data-stu-id="f83c3-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="f83c3-107">Tuttavia, gli scenari seguenti rappresenta un'eccezione a questa regola.</span><span class="sxs-lookup"><span data-stu-id="f83c3-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="f83c3-108">Un metodo di servizio chiama il metodo <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="f83c3-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="f83c3-109">Viene applicata un'enumerazione <xref:System.ServiceModel.ReleaseInstanceMode> a un'istanza di <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="f83c3-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f83c3-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f83c3-110">See Also</span></span>  
 <xref:System.ServiceModel.OperationBehaviorAttribute>
