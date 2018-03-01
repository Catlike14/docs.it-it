---
title: Metodo IGCThreadControl::ThreadIsBlockingForSuspension
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
- IGCThreadControl.ThreadIsBlockingForSuspension
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ThreadIsBlockingForSuspension
helpviewer_keywords:
- IGCThreadControl::ThreadIsBlockingForSuspension method [.NET Framework hosting]
- ThreadIsBlockingForSuspension method [.NET Framework hosting]
ms.assetid: ed5b5b58-7db7-46b5-9e2c-278db7159cee
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 0cb7cfbab18334f1892c24225311160179920f81
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="igcthreadcontrolthreadisblockingforsuspension-method"></a><span data-ttu-id="9f3e8-102">Metodo IGCThreadControl::ThreadIsBlockingForSuspension</span><span class="sxs-lookup"><span data-stu-id="9f3e8-102">IGCThreadControl::ThreadIsBlockingForSuspension Method</span></span>
<span data-ttu-id="9f3e8-103">Notifica all'host che il thread che effettua la chiamata sta per bloccare, ad esempio per un'operazione di garbage collection o un'altra sospensione.</span><span class="sxs-lookup"><span data-stu-id="9f3e8-103">Notifies the host that the thread that is making the call is about to block, perhaps for a garbage collection or other suspension.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f3e8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f3e8-104">Syntax</span></span>  
  
```  
HRESULT ThreadIsBlockingForSuspension ( );  
```  
  
## <a name="remarks"></a><span data-ttu-id="9f3e8-105">Note</span><span class="sxs-lookup"><span data-stu-id="9f3e8-105">Remarks</span></span>  
 <span data-ttu-id="9f3e8-106">L'host può scegliere all'interno di `ThreadIsBlockingForSuspension` callback se ripianificare un thread.</span><span class="sxs-lookup"><span data-stu-id="9f3e8-106">The host may choose within the `ThreadIsBlockingForSuspension` callback whether to reschedule a thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f3e8-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f3e8-107">Requirements</span></span>  
 <span data-ttu-id="9f3e8-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f3e8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f3e8-109">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="9f3e8-109">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9f3e8-110">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f3e8-110">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9f3e8-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f3e8-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f3e8-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9f3e8-112">See Also</span></span>  
 [<span data-ttu-id="9f3e8-113">Interfaccia IGCThreadControl</span><span class="sxs-lookup"><span data-stu-id="9f3e8-113">IGCThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igcthreadcontrol-interface.md)
