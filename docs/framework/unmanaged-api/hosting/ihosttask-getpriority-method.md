---
title: Metodo IHostTask::GetPriority
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTask.GetPriority
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTask::GetPriority
helpviewer_keywords:
- GetPriority method [.NET Framework hosting]
- IHostTask::GetPriority method [.NET Framework hosting]
ms.assetid: 4b463cd6-77c1-4f9a-8518-346ad8fc4b70
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: ba32e8c442042f59c8346d68cef7d9f6678ae7dc
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ihosttaskgetpriority-method"></a><span data-ttu-id="78ccb-102">Metodo IHostTask::GetPriority</span><span class="sxs-lookup"><span data-stu-id="78ccb-102">IHostTask::GetPriority Method</span></span>
<span data-ttu-id="78ccb-103">Ottiene il livello di priorità di thread per l'attività rappresentata dall'oggetto corrente [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) istanza.</span><span class="sxs-lookup"><span data-stu-id="78ccb-103">Gets the thread priority level of the task represented by the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78ccb-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78ccb-104">Syntax</span></span>  
  
```  
HRESULT GetPriority (  
    [out] int *pPriority  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="78ccb-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="78ccb-105">Parameters</span></span>  
 `pPriority`  
 <span data-ttu-id="78ccb-106">[out] Un puntatore a un intero che indica il livello di priorità di thread per l'attività rappresentata dall'oggetto corrente `IHostTask` istanza.</span><span class="sxs-lookup"><span data-stu-id="78ccb-106">[out] A pointer to an integer that indicates the thread priority level of the task represented by the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="78ccb-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78ccb-107">Return Value</span></span>  
  
|<span data-ttu-id="78ccb-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="78ccb-108">HRESULT</span></span>|<span data-ttu-id="78ccb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78ccb-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="78ccb-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="78ccb-110">S_OK</span></span>|<span data-ttu-id="78ccb-111">`GetPriority`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="78ccb-111">`GetPriority` returned successfully.</span></span>|  
|<span data-ttu-id="78ccb-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="78ccb-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="78ccb-113">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="78ccb-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="78ccb-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="78ccb-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="78ccb-115">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="78ccb-115">The call timed out.</span></span>|  
|<span data-ttu-id="78ccb-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="78ccb-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="78ccb-117">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="78ccb-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="78ccb-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="78ccb-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="78ccb-119">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="78ccb-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="78ccb-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="78ccb-120">E_FAIL</span></span>|<span data-ttu-id="78ccb-121">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="78ccb-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="78ccb-122">Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="78ccb-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="78ccb-123">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="78ccb-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="78ccb-124">Note</span><span class="sxs-lookup"><span data-stu-id="78ccb-124">Remarks</span></span>  
 <span data-ttu-id="78ccb-125">I valori del livello di priorità del thread sono definiti da Win32 `SetThreadPriority` (funzione).</span><span class="sxs-lookup"><span data-stu-id="78ccb-125">Thread priority level values are defined by the Win32 `SetThreadPriority` function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="78ccb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78ccb-126">Requirements</span></span>  
 <span data-ttu-id="78ccb-127">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="78ccb-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="78ccb-128">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="78ccb-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="78ccb-129">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="78ccb-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="78ccb-130">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="78ccb-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="78ccb-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="78ccb-131">See Also</span></span>  
 [<span data-ttu-id="78ccb-132">ICLRTask (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="78ccb-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="78ccb-133">ICLRTaskManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="78ccb-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="78ccb-134">IHostTask (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="78ccb-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="78ccb-135">IHostTaskManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="78ccb-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)