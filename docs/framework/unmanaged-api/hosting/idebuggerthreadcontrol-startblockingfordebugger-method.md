---
title: Metodo IDebuggerThreadControl::StartBlockingForDebugger
ms.date: 03/30/2017
api_name:
- IDebuggerThreadControl.StartBlockingForDebugger
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- StartBlockingForDebugger
helpviewer_keywords:
- IDebuggerThreadControl::StartBlockingForDebugger method [.NET Framework hosting]
- StartBlockingForDebugger method [.NET Framework hosting]
ms.assetid: 5c8f11b4-35d3-4c39-9bbd-58b896ba5ba6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 48aa7452373f83465b3e5ec8a09a9a00c902a22c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437934"
---
# <a name="idebuggerthreadcontrolstartblockingfordebugger-method"></a><span data-ttu-id="12eaa-102">Metodo IDebuggerThreadControl::StartBlockingForDebugger</span><span class="sxs-lookup"><span data-stu-id="12eaa-102">IDebuggerThreadControl::StartBlockingForDebugger Method</span></span>
<span data-ttu-id="12eaa-103">Notifica all'host che i servizi di debug stanno per avviare il blocco di tutti i thread.</span><span class="sxs-lookup"><span data-stu-id="12eaa-103">Notifies the host that the debugging services are about to start blocking all threads.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="12eaa-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12eaa-104">Syntax</span></span>  
  
```  
HRESULT StartBlockingForDebugger (  
    [in] DWORD dwUnused  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="12eaa-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="12eaa-105">Parameters</span></span>  
 `dwUnused`  
 <span data-ttu-id="12eaa-106">[in] Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="12eaa-106">[in] Reserved for future use.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="12eaa-107">Note</span><span class="sxs-lookup"><span data-stu-id="12eaa-107">Remarks</span></span>  
 <span data-ttu-id="12eaa-108">Il `StartBlockingForDebugger` metodo potrebbe essere chiamato su un thread di runtime.</span><span class="sxs-lookup"><span data-stu-id="12eaa-108">The `StartBlockingForDebugger` method could be called on a runtime thread.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="12eaa-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12eaa-109">Requirements</span></span>  
 <span data-ttu-id="12eaa-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="12eaa-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="12eaa-111">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="12eaa-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="12eaa-112">**Libreria:** inclusa come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="12eaa-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="12eaa-113">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="12eaa-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12eaa-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="12eaa-114">See Also</span></span>  
 [<span data-ttu-id="12eaa-115">Interfaccia IDebuggerThreadControl</span><span class="sxs-lookup"><span data-stu-id="12eaa-115">IDebuggerThreadControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/idebuggerthreadcontrol-interface.md)
