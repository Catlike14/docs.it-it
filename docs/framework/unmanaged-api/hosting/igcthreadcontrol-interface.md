---
title: Interfaccia IGCThreadControl
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- IGCThreadControl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IGCThreadControl
helpviewer_keywords:
- IGCThreadControl interface [.NET Framework hosting]
ms.assetid: 3ff04d75-85ac-4df9-886d-dbaa037c0552
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: def6ae3c8bf8eea9cb135529e2b6e672b180e68c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="igcthreadcontrol-interface"></a><span data-ttu-id="46729-102">Interfaccia IGCThreadControl</span><span class="sxs-lookup"><span data-stu-id="46729-102">IGCThreadControl Interface</span></span>
<span data-ttu-id="46729-103">Fornisce metodi per partecipare alla pianificazione di thread che altrimenti sarebbero bloccati per una garbage collection.</span><span class="sxs-lookup"><span data-stu-id="46729-103">Provides methods for participating in the scheduling of threads that would otherwise be blocked for a garbage collection.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="46729-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="46729-104">Methods</span></span>  
  
|<span data-ttu-id="46729-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="46729-105">Method</span></span>|<span data-ttu-id="46729-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46729-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="46729-107">Metodo SuspensionEnding</span><span class="sxs-lookup"><span data-stu-id="46729-107">SuspensionEnding Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionending-method.md)|<span data-ttu-id="46729-108">Notifica all'host che il runtime viene ripresa dei thread dopo un'operazione di garbage collection o un'altra sospensione.</span><span class="sxs-lookup"><span data-stu-id="46729-108">Notifies the host that the runtime is resuming threads after a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="46729-109">Metodo SuspensionStarting</span><span class="sxs-lookup"><span data-stu-id="46729-109">SuspensionStarting Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-suspensionstarting-method.md)|<span data-ttu-id="46729-110">Notifica all'host che il runtime sta avviando una sospensione di thread per una garbage collection o un'altra sospensione.</span><span class="sxs-lookup"><span data-stu-id="46729-110">Notifies the host that the runtime is beginning a thread suspension for a garbage collection or other suspension.</span></span>|  
|[<span data-ttu-id="46729-111">Metodo ThreadIsBlockingForSuspension</span><span class="sxs-lookup"><span data-stu-id="46729-111">ThreadIsBlockingForSuspension Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-threadisblockingforsuspension-method.md)|<span data-ttu-id="46729-112">Notifica all'host che il thread chiamante sta per bloccare, ad esempio per un'operazione di garbage collection o un'altra sospensione.</span><span class="sxs-lookup"><span data-stu-id="46729-112">Notifies the host that the thread making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="46729-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46729-113">Requirements</span></span>  
 <span data-ttu-id="46729-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="46729-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="46729-115">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="46729-115">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="46729-116">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="46729-116">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="46729-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="46729-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46729-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="46729-118">See Also</span></span>  
 [<span data-ttu-id="46729-119">Interfacce di hosting</span><span class="sxs-lookup"><span data-stu-id="46729-119">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)
