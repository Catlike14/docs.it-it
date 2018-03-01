---
title: Metodo ICorPublishProcess::IsManaged
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
- ICorPublishProcess.IsManaged
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorPublishProcess::IsManaged
helpviewer_keywords:
- IsManaged method, ICorPublishProcess interface [.NET Framework debugging]
- ICorPublishProcess::IsManaged method [.NET Framework debugging]
ms.assetid: 06b1f7cc-acdf-47a6-9d53-d9dec2424152
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 21fdb09820acb6357fe1457d2f96c3319b3152a1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorpublishprocessismanaged-method"></a><span data-ttu-id="0dc66-102">Metodo ICorPublishProcess::IsManaged</span><span class="sxs-lookup"><span data-stu-id="0dc66-102">ICorPublishProcess::IsManaged Method</span></span>
<span data-ttu-id="0dc66-103">Ottiene un valore che indica se il processo a cui fa riferimento questo [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) è noto al codice gestito.</span><span class="sxs-lookup"><span data-stu-id="0dc66-103">Gets a value that indicates whether the process referenced by this [ICorPublishProcess](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md) is known to have managed code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0dc66-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0dc66-104">Syntax</span></span>  
  
```  
HRESULT IsManaged (  
    [out] BOOL   *pbManaged  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0dc66-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0dc66-105">Parameters</span></span>  
 `pbManaged`  
 <span data-ttu-id="0dc66-106">[out] Un puntatore a un valore booleano che indica se il processo con codice gestito.</span><span class="sxs-lookup"><span data-stu-id="0dc66-106">[out] A pointer to a Boolean value that indicates whether the process has managed code.</span></span> <span data-ttu-id="0dc66-107">Il valore è `true` se il processo dispone di codice gestito; in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="0dc66-107">The value is `true` if the process has managed code; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0dc66-108">Note</span><span class="sxs-lookup"><span data-stu-id="0dc66-108">Remarks</span></span>  
 <span data-ttu-id="0dc66-109">Rispetto alla versione corrente di `ICorPublishProcess` consente l'accesso solo ai processi con codice gestito, `IsManaged` restituisce sempre `true`.</span><span class="sxs-lookup"><span data-stu-id="0dc66-109">Since the current version of `ICorPublishProcess` allows access only to processes that have managed code, `IsManaged` always returns `true`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0dc66-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0dc66-110">Requirements</span></span>  
 <span data-ttu-id="0dc66-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0dc66-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0dc66-112">**Intestazione:** Corpub. idl, CorPub.h</span><span class="sxs-lookup"><span data-stu-id="0dc66-112">**Header:** CorPub.idl, CorPub.h</span></span>  
  
 <span data-ttu-id="0dc66-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0dc66-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0dc66-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0dc66-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0dc66-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0dc66-115">See Also</span></span>  
 [<span data-ttu-id="0dc66-116">Interfaccia ICorPublishProcess</span><span class="sxs-lookup"><span data-stu-id="0dc66-116">ICorPublishProcess Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icorpublishprocess-interface.md)
