---
title: Metodo IMethodMalloc::Alloc
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMethodMalloc.Alloc
api_location: mscorwks.dll
api_type: COM
f1_keywords: IMethodMalloc::Alloc
helpviewer_keywords:
- IMethodMalloc::Alloc method [.NET Framework profiling]
- Alloc method, IMethodMalloc interface [.NET Framework profiling]
ms.assetid: 8653bd4c-2290-43d2-a3e1-cbbd50033f4f
topic_type: apiref
caps.latest.revision: "15"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ae0fa84c08cb8e366db36b6727a3058f24789801
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="imethodmallocalloc-method"></a><span data-ttu-id="0af9d-102">Metodo IMethodMalloc::Alloc</span><span class="sxs-lookup"><span data-stu-id="0af9d-102">IMethodMalloc::Alloc Method</span></span>
<span data-ttu-id="0af9d-103">Tenta di allocare una quantità specificata di memoria per un nuovo corpo della funzione Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="0af9d-103">Attempts to allocate a specified amount of memory for a new Microsoft intermediate language (MSIL) function body.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0af9d-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0af9d-104">Syntax</span></span>  
  
```  
PVOID Alloc (  
    [in] ULONG   cb  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0af9d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0af9d-105">Parameters</span></span>  
 `cb`  
 <span data-ttu-id="0af9d-106">[in] Il numero di byte da allocare per il corpo del metodo.</span><span class="sxs-lookup"><span data-stu-id="0af9d-106">[in] The number of bytes to allocate for the method body.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0af9d-107">Note</span><span class="sxs-lookup"><span data-stu-id="0af9d-107">Remarks</span></span>  
 <span data-ttu-id="0af9d-108">La memoria allocata inizierà in corrispondenza di un indirizzo maggiore dell'indirizzo di base del modulo che è associato l'allocatore.</span><span class="sxs-lookup"><span data-stu-id="0af9d-108">The allocated memory will begin at an address greater than the base address of the module that is associated with this allocator.</span></span> <span data-ttu-id="0af9d-109">In altre parole, ogni allocatore viene creato per un particolare modulo e tenterà di allocare memoria a un offset positivo dal relativo indirizzo di base.</span><span class="sxs-lookup"><span data-stu-id="0af9d-109">In other words, each allocator is created for a particular module, and will attempt to allocate memory at a positive offset from its base address.</span></span> <span data-ttu-id="0af9d-110">Se `Alloc` non riesce ad allocare il numero richiesto di byte in un indirizzo maggiore dell'indirizzo di base del modulo, restituisce E_OUTOFMEMORY, indipendentemente dalla quantità effettiva di spazio di memoria disponibile.</span><span class="sxs-lookup"><span data-stu-id="0af9d-110">If `Alloc` fails to allocate the requested number of bytes at an address greater than the base address of the module, it returns E_OUTOFMEMORY, regardless of the actual amount of memory space available.</span></span>  
  
 <span data-ttu-id="0af9d-111">Il `Alloc` metodo deve essere utilizzato in combinazione con il [ICorProfilerInfo:: SetILFunctionBody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="0af9d-111">The `Alloc` method should be used in conjunction with the [ICorProfilerInfo::SetILFunctionBody](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-setilfunctionbody-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0af9d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0af9d-112">Requirements</span></span>  
 <span data-ttu-id="0af9d-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0af9d-113">**Platforms:** WindSee [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0af9d-114">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="0af9d-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="0af9d-115">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0af9d-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0af9d-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0af9d-116">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0af9d-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0af9d-117">See Also</span></span>  
 [<span data-ttu-id="0af9d-118">IMethodMalloc (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="0af9d-118">IMethodMalloc Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/imethodmalloc-interface.md)
