---
title: Metodo ICorDebugValue::GetSize
ms.date: 03/30/2017
api_name:
- ICorDebugValue.GetSize
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugValue::GetSize
helpviewer_keywords:
- GetSize method, ICorDebugValue interface [.NET Framework debugging]
- ICorDebugValue::GetSize method [.NET Framework debugging]
ms.assetid: 445a9ee3-e050-4f3a-931a-96b0efb00110
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 0023b8ad815b9204ed56791698c7242dfe90bec4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33421658"
---
# <a name="icordebugvaluegetsize-method"></a><span data-ttu-id="66ff7-102">Metodo ICorDebugValue::GetSize</span><span class="sxs-lookup"><span data-stu-id="66ff7-102">ICorDebugValue::GetSize Method</span></span>
<span data-ttu-id="66ff7-103">Ottiene le dimensioni, in byte, di questo oggetto "ICorDebugValue".</span><span class="sxs-lookup"><span data-stu-id="66ff7-103">Gets the size, in bytes, of this "ICorDebugValue" object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="66ff7-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66ff7-104">Syntax</span></span>  
  
```  
HRESULT GetSize (  
    [out] ULONG32   *pSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="66ff7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="66ff7-105">Parameters</span></span>  
 `pSize`  
 <span data-ttu-id="66ff7-106">[out] Le dimensioni in byte, di questo oggetto valore.</span><span class="sxs-lookup"><span data-stu-id="66ff7-106">[out] The size, in bytes, of this value object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="66ff7-107">Note</span><span class="sxs-lookup"><span data-stu-id="66ff7-107">Remarks</span></span>  
 <span data-ttu-id="66ff7-108">Se il tipo del valore è un tipo riferimento, questo metodo restituisce le dimensioni dell'indicatore di misura anziché la dimensione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="66ff7-108">If the value's type is a reference type, this method returns the size of the pointer rather than the size of the object.</span></span>  
  
 <span data-ttu-id="66ff7-109">Il `ICorDebugValue::GetSize` restituisce `COR_E_OVERFLOW` per gli oggetti che sono maggiori di 4 GB su piattaforme a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="66ff7-109">The `ICorDebugValue::GetSize` method returns `COR_E_OVERFLOW` for objects that are larger than 4 GB on 64-bit platforms.</span></span> <span data-ttu-id="66ff7-110">Utilizzare il [icordebugvalue3:: Getsize64](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) metodo invece per gli oggetti che sono maggiori di 4 GB.</span><span class="sxs-lookup"><span data-stu-id="66ff7-110">Use the [ICorDebugValue3::GetSize64](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) method instead for objects that are larger than 4 GB.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="66ff7-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66ff7-111">Requirements</span></span>  
 <span data-ttu-id="66ff7-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="66ff7-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="66ff7-113">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="66ff7-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="66ff7-114">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="66ff7-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="66ff7-115">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="66ff7-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66ff7-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="66ff7-116">See Also</span></span>  
    
 [<span data-ttu-id="66ff7-117">Metodo GetSize64</span><span class="sxs-lookup"><span data-stu-id="66ff7-117">GetSize64 Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)
