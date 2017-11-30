---
title: '&lt;serviceTimeouts&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ada536cf-97dc-4cd7-89ec-ed1466c1c557
caps.latest.revision: "11"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: ecefda0a3447aa029079fbb3633b05054f42195a
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="ltservicetimeoutsgt"></a><span data-ttu-id="489bc-102">&lt;serviceTimeouts&gt;</span><span class="sxs-lookup"><span data-stu-id="489bc-102">&lt;serviceTimeouts&gt;</span></span>
<span data-ttu-id="489bc-103">Specifica il timeout per un servizio.</span><span class="sxs-lookup"><span data-stu-id="489bc-103">Specifies the timeout for a service.</span></span>  
  
 <span data-ttu-id="489bc-104">\<System. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="489bc-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="489bc-105">\<i comportamenti ></span><span class="sxs-lookup"><span data-stu-id="489bc-105">\<behaviors></span></span>  
<span data-ttu-id="489bc-106">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="489bc-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="489bc-107">\<comportamento ></span><span class="sxs-lookup"><span data-stu-id="489bc-107">\<behavior></span></span>  
<span data-ttu-id="489bc-108">\<serviceTimeouts ></span><span class="sxs-lookup"><span data-stu-id="489bc-108">\<serviceTimeouts></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="489bc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="489bc-109">Syntax</span></span>  
  
```xml  
<serviceTimeouts transactionTimeout="TimeSpan" />  
```  
  
## <a name="type"></a><span data-ttu-id="489bc-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="489bc-110">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="489bc-111">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="489bc-111">Attributes and Elements</span></span>  
 <span data-ttu-id="489bc-112">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="489bc-112">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="489bc-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="489bc-113">Attributes</span></span>  
  
|<span data-ttu-id="489bc-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="489bc-114">Attribute</span></span>|<span data-ttu-id="489bc-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489bc-115">Description</span></span>|  
|---------------|-----------------|  
|`transactionTimeout`|<span data-ttu-id="489bc-116">Valore <xref:System.TimeSpan> che specifica l'intervallo di tempo entro il quale una transazione deve essere propagata dal client al server.</span><span class="sxs-lookup"><span data-stu-id="489bc-116">A <xref:System.TimeSpan> value that specifies the interval of time a transaction must flow from client to server.</span></span> <span data-ttu-id="489bc-117">Il valore predefinito è "00: 00:00".</span><span class="sxs-lookup"><span data-stu-id="489bc-117">The default is "00:00:00".</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="489bc-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="489bc-118">Child Elements</span></span>  
 <span data-ttu-id="489bc-119">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="489bc-119">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="489bc-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="489bc-120">Parent Elements</span></span>  
  
|<span data-ttu-id="489bc-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="489bc-121">Element</span></span>|<span data-ttu-id="489bc-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="489bc-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="489bc-123">\<comportamento ></span><span class="sxs-lookup"><span data-stu-id="489bc-123">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="489bc-124">Specifica un elemento di comportamento.</span><span class="sxs-lookup"><span data-stu-id="489bc-124">Specifies a behavior element.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="489bc-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="489bc-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ServiceTimeoutsElement>
