---
title: Metodo ICorDebugFrame::CreateStepper
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
- ICorDebugFrame.CreateStepper
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFrame::CreateStepper
helpviewer_keywords:
- ICorDebugFrame::CreateStepper method [.NET Framework debugging]
- CreateStepper method, ICorDebugFrame interface [.NET Framework debugging]
ms.assetid: 689e7f28-20c1-4d5c-9baa-17441cd63a88
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 93f6741a030e72406fb8099c6373896d14cb9332
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugframecreatestepper-method"></a><span data-ttu-id="28fe8-102">Metodo ICorDebugFrame::CreateStepper</span><span class="sxs-lookup"><span data-stu-id="28fe8-102">ICorDebugFrame::CreateStepper Method</span></span>
<span data-ttu-id="28fe8-103">Ottiene un gestore di istruzioni che consente al debugger di eseguire operazioni di debug passo a passo ICorDebugFrame.</span><span class="sxs-lookup"><span data-stu-id="28fe8-103">Gets a stepper that allows the debugger to perform stepping operations relative to this ICorDebugFrame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="28fe8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28fe8-104">Syntax</span></span>  
  
```  
HRESULT CreateStepper (  
    [out] ICorDebugStepper   **ppStepper  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="28fe8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="28fe8-105">Parameters</span></span>  
 `ppStepper`  
 <span data-ttu-id="28fe8-106">[out] Un puntatore all'indirizzo di un oggetto ICorDebugStepper che consente al debugger di eseguire operazioni di debug passo a passo relative al frame corrente.</span><span class="sxs-lookup"><span data-stu-id="28fe8-106">[out] A pointer to the address of an ICorDebugStepper object that allows the debugger to perform stepping operations relative to the current frame.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="28fe8-107">Note</span><span class="sxs-lookup"><span data-stu-id="28fe8-107">Remarks</span></span>  
 <span data-ttu-id="28fe8-108">Se il frame non è attivo, l'oggetto di gestore di istruzioni in genere dovrà restituire al frame prima che il completamento del passaggio.</span><span class="sxs-lookup"><span data-stu-id="28fe8-108">If the frame is not active, the stepper object will typically have to return to the frame before the step is completed.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="28fe8-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28fe8-109">Requirements</span></span>  
 <span data-ttu-id="28fe8-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="28fe8-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="28fe8-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="28fe8-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="28fe8-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="28fe8-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="28fe8-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="28fe8-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
