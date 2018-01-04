---
title: Metodo IGCHost2::SetGCStartupLimitsEx
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IGCHost2.SetGCStartupLimitsEx
api_location: mscoree.dll
api_type: COM
f1_keywords: IGCHost2::SetGCStartupLimitsEx
helpviewer_keywords:
- IGCHost2::SetGCStartupLimitsEx method [.NET Framework hosting]
- SetGCStartupLimitsEx method, IGCHost2 interface [.NET Framework hosting]
ms.assetid: bba941c2-1c57-46d3-bbf5-5fb92700c490
topic_type: apiref
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: f8ed2b2aa43fcf925b6202ab339209904e7c53af
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="igchost2setgcstartuplimitsex-method"></a><span data-ttu-id="155aa-102">Metodo IGCHost2::SetGCStartupLimitsEx</span><span class="sxs-lookup"><span data-stu-id="155aa-102">IGCHost2::SetGCStartupLimitsEx Method</span></span>
<span data-ttu-id="155aa-103">Imposta le dimensioni del segmento e la dimensione massima per la generazione 0.</span><span class="sxs-lookup"><span data-stu-id="155aa-103">Sets the segment size and the maximum size for generation 0.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="155aa-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="155aa-104">Syntax</span></span>  
  
```  
HRESULT SetGCStartupLimitsEx (  
    [in] SIZE_T SegmentSize,  
    [in] SIZE_T MaxGen0Size  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="155aa-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="155aa-105">Parameters</span></span>  
 `SegmentSize`  
 <span data-ttu-id="155aa-106">[in] Dimensione del segmento utilizzata dal sistema di garbage collection.</span><span class="sxs-lookup"><span data-stu-id="155aa-106">[in] The size of the segment used by the garbage collection system.</span></span>  
  
 `MaxGen0Size`  
 <span data-ttu-id="155aa-107">[in] La dimensione massima per la generazione 0.</span><span class="sxs-lookup"><span data-stu-id="155aa-107">[in] The maximum size for generation 0.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="155aa-108">Note</span><span class="sxs-lookup"><span data-stu-id="155aa-108">Remarks</span></span>  
 <span data-ttu-id="155aa-109">I valori che `SetGCStartupLimitsEx` set possono essere specificati solo prima che l'host viene avviata.</span><span class="sxs-lookup"><span data-stu-id="155aa-109">The values that `SetGCStartupLimitsEx` sets can be specified only before the host is started.</span></span> <span data-ttu-id="155aa-110">Questi valori non possono essere modificati successivamente.</span><span class="sxs-lookup"><span data-stu-id="155aa-110">These values cannot be changed later.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="155aa-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="155aa-111">Requirements</span></span>  
 <span data-ttu-id="155aa-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="155aa-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="155aa-113">**Intestazione:** GCHost. idl, GCHost. H</span><span class="sxs-lookup"><span data-stu-id="155aa-113">**Header:** GCHost.idl, GCHost.h</span></span>  
  
 <span data-ttu-id="155aa-114">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="155aa-114">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="155aa-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="155aa-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="155aa-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="155aa-116">See Also</span></span>  
 [<span data-ttu-id="155aa-117">Interfaccia IGCHost2</span><span class="sxs-lookup"><span data-stu-id="155aa-117">IGCHost2 Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchost2-interface.md)
