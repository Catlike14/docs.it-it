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
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 23182f18f28cfb843c1c3a70996590a92d9cdea8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="instances"></a><span data-ttu-id="2aaa5-102">Istanze</span><span class="sxs-lookup"><span data-stu-id="2aaa5-102">Instances</span></span>
<span data-ttu-id="2aaa5-103">Nome contatore: istanze.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-103">Counter Name: Instances.</span></span>  
  
## <a name="description"></a><span data-ttu-id="2aaa5-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2aaa5-104">Description</span></span>  
 <span data-ttu-id="2aaa5-105">Numero di contesti di istanza attualmente contenuti dal servizio.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-105">Number of instance contexts that the service currently contains.</span></span>  
  
 <span data-ttu-id="2aaa5-106">In genere, il numero di contesti di istanza è identico al numero di istanze.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-106">Most of the time, the number of instance contexts is identical to the number of instances.</span></span> <span data-ttu-id="2aaa5-107">Tuttavia, gli scenari seguenti rappresenta un'eccezione a questa regola.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-107">However, the following scenarios are exception to this rule.</span></span>  
  
-   <span data-ttu-id="2aaa5-108">Un metodo di servizio chiama il metodo <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-108">A service method calls the <xref:System.ServiceModel.Dispatcher.IInstanceProvider.ReleaseInstance%2A> method explicitly.</span></span>  
  
-   <span data-ttu-id="2aaa5-109">Viene applicata un'enumerazione <xref:System.ServiceModel.ReleaseInstanceMode> a un'istanza di <xref:System.ServiceModel.OperationBehaviorAttribute>.</span><span class="sxs-lookup"><span data-stu-id="2aaa5-109">A <xref:System.ServiceModel.ReleaseInstanceMode> is applied to an <xref:System.ServiceModel.OperationBehaviorAttribute> instance.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2aaa5-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2aaa5-110">See Also</span></span>  
 <xref:System.ServiceModel.OperationBehaviorAttribute>
