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
ms.openlocfilehash: 87423c3de551cb9fbf8c5a7756e2f0f999129a3b
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="instances"></a><span data-ttu-id="712b3-102">Istanze</span><span class="sxs-lookup"><span data-stu-id="712b3-102">Instances</span></span>
<span data-ttu-id="712b3-103">Nome contatore: istanze.</span><span class="sxs-lookup"><span data-stu-id="712b3-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="712b3-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="712b3-104">Description</span></span>  
 <span data-ttu-id="712b3-105">Numero di contesti di istanza attualmente contenuti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="712b3-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="712b3-106">In genere, il numero di contesti di istanza è identico al numero di istanze.</span><span class="sxs-lookup"><span data-stu-id="712b3-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="712b3-107">Tuttavia, gli scenari seguenti rappresenta un'eccezione a questa regola.</span><span class="sxs-lookup"><span data-stu-id="712b3-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="712b3-108">Un metodo di servizio chiama il metodo <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="712b3-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="712b3-109">Viene applicata un'enumerazione <xref:System.ServiceModel.ReleaseInstanceMode> a un'istanza di <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="712b3-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="712b3-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="712b3-110">See Also</span></span>  
 <xref:System.ServiceModel.OperationBehaviorAttribute>
