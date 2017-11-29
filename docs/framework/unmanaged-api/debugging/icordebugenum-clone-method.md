---
title: Metodo ICorDebugEnum::Clone
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugEnum.Clone
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugEnum::Clone
helpviewer_keywords:
- Clone method, ICorDebugEnum interface [.NET Framework debugging]
- ICorDebugEnum::Clone method [.NET Framework debugging]
ms.assetid: 57eefaf3-75cf-4496-bc94-88c0706861b7
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c992410349a7bc1e16b192f564c56e0e17be4a58
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugenumclone-method"></a><span data-ttu-id="aae4d-102">Metodo ICorDebugEnum::Clone</span><span class="sxs-lookup"><span data-stu-id="aae4d-102">ICorDebugEnum::Clone Method</span></span>
<span data-ttu-id="aae4d-103">Crea una copia dell'oggetto ICorDebugEnum.</span><span class="sxs-lookup"><span data-stu-id="aae4d-103">Creates a copy of this ICorDebugEnum object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="aae4d-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aae4d-104">Syntax</span></span>  
  
```  
HRESULT Clone (  
    [out] ICorDebugEnum **ppEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="aae4d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="aae4d-105">Parameters</span></span>  
 `ppEnum`  
 <span data-ttu-id="aae4d-106">[out] Un puntatore all'indirizzo di un `ICorDebugEnum` oggetto che è una copia di questo `ICorDebugEnum` oggetto.</span><span class="sxs-lookup"><span data-stu-id="aae4d-106">[out] A pointer to the address of an `ICorDebugEnum` object that is a copy of this `ICorDebugEnum` object.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="aae4d-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aae4d-107">Requirements</span></span>  
 <span data-ttu-id="aae4d-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="aae4d-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="aae4d-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="aae4d-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="aae4d-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="aae4d-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="aae4d-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="aae4d-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
