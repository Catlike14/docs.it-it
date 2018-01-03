---
title: Metodo ICorDebugGenericValue::SetValue
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugGenericValue.SetValue
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugGenericValue::SetValue
helpviewer_keywords:
- ICorDebugGenericValue::SetValue method [.NET Framework debugging]
- SetValue method, ICorDebugGenericValue interface [.NET Framework debugging]
ms.assetid: ed4c6458-0435-44fc-8e78-8ba00be362f2
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 11cb4ab6d32f3dbada25fe42f062fdc2c1fabd17
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebuggenericvaluesetvalue-method"></a><span data-ttu-id="ac31e-102">Metodo ICorDebugGenericValue::SetValue</span><span class="sxs-lookup"><span data-stu-id="ac31e-102">ICorDebugGenericValue::SetValue Method</span></span>
<span data-ttu-id="ac31e-103">Copia un nuovo valore dal buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="ac31e-103">Copies a new value from the specified buffer.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ac31e-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ac31e-104">Syntax</span></span>  
  
```  
HRESULT SetValue (  
    [in] void      *pFrom  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ac31e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac31e-105">Parameters</span></span>  
 `pFrom`  
 <span data-ttu-id="ac31e-106">[in] Un puntatore al buffer da cui copiare il valore.</span><span class="sxs-lookup"><span data-stu-id="ac31e-106">[in] A pointer to the buffer from which to copy the value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ac31e-107">Note</span><span class="sxs-lookup"><span data-stu-id="ac31e-107">Remarks</span></span>  
 <span data-ttu-id="ac31e-108">Per i tipi di riferimento, il valore è il riferimento, non il contenuto.</span><span class="sxs-lookup"><span data-stu-id="ac31e-108">For reference types, the value is the reference, not the content.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ac31e-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac31e-109">Requirements</span></span>  
 <span data-ttu-id="ac31e-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ac31e-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ac31e-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="ac31e-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="ac31e-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ac31e-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ac31e-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ac31e-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
