---
title: Enumerazione CorDebugThreadState
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- CorDebugThreadState
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugThreadState
helpviewer_keywords:
- CorDebugThreadState enumeration [.NET Framework debugging]
ms.assetid: a3ccdf18-4ec6-494d-9024-48e5c8c724f5
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: a5363282f2efed003238014390f50c448c529ce2
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="cordebugthreadstate-enumeration"></a><span data-ttu-id="48296-102">Enumerazione CorDebugThreadState</span><span class="sxs-lookup"><span data-stu-id="48296-102">CorDebugThreadState Enumeration</span></span>
<span data-ttu-id="48296-103">Specifica lo stato di un thread per il debug.</span><span class="sxs-lookup"><span data-stu-id="48296-103">Specifies the state of a thread for debugging.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="48296-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48296-104">Syntax</span></span>  
  
```  
typedef enum CorDebugThreadState {  
    THREAD_RUN,  
    THREAD_SUSPEND  
} CorDebugThreadState;  
```  
  
## <a name="members"></a><span data-ttu-id="48296-105">Membri</span><span class="sxs-lookup"><span data-stu-id="48296-105">Members</span></span>  
  
|<span data-ttu-id="48296-106">Membro</span><span class="sxs-lookup"><span data-stu-id="48296-106">Member</span></span>|<span data-ttu-id="48296-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48296-107">Description</span></span>|  
|------------|-----------------|  
|`THREAD_RUN`|<span data-ttu-id="48296-108">Il thread viene eseguito liberamente, a meno che non si verifica un evento di debug.</span><span class="sxs-lookup"><span data-stu-id="48296-108">The thread runs freely, unless a debug event occurs.</span></span>|  
|`THREAD_SUSPEND`|<span data-ttu-id="48296-109">Impossibile eseguire il thread.</span><span class="sxs-lookup"><span data-stu-id="48296-109">The thread cannot run.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="48296-110">Note</span><span class="sxs-lookup"><span data-stu-id="48296-110">Remarks</span></span>  
 <span data-ttu-id="48296-111">Il debugger usa il `CorDebugThreadState` enumerazione per controllare l'esecuzione di un thread.</span><span class="sxs-lookup"><span data-stu-id="48296-111">The debugger uses the `CorDebugThreadState` enumeration to control a thread's execution.</span></span> <span data-ttu-id="48296-112">Lo stato di un thread può essere impostato utilizzando il [ICorDebugThread:: SetDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugthread-setdebugstate-method.md) o [ICorDebugController:: SetAllThreadsDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="48296-112">The state of a thread can be set by using the [ICorDebugThread::SetDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugthread-setdebugstate-method.md) or [ICorDebugController::SetAllThreadsDebugState](../../../../docs/framework/unmanaged-api/debugging/icordebugcontroller-setallthreadsdebugstate-method.md) method.</span></span>  
  
 <span data-ttu-id="48296-113">Un callback fornito per il [API di hosting](../../../../docs/framework/unmanaged-api/hosting/index.md) consente la distribuzione dei messaggi, pertanto non è necessario uno stato interrotto.</span><span class="sxs-lookup"><span data-stu-id="48296-113">A callback provided to the [hosting API](../../../../docs/framework/unmanaged-api/hosting/index.md) enables message pumping, so an interrupted state is not needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="48296-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48296-114">Requirements</span></span>  
 <span data-ttu-id="48296-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="48296-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="48296-116">**Intestazione:** CorDebug.idl, CorDegug.h</span><span class="sxs-lookup"><span data-stu-id="48296-116">**Header:** CorDebug.idl, CorDegug.h</span></span>  
  
 <span data-ttu-id="48296-117">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="48296-117">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="48296-118">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="48296-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="48296-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="48296-119">See Also</span></span>  
 [<span data-ttu-id="48296-120">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="48296-120">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
