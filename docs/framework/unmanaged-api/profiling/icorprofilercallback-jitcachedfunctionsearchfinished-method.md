---
title: Metodo ICorProfilerCallback::JITCachedFunctionSearchFinished
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.JITCachedFunctionSearchFinished
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::JITCachedFunctionSearchFinished
helpviewer_keywords:
- JITCachedFunctionSearchFinished method [.NET Framework profiling]
- ICorProfilerCallback::JITCachedFunctionSearchFinished method [.NET Framework profiling]
ms.assetid: 3c325c82-cddd-4b00-b3da-e450c36abf62
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ffbe331399334d179cf8325e7d9e6773b5bf7012
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackjitcachedfunctionsearchfinished-method"></a><span data-ttu-id="e8034-102">Metodo ICorProfilerCallback::JITCachedFunctionSearchFinished</span><span class="sxs-lookup"><span data-stu-id="e8034-102">ICorProfilerCallback::JITCachedFunctionSearchFinished Method</span></span>
<span data-ttu-id="e8034-103">Notifica al profiler che una ricerca è stato completato per una funzione che è stata compilata in precedenza utilizzando il generatore di immagini Native (NGen.exe).</span><span class="sxs-lookup"><span data-stu-id="e8034-103">Notifies the profiler that a search has finished for a function that was compiled previously using the Native Image Generator (NGen.exe).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8034-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8034-104">Syntax</span></span>  
  
```  
HRESULT JITCachedFunctionSearchFinished(  
    [in] FunctionID        functionId,  
    [in] COR_PRF_JIT_CACHE result);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8034-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8034-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="e8034-106">[in] L'ID della funzione per cui è stata eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="e8034-106">[in] The ID of the function for which the search was performed.</span></span>  
  
 `result`  
 <span data-ttu-id="e8034-107">[in] Il valore di [COR_PRF_JIT_CACHE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-jit-cache-enumeration.md) enumerazione che indica il risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="e8034-107">[in] A value of the [COR_PRF_JIT_CACHE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-jit-cache-enumeration.md) enumeration that indicates the result of the search.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e8034-108">Note</span><span class="sxs-lookup"><span data-stu-id="e8034-108">Remarks</span></span>  
 <span data-ttu-id="e8034-109">In .NET Framework versione 2.0, il [ICorProfilerCallback:: JITCachedFunctionSearchStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcachedfunctionsearchstarted-method.md) e `JITCachedFunctionSearchFinished` i callback non verranno effettuati per tutte le funzioni nelle immagini NGen normali.</span><span class="sxs-lookup"><span data-stu-id="e8034-109">In the .NET Framework version 2.0, the [ICorProfilerCallback::JITCachedFunctionSearchStarted](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-jitcachedfunctionsearchstarted-method.md) and `JITCachedFunctionSearchFinished` callbacks will not be made for all functions in regular NGen images.</span></span> <span data-ttu-id="e8034-110">Solo le immagini NGen ottimizzate per un profiler genererà i callback per tutte le funzioni nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="e8034-110">Only NGen images optimized for a profiler will generate callbacks for all functions in the image.</span></span> <span data-ttu-id="e8034-111">Tuttavia, a causa del sovraccarico aggiuntivo, un profiler deve richiedere immagini NGen ottimizzate profiler solo se intende utilizzare questi callback per forzare una funzione compilati just-in-time (JIT).</span><span class="sxs-lookup"><span data-stu-id="e8034-111">However, due to the additional overhead, a profiler should request profiler-optimized NGen images only if it intends to use these callbacks to force a function to be compiled just-in-time (JIT).</span></span> <span data-ttu-id="e8034-112">In caso contrario, il profiler deve utilizzare una strategia lenta per raccogliere le informazioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="e8034-112">Otherwise, the profiler should use a lazy strategy for gathering function information.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8034-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8034-113">Requirements</span></span>  
 <span data-ttu-id="e8034-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e8034-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8034-115">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e8034-115">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e8034-116">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e8034-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e8034-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8034-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8034-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e8034-118">See Also</span></span>  
 [<span data-ttu-id="e8034-119">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="e8034-119">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
