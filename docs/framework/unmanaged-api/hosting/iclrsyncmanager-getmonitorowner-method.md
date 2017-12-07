---
title: Metodo ICLRSyncManager::GetMonitorOwner
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRSyncManager.GetMonitorOwner
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRSyncManager::GetMonitorOwner
helpviewer_keywords:
- ICLRSyncManager::GetMonitorOwner method [.NET Framework hosting]
- GetMonitorOwner method [.NET Framework hosting]
ms.assetid: 840983a4-396d-47b4-86a0-d35f9b437cdb
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 90fbba9a5aead27d79c5355d69bc12481e826b65
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="iclrsyncmanagergetmonitorowner-method"></a><span data-ttu-id="bf555-102">Metodo ICLRSyncManager::GetMonitorOwner</span><span class="sxs-lookup"><span data-stu-id="bf555-102">ICLRSyncManager::GetMonitorOwner Method</span></span>
<span data-ttu-id="bf555-103">Ottiene il [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) istanza che possiede il monitor identificato dal cookie specificato.</span><span class="sxs-lookup"><span data-stu-id="bf555-103">Gets the [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance that owns the monitor identified by the specified cookie.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bf555-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bf555-104">Syntax</span></span>  
  
```  
HRESULT GetMonitorOwner (  
    [in]  SIZE_T     cookie,  
    [out] IHostTask *ppOwnerHostTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="bf555-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="bf555-105">Parameters</span></span>  
 `cookie`  
 <span data-ttu-id="bf555-106">[in] Il cookie associato al monitor.</span><span class="sxs-lookup"><span data-stu-id="bf555-106">[in] The cookie associated with the monitor.</span></span>  
  
 `ppOwnerHostTask`  
 <span data-ttu-id="bf555-107">[out] Un puntatore al `IHostTask` che possiede attualmente il monitor oppure null se nessuna attività dispone di proprietà.</span><span class="sxs-lookup"><span data-stu-id="bf555-107">[out] A pointer to the `IHostTask` that currently owns the monitor, or null if no task has ownership.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="bf555-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bf555-108">Return Value</span></span>  
  
|<span data-ttu-id="bf555-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bf555-109">HRESULT</span></span>|<span data-ttu-id="bf555-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf555-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="bf555-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf555-111">S_OK</span></span>|<span data-ttu-id="bf555-112">`GetMonitorOwner`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="bf555-112">`GetMonitorOwner` returned successfully.</span></span>|  
|<span data-ttu-id="bf555-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="bf555-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="bf555-114">CLR non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf555-114">The CLR has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="bf555-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="bf555-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="bf555-116">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="bf555-116">The call timed out.</span></span>|  
|<span data-ttu-id="bf555-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="bf555-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="bf555-118">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="bf555-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="bf555-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="bf555-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="bf555-120">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="bf555-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="bf555-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="bf555-121">E_FAIL</span></span>|<span data-ttu-id="bf555-122">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="bf555-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="bf555-123">Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="bf555-123">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="bf555-124">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="bf555-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="bf555-125">Note</span><span class="sxs-lookup"><span data-stu-id="bf555-125">Remarks</span></span>  
 <span data-ttu-id="bf555-126">L'host chiama in genere `GetMonitorOwner` come parte di un meccanismo di rilevamento di deadlock.</span><span class="sxs-lookup"><span data-stu-id="bf555-126">The host typically calls `GetMonitorOwner` as part of a deadlock-detection mechanism.</span></span> <span data-ttu-id="bf555-127">Il cookie è associato a un monitoraggio quando viene creato mediante una chiamata a [IHostSyncManager:: CreateMonitorEvent](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md).</span><span class="sxs-lookup"><span data-stu-id="bf555-127">The cookie is associated with a monitor when it is created by using a call to [IHostSyncManager::CreateMonitorEvent](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-createmonitorevent-method.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="bf555-128">Una chiamata per il rilascio dell'evento sottostante il monitoraggio potrebbe bloccarsi, ma non un deadlock, se una chiamata a questo metodo è attualmente attiva nel cookie associato al monitor.</span><span class="sxs-lookup"><span data-stu-id="bf555-128">A call to release the event underlying the monitor might block—but will not deadlock—if a call to this method is currently in effect on the cookie associated with that monitor.</span></span> <span data-ttu-id="bf555-129">Se si tenta di acquisire il monitor, potrebbe bloccare anche altre attività.</span><span class="sxs-lookup"><span data-stu-id="bf555-129">Other tasks might also block if they attempt to acquire this monitor.</span></span>  
  
 <span data-ttu-id="bf555-130">`GetMonitorOwner`sempre immediatamente e può essere chiamato in qualsiasi momento dopo una chiamata a `CreateMonitorEvent`.</span><span class="sxs-lookup"><span data-stu-id="bf555-130">`GetMonitorOwner` always returns immediately and can be called any time after a call to `CreateMonitorEvent`.</span></span> <span data-ttu-id="bf555-131">L'host non è necessario attendere fino a quando un'attività è in attesa dell'evento.</span><span class="sxs-lookup"><span data-stu-id="bf555-131">The host does not need to wait until a task is waiting on the event.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="bf555-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bf555-132">Requirements</span></span>  
 <span data-ttu-id="bf555-133">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bf555-133">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bf555-134">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="bf555-134">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="bf555-135">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="bf555-135">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="bf555-136">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bf555-136">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf555-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bf555-137">See Also</span></span>  
 [<span data-ttu-id="bf555-138">ICLRSyncManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="bf555-138">ICLRSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrsyncmanager-interface.md)  
 [<span data-ttu-id="bf555-139">IHostSyncManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="bf555-139">IHostSyncManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostsyncmanager-interface.md)