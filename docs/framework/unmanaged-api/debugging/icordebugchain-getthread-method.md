---
title: Metodo ICorDebugChain::GetThread
ms.date: 03/30/2017
api_name:
- ICorDebugChain.GetThread
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugChain::GetThread
helpviewer_keywords:
- GetThread method, ICorDebugChain interface [.NET Framework debugging]
- ICorDebugChain::GetThread method [.NET Framework debugging]
ms.assetid: b3390319-6366-418c-ba80-b552ac4dfc1e
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 291c8129a790c235ee6e7f163c49c4e1e726cce5
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33402713"
---
# <a name="icordebugchaingetthread-method"></a><span data-ttu-id="d26b0-102">Metodo ICorDebugChain::GetThread</span><span class="sxs-lookup"><span data-stu-id="d26b0-102">ICorDebugChain::GetThread Method</span></span>
<span data-ttu-id="d26b0-103">Ottiene il thread fisico che questa catena di chiamate è parte di.</span><span class="sxs-lookup"><span data-stu-id="d26b0-103">Gets the physical thread this call chain is part of.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d26b0-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d26b0-104">Syntax</span></span>  
  
```  
HRESULT GetThread (  
    [out] ICorDebugThread    **ppThread  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d26b0-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d26b0-105">Parameters</span></span>  
 `ppThread`  
 <span data-ttu-id="d26b0-106">[out] Un puntatore a un oggetto ICorDebugThread che rappresenta il thread fisico questa catena di chiamate è parte di.</span><span class="sxs-lookup"><span data-stu-id="d26b0-106">[out] A pointer to an ICorDebugThread object that represents the physical thread this call chain is part of.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d26b0-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d26b0-107">Requirements</span></span>  
 <span data-ttu-id="d26b0-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d26b0-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d26b0-109">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="d26b0-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="d26b0-110">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="d26b0-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="d26b0-111">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d26b0-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
