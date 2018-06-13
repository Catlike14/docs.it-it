---
title: Metodo ICorDebugBreakpoint::Activate
ms.date: 03/30/2017
api_name:
- ICorDebugBreakpoint.Activate
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugBreakpoint::Activate
helpviewer_keywords:
- ICorDebugBreakpoint::Activate method [.NET Framework debugging]
- Activate method [.NET Framework debugging]
ms.assetid: e30c29f7-3f19-4081-b572-a731aa14cd44
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 82dad6af545464baade2b82d65e7ad4dba19fe3d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402340"
---
# <a name="icordebugbreakpointactivate-method"></a><span data-ttu-id="35ac4-102">Metodo ICorDebugBreakpoint::Activate</span><span class="sxs-lookup"><span data-stu-id="35ac4-102">ICorDebugBreakpoint::Activate Method</span></span>
<span data-ttu-id="35ac4-103">Imposta lo stato attivo di questo `ICorDebugBreakpoint`.</span><span class="sxs-lookup"><span data-stu-id="35ac4-103">Sets the active state of this `ICorDebugBreakpoint`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="35ac4-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35ac4-104">Syntax</span></span>  
  
```  
HRESULT Activate (  
    [in] BOOL bActive  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="35ac4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="35ac4-105">Parameters</span></span>  
 `bActive`  
 <span data-ttu-id="35ac4-106">[in] Impostare questo valore su `true` per specificare lo stato come attivo; in caso contrario, impostare questo valore su `false`.</span><span class="sxs-lookup"><span data-stu-id="35ac4-106">[in] Set this value to `true` to specify the state as active; otherwise, set this value to `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="35ac4-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35ac4-107">Requirements</span></span>  
 <span data-ttu-id="35ac4-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="35ac4-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="35ac4-109">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="35ac4-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="35ac4-110">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="35ac4-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="35ac4-111">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="35ac4-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
