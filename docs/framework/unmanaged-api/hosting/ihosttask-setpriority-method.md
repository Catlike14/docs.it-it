---
title: Metodo IHostTask::SetPriority
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTask.SetPriority
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTask::SetPriority
helpviewer_keywords:
- IHostTask::SetPriority method [.NET Framework hosting]
- SetPriority method [.NET Framework hosting]
ms.assetid: cd8c379b-c7a0-434f-8e23-899bd26be75d
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 34dabcb35f46d4a2b0536e00fa1fd69637b14cb2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ihosttasksetpriority-method"></a><span data-ttu-id="00f89-102">Metodo IHostTask::SetPriority</span><span class="sxs-lookup"><span data-stu-id="00f89-102">IHostTask::SetPriority Method</span></span>
<span data-ttu-id="00f89-103">Il livello di richiede che l'host di modificare la priorità del thread per l'attività rappresentata dall'oggetto corrente [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) istanza.</span><span class="sxs-lookup"><span data-stu-id="00f89-103">Requests that the host adjust the thread priority level for the task represented by the current [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="00f89-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00f89-104">Syntax</span></span>  
  
```  
HRESULT SetPriority (  
    [in] int newPriority  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="00f89-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="00f89-105">Parameters</span></span>  
 `newPriority`  
 <span data-ttu-id="00f89-106">[in] Valore intero che rappresenta il valore di priorità di thread richiesti per l'attività rappresentata dall'oggetto corrente `IHostTask` istanza.</span><span class="sxs-lookup"><span data-stu-id="00f89-106">[in] An integer that represents the requested thread priority value for the task represented by the current `IHostTask` instance.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="00f89-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00f89-107">Return Value</span></span>  
  
|<span data-ttu-id="00f89-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="00f89-108">HRESULT</span></span>|<span data-ttu-id="00f89-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00f89-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="00f89-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="00f89-110">S_OK</span></span>|<span data-ttu-id="00f89-111">`SetPriority`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="00f89-111">`SetPriority` returned successfully.</span></span>|  
|<span data-ttu-id="00f89-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="00f89-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="00f89-113">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="00f89-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="00f89-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="00f89-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="00f89-115">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="00f89-115">The call timed out.</span></span>|  
|<span data-ttu-id="00f89-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="00f89-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="00f89-117">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="00f89-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="00f89-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="00f89-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="00f89-119">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="00f89-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="00f89-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="00f89-120">E_FAIL</span></span>|<span data-ttu-id="00f89-121">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="00f89-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="00f89-122">Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="00f89-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="00f89-123">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="00f89-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="00f89-124">Note</span><span class="sxs-lookup"><span data-stu-id="00f89-124">Remarks</span></span>  
 <span data-ttu-id="00f89-125">Thread vengono concesse tempo di elaborazione utilizzando un sistema round robin parzialmente basato sul livello di priorità di un thread.</span><span class="sxs-lookup"><span data-stu-id="00f89-125">Threads are granted processing time using a round-robin system that is partly based on a thread's priority level.</span></span> <span data-ttu-id="00f89-126">`SetPriority`consente a CLR di impostare tale livello di priorità di thread per l'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="00f89-126">`SetPriority` allows the CLR to set that thread priority level for the current task.</span></span> <span data-ttu-id="00f89-127">Le operazioni seguenti `newPriority` i valori sono supportati.</span><span class="sxs-lookup"><span data-stu-id="00f89-127">The following `newPriority` values are supported.</span></span>  
  
-   <span data-ttu-id="00f89-128">THREAD_PRIORITY_ABOVE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="00f89-128">THREAD_PRIORITY_ABOVE_NORMAL</span></span>  
  
-   <span data-ttu-id="00f89-129">THREAD_PRIORITY_BELOW_NORMAL</span><span class="sxs-lookup"><span data-stu-id="00f89-129">THREAD_PRIORITY_BELOW_NORMAL</span></span>  
  
-   <span data-ttu-id="00f89-130">THREAD_PRIORITY_HIGHEST</span><span class="sxs-lookup"><span data-stu-id="00f89-130">THREAD_PRIORITY_HIGHEST</span></span>  
  
-   <span data-ttu-id="00f89-131">THREAD_PRIORITY_IDLE</span><span class="sxs-lookup"><span data-stu-id="00f89-131">THREAD_PRIORITY_IDLE</span></span>  
  
-   <span data-ttu-id="00f89-132">THREAD_PRIORITY_LOWEST</span><span class="sxs-lookup"><span data-stu-id="00f89-132">THREAD_PRIORITY_LOWEST</span></span>  
  
-   <span data-ttu-id="00f89-133">THREAD_PRIORITY_NORMAL</span><span class="sxs-lookup"><span data-stu-id="00f89-133">THREAD_PRIORITY_NORMAL</span></span>  
  
-   <span data-ttu-id="00f89-134">THREAD_PRIORITY_TIME_CRITICAL</span><span class="sxs-lookup"><span data-stu-id="00f89-134">THREAD_PRIORITY_TIME_CRITICAL</span></span>  
  
 <span data-ttu-id="00f89-135">CLR chiama `SetPriority` quando il valore di <xref:System.Threading.Thread.Priority%2A?displayProperty=nameWithType> viene modificato dal codice utente.</span><span class="sxs-lookup"><span data-stu-id="00f89-135">The CLR calls `SetPriority` when the value of the <xref:System.Threading.Thread.Priority%2A?displayProperty=nameWithType> is modified by user code.</span></span> <span data-ttu-id="00f89-136">Un host può definire i propri algoritmi per l'assegnazione di priorità di thread e può ignorare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="00f89-136">A host can define its own algorithms for thread priority assignment, and is free to ignore this request.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="00f89-137">`SetPriority`indica se il livello di priorità di thread è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="00f89-137">`SetPriority` does not report whether the thread priority level was changed.</span></span> <span data-ttu-id="00f89-138">Chiamare [IHostTask:: GetPriority](../../../../docs/framework/unmanaged-api/hosting/ihosttask-getpriority-method.md) per determinare il valore del livello di priorità di thread dell'attività.</span><span class="sxs-lookup"><span data-stu-id="00f89-138">Call [IHostTask::GetPriority](../../../../docs/framework/unmanaged-api/hosting/ihosttask-getpriority-method.md) to determine the value of the task's thread priority level.</span></span>  
  
 <span data-ttu-id="00f89-139">I valori del livello di priorità del thread sono definiti da Win32 `SetThreadPriority` (funzione).</span><span class="sxs-lookup"><span data-stu-id="00f89-139">Thread priority level values are defined by the Win32 `SetThreadPriority` function.</span></span> <span data-ttu-id="00f89-140">Per ulteriori informazioni sulla priorità di thread, vedere la documentazione di piattaforma di Windows.</span><span class="sxs-lookup"><span data-stu-id="00f89-140">For more information about thread priority, see the Windows Platform documentation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="00f89-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00f89-141">Requirements</span></span>  
 <span data-ttu-id="00f89-142">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="00f89-142">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="00f89-143">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="00f89-143">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="00f89-144">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="00f89-144">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="00f89-145">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="00f89-145">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="00f89-146">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="00f89-146">See Also</span></span>  
 <xref:System.Threading.Thread>  
 [<span data-ttu-id="00f89-147">ICLRTask (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="00f89-147">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="00f89-148">ICLRTaskManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="00f89-148">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="00f89-149">IHostTask (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="00f89-149">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="00f89-150">GetPriority (metodo)</span><span class="sxs-lookup"><span data-stu-id="00f89-150">GetPriority Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-getpriority-method.md)  
 [<span data-ttu-id="00f89-151">IHostTaskManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="00f89-151">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)