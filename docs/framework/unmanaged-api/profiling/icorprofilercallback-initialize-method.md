---
title: Metodo ICorProfilerCallback::Initialize
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.Initialize
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::Initialize
helpviewer_keywords:
- Initialize method, ICorProfilerCallback interface [.NET Framework profiling]
- ICorProfilerCallback::Initialize method [.NET Framework profiling]
ms.assetid: dc5fab2a-4b45-4b12-8727-b89c9915f23e
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: cd53d74dfe8199617df47e46641b71203abf6e5e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33452348"
---
# <a name="icorprofilercallbackinitialize-method"></a><span data-ttu-id="e7061-102">Metodo ICorProfilerCallback::Initialize</span><span class="sxs-lookup"><span data-stu-id="e7061-102">ICorProfilerCallback::Initialize Method</span></span>
<span data-ttu-id="e7061-103">Chiamato per inizializzare il profiler di codice ogni volta che viene avviata una nuova applicazione di common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="e7061-103">Called to initialize the code profiler whenever a new common language runtime (CLR) application is started.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e7061-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7061-104">Syntax</span></span>  
  
```  
HRESULT Initialize(  
    [in] IUnknown     *pICorProfilerInfoUnk);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e7061-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7061-105">Parameters</span></span>  
 `pICorProfilerInfoUnk`  
 <span data-ttu-id="e7061-106">[in](/cpp/atl/iunknown) interfaccia che il profiler deve eseguire una query per un [ICorProfilerInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md) puntatore a interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e7061-106">[in](/cpp/atl/iunknown) interface that the profiler must query for an [ICorProfilerInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md) interface pointer.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e7061-107">Note</span><span class="sxs-lookup"><span data-stu-id="e7061-107">Remarks</span></span>  
 <span data-ttu-id="e7061-108">Il `Initialize` chiamata è l'unico modo per abilitare (o disabilitare) callback non sono modificabili.</span><span class="sxs-lookup"><span data-stu-id="e7061-108">The `Initialize` call is the only opportunity to enable (or disable) callbacks that are immutable.</span></span> <span data-ttu-id="e7061-109">Dopo aver abilitato da un callback di `Initialize` chiama, non può essere disabilitata in seguito utilizzando [ICorProfilerInfo:: SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md).</span><span class="sxs-lookup"><span data-stu-id="e7061-109">Once a callback is enabled by the `Initialize` call, it cannot be disabled later using [ICorProfilerInfo::SetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-seteventmask-method.md).</span></span> <span data-ttu-id="e7061-110">Il valore COR_PRF_MONITOR_IMMUTABLE il [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumerazione indica gli eventi che non sono modificabili.</span><span class="sxs-lookup"><span data-stu-id="e7061-110">The COR_PRF_MONITOR_IMMUTABLE value of the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration indicates which events are immutable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e7061-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7061-111">Requirements</span></span>  
 <span data-ttu-id="e7061-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e7061-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e7061-113">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e7061-113">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e7061-114">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="e7061-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e7061-115">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e7061-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e7061-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7061-116">See Also</span></span>  
 [<span data-ttu-id="e7061-117">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="e7061-117">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="e7061-118">Metodo Shutdown</span><span class="sxs-lookup"><span data-stu-id="e7061-118">Shutdown Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-shutdown-method.md)
