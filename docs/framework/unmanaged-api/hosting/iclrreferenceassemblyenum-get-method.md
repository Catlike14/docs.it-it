---
title: Metodo ICLRReferenceAssemblyEnum::Get
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
- ICLRReferenceAssemblyEnum.Get
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRReferenceAssemblyEnum::Get
helpviewer_keywords:
- ICLRReferenceAssemblyEnum::Get method [.NET Framework hosting]
- Get method, ICLRReferenceAssemblyEnum interface [.NET Framework hosting]
ms.assetid: f21c1612-9c5d-4abc-a337-577086d29c17
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e3cdf6a8eb761367d23e1ce61cd24727e7a3d6ee
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iclrreferenceassemblyenumget-method"></a><span data-ttu-id="f5503-102">Metodo ICLRReferenceAssemblyEnum::Get</span><span class="sxs-lookup"><span data-stu-id="f5503-102">ICLRReferenceAssemblyEnum::Get Method</span></span>
<span data-ttu-id="f5503-103">Ottiene l'identità dell'assembly in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f5503-103">Gets the assembly identity at the supplied index.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5503-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5503-104">Syntax</span></span>  
  
```  
HRESULT Get (  
    [in] DWORD dwIndex,  
    [out, size_is(*pcchBufferSize)] LPWSTR pwzBuffer,  
    [in, out] DWORD *pcchBufferSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f5503-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5503-105">Parameters</span></span>  
 `dwIndex`  
 <span data-ttu-id="f5503-106">[in] Indice in base zero dell'identità dell'assembly da restituire.</span><span class="sxs-lookup"><span data-stu-id="f5503-106">[in] The zero-based index of the assembly identity to return.</span></span>  
  
 `pwzBuffer`  
 <span data-ttu-id="f5503-107">[out] Un buffer contenente i dati di identità di assembly.</span><span class="sxs-lookup"><span data-stu-id="f5503-107">[out] A buffer containing the assembly identity data.</span></span>  
  
 `pcchBufferSize`  
 <span data-ttu-id="f5503-108">[in, out] Le dimensioni del `pwzBuffer` buffer.</span><span class="sxs-lookup"><span data-stu-id="f5503-108">[in, out] The size of the `pwzBuffer` buffer.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="f5503-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5503-109">Return Value</span></span>  
  
|<span data-ttu-id="f5503-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="f5503-110">HRESULT</span></span>|<span data-ttu-id="f5503-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5503-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="f5503-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5503-112">S_OK</span></span>|<span data-ttu-id="f5503-113">`Get`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="f5503-113">`Get` returned successfully.</span></span>|  
|<span data-ttu-id="f5503-114">ERROR_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="f5503-114">ERROR_INSUFFICIENT_BUFFER</span></span>|<span data-ttu-id="f5503-115">`pwzBuffer`è troppo piccolo.</span><span class="sxs-lookup"><span data-stu-id="f5503-115">`pwzBuffer` is too small.</span></span>|  
|<span data-ttu-id="f5503-116">ERROR_NO_MORE_ITEMS</span><span class="sxs-lookup"><span data-stu-id="f5503-116">ERROR_NO_MORE_ITEMS</span></span>|<span data-ttu-id="f5503-117">L'enumerazione non contiene più elementi.</span><span class="sxs-lookup"><span data-stu-id="f5503-117">The enumeration contains no more items.</span></span>|  
|<span data-ttu-id="f5503-118">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f5503-118">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="f5503-119">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="f5503-119">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="f5503-120">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="f5503-120">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="f5503-121">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="f5503-121">The call timed out.</span></span>|  
|<span data-ttu-id="f5503-122">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="f5503-122">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="f5503-123">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="f5503-123">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="f5503-124">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="f5503-124">HOST_E_ABANDONED</span></span>|<span data-ttu-id="f5503-125">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="f5503-125">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="f5503-126">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f5503-126">E_FAIL</span></span>|<span data-ttu-id="f5503-127">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f5503-127">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="f5503-128">Se un metodo restituisce E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="f5503-128">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="f5503-129">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="f5503-129">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="f5503-130">Note</span><span class="sxs-lookup"><span data-stu-id="f5503-130">Remarks</span></span>  
 <span data-ttu-id="f5503-131">`Get`viene in genere chiamato due volte.</span><span class="sxs-lookup"><span data-stu-id="f5503-131">`Get` is typically called twice.</span></span> <span data-ttu-id="f5503-132">La prima chiamata fornisce un valore null per `pwzBuffer`e imposta `pcchBufferSize` per le dimensioni appropriate per `pwzBuffer`.</span><span class="sxs-lookup"><span data-stu-id="f5503-132">The first call supplies a null value for `pwzBuffer`, and sets `pcchBufferSize` to the size appropriate for `pwzBuffer`.</span></span> <span data-ttu-id="f5503-133">La seconda chiamata viene fornito un dimensionati `pwzBuffer`e contiene i dati di identità assembly canonica dopo il completamento.</span><span class="sxs-lookup"><span data-stu-id="f5503-133">The second call supplies an appropriately sized `pwzBuffer`, and contains the canonical assembly identity data upon completion.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f5503-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5503-134">Requirements</span></span>  
 <span data-ttu-id="f5503-135">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f5503-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f5503-136">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="f5503-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f5503-137">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f5503-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f5503-138">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f5503-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5503-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f5503-139">See Also</span></span>  
 [<span data-ttu-id="f5503-140">Interfaccia ICLRAssemblyReferenceList</span><span class="sxs-lookup"><span data-stu-id="f5503-140">ICLRAssemblyReferenceList Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyreferencelist-interface.md)  
 [<span data-ttu-id="f5503-141">Interfaccia ICLRReferenceAssemblyEnum</span><span class="sxs-lookup"><span data-stu-id="f5503-141">ICLRReferenceAssemblyEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrreferenceassemblyenum-interface.md)
