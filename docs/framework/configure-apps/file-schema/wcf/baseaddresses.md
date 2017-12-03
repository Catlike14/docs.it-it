---
title: '&lt;baseAddresses&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 78918102-2898-46e0-9ea8-6b8afe65603e
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: bfe66b499eb50a058ed8b6a46769893f6dc5fd6e
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="ltbaseaddressesgt"></a><span data-ttu-id="97d95-102">&lt;baseAddresses&gt;</span><span class="sxs-lookup"><span data-stu-id="97d95-102">&lt;baseAddresses&gt;</span></span>
<span data-ttu-id="97d95-103">Rappresenta una raccolta di elementi `baseAddress` costituiti da indirizzi di base per un host del servizio in un ambiente indipendente.</span><span class="sxs-lookup"><span data-stu-id="97d95-103">Represents a collection of `baseAddress` elements, which are base addresses for a service host in a self-hosted environment.</span></span> <span data-ttu-id="97d95-104">Se è presente un indirizzo di base, gli endpoint possono essere configurati con indirizzi relativi all'indirizzo di base.</span><span class="sxs-lookup"><span data-stu-id="97d95-104">If a base address is present, endpoints can be configured with addresses relative to the base address.</span></span>  
  
 <span data-ttu-id="97d95-105">\<System. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="97d95-105">\<system.ServiceModel></span></span>  
<span data-ttu-id="97d95-106">\<client ></span><span class="sxs-lookup"><span data-stu-id="97d95-106">\<client></span></span>  
<span data-ttu-id="97d95-107">\<endpoint ></span><span class="sxs-lookup"><span data-stu-id="97d95-107">\<endpoint></span></span>  
<span data-ttu-id="97d95-108">\<host ></span><span class="sxs-lookup"><span data-stu-id="97d95-108">\<host></span></span>  
<span data-ttu-id="97d95-109">\<baseAddresses ></span><span class="sxs-lookup"><span data-stu-id="97d95-109">\<baseAddresses></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="97d95-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97d95-110">Syntax</span></span>  
  
```xml  
<baseAddresses>  
   <add baseAddress="string" />  
</baseAddresses>  
```  
  
## <a name="type"></a><span data-ttu-id="97d95-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="97d95-111">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="97d95-112">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="97d95-112">Attributes and Elements</span></span>  
 <span data-ttu-id="97d95-113">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="97d95-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="97d95-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="97d95-114">Attributes</span></span>  
 <span data-ttu-id="97d95-115">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="97d95-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="97d95-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="97d95-116">Child Elements</span></span>  
  
|<span data-ttu-id="97d95-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="97d95-117">Element</span></span>|<span data-ttu-id="97d95-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97d95-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="97d95-119">\<add></span><span class="sxs-lookup"><span data-stu-id="97d95-119">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/add-of-baseaddresses.md)|<span data-ttu-id="97d95-120">Elemento di configurazione che specifica gli indirizzi di base usati dall'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="97d95-120">A configuration element that specifies the base addresses used by the service host.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="97d95-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="97d95-121">Parent Elements</span></span>  
  
|<span data-ttu-id="97d95-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="97d95-122">Element</span></span>|<span data-ttu-id="97d95-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97d95-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="97d95-124">\<host ></span><span class="sxs-lookup"><span data-stu-id="97d95-124">\<host></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/host.md)|<span data-ttu-id="97d95-125">Elemento di configurazione che specifica le impostazioni per un host del servizio.</span><span class="sxs-lookup"><span data-stu-id="97d95-125">A configuration element that specifies settings for a service host.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="97d95-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="97d95-126">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.HostElement>  
 <xref:System.ServiceModel.ServiceHost>  
 <xref:System.ServiceModel.ServiceHostBase.BaseAddresses%2A>  
 [<span data-ttu-id="97d95-127">Hosting</span><span class="sxs-lookup"><span data-stu-id="97d95-127">Hosting</span></span>](../../../../../docs/framework/wcf/feature-details/hosting.md)
