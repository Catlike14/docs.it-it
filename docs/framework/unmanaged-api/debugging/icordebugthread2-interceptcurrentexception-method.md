---
title: Metodo ICorDebugThread2::InterceptCurrentException
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread2.InterceptCurrentException
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread2::InterceptCurrentException
helpviewer_keywords:
- InterceptCurrentException method [.NET Framework debugging]
- ICorDebugThread2::InterceptCurrentException method [.NET Framework debugging]
ms.assetid: 536d2357-1b97-49e0-a10c-c860aed74e6e
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 169ce528a2a6fd6ac415989437e721509d9fcda1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugthread2interceptcurrentexception-method"></a><span data-ttu-id="dcf46-102">Metodo ICorDebugThread2::InterceptCurrentException</span><span class="sxs-lookup"><span data-stu-id="dcf46-102">ICorDebugThread2::InterceptCurrentException Method</span></span>
<span data-ttu-id="dcf46-103">Consente a un debugger intercettare l'eccezione corrente su questo thread.</span><span class="sxs-lookup"><span data-stu-id="dcf46-103">Allows a debugger to intercept the current exception on this thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dcf46-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcf46-104">Syntax</span></span>  
  
```  
HRESULT InterceptCurrentException (  
    [in] ICorDebugFrame  *pFrame  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dcf46-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcf46-105">Parameters</span></span>  
 `pFrame`  
 <span data-ttu-id="dcf46-106">[in] Un puntatore a un'interfaccia ICorDebugFrame che rappresenta lo stack frame attivo.</span><span class="sxs-lookup"><span data-stu-id="dcf46-106">[in] A pointer to an ICorDebugFrame that represents the active stack frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dcf46-107">Note</span><span class="sxs-lookup"><span data-stu-id="dcf46-107">Remarks</span></span>  
 <span data-ttu-id="dcf46-108">Il `InterceptCurrentException` metodo può essere chiamato tra un callback di eccezione ([ICorDebugManagedCallback:: Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exception-method.md) o [ICorDebugManagedCallback2:: Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md)) e la chiamata a associata[ICorDebugController:: Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md).</span><span class="sxs-lookup"><span data-stu-id="dcf46-108">The `InterceptCurrentException` method can be called between an exception callback ([ICorDebugManagedCallback::Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exception-method.md) or [ICorDebugManagedCallback2::Exception](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md)) and the associated call to [ICorDebugController::Continue](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-continue-method.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dcf46-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcf46-109">Requirements</span></span>  
 <span data-ttu-id="dcf46-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="dcf46-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="dcf46-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="dcf46-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="dcf46-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="dcf46-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="dcf46-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="dcf46-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
