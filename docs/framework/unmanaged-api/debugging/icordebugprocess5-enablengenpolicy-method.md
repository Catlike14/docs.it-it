---
title: Metodo ICorDebugProcess5::EnableNGENPolicy
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess5::EnableNGenPolicy
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess5::EnableNGENPolicy
helpviewer_keywords:
- ICorDebugProcess5::EnableNGENPolicy method [.NET Framework debugging]
- EnableNGENPolicy method, ICorDebugProcess5 interface [.NET Framework debugging]
ms.assetid: 3b8e15ca-3c72-4685-a937-da4c739cb9e9
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: cd259308494e1a86f0a6cdec8866bb66a1614b76
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugprocess5enablengenpolicy-method"></a><span data-ttu-id="4e893-102">Metodo ICorDebugProcess5::EnableNGENPolicy</span><span class="sxs-lookup"><span data-stu-id="4e893-102">ICorDebugProcess5::EnableNGENPolicy Method</span></span>
<span data-ttu-id="4e893-103">Imposta un valore che determina come un'applicazione carica le immagini native durante l'esecuzione in un debugger gestito.</span><span class="sxs-lookup"><span data-stu-id="4e893-103">Sets a value that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4e893-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e893-104">Syntax</span></span>  
  
```  
HRESULT EnableNGENPolicy(  
    [in] CorDebugNGENPolicy ePolicy  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4e893-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e893-105">Parameters</span></span>  
 `ePolicy`  
 <span data-ttu-id="4e893-106">[in] Oggetto [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md) costante che determina come un'applicazione carica le immagini native durante l'esecuzione in un debugger gestito.</span><span class="sxs-lookup"><span data-stu-id="4e893-106">[in] A [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md) constant that determines how an application loads native images while running under a managed debugger.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4e893-107">Note</span><span class="sxs-lookup"><span data-stu-id="4e893-107">Remarks</span></span>  
 <span data-ttu-id="4e893-108">Se i criteri sono impostati correttamente, il metodo restituisce `S_OK`.</span><span class="sxs-lookup"><span data-stu-id="4e893-108">If the policy is set successfully, the method returns `S_OK`.</span></span> <span data-ttu-id="4e893-109">Se `ePolicy` è compreso nell'intervallo dei valori enumerati definiti da [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md), il metodo restituisce `E_INVALIDARG` e la chiamata al metodo non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="4e893-109">If `ePolicy` is outside the range of the enumerated values defined by [CorDebugNGenPolicy](../../../../docs/framework/unmanaged-api/debugging/cordebugngenpolicy-enumeration.md), the method returns `E_INVALIDARG` and the method call has no effect.</span></span> <span data-ttu-id="4e893-110">Se non è possibile aggiornare i criteri del generatore di immagini Native (Ngen.exe), il metodo restituisce `E_FAIL`.</span><span class="sxs-lookup"><span data-stu-id="4e893-110">If the policy of the Native Image Generator (Ngen.exe) cannot be updated, the method returns `E_FAIL`.</span></span>  
  
 <span data-ttu-id="4e893-111">Il `ICorDebugProcess5::EnableNGenPolicy` metodo può essere chiamato in qualsiasi momento durante la durata del processo.</span><span class="sxs-lookup"><span data-stu-id="4e893-111">The `ICorDebugProcess5::EnableNGenPolicy` method can be called at any time during the lifetime of the process.</span></span> <span data-ttu-id="4e893-112">I criteri sono validi per tutti i moduli caricati dopo i criteri sono impostati.</span><span class="sxs-lookup"><span data-stu-id="4e893-112">The policy is in effect for any modules that are loaded after the policy is set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4e893-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e893-113">Requirements</span></span>  
 <span data-ttu-id="4e893-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4e893-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4e893-115">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="4e893-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4e893-116">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4e893-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4e893-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4e893-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4e893-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4e893-118">See Also</span></span>  
 [<span data-ttu-id="4e893-119">ICorDebugProcess5 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="4e893-119">ICorDebugProcess5 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugprocess5-interface.md)  
 [<span data-ttu-id="4e893-120">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="4e893-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="4e893-121">Debug</span><span class="sxs-lookup"><span data-stu-id="4e893-121">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)