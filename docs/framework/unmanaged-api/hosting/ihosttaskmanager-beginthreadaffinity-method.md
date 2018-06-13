---
title: Metodo IHostTaskManager::BeginThreadAffinity
ms.date: 03/30/2017
api_name:
- IHostTaskManager.BeginThreadAffinity
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::BeginThreadAffinity
helpviewer_keywords:
- IHostTaskManager::BeginThreadAffinity method [.NET Framework hosting]
- BeginThreadAffinity method [.NET Framework hosting]
ms.assetid: fea3ab88-ce41-4c5a-847b-bb78cd748da6
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 6a94797e6279a1f1d419b977c22d73ca41bbafc9
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33443374"
---
# <a name="ihosttaskmanagerbeginthreadaffinity-method"></a><span data-ttu-id="e3ae6-102">Metodo IHostTaskManager::BeginThreadAffinity</span><span class="sxs-lookup"><span data-stu-id="e3ae6-102">IHostTaskManager::BeginThreadAffinity Method</span></span>
<span data-ttu-id="e3ae6-103">Notifica all'host che il codice gestito sta entrando in un periodo in cui l'attività corrente non deve essere spostata a un altro thread del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-103">Notifies the host that managed code is entering a period in which the current task must not be moved to another operating system thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e3ae6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3ae6-104">Syntax</span></span>  
  
```  
HRESULT BeginThreadAffinity ();  
```  
  
## <a name="return-value"></a><span data-ttu-id="e3ae6-105">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3ae6-105">Return Value</span></span>  
  
|<span data-ttu-id="e3ae6-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="e3ae6-106">HRESULT</span></span>|<span data-ttu-id="e3ae6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3ae6-107">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="e3ae6-108">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3ae6-108">S_OK</span></span>|<span data-ttu-id="e3ae6-109">`BeginThreadAffinity` stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-109">`BeginThreadAffinity` returned successfully.</span></span>|  
|<span data-ttu-id="e3ae6-110">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="e3ae6-110">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="e3ae6-111">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-111">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="e3ae6-112">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="e3ae6-112">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="e3ae6-113">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-113">The call timed out.</span></span>|  
|<span data-ttu-id="e3ae6-114">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="e3ae6-114">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="e3ae6-115">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-115">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="e3ae6-116">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="e3ae6-116">HOST_E_ABANDONED</span></span>|<span data-ttu-id="e3ae6-117">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-117">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="e3ae6-118">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="e3ae6-118">E_FAIL</span></span>|<span data-ttu-id="e3ae6-119">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-119">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="e3ae6-120">Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-120">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="e3ae6-121">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-121">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e3ae6-122">Note</span><span class="sxs-lookup"><span data-stu-id="e3ae6-122">Remarks</span></span>  
 <span data-ttu-id="e3ae6-123">CLR chiama in genere `IHostTaskManager::BeginThreadAffinity` nel contesto di una chiamata a <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-123">The CLR typically calls `IHostTaskManager::BeginThreadAffinity` in the context of a call to <xref:System.Threading.Thread.BeginThreadAffinity%2A?displayProperty=nameWithType>.</span></span> <span data-ttu-id="e3ae6-124">L'attività corrente non deve essere ripianificata fino a quando non viene effettuata una chiamata corrispondente a [IHostTaskManager:: EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span><span class="sxs-lookup"><span data-stu-id="e3ae6-124">The current task must not be rescheduled until a corresponding call is made to [IHostTaskManager::EndThreadAffinity](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-endthreadaffinity-method.md).</span></span> <span data-ttu-id="e3ae6-125">Attività possono essere disattivate, ma quando essi vengono riattivate, deve essere assegnati allo stesso thread del sistema operativo da cui erano state disattivate. Le chiamate annidate a `BeginThreadAffinity` non hanno alcun effetto, poiché la chiamata fa riferimento all'attività corrente.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-125">Tasks can be switched out, but when they are switched back in, they must be assigned to the same operating system thread from which they were switched out. Nested calls to `BeginThreadAffinity` have no effect, because the call refers to the current task.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e3ae6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3ae6-126">Requirements</span></span>  
 <span data-ttu-id="e3ae6-127">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e3ae6-127">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e3ae6-128">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="e3ae6-128">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="e3ae6-129">**Libreria:** inclusa come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="e3ae6-129">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="e3ae6-130">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e3ae6-130">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e3ae6-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e3ae6-131">See Also</span></span>  
 [<span data-ttu-id="e3ae6-132">Interfaccia ICLRTask</span><span class="sxs-lookup"><span data-stu-id="e3ae6-132">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="e3ae6-133">Interfaccia ICLRTaskManager</span><span class="sxs-lookup"><span data-stu-id="e3ae6-133">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="e3ae6-134">Interfaccia IHostTask</span><span class="sxs-lookup"><span data-stu-id="e3ae6-134">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="e3ae6-135">Interfaccia IHostTaskManager</span><span class="sxs-lookup"><span data-stu-id="e3ae6-135">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
