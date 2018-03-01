---
title: Metodo ICorDebugArrayValue::GetRank
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
- ICorDebugArrayValue.GetRank
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugArrayValue::GetRank
helpviewer_keywords:
- ICorDebugArrayValue::GetRank method [.NET Framework debugging]
- GetRank method, ICorDebugArrayValue interface [.NET Framework debugging]
ms.assetid: 5e83c82c-593d-4691-90b0-383d218b415e
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: b821e23b9b45932fb9296e0d4dac81d2b8c06135
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugarrayvaluegetrank-method"></a><span data-ttu-id="2faa5-102">Metodo ICorDebugArrayValue::GetRank</span><span class="sxs-lookup"><span data-stu-id="2faa5-102">ICorDebugArrayValue::GetRank Method</span></span>
<span data-ttu-id="2faa5-103">Ottiene il numero di dimensioni nella matrice.</span><span class="sxs-lookup"><span data-stu-id="2faa5-103">Gets the number of dimensions in the array.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2faa5-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2faa5-104">Syntax</span></span>  
  
```  
HRESULT GetRank (  
    [out] ULONG32   *pnRank  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="2faa5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="2faa5-105">Parameters</span></span>  
 `pnRank`  
 <span data-ttu-id="2faa5-106">[out] Un puntatore al numero di dimensioni in questo `ICorDebugArrayValue` oggetto.</span><span class="sxs-lookup"><span data-stu-id="2faa5-106">[out] A pointer to the number of dimensions in this `ICorDebugArrayValue` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="2faa5-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2faa5-107">Requirements</span></span>  
 <span data-ttu-id="2faa5-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="2faa5-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="2faa5-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="2faa5-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="2faa5-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="2faa5-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="2faa5-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="2faa5-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
