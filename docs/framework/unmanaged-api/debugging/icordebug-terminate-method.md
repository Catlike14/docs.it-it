---
title: Metodo ICorDebug::Terminate
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebug.Terminate
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebug::Terminate
helpviewer_keywords:
- Terminate method, ICorDebug interface [.NET Framework debugging]
- ICorDebug::Terminate method [.NET Framework debugging]
ms.assetid: fffe5616-0896-4426-ab5e-21869b514883
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: b18bb6222296c5e8875f983d47118f938a54bcc2
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugterminate-method"></a><span data-ttu-id="954fe-102">Metodo ICorDebug::Terminate</span><span class="sxs-lookup"><span data-stu-id="954fe-102">ICorDebug::Terminate Method</span></span>
<span data-ttu-id="954fe-103">Termina il `ICorDebug` oggetto.</span><span class="sxs-lookup"><span data-stu-id="954fe-103">Terminates the `ICorDebug` object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="954fe-104">`Terminate`non deve essere chiamata finché un [ICorDebugManagedCallback::](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback è stato ricevuto per tutti i processi in corso il debug.</span><span class="sxs-lookup"><span data-stu-id="954fe-104">`Terminate` should not be called until an [ICorDebugManagedCallback::ExitProcess](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-exitprocess-method.md) callback has been received for all processes being debugged.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="954fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="954fe-105">Syntax</span></span>  
  
```  
HRESULT Terminate ();  
```  
  
## <a name="remarks"></a><span data-ttu-id="954fe-106">Note</span><span class="sxs-lookup"><span data-stu-id="954fe-106">Remarks</span></span>  
 <span data-ttu-id="954fe-107">`Terminate`deve essere chiamato quando il `ICorDebug` oggetto non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="954fe-107">`Terminate` must be called when the `ICorDebug` object is no longer needed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="954fe-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="954fe-108">Requirements</span></span>  
 <span data-ttu-id="954fe-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="954fe-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="954fe-110">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="954fe-110">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="954fe-111">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="954fe-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="954fe-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="954fe-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="954fe-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="954fe-113">See Also</span></span>  
 [<span data-ttu-id="954fe-114">Interfaccia ICorDebug</span><span class="sxs-lookup"><span data-stu-id="954fe-114">ICorDebug Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)
