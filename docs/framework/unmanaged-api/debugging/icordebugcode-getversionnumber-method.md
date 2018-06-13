---
title: Metodo ICorDebugCode::GetVersionNumber
ms.date: 03/30/2017
api_name:
- ICorDebugCode.GetVersionNumber
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugCode::GetVersionNumber
helpviewer_keywords:
- GetVersionNumber method, ICorDebugCode interface [.NET Framework debugging]
- ICorDebugCode::GetVersionNumber method [.NET Framework debugging]
ms.assetid: c8e02518-679f-4e9f-8a28-ba4a89a3876f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a3d4609d79bb424cabc011122480f952f0f877f1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33411234"
---
# <a name="icordebugcodegetversionnumber-method"></a><span data-ttu-id="563f7-102">Metodo ICorDebugCode::GetVersionNumber</span><span class="sxs-lookup"><span data-stu-id="563f7-102">ICorDebugCode::GetVersionNumber Method</span></span>
<span data-ttu-id="563f7-103">Ottiene il numero in base 1 che identifica la versione del codice che rappresenta "ICorDebugCode".</span><span class="sxs-lookup"><span data-stu-id="563f7-103">Gets the one-based number that identifies the version of the code that this "ICorDebugCode" represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="563f7-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="563f7-104">Syntax</span></span>  
  
```  
HRESULT GetVersionNumber (  
    [out] ULONG32    *nVersion  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="563f7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="563f7-105">Parameters</span></span>  
 `nVersion`  
 <span data-ttu-id="563f7-106">[out] Puntatore al numero di versione del codice.</span><span class="sxs-lookup"><span data-stu-id="563f7-106">[out] A pointer to the version number of the code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="563f7-107">Note</span><span class="sxs-lookup"><span data-stu-id="563f7-107">Remarks</span></span>  
 <span data-ttu-id="563f7-108">Il numero di versione viene incrementato ogni volta che modifica e continuazione (EnC) è un'operazione sul codice.</span><span class="sxs-lookup"><span data-stu-id="563f7-108">The version number is incremented each time an edit-and-continue (EnC) operation is performed on the code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="563f7-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="563f7-109">Requirements</span></span>  
 <span data-ttu-id="563f7-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="563f7-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="563f7-111">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="563f7-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="563f7-112">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="563f7-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="563f7-113">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="563f7-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="563f7-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="563f7-114">See Also</span></span>  
 
