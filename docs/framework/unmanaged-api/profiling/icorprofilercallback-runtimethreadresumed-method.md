---
title: Metodo ICorProfilerCallback::RuntimeThreadResumed
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.RuntimeThreadResumed
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::RuntimeThreadResumed
helpviewer_keywords:
- ICorProfilerCallback::RuntimeThreadResumed method [.NET Framework profiling]
- RuntimeThreadResumed method [.NET Framework profiling]
ms.assetid: da984f89-4f53-4ab0-ae6f-3e2ee6085994
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: b460f87ead93c5f375c758a5547c0ae0be2b5691
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackruntimethreadresumed-method"></a><span data-ttu-id="e4efd-102">Metodo ICorProfilerCallback::RuntimeThreadResumed</span><span class="sxs-lookup"><span data-stu-id="e4efd-102">ICorProfilerCallback::RuntimeThreadResumed Method</span></span>
<span data-ttu-id="e4efd-103">Notifica al profiler che il thread specificato ha ripreso dopo la sospensione.</span><span class="sxs-lookup"><span data-stu-id="e4efd-103">Notifies the profiler that the specified thread has resumed after being suspended.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e4efd-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4efd-104">Syntax</span></span>  
  
```  
HRESULT RuntimeThreadResumed(  
    [in] ThreadID threadId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e4efd-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4efd-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="e4efd-106">[in] L'ID del thread che è stata ripresa.</span><span class="sxs-lookup"><span data-stu-id="e4efd-106">[in] The ID of the thread that has been resumed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e4efd-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4efd-107">Requirements</span></span>  
 <span data-ttu-id="e4efd-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e4efd-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e4efd-109">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e4efd-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e4efd-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e4efd-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e4efd-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e4efd-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e4efd-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e4efd-112">See Also</span></span>  
 [<span data-ttu-id="e4efd-113">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="e4efd-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="e4efd-114">RuntimeThreadSuspended (metodo)</span><span class="sxs-lookup"><span data-stu-id="e4efd-114">RuntimeThreadSuspended Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-runtimethreadsuspended-method.md)
