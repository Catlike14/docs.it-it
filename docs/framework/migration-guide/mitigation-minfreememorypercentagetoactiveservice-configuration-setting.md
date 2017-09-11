---
title: 'Mitigazione: impostazione della configurazione minFreeMemoryPercentageToActiveService'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a7875f26-0da8-4afe-9846-7a21778f757b
caps.latest.revision: 4
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: f7f228890476d45517a21bc09806538139c5e389
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="mitigation-minfreememorypercentagetoactiveservice-configuration-setting"></a><span data-ttu-id="1aed2-102">Mitigazione: impostazione della configurazione minFreeMemoryPercentageToActiveService</span><span class="sxs-lookup"><span data-stu-id="1aed2-102">Mitigation: minFreeMemoryPercentageToActiveService Configuration Setting</span></span>
<span data-ttu-id="1aed2-103">In [!INCLUDE[net_v451](../../../includes/net-v451-md.md)] viene generata un'eccezione se la memoria disponibile sul server Web è inferiore alla percentuale specificata per l'impostazione di configurazione [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md).</span><span class="sxs-lookup"><span data-stu-id="1aed2-103">In the [!INCLUDE[net_v451](../../../includes/net-v451-md.md)], an exception is thrown if the available memory on the web server is less than the percentage specified by the [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md) configuration setting.</span></span> <span data-ttu-id="1aed2-104">In [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] questa impostazione è stata ignorata.</span><span class="sxs-lookup"><span data-stu-id="1aed2-104">In the [!INCLUDE[net_v45](../../../includes/net-v45-md.md)], this setting was ignored.</span></span>  
  
## <a name="impact"></a><span data-ttu-id="1aed2-105">Impatto</span><span class="sxs-lookup"><span data-stu-id="1aed2-105">Impact</span></span>  
 <span data-ttu-id="1aed2-106">Nella maggior parte dei casi è utile l'impatto dell'osservazione dell'impostazione [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md): migliora la stabilità del sistema impedendo le eccezioni <xref:System.OutOfMemoryException> che possono verificarsi durante l'avvio di un servizio Windows Communication Foundation (WCF) in un sistema con memoria limitata.</span><span class="sxs-lookup"><span data-stu-id="1aed2-106">In most cases, the impact of observing the [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md) setting is desirable: It improves system stability by preventing the <xref:System.OutOfMemoryException> exceptions that can occur when a Windows Communication Foundation (WCF) service is started on a system that has constrained memory.</span></span>  
  
 <span data-ttu-id="1aed2-107">Tuttavia, in alcuni casi, potrebbe non essere possibile l’avvio di un servizio che era stato avviato correttamente in precedenza.</span><span class="sxs-lookup"><span data-stu-id="1aed2-107">However, in some cases, a service that previously started successfully may be unable to start.</span></span> <span data-ttu-id="1aed2-108">In tal caso, viene visualizzato un messaggio di errore dettagliato:</span><span class="sxs-lookup"><span data-stu-id="1aed2-108">In that case, a detailed error message appears:</span></span>  
  
```console
Memory gates checking failed because the free memory (nnnn bytes) is less than nn% of total memory. As a result, the service will not be available for incoming requests. To resolve this, either reduce the load on the machine or adjust the value of minFreeMemoryPercentageToActivateService on the serviceHostingEnvironment config element.
```
  
## <a name="mitigation"></a><span data-ttu-id="1aed2-109">Attenuazione</span><span class="sxs-lookup"><span data-stu-id="1aed2-109">Mitigation</span></span>  
 <span data-ttu-id="1aed2-110">Per ripristinare il comportamento precedente dove è stata ignorata l'impostazione [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md), modificare il file web.config come segue:</span><span class="sxs-lookup"><span data-stu-id="1aed2-110">To revert to the previous behavior where the [minFreeMemoryPercentageToActivateService](../../../docs/framework/configure-apps/file-schema/wcf/servicehostingenvironment.md) setting was ignored, modify the web.config file as follows:</span></span>  
  
```xml
<serviceHostingEnvironment multipleSiteBindingsEnabled="true"   
                           minFreeMemoryPercentageToActivateService="0">  
   <serviceActivations>  
   ...  
   </serviceActivations>  
</serviceHostingEnvironment>  
```  
  
## <a name="see-also"></a><span data-ttu-id="1aed2-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1aed2-111">See Also</span></span>  
 [<span data-ttu-id="1aed2-112">Modifiche al runtime</span><span class="sxs-lookup"><span data-stu-id="1aed2-112">Runtime Changes</span></span>](../../../docs/framework/migration-guide/runtime-changes-in-the-net-framework-4-5-1.md)

