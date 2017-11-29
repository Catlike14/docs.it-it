---
title: Metodo ICLRErrorReportingManager::BeginCustomDump
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRErrorReportingManager.BeginCustomDump
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRErrorReportingManager::BeginCustomDump
helpviewer_keywords:
- ICLRErrorReportingManager::BeginCustomDump method [.NET Framework hosting]
- BeginCustomDump method
ms.assetid: 93424a87-ba13-4fa1-b4dc-69d44437b7ae
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c90357f969b19c767d4bb45d4d3105f50cd5682a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="iclrerrorreportingmanagerbegincustomdump-method"></a><span data-ttu-id="95c3a-102">Metodo ICLRErrorReportingManager::BeginCustomDump</span><span class="sxs-lookup"><span data-stu-id="95c3a-102">ICLRErrorReportingManager::BeginCustomDump Method</span></span>
<span data-ttu-id="95c3a-103">Specifica la configurazione di dump dell'heap personalizzati per la segnalazione errori.</span><span class="sxs-lookup"><span data-stu-id="95c3a-103">Specifies the configuration of custom heap dumps for error reporting.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="95c3a-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95c3a-104">Syntax</span></span>  
  
```  
HRESULT BeginCustomDump (  
    [in] ECustomDumpFlavor dwFlavor,  
    [in] DWORD dwNumItems,  
    [in, size_is(dwNumItems), length_is(dwNumItems)] CustomDumpItem items[],  
    DWORD dwReserved  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="95c3a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="95c3a-105">Parameters</span></span>  
 `dwFlavor`  
 <span data-ttu-id="95c3a-106">[in] Oggetto [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) valore che indica il tipo di dump dell'heap in base al quale compilare il dump dell'heap personalizzati.</span><span class="sxs-lookup"><span data-stu-id="95c3a-106">[in] A [ECustomDumpFlavor](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md) value that indicates the kind of heap dump upon which to build the custom heap dump.</span></span>  
  
 `dwNumItems`  
 <span data-ttu-id="95c3a-107">[in] La lunghezza del `items` matrice.</span><span class="sxs-lookup"><span data-stu-id="95c3a-107">[in] The length of the `items` array.</span></span> <span data-ttu-id="95c3a-108">Se `dwFlavor` non è DUMP_FLAVOR_Mini, `dwNumItems` deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="95c3a-108">If `dwFlavor` is not DUMP_FLAVOR_Mini, `dwNumItems` should be zero.</span></span>  
  
 `items`  
 <span data-ttu-id="95c3a-109">[in] Matrice di [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) istanze, che specifica gli elementi da aggiungere al minidump.</span><span class="sxs-lookup"><span data-stu-id="95c3a-109">[in] An array of [CustomDumpItem](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md) instances, specifying the items to add to the mini-dump.</span></span> <span data-ttu-id="95c3a-110">Se `dwFlavor` non è DUMP_FLAVOR_Mini, `items` deve essere null.</span><span class="sxs-lookup"><span data-stu-id="95c3a-110">If `dwFlavor` is not DUMP_FLAVOR_Mini, `items` should be null.</span></span>  
  
 `dwReserved`  
 <span data-ttu-id="95c3a-111">[in] Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="95c3a-111">[in] Reserved for future use.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="95c3a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95c3a-112">Return Value</span></span>  
  
|<span data-ttu-id="95c3a-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="95c3a-113">HRESULT</span></span>|<span data-ttu-id="95c3a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95c3a-114">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="95c3a-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="95c3a-115">S_OK</span></span>|<span data-ttu-id="95c3a-116">Il metodo è stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="95c3a-116">The method returned successfully.</span></span>|  
|<span data-ttu-id="95c3a-117">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="95c3a-117">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="95c3a-118">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="95c3a-118">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="95c3a-119">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="95c3a-119">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="95c3a-120">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="95c3a-120">The call timed out.</span></span>|  
|<span data-ttu-id="95c3a-121">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="95c3a-121">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="95c3a-122">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="95c3a-122">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="95c3a-123">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="95c3a-123">HOST_E_ABANDONED</span></span>|<span data-ttu-id="95c3a-124">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="95c3a-124">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="95c3a-125">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="95c3a-125">E_FAIL</span></span>|<span data-ttu-id="95c3a-126">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="95c3a-126">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="95c3a-127">Se un metodo restituisce E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="95c3a-127">After a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="95c3a-128">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="95c3a-128">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="95c3a-129">Note</span><span class="sxs-lookup"><span data-stu-id="95c3a-129">Remarks</span></span>  
 <span data-ttu-id="95c3a-130">Il `BeginCustomDump` metodo imposta la configurazione di dump dell'heap personalizzati.</span><span class="sxs-lookup"><span data-stu-id="95c3a-130">The `BeginCustomDump` method sets custom heap dump configuration.</span></span> <span data-ttu-id="95c3a-131">Il [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) metodo cancella la configurazione di dump dell'heap personalizzati e rilascia qualsiasi stato associato.</span><span class="sxs-lookup"><span data-stu-id="95c3a-131">The [EndCustomDump](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-endcustomdump-method.md) method clears the custom heap dump configuration and frees any associated state.</span></span> <span data-ttu-id="95c3a-132">Deve essere chiamato dopo il dump dell'heap personalizzata è stato completato.</span><span class="sxs-lookup"><span data-stu-id="95c3a-132">It should be called after the custom heap dump is complete.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="95c3a-133">Errore durante la chiamata `EndCustomDump` provoca perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="95c3a-133">Failure to call `EndCustomDump` causes memory to leak.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="95c3a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95c3a-134">Requirements</span></span>  
 <span data-ttu-id="95c3a-135">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="95c3a-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="95c3a-136">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="95c3a-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="95c3a-137">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="95c3a-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="95c3a-138">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="95c3a-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="95c3a-139">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="95c3a-139">See Also</span></span>  
 [<span data-ttu-id="95c3a-140">CustomDumpItem (struttura)</span><span class="sxs-lookup"><span data-stu-id="95c3a-140">CustomDumpItem Structure</span></span>](../../../../docs/framework/unmanaged-api/hosting/customdumpitem-structure.md)  
 [<span data-ttu-id="95c3a-141">ECustomDumpFlavor (enumerazione)</span><span class="sxs-lookup"><span data-stu-id="95c3a-141">ECustomDumpFlavor Enumeration</span></span>](../../../../docs/framework/unmanaged-api/hosting/ecustomdumpflavor-enumeration.md)  
 [<span data-ttu-id="95c3a-142">ICLRErrorReportingManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="95c3a-142">ICLRErrorReportingManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrerrorreportingmanager-interface.md)
