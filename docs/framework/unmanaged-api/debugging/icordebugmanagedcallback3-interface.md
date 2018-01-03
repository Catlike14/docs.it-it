---
title: Interfaccia ICorDebugManagedCallback3
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback3
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback3
helpviewer_keywords: ICorDebugManagedCallback3 interface [.NET Framework debugging]
ms.assetid: a95389d3-cf2e-47a4-9805-61426acc6b65
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: a517a9557f84b7eac5d9a773b85ffc7605eba8c6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugmanagedcallback3-interface"></a><span data-ttu-id="9d0c0-102">Interfaccia ICorDebugManagedCallback3</span><span class="sxs-lookup"><span data-stu-id="9d0c0-102">ICorDebugManagedCallback3 Interface</span></span>
<span data-ttu-id="9d0c0-103">Fornisce un metodo di callback che indica che è stata generata una notifica di debugger personalizzata abilitata.</span><span class="sxs-lookup"><span data-stu-id="9d0c0-103">Provides a callback method that indicates that an enabled custom debugger notification has been raised.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9d0c0-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="9d0c0-104">Methods</span></span>  
  
|<span data-ttu-id="9d0c0-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="9d0c0-105">Method</span></span>|<span data-ttu-id="9d0c0-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d0c0-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="9d0c0-107">Metodo CustomNotification</span><span class="sxs-lookup"><span data-stu-id="9d0c0-107">CustomNotification Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback3-customnotification-method.md)|<span data-ttu-id="9d0c0-108">Indica che è stata generata una notifica di debugger personalizzata abilitata.</span><span class="sxs-lookup"><span data-stu-id="9d0c0-108">Indicates that an enabled custom debugger notification has been raised.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="9d0c0-109">Note</span><span class="sxs-lookup"><span data-stu-id="9d0c0-109">Remarks</span></span>  
 <span data-ttu-id="9d0c0-110">Questa interfaccia è un'estensione logica del [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) e [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) interfacce.</span><span class="sxs-lookup"><span data-stu-id="9d0c0-110">This interface is a logical extension of the [ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md) and [ICorDebugManagedCallback2](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md) interfaces.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9d0c0-111">Questa interfaccia non supporta la chiamata in modalità remota, tra computer o tra processi.</span><span class="sxs-lookup"><span data-stu-id="9d0c0-111">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9d0c0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9d0c0-112">Requirements</span></span>  
 <span data-ttu-id="9d0c0-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9d0c0-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9d0c0-114">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="9d0c0-114">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="9d0c0-115">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="9d0c0-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="9d0c0-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9d0c0-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9d0c0-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9d0c0-117">See Also</span></span>  
 [<span data-ttu-id="9d0c0-118">Interfaccia ICorDebugManagedCallback</span><span class="sxs-lookup"><span data-stu-id="9d0c0-118">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)  
 [<span data-ttu-id="9d0c0-119">Interfaccia ICorDebugManagedCallback2</span><span class="sxs-lookup"><span data-stu-id="9d0c0-119">ICorDebugManagedCallback2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-interface.md)  
 [<span data-ttu-id="9d0c0-120">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="9d0c0-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="9d0c0-121">Debug</span><span class="sxs-lookup"><span data-stu-id="9d0c0-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
