---
title: Struttura COR_PRF_EX_CLAUSE_INFO
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_EX_CLAUSE_INFO
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_EX_CLAUSE_INFO
helpviewer_keywords: COR_PRF_EX_CLAUSE_INFO structure [.NET Framework profiling]
ms.assetid: 7d0d6fb7-bc9d-40f0-8163-c0d162eaba7d
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 9952ea1d8c806c9d3ac5357d933092fb82351484
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corprfexclauseinfo-structure"></a><span data-ttu-id="eb383-102">Struttura COR_PRF_EX_CLAUSE_INFO</span><span class="sxs-lookup"><span data-stu-id="eb383-102">COR_PRF_EX_CLAUSE_INFO Structure</span></span>
<span data-ttu-id="eb383-103">Archivia le informazioni su un'istanza di una clausola di eccezione specifica e il relativo frame associato.</span><span class="sxs-lookup"><span data-stu-id="eb383-103">Stores information about a specific exception clause instance and its associated frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eb383-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb383-104">Syntax</span></span>  
  
```  
typedef struct COR_PRF_EX_CLAUSE_INFO {  
    COR_PRF_CLAUSE_TYPE clauseType;  
    UINT_PTR programCounter;  
    UINT_PTR framePointer;  
    UINT_PTR shadowStackPointer;  
} COR_PRF_EX_CLAUSE_INFO;  
```  
  
## <a name="members"></a><span data-ttu-id="eb383-105">Membri</span><span class="sxs-lookup"><span data-stu-id="eb383-105">Members</span></span>  
  
|<span data-ttu-id="eb383-106">Membro</span><span class="sxs-lookup"><span data-stu-id="eb383-106">Member</span></span>|<span data-ttu-id="eb383-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb383-107">Description</span></span>|  
|------------|-----------------|  
|`clauseType`|<span data-ttu-id="eb383-108">Il valore di [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) enumerazione che specifica il tipo di clausola di eccezione, il codice è appena entrato o da sinistra.</span><span class="sxs-lookup"><span data-stu-id="eb383-108">A value of the [COR_PRF_CLAUSE_TYPE](../../../../docs/framework/unmanaged-api/profiling/cor-prf-clause-type-enumeration.md) enumeration that specifies the type of exception clause the code just entered or left.</span></span>|  
|`programCounter`|<span data-ttu-id="eb383-109">Il punto di ingresso nativo del gestore clausola, ad esempio, il contenuto del registro X86 EIP.</span><span class="sxs-lookup"><span data-stu-id="eb383-109">The native entry point of the clause handler — for example, the contents of the X86 EIP register.</span></span>|  
|`framePointer`|<span data-ttu-id="eb383-110">Il puntatore al frame logico per il gestore della clausola, ad esempio, il contenuto del registro X86 EBP.</span><span class="sxs-lookup"><span data-stu-id="eb383-110">The pointer to the logical frame for the clause handler — for example, the contents of the X86 EBP register.</span></span>|  
|`shadowStackPointer`|<span data-ttu-id="eb383-111">Puntatore allo stack di ombreggiatura.</span><span class="sxs-lookup"><span data-stu-id="eb383-111">The pointer to the shadow stack.</span></span> <span data-ttu-id="eb383-112">Questo valore è il contenuto del registro BSP e si applica solo a IA64.</span><span class="sxs-lookup"><span data-stu-id="eb383-112">This value is the contents of the BSP register and applies only to IA64.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="eb383-113">Note</span><span class="sxs-lookup"><span data-stu-id="eb383-113">Remarks</span></span>  
 <span data-ttu-id="eb383-114">Quando viene ricevuta una notifica di eccezione, [ICorProfilerInfo2:: GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) può essere utilizzato per ottenere informazioni sull'indirizzo e il frame nativi per la clausola di eccezione (`catch` / `finally`/dati del filtro) che sta per essere eseguito o si è appena stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb383-114">When an exception notification is received, [ICorProfilerInfo2::GetNotifiedExceptionClauseInfo](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getnotifiedexceptionclauseinfo-method.md) can be used to get the native address and frame information for the exception clause (`catch`/`finally`/filter) that is about to be run or has just been run.</span></span>  
  
 <span data-ttu-id="eb383-115">Esecuzione di una clausola di eccezione comporta questi callback da common language runtime (CLR):</span><span class="sxs-lookup"><span data-stu-id="eb383-115">Execution of an exception clause involves these callbacks from the common language runtime (CLR):</span></span>  
  
-   [<span data-ttu-id="eb383-116">ICorProfilerCallback:: ExceptionCatcherEnter</span><span class="sxs-lookup"><span data-stu-id="eb383-116">ICorProfilerCallback::ExceptionCatcherEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherenter-method.md)  
  
-   [<span data-ttu-id="eb383-117">ICorProfilerCallback:: ExceptionUnwindFinallyEnter</span><span class="sxs-lookup"><span data-stu-id="eb383-117">ICorProfilerCallback::ExceptionUnwindFinallyEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyenter-method.md)  
  
-   [<span data-ttu-id="eb383-118">ICorProfilerCallback:: ExceptionSearchFilterEnter</span><span class="sxs-lookup"><span data-stu-id="eb383-118">ICorProfilerCallback::ExceptionSearchFilterEnter</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterenter-method.md)  
  
-   [<span data-ttu-id="eb383-119">ICorProfilerCallback:: ExceptionCatcherLeave</span><span class="sxs-lookup"><span data-stu-id="eb383-119">ICorProfilerCallback::ExceptionCatcherLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptioncatcherleave-method.md)  
  
-   [<span data-ttu-id="eb383-120">ICorProfilerCallback:: ExceptionUnwindFinallyLeave</span><span class="sxs-lookup"><span data-stu-id="eb383-120">ICorProfilerCallback::ExceptionUnwindFinallyLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionunwindfinallyleave-method.md)  
  
-   [<span data-ttu-id="eb383-121">ICorProfilerCallback:: ExceptionSearchFilterLeave</span><span class="sxs-lookup"><span data-stu-id="eb383-121">ICorProfilerCallback::ExceptionSearchFilterLeave</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-exceptionsearchfilterleave-method.md)  
  
## <a name="requirements"></a><span data-ttu-id="eb383-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb383-122">Requirements</span></span>  
 <span data-ttu-id="eb383-123">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eb383-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eb383-124">**Intestazione:** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="eb383-124">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="eb383-125">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eb383-125">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eb383-126">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eb383-126">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb383-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eb383-127">See Also</span></span>  
 [<span data-ttu-id="eb383-128">Strutture di profilatura</span><span class="sxs-lookup"><span data-stu-id="eb383-128">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
