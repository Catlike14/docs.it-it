---
title: Enumerazione COR_PRF_SUSPEND_REASON
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_SUSPEND_REASON
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_SUSPEND_REASON
helpviewer_keywords: COR_PRF_SUSPEND_REASON enumeration [.NET Framework profiling]
ms.assetid: 75594833-bed3-47b2-a426-b75c5fe6fbcf
topic_type: apiref
caps.latest.revision: "16"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: aef9688d3da047645d53f6fcf113153393780c8c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corprfsuspendreason-enumeration"></a><span data-ttu-id="0d5ee-102">Enumerazione COR_PRF_SUSPEND_REASON</span><span class="sxs-lookup"><span data-stu-id="0d5ee-102">COR_PRF_SUSPEND_REASON Enumeration</span></span>
<span data-ttu-id="0d5ee-103">Indica il motivo per cui il runtime è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-103">Indicates the reason that the runtime is suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0d5ee-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d5ee-104">Syntax</span></span>  
  
```  
typedef enum {  
    COR_PRF_SUSPEND_OTHER                   = 0x00,  
    COR_PRF_SUSPEND_FOR_GC                  = 0x01,  
    COR_PRF_SUSPEND_FOR_APPDOMAIN_SHUTDOWN  = 0x02,  
    COR_PRF_SUSPEND_FOR_CODE_PITCHING       = 0x03,  
    COR_PRF_SUSPEND_FOR_SHUTDOWN            = 0x04,  
    COR_PRF_SUSPEND_FOR_INPROC_DEBUGGER     = 0x06,  
    COR_PRF_SUSPEND_FOR_GC_PREP             = 0x07,    COR_PRF_SUSPEND_FOR_REJIT               = 8  
} COR_PRF_SUSPEND_REASON;  
```  
  
## <a name="members"></a><span data-ttu-id="0d5ee-105">Membri</span><span class="sxs-lookup"><span data-stu-id="0d5ee-105">Members</span></span>  
  
