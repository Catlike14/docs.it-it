---
title: Metodo ICorProfilerCallback::AssemblyLoadStarted
ms.date: 03/30/2017
api_name:
- ICorProfilerCallback.AssemblyLoadStarted
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerCallback::AssemblyLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::AssemblyLoadStarted method [.NET Framework profiling]
- AssemblyLoadStarted method [.NET Framework profiling]
ms.assetid: 67e8209d-a0ca-4118-a6e6-c1ee0abc2221
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: af40d8b603d3bd13abbc5a1c06464583bfa7842d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33450219"
---
# <a name="icorprofilercallbackassemblyloadstarted-method"></a><span data-ttu-id="4e980-102">Metodo ICorProfilerCallback::AssemblyLoadStarted</span><span class="sxs-lookup"><span data-stu-id="4e980-102">ICorProfilerCallback::AssemblyLoadStarted Method</span></span>
<span data-ttu-id="4e980-103">Notifica al profiler che un assembly viene caricato.</span><span class="sxs-lookup"><span data-stu-id="4e980-103">Notifies the profiler that an assembly is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e980-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e980-104">Syntax</span></span>  
  
```  
HRESULT AssemblyLoadStarted(  
    [in] AssemblyID assemblyId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4e980-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e980-105">Parameters</span></span>  
 `assemblyId`  
 <span data-ttu-id="4e980-106">[in] Identifica l'assembly caricato.</span><span class="sxs-lookup"><span data-stu-id="4e980-106">[in] Identifies the assembly that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4e980-107">Note</span><span class="sxs-lookup"><span data-stu-id="4e980-107">Remarks</span></span>  
 <span data-ttu-id="4e980-108">Il valore di `assemblyId` non è valido per una richiesta di informazioni fino a quando il [ICorProfilerCallback:: AssemblyLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyloadfinished-method.md) metodo viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="4e980-108">The value of `assemblyId` is not valid for an information request until the [ICorProfilerCallback::AssemblyLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-assemblyloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e980-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e980-109">Requirements</span></span>  
 <span data-ttu-id="4e980-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e980-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e980-111">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="4e980-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="4e980-112">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="4e980-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4e980-113">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e980-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e980-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4e980-114">See Also</span></span>  
 [<span data-ttu-id="4e980-115">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="4e980-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
