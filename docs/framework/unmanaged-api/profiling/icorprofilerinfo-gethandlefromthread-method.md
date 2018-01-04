---
title: Metodo ICorProfilerInfo::GetHandleFromThread
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetHandleFromThread
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetHandleFromThread
helpviewer_keywords:
- GetHandleFromThread method [.NET Framework profiling]
- ICorProfilerInfo::GetHandleFromThread method [.NET Framework profiling]
ms.assetid: 36cdc9f5-7579-4cd2-aa36-fc05c741584c
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 465fb61d17269873b3a2aa2f323086f209cab946
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilerinfogethandlefromthread-method"></a><span data-ttu-id="486d6-102">Metodo ICorProfilerInfo::GetHandleFromThread</span><span class="sxs-lookup"><span data-stu-id="486d6-102">ICorProfilerInfo::GetHandleFromThread Method</span></span>
<span data-ttu-id="486d6-103">L'ID di un thread viene eseguito il mapping a un handle del thread Win32.</span><span class="sxs-lookup"><span data-stu-id="486d6-103">Maps the ID of a thread to a Win32 thread handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="486d6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="486d6-104">Syntax</span></span>  
  
```  
HRESULT GetHandleFromThread(  
    [in]  ThreadID threadId,  
    [out] HANDLE  *phThread);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="486d6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="486d6-105">Parameters</span></span>  
 `threadId`  
 <span data-ttu-id="486d6-106">[in] ID del thread per eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="486d6-106">[in] The thread ID to be mapped.</span></span>  
  
 `phThread`  
 <span data-ttu-id="486d6-107">[out] Puntatore a un handle del thread Win32.</span><span class="sxs-lookup"><span data-stu-id="486d6-107">[out] A pointer to a Win32 thread handle.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="486d6-108">Note</span><span class="sxs-lookup"><span data-stu-id="486d6-108">Remarks</span></span>  
 <span data-ttu-id="486d6-109">Il profiler deve chiamare Win32 `DuplicateHandle` funzione l'handle prima di utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="486d6-109">The profiler must call the Win32 `DuplicateHandle` function on the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="486d6-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="486d6-110">Requirements</span></span>  
 <span data-ttu-id="486d6-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="486d6-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="486d6-112">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="486d6-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="486d6-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="486d6-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="486d6-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="486d6-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="486d6-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="486d6-115">See Also</span></span>  
 [<span data-ttu-id="486d6-116">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="486d6-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
