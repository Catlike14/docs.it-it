---
title: Metodo ICorProfilerInfo5::GetEventMask2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
dev_langs: cpp
api_name: ICorProfilerInfo5.GetEventMask2
api_location: mscorwks.dll
api_type: COM
ms.assetid: f854b68f-009c-4ffb-89cd-ca874d1c0fb7
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: da1c4c11adaac21e9769330ee24beceff64e020b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo5geteventmask2-method"></a><span data-ttu-id="88987-102">Metodo ICorProfilerInfo5::GetEventMask2</span><span class="sxs-lookup"><span data-stu-id="88987-102">ICorProfilerInfo5::GetEventMask2 Method</span></span>
<span data-ttu-id="88987-103">[Supportato in .NET Framework 4.5.2 e versioni successive]</span><span class="sxs-lookup"><span data-stu-id="88987-103">[Supported in the .NET Framework 4.5.2 and later versions]</span></span>  
  
 <span data-ttu-id="88987-104">Ottiene le categorie di eventi correnti per le quali il profiler richiede la ricezione delle notifiche da Common Language Runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="88987-104">Gets the current event categories for which the profiler wants to receive notifications from the common language runtime (CLR).</span></span>  <span data-ttu-id="88987-105">Fornisce una funzionalità non fornite dal [ICorProfilerInfo:: GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="88987-105">It provides functionality not provided by the [ICorProfilerInfo::GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="88987-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88987-106">Syntax</span></span>  
  
```cpp
HRESULT GetEventMask2(  
        [out] DWORD* pdwEventsLow,  
        [out] DWORD* pdwEventsHigh  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="88987-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="88987-107">Parameters</span></span>  
 `pdwEventsLow`  
 <span data-ttu-id="88987-108">[out] Puntatore a un valore a 4 byte che specifica le categorie di eventi.</span><span class="sxs-lookup"><span data-stu-id="88987-108">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span> <span data-ttu-id="88987-109">Ogni bit controlla una funzionalità, un comportamento o un tipo di evento diverso.</span><span class="sxs-lookup"><span data-stu-id="88987-109">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="88987-110">I bit sono descritti nel [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumerazione.</span><span class="sxs-lookup"><span data-stu-id="88987-110">The bits are described in the [COR_PRF_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-monitor-enumeration.md) enumeration.</span></span>  
  
 `pdwEventsHigh`  
 <span data-ttu-id="88987-111">[out] Puntatore a un valore a 4 byte che specifica le categorie di eventi.</span><span class="sxs-lookup"><span data-stu-id="88987-111">[out] A pointer to a 4-byte value that specifies the categories of events.</span></span>  <span data-ttu-id="88987-112">Ogni bit controlla una funzionalità, un comportamento o un tipo di evento diverso.</span><span class="sxs-lookup"><span data-stu-id="88987-112">Each bit controls a different capability, behavior, or type of event.</span></span> <span data-ttu-id="88987-113">I bit sono descritti nel [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumerazione.</span><span class="sxs-lookup"><span data-stu-id="88987-113">The bits are described in the [COR_PRF_HIGH_MONITOR](../../../../docs/framework/unmanaged-api/profiling/cor-prf-high-monitor-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="88987-114">Note</span><span class="sxs-lookup"><span data-stu-id="88987-114">Remarks</span></span>  
 <span data-ttu-id="88987-115">Il metodo `GetEventMask2` consente di determinare i callback a cui il profiler ha eseguito la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="88987-115">The `GetEventMask2` method is used to determine which callbacks the profiler has subscribed to.</span></span> <span data-ttu-id="88987-116">In genere, si esegue un OR logico del `pdwEventsLow` e `pdwEventsHigh` valori e dei nuovi bit che si desidera impostare, quindi chiamare il [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="88987-116">Typically, you perform a logical OR of the `pdwEventsLow` and `pdwEventsHigh` values and any new bits you want to set, and then call the [SetEventMask2](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md) method.</span></span>  
  
 <span data-ttu-id="88987-117">Questo metodo è l'alternativa consigliata per la [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="88987-117">This method is the recommended alternative to the [GetEventMask](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-geteventmask-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="88987-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88987-118">Requirements</span></span>  
 <span data-ttu-id="88987-119">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="88987-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="88987-120">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="88987-120">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="88987-121">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="88987-121">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="88987-122">**Versioni di .NET framework:**[!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="88987-122">**.NET Framework Versions:** [!INCLUDE[net_current_v452plus](../../../../includes/net-current-v452plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="88987-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="88987-123">See Also</span></span>  
 [<span data-ttu-id="88987-124">Interfaccia ICorProfilerInfo5</span><span class="sxs-lookup"><span data-stu-id="88987-124">ICorProfilerInfo5 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-interface.md)  
 [<span data-ttu-id="88987-125">Metodo SetEventMask2</span><span class="sxs-lookup"><span data-stu-id="88987-125">SetEventMask2 Method</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo5-seteventmask2-method.md)
