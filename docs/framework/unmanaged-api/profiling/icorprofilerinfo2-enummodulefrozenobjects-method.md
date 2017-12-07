---
title: Metodo ICorProfilerInfo2::EnumModuleFrozenObjects
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo2.EnumModuleFrozenObjects
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo2::EnumModuleFrozenObjects
helpviewer_keywords:
- EnumModuleFrozenObjects method [.NET Framework profiling]
- ICorProfilerInfo2::EnumModuleFrozenObjects method [.NET Framework profiling]
ms.assetid: 920b6483-7064-4d64-8613-fcc38ccf9b1e
topic_type: apiref
caps.latest.revision: "14"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3214468045e98d83e2fb0f9c14c851abb45e217b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo2enummodulefrozenobjects-method"></a><span data-ttu-id="e12d3-102">Metodo ICorProfilerInfo2::EnumModuleFrozenObjects</span><span class="sxs-lookup"><span data-stu-id="e12d3-102">ICorProfilerInfo2::EnumModuleFrozenObjects Method</span></span>
<span data-ttu-id="e12d3-103">Ottiene un enumeratore che consente di scorrere gli oggetti bloccati nel modulo specificato. Questo metodo è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="e12d3-103">Gets an enumerator that allows iteration over the frozen objects in the specified module.This method is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e12d3-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e12d3-104">Syntax</span></span>  
  
```  
HRESULT EnumModuleFrozenObjects(  
    [in] ModuleID moduleID,  
    [out] ICorProfilerObjectEnum** ppEnum);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e12d3-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e12d3-105">Parameters</span></span>  
 `moduleID`  
 <span data-ttu-id="e12d3-106">[in] L'ID del modulo che contiene gli oggetti bloccati da enumerare.</span><span class="sxs-lookup"><span data-stu-id="e12d3-106">[in] The ID of the module that contains the frozen objects to be enumerated.</span></span>  
  
 `ppEnum`  
 <span data-ttu-id="e12d3-107">[out] Un puntatore all'indirizzo di un [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interfaccia che enumera gli oggetti bloccati.</span><span class="sxs-lookup"><span data-stu-id="e12d3-107">[out] A pointer to the address of an [ICorProfilerObjectEnum](../../../../docs/framework/unmanaged-api/profiling/icorprofilerobjectenum-interface.md) interface, which enumerates the frozen objects.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e12d3-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e12d3-108">Requirements</span></span>  
 <span data-ttu-id="e12d3-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e12d3-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e12d3-110">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="e12d3-110">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="e12d3-111">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e12d3-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e12d3-112">**Versioni di .NET framework:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span><span class="sxs-lookup"><span data-stu-id="e12d3-112">**.NET Framework Versions:** 3.5, 3.0 SP1, 3.0, 2.0 SP1, 2.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e12d3-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e12d3-113">See Also</span></span>  
 [<span data-ttu-id="e12d3-114">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="e12d3-114">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="e12d3-115">Interfaccia ICorProfilerInfo2</span><span class="sxs-lookup"><span data-stu-id="e12d3-115">ICorProfilerInfo2 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-interface.md)