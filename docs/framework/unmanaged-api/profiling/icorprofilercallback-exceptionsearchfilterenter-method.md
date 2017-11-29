---
title: Metodo ICorProfilerCallback::ExceptionSearchFilterEnter
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ExceptionSearchFilterEnter
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ExceptionSearchFilterEnter
helpviewer_keywords:
- ExceptionSearchFilterEnter method [.NET Framework profiling]
- ICorProfilerCallback::ExceptionSearchFilterEnter method [.NET Framework profiling]
ms.assetid: acc239ce-3eef-418c-b1df-c5a6dd8e8a4c
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 129bc39fc9edd8f3101e7d03272bcab35c746d73
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilercallbackexceptionsearchfilterenter-method"></a><span data-ttu-id="25aad-102">Metodo ICorProfilerCallback::ExceptionSearchFilterEnter</span><span class="sxs-lookup"><span data-stu-id="25aad-102">ICorProfilerCallback::ExceptionSearchFilterEnter Method</span></span>
<span data-ttu-id="25aad-103">Notifica al profiler che la fase di ricerca di gestione delle eccezioni ha iniziato l'esecuzione di un filtro eccezioni definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="25aad-103">Notifies the profiler that the search phase of exception handling has begun executing a user-defined exception filter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="25aad-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25aad-104">Syntax</span></span>  
  
```  
HRESULT ExceptionSearchFilterEnter(  
    [in] FunctionID functionId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="25aad-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="25aad-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="25aad-106">[in] L'ID della funzione che contiene il filtro.</span><span class="sxs-lookup"><span data-stu-id="25aad-106">[in] The ID of the function that contains the filter.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="25aad-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25aad-107">Requirements</span></span>  
 <span data-ttu-id="25aad-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="25aad-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="25aad-109">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="25aad-109">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="25aad-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="25aad-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="25aad-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="25aad-111">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25aad-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="25aad-112">See Also</span></span>  
 [<span data-ttu-id="25aad-113">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="25aad-113">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)  
 [<span data-ttu-id="25aad-114">ExceptionSearchFilterLeave (metodo)</span><span class="sxs-lookup"><span data-stu-id="25aad-114">ExceptionSearchFilterLeave Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)
