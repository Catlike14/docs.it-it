---
title: Metodo ICorDebugInternalFrame2::GetFrameAddress
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugInternalFrame2.GetFrameAddress Method
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugInternalFrame2::GetFrameAddress
helpviewer_keywords:
- GetFrameAddress method [.NET Framework debugging]
- ICorDebugInternalFrame2::GetFrameAddress method [.NET Framework debugging]
ms.assetid: 4ee8d058-ffc8-4967-9133-a5adfef4e518
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 9ee867afe99fc5d2f2eb27bb1e6888aef8341d71
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebuginternalframe2getframeaddress-method"></a><span data-ttu-id="b5c5e-102">Metodo ICorDebugInternalFrame2::GetFrameAddress</span><span class="sxs-lookup"><span data-stu-id="b5c5e-102">ICorDebugInternalFrame2::GetFrameAddress Method</span></span>
<span data-ttu-id="b5c5e-103">Restituisce l'indirizzo dello stack del frame interno.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-103">Returns the stack address of the internal frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5c5e-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c5e-104">Syntax</span></span>  
  
```  
HRESULT GetFrameAddress([out] CORDB_ADDRESS *pAddress);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b5c5e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5c5e-105">Parameters</span></span>  
 `pAddress`  
 <span data-ttu-id="b5c5e-106">[out] Puntatore al `CORDB_ADDRESS` del frame interno.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-106">[out] Pointer to the `CORDB_ADDRESS` for the internal frame.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="b5c5e-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5c5e-107">Return Value</span></span>  
 <span data-ttu-id="b5c5e-108">Questo metodo restituisce gli specifici HRESULT seguenti, nonché gli errori di HRESULT che indicano la mancata riuscita del metodo.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="b5c5e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="b5c5e-109">HRESULT</span></span>|<span data-ttu-id="b5c5e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5c5e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="b5c5e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b5c5e-111">S_OK</span></span>|<span data-ttu-id="b5c5e-112">L'indirizzo del frame interno è stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-112">The address of the internal frame was successfully returned.</span></span>|  
|<span data-ttu-id="b5c5e-113">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="b5c5e-113">E_FAIL</span></span>|<span data-ttu-id="b5c5e-114">Non è stato possibile restituire l'indirizzo del frame interno.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-114">The address of the internal frame could not be returned.</span></span>|  
|<span data-ttu-id="b5c5e-115">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b5c5e-115">E_INVALIDARG</span></span>|<span data-ttu-id="b5c5e-116">`pAddress` è `null`.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-116">`pAddress` is `null`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b5c5e-117">Note</span><span class="sxs-lookup"><span data-stu-id="b5c5e-117">Remarks</span></span>  
 <span data-ttu-id="b5c5e-118">Il valore restituito in `pAddress` può essere utilizzato per determinare la posizione del frame interno relativa ad altri frame nello stack.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-118">The value returned in `pAddress` can be used to determine the location of the internal frame relative to other frames on the stack.</span></span> <span data-ttu-id="b5c5e-119">Anche nei computer basati su IA-64, frame interni risiede solo lo stack e nessun puntatore a un archivio di backup corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b5c5e-119">Even on IA-64-based computers, the internal frame lives on the stack only, and there is no corresponding pointer to a backing store.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5c5e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5c5e-120">Requirements</span></span>  
 <span data-ttu-id="b5c5e-121">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b5c5e-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5c5e-122">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b5c5e-122">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5c5e-123">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5c5e-123">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5c5e-124">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5c5e-124">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5c5e-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5c5e-125">See Also</span></span>  
 [<span data-ttu-id="b5c5e-126">ICorDebugInternalFrame2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="b5c5e-126">ICorDebugInternalFrame2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebuginternalframe2-interface.md)  
 [<span data-ttu-id="b5c5e-127">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="b5c5e-127">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="b5c5e-128">Debug</span><span class="sxs-lookup"><span data-stu-id="b5c5e-128">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