|<span data-ttu-id="0d5ee-106">Membro</span><span class="sxs-lookup"><span data-stu-id="0d5ee-106">Member</span></span>|<span data-ttu-id="0d5ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d5ee-107">Description</span></span>|  
|------------|-----------------|  
|`COR_PRF_FIELD_SUSPEND_OTHER`|<span data-ttu-id="0d5ee-108">Il runtime è sospeso per un motivo non specificato.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-108">The runtime is suspended for an unspecified reason.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_GC`|<span data-ttu-id="0d5ee-109">Il runtime è sospeso per una richiesta di garbage collection del servizio.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-109">The runtime is suspended to service a garbage collection request.</span></span><br /><br /> <span data-ttu-id="0d5ee-110">I callback relativi a garbage si verificano tra il [ICorProfilerCallback:: RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) e [ICorProfilerCallback:: RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) callback.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-110">The garbage collection-related callbacks occur between the [ICorProfilerCallback::RuntimeSuspendFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimesuspendfinished-method.md) and [ICorProfilerCallback::RuntimeResumeStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimeresumestarted-method.md) callbacks.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_APPDOMAIN_SHUTDOWN`|<span data-ttu-id="0d5ee-111">Il runtime è stato sospeso in modo che un `AppDomain` può essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-111">The runtime is suspended so that an `AppDomain` can be shut down.</span></span><br /><br /> <span data-ttu-id="0d5ee-112">Durante la fase di esecuzione viene sospesa, il runtime determina quali thread si trovano nel `AppDomain` ovvero viene chiuso e impostarle per l'interruzione quando viene ripristinata.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-112">While the runtime is suspended, the runtime will determine which threads are in the `AppDomain` that is being shut down and set them to abort when they resume.</span></span> <span data-ttu-id="0d5ee-113">Esistono alcun `AppDomain`-callback specifici durante la sospensione.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-113">There are no `AppDomain`-specific callbacks during this suspension.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_CODE_PITCHING`|<span data-ttu-id="0d5ee-114">La fase di esecuzione viene sospesa in modo che può verificarsi lancio del codice.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-114">The runtime is suspended so that code pitching can occur.</span></span><br /><br /> <span data-ttu-id="0d5ee-115">Lancio del codice viene utilizzata solo quando il compilatore di just-in-time (JIT) è attivo con abilitato lancio del codice.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-115">Code pitching ensues only when the just-in-time (JIT) compiler is active with code pitching enabled.</span></span> <span data-ttu-id="0d5ee-116">Codice di callback pitching si verificano tra il `ICorProfilerCallback::RuntimeSuspendFinished` e `ICorProfilerCallback::RuntimeResumeStarted` callback.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-116">Code pitching callbacks occur between the `ICorProfilerCallback::RuntimeSuspendFinished` and `ICorProfilerCallback::RuntimeResumeStarted` callbacks.</span></span> <span data-ttu-id="0d5ee-117">**Nota:** JIT CLR non intonazione funzioni in .NET Framework versione 2.0, questo valore non viene usata in 2.0.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-117">**Note:**  The CLR JIT does not pitch functions in the .NET Framework version 2.0, so this value is not used in 2.0.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_SHUTDOWN`|<span data-ttu-id="0d5ee-118">La fase di esecuzione viene sospesa in modo da poter essere arrestato.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-118">The runtime is suspended so that it can shut down.</span></span> <span data-ttu-id="0d5ee-119">È necessario sospendere tutti i thread per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-119">It must suspend all threads to complete the operation.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_INPROC_DEBUGGER`|<span data-ttu-id="0d5ee-120">Il runtime è sospeso per il debug in-process.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-120">The runtime is suspended for in-process debugging.</span></span>|  
|`COR_PRF_FIELD_SUSPEND_FOR_GC_PREP`|<span data-ttu-id="0d5ee-121">Il runtime è sospeso per preparare per una garbage collection.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-121">The runtime is suspended to prepare for a garbage collection.</span></span>|  
|`COR_PRF_SUSPEND_FOR_REJIT`|<span data-ttu-id="0d5ee-122">Il runtime è sospeso per la ricompilazione JIT.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-122">The runtime is suspended for JIT recompilation.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="0d5ee-123">Note</span><span class="sxs-lookup"><span data-stu-id="0d5ee-123">Remarks</span></span>  
 <span data-ttu-id="0d5ee-124">Tutti i thread di runtime nel codice non gestito è possibile continuare l'esecuzione fino a quando non si tenta di immettere nuovamente la fase di esecuzione, a quel punto si verrà inoltre sospeso fino a quando il runtime riprende.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-124">All runtime threads that are in unmanaged code are permitted to continue running until they try to re-enter the runtime, at which point they will also be suspended until the runtime resumes.</span></span> <span data-ttu-id="0d5ee-125">Questo vale anche per i nuovi thread che accedono al runtime.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-125">This also applies to new threads that enter the runtime.</span></span> <span data-ttu-id="0d5ee-126">Tutti i thread nel runtime vengono sospesi immediatamente se si trovano nel codice che possono essere interrotte o richiesto di sospendere l'esecuzione quando raggiungono codice.</span><span class="sxs-lookup"><span data-stu-id="0d5ee-126">All threads within the runtime are either suspended immediately if they are in interruptible code, or asked to suspend when they do reach interruptible code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0d5ee-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d5ee-127">Requirements</span></span>  
 <span data-ttu-id="0d5ee-128">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0d5ee-128">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0d5ee-129">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0d5ee-129">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0d5ee-130">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0d5ee-130">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0d5ee-131">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0d5ee-131">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0d5ee-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0d5ee-132">See Also</span></span>  
 [<span data-ttu-id="0d5ee-133">Enumerazioni di profilatura</span><span class="sxs-lookup"><span data-stu-id="0d5ee-133">Profiling Enumerations</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-enumerations.md)
