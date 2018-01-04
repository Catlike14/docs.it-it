---
title: Metodo IHostMemoryManager::NeedsVirtualAddressSpace
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostMemoryManager.NeedsVirtualAddressSpace
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostMemoryManager::NeedsVirtualAddressSpace
helpviewer_keywords:
- IHostMemoryManager::NeedsVirtualAddressSpace method [.NET Framework hosting]
- NeedsVirtualAddressSpace method [.NET Framework hosting]
ms.assetid: 71f0eab5-0170-46f8-9f88-1df5abdeb34a
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 9251cbadaf182cda8d52f3f5792452310561c376
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="ihostmemorymanagerneedsvirtualaddressspace-method"></a><span data-ttu-id="169c5-102">Metodo IHostMemoryManager::NeedsVirtualAddressSpace</span><span class="sxs-lookup"><span data-stu-id="169c5-102">IHostMemoryManager::NeedsVirtualAddressSpace Method</span></span>
<span data-ttu-id="169c5-103">Notifica all'host che common language runtime (CLR) tenterà di utilizzare la memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="169c5-103">Notifies the host that the common language runtime (CLR) is going to attempt to use the specified memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="169c5-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="169c5-104">Syntax</span></span>  
  
```  
HRESULT NeedsVirtualAddressSpace (  
    [in] LPVOID  startAddress,  
    [in] SIZE_T  size  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="169c5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="169c5-105">Parameters</span></span>  
 `startAddress`  
 <span data-ttu-id="169c5-106">[in] L'indirizzo iniziale della memoria.</span><span class="sxs-lookup"><span data-stu-id="169c5-106">[in] The starting address of the memory.</span></span>  
  
 `size`  
 <span data-ttu-id="169c5-107">[in] Le dimensioni in byte, della memoria.</span><span class="sxs-lookup"><span data-stu-id="169c5-107">[in] The size, in bytes, of the memory.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="169c5-108">Note</span><span class="sxs-lookup"><span data-stu-id="169c5-108">Remarks</span></span>  
 <span data-ttu-id="169c5-109">Il `NeedsVirtualAddressSpace` metodo è un metodo di callback e deve essere implementato dal writer dell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="169c5-109">The `NeedsVirtualAddressSpace` method is a callback method and must be implemented by the writer of the hosting application.</span></span> <span data-ttu-id="169c5-110">Viene chiamato da CLR.</span><span class="sxs-lookup"><span data-stu-id="169c5-110">It is called by the CLR.</span></span>  
  
 <span data-ttu-id="169c5-111">Se l'host non desidera che il Common Language Runtime utilizza la memoria specificata, può restituire un valore HRESULT E_OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="169c5-111">If the host does not want the CLR to use the specified memory, it may return an E_OUTOFMEMORY HRESULT.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="169c5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="169c5-112">Requirements</span></span>  
 <span data-ttu-id="169c5-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="169c5-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="169c5-114">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="169c5-114">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="169c5-115">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="169c5-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="169c5-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="169c5-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="169c5-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="169c5-117">See Also</span></span>  
 [<span data-ttu-id="169c5-118">Interfaccia IHostMemoryManager</span><span class="sxs-lookup"><span data-stu-id="169c5-118">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)
