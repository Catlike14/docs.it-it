---
title: Metodo ICorDebug::EnumerateProcesses
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebug.EnumerateProcesses
api_location: mscordbi.dll
api_type: COM
f1_keywords: EnumerateProcesses
helpviewer_keywords:
- EnumerateProcesses method [.NET Framework debugging]
- ICorDebug::EnumerateProcesses method [.NET Framework debugging]
ms.assetid: ba25d166-1d28-4f1d-aca2-de298bbca669
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4ffabcc97a4af33fc859cd096e671f98d52e89e1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugenumerateprocesses-method"></a><span data-ttu-id="f4ee6-102">Metodo ICorDebug::EnumerateProcesses</span><span class="sxs-lookup"><span data-stu-id="f4ee6-102">ICorDebug::EnumerateProcesses Method</span></span>
<span data-ttu-id="f4ee6-103">Ottiene un enumeratore per i processi sottoposti a debug.</span><span class="sxs-lookup"><span data-stu-id="f4ee6-103">Gets an enumerator for the processes that are being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4ee6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4ee6-104">Syntax</span></span>  
  
```  
HRESULT EnumerateProcesses (  
    [out] ICorDebugProcessEnum      **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f4ee6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4ee6-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="f4ee6-106">Un puntatore all'indirizzo di un oggetto ICorDebugProcessEnum che è l'enumeratore per i processi in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="f4ee6-106">A pointer to the address of an ICorDebugProcessEnum object that is the enumerator for the processes being debugged.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4ee6-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4ee6-107">Requirements</span></span>  
 <span data-ttu-id="f4ee6-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f4ee6-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4ee6-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="f4ee6-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f4ee6-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f4ee6-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f4ee6-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4ee6-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4ee6-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f4ee6-112">See Also</span></span>  
 [<span data-ttu-id="f4ee6-113">Interfaccia ICorDebug</span><span class="sxs-lookup"><span data-stu-id="f4ee6-113">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
