---
title: Metodo ICorDebugManagedCallback::CreateThread
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback.CreateThread
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback::CreateThread method
helpviewer_keywords:
- ICorDebugManagedCallback::CreateThread method [.NET Framework debugging]
- CreateThread method [.NET Framework debugging]
ms.assetid: 6b961728-21c4-4e8d-ae81-197458be62f4
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 525ad78142d624e840cb71330556fda952b1d2d1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmanagedcallbackcreatethread-method"></a><span data-ttu-id="3c4e4-102">Metodo ICorDebugManagedCallback::CreateThread</span><span class="sxs-lookup"><span data-stu-id="3c4e4-102">ICorDebugManagedCallback::CreateThread Method</span></span>
<span data-ttu-id="3c4e4-103">Notifica al debugger che un thread ha avviato l'esecuzione di codice gestito.</span><span class="sxs-lookup"><span data-stu-id="3c4e4-103">Notifies the debugger that a thread has started executing managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3c4e4-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c4e4-104">Syntax</span></span>  
  
```  
HRESULT CreateThread (  
    [in] ICorDebugAppDomain *pAppDomain,  
    [in] ICorDebugThread    *thread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3c4e4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c4e4-105">Parameters</span></span>  
 `pAppDomain`  
 <span data-ttu-id="3c4e4-106">[in] Un puntatore a un oggetto ICorDebugAppDomain che rappresenta il dominio applicazione che contiene il thread.</span><span class="sxs-lookup"><span data-stu-id="3c4e4-106">[in] A pointer to an ICorDebugAppDomain object that represents the application domain that contains the thread.</span></span>  
  
 `thread`  
 <span data-ttu-id="3c4e4-107">[in] Un puntatore a un oggetto ICorDebugThread che rappresenta il thread.</span><span class="sxs-lookup"><span data-stu-id="3c4e4-107">[in] A pointer to an ICorDebugThread object that represents the thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3c4e4-108">Note</span><span class="sxs-lookup"><span data-stu-id="3c4e4-108">Remarks</span></span>  
 <span data-ttu-id="3c4e4-109">Il thread viene posizionato in corrispondenza dell'istruzione di codice gestito prima deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c4e4-109">The thread will be positioned at the first managed code instruction to be executed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3c4e4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c4e4-110">Requirements</span></span>  
 <span data-ttu-id="3c4e4-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="3c4e4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3c4e4-112">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="3c4e4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="3c4e4-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3c4e4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3c4e4-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3c4e4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c4e4-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c4e4-115">See Also</span></span>  
 [<span data-ttu-id="3c4e4-116">ICorDebugManagedCallback (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="3c4e4-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
