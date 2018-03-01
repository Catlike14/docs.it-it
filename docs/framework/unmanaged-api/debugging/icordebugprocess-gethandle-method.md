---
title: Metodo ICorDebugProcess::GetHandle
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
- ICorDebugProcess.GetHandle
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugProcess::GetHandle
helpviewer_keywords:
- GetHandle method, ICorDebugProcess interface [.NET Framework debugging]
- ICorDebugProcess::GetHandle method [.NET Framework debugging]
ms.assetid: e7d3ecf5-09d2-4d94-abb6-ff3483deebb6
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 28065bff38fdf8c7f69920be1f7c6704dd03d69d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugprocessgethandle-method"></a><span data-ttu-id="694e4-102">Metodo ICorDebugProcess::GetHandle</span><span class="sxs-lookup"><span data-stu-id="694e4-102">ICorDebugProcess::GetHandle Method</span></span>
<span data-ttu-id="694e4-103">Ottiene un handle per il processo.</span><span class="sxs-lookup"><span data-stu-id="694e4-103">Gets a handle to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="694e4-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="694e4-104">Syntax</span></span>  
  
```  
HRESULT GetHandle([out] HPROCESS *phProcessHandle);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="694e4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="694e4-105">Parameters</span></span>  
 `phProcessHandle`  
 <span data-ttu-id="694e4-106">[out] Un puntatore a un `HPROCESS` che rappresenta l'handle del processo.</span><span class="sxs-lookup"><span data-stu-id="694e4-106">[out] A pointer to an `HPROCESS` that is the handle to the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="694e4-107">Note</span><span class="sxs-lookup"><span data-stu-id="694e4-107">Remarks</span></span>  
 <span data-ttu-id="694e4-108">L'handle recuperato è di proprietà dell'interfaccia di debug.</span><span class="sxs-lookup"><span data-stu-id="694e4-108">The retrieved handle is owned by the debugging interface.</span></span> <span data-ttu-id="694e4-109">Il debugger deve duplicare l'handle prima di utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="694e4-109">The debugger should duplicate the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="694e4-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="694e4-110">Requirements</span></span>  
 <span data-ttu-id="694e4-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="694e4-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="694e4-112">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="694e4-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="694e4-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="694e4-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="694e4-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="694e4-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
