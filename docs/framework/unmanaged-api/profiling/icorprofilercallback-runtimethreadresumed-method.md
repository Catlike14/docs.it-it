---
title: Metodo ICorProfilerCallback::RuntimeThreadResumed
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
- ICorProfilerCallback.RuntimeThreadResumed
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::RuntimeThreadResumed
helpviewer_keywords:
- ICorProfilerCallback::RuntimeThreadResumed method [.NET Framework profiling]
- RuntimeThreadResumed method [.NET Framework profiling]
ms.assetid: da984f89-4f53-4ab0-ae6f-3e2ee6085994
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 94d7e46140b36d6fcce788d70cc856a6776e9f24
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="b4b34-102">Metodo ICorProfilerCallback::RuntimeThreadResumed</span><span class="sxs-lookup"><span data-stu-id="b4b34-102">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>
<span data-ttu-id="b4b34-103">Notifica al profiler che il thread specificato ha ripreso dopo la sospensione.</span><span class="sxs-lookup"><span data-stu-id="b4b34-103">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b4b34-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4b34-104">Syntax</span></span>  
  
```  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b4b34-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4b34-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="b4b34-106">[in] L'ID del thread che è stata ripresa.</span><span class="sxs-lookup"><span data-stu-id="b4b34-106">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b4b34-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4b34-107">Requirements</span></span>  
 <span data-ttu-id="b4b34-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b4b34-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b4b34-109">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="b4b34-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="b4b34-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b4b34-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b4b34-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b4b34-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b4b34-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b4b34-112">See Also</span></span>  
 [<span data-ttu-id="b4b34-113">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="b4b34-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="b4b34-114">Metodo RuntimeThreadSuspended</span><span class="sxs-lookup"><span data-stu-id="b4b34-114">RuntimeThreadSuspended Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimethreadsuspended-method.md)
