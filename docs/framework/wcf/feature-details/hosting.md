---
title: Hosting2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0820c7e5-0b50-4cde-80e7-74e346513002
caps.latest.revision: "20"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 8b0e8aa1dfe2e7a737e88530a206739eef39b2cb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="hosting"></a><span data-ttu-id="9feb5-102">Hosting</span><span class="sxs-lookup"><span data-stu-id="9feb5-102">Hosting</span></span>
<span data-ttu-id="9feb5-103">Negli argomenti di questa sezione viene descritto l'hosting dei servizi.</span><span class="sxs-lookup"><span data-stu-id="9feb5-103">The topics in the section describe service hosting.</span></span> <span data-ttu-id="9feb5-104">Un servizio può essere ospitato da Internet Information Services (IIS), servizio Attivazione processo Windows (WAS), Windows Server AppFabric, un servizio Windows o da un'applicazione gestita, questa opzione è noto anche come *self-hosting*.</span><span class="sxs-lookup"><span data-stu-id="9feb5-104">A service can be hosted by Internet Information Services (IIS), Windows Process Activation Service (WAS), Windows Server AppFabric, a Windows service, or by a managed application—this option is often referred to as *self hosting*.</span></span>  
  
 <span data-ttu-id="9feb5-105">È importante notare che l'esecuzione di un servizio o di una qualsiasi estensione da un host non attendibile compromette la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="9feb5-105">It is important to note that running a service or any extension from an untrusted host compromises security.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="9feb5-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9feb5-106">In This Section</span></span>  
 [<span data-ttu-id="9feb5-107">Hosting in Internet Information Services</span><span class="sxs-lookup"><span data-stu-id="9feb5-107">Hosting in Internet Information Services</span></span>](../../../../docs/framework/wcf/feature-details/hosting-in-internet-information-services.md)  
 <span data-ttu-id="9feb5-108">Viene descritto come un [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] servizio è ospitato in Internet Information Services o [Windows Server AppFabric](http://go.microsoft.com/fwlink/?LinkId=196496).</span><span class="sxs-lookup"><span data-stu-id="9feb5-108">Describes how a [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] service is hosted in Internet Information Services or [Windows Server AppFabric](http://go.microsoft.com/fwlink/?LinkId=196496).</span></span>  
  
 [<span data-ttu-id="9feb5-109">Hosting nel servizio di attivazione dei processi di Windows</span><span class="sxs-lookup"><span data-stu-id="9feb5-109">Hosting in Windows Process Activation Service</span></span>](../../../../docs/framework/wcf/feature-details/hosting-in-windows-process-activation-service.md)  
 <span data-ttu-id="9feb5-110">Descrive il modo in cui un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è ospitato nel servizio Attivazione processo Windows.</span><span class="sxs-lookup"><span data-stu-id="9feb5-110">Describes how a [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] service is hosted by Windows Process Activation Service.</span></span>  
  
 [<span data-ttu-id="9feb5-111">Hosting in un'applicazione di servizio Windows</span><span class="sxs-lookup"><span data-stu-id="9feb5-111">Hosting in a Windows Service Application</span></span>](../../../../docs/framework/wcf/feature-details/hosting-in-a-windows-service-application.md)  
 <span data-ttu-id="9feb5-112">Descrive come un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] viene ospitato da un servizio di Windows.</span><span class="sxs-lookup"><span data-stu-id="9feb5-112">Describes how a [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] service is hosted by a Windows service.</span></span>  
  
 [<span data-ttu-id="9feb5-113">Hosting in un'applicazione gestita</span><span class="sxs-lookup"><span data-stu-id="9feb5-113">Hosting in a Managed Application</span></span>](../../../../docs/framework/wcf/feature-details/hosting-in-a-managed-application.md)  
 <span data-ttu-id="9feb5-114">Descrive il modo in cui un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] viene ospitato in un'applicazione gestita.</span><span class="sxs-lookup"><span data-stu-id="9feb5-114">Describes how a [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] service is hosted in a managed application.</span></span>  
  
 [<span data-ttu-id="9feb5-115">Attivazione basata sulla configurazione in IIS e WAS</span><span class="sxs-lookup"><span data-stu-id="9feb5-115">Configuration-Based Activation in IIS and WAS</span></span>](../../../../docs/framework/wcf/feature-details/configuration-based-activation-in-iis-and-was.md)  
 <span data-ttu-id="9feb5-116">Descrive il modo in cui un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] viene ospitato in IIS o WAS senza utilizzare un file con estensione svc.</span><span class="sxs-lookup"><span data-stu-id="9feb5-116">Describes how a [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] service is hosted under IIS or WAS without using a .svc file.</span></span>  
  
 [<span data-ttu-id="9feb5-117">Supporto di più associazioni del sito IIS</span><span class="sxs-lookup"><span data-stu-id="9feb5-117">Supporting Multiple IIS Site Bindings</span></span>](../../../../docs/framework/wcf/feature-details/supporting-multiple-iis-site-bindings.md)  
 <span data-ttu-id="9feb5-118">Descrive il modo in cui specificare più indirizzi di base per un servizio utilizzando lo stesso schema URI su un solo sito Web.</span><span class="sxs-lookup"><span data-stu-id="9feb5-118">Describes how to specify multiple base addresses for a service using the same URI scheme on a single Web site.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9feb5-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9feb5-119">See Also</span></span>  
 [<span data-ttu-id="9feb5-120">Servizi di hosting</span><span class="sxs-lookup"><span data-stu-id="9feb5-120">Hosting Services</span></span>](../../../../docs/framework/wcf/hosting-services.md)  
 [<span data-ttu-id="9feb5-121">Windows Server AppFabric con funzionalità di Hosting</span><span class="sxs-lookup"><span data-stu-id="9feb5-121">Windows Server App Fabric Hosting Features</span></span>](http://go.microsoft.com/fwlink/?LinkId=201276)
