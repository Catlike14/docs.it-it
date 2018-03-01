---
title: Metodo ICorDebugModule2::ResolveAssembly
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
- ICorDebugModule2.ResolveAssembly
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugModule2::ResolveAssembly
helpviewer_keywords:
- ICorDebugModule2::ResolveAssembly method [.NET Framework debugging]
- ResolveAssembly method [.NET Framework debugging]
ms.assetid: ddf9085c-7161-44bd-9609-cd2732b9009f
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8e72d2ed69c8d189adb4980c82e07ad71892dc56
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugmodule2resolveassembly-method"></a><span data-ttu-id="e94e8-102">Metodo ICorDebugModule2::ResolveAssembly</span><span class="sxs-lookup"><span data-stu-id="e94e8-102">ICorDebugModule2::ResolveAssembly Method</span></span>
<span data-ttu-id="e94e8-103">Consente di risolvere l'assembly a cui fa riferimento il token di metadati specificato.</span><span class="sxs-lookup"><span data-stu-id="e94e8-103">Resolves the assembly referenced by the specified metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e94e8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e94e8-104">Syntax</span></span>  
  
```  
HRESULT ResolveAssembly (  
    [in]  mdToken             tkAssemblyRef,  
    [out] ICorDebugAssembly   **ppAssembly  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e94e8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e94e8-105">Parameters</span></span>  
 `tkAsemblyRef`  
 <span data-ttu-id="e94e8-106">[in] Un `mdToken` valore che fa riferimento all'assembly.</span><span class="sxs-lookup"><span data-stu-id="e94e8-106">[in] An `mdToken` value that references the assembly.</span></span>  
  
 `ppAssembly`  
 <span data-ttu-id="e94e8-107">[out] Un puntatore all'indirizzo di un oggetto ICorDebugAssembly che rappresenta l'assembly.</span><span class="sxs-lookup"><span data-stu-id="e94e8-107">[out] A pointer to the address of an ICorDebugAssembly object that represents the assembly.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e94e8-108">Note</span><span class="sxs-lookup"><span data-stu-id="e94e8-108">Remarks</span></span>  
 <span data-ttu-id="e94e8-109">Se l'assembly non è già caricato quando `ResolveAssembly` viene chiamato, un valore HRESULT restituito CORDBG_E_CANNOT_RESOLVE_ASSEMBLY.</span><span class="sxs-lookup"><span data-stu-id="e94e8-109">If the assembly is not already loaded when `ResolveAssembly` is called, an HRESULT value of CORDBG_E_CANNOT_RESOLVE_ASSEMBLY is returned.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e94e8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e94e8-110">Requirements</span></span>  
 <span data-ttu-id="e94e8-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e94e8-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e94e8-112">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="e94e8-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e94e8-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e94e8-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e94e8-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e94e8-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
