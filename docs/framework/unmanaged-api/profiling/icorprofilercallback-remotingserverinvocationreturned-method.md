---
title: Metodo ICorProfilerCallback::RemotingServerInvocationReturned
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.RemotingServerInvocationReturned
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::RemotingServerInvocationReturned
helpviewer_keywords:
- ICorProfilerCallback::RemotingServerInvocationReturned method [.NET Framework profiling]
- RemotingServerInvocationReturned method [.NET Framework profiling]
ms.assetid: a4de6805-e159-4280-99e5-3390c86166d0
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: dac859c52f5e85173bb28821672a6437f3e0718f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilercallbackremotingserverinvocationreturned-method"></a><span data-ttu-id="a6352-102">Metodo ICorProfilerCallback::RemotingServerInvocationReturned</span><span class="sxs-lookup"><span data-stu-id="a6352-102">ICorProfilerCallback::RemotingServerInvocationReturned Method</span></span>
<span data-ttu-id="a6352-103">Notifica al profiler che il processo è terminato chiamando un metodo in risposta a una richiesta di chiamata di metodo remoto.</span><span class="sxs-lookup"><span data-stu-id="a6352-103">Notifies the profiler that the process has finished invoking a method in response to a remote method invocation request.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a6352-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6352-104">Syntax</span></span>  
  
```  
HRESULT RemotingServerInvocationReturned();  
```  
  
## <a name="requirements"></a><span data-ttu-id="a6352-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6352-105">Requirements</span></span>  
 <span data-ttu-id="a6352-106">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a6352-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a6352-107">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="a6352-107">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="a6352-108">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a6352-108">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a6352-109">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a6352-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a6352-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a6352-110">See Also</span></span>  
 [<span data-ttu-id="a6352-111">Interfaccia ICorProfilerCallback</span><span class="sxs-lookup"><span data-stu-id="a6352-111">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)
