---
title: Metodo ICorDebugProcess::GetHandle
ms.date: 03/30/2017
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
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 60bd7567f541a0bbaa3591d2f2905d13064dec3c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33423442"
---
# <a name="icordebugprocessgethandle-method"></a><span data-ttu-id="396ac-102">Metodo ICorDebugProcess::GetHandle</span><span class="sxs-lookup"><span data-stu-id="396ac-102">ICorDebugProcess::GetHandle Method</span></span>
<span data-ttu-id="396ac-103">Ottiene un handle per il processo.</span><span class="sxs-lookup"><span data-stu-id="396ac-103">Gets a handle to the process.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="396ac-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="396ac-104">Syntax</span></span>  
  
```  
HRESULT GetHandle([out] HPROCESS *phProcessHandle);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="396ac-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="396ac-105">Parameters</span></span>  
 `phProcessHandle`  
 <span data-ttu-id="396ac-106">[out] Un puntatore a un `HPROCESS` che rappresenta l'handle del processo.</span><span class="sxs-lookup"><span data-stu-id="396ac-106">[out] A pointer to an `HPROCESS` that is the handle to the process.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="396ac-107">Note</span><span class="sxs-lookup"><span data-stu-id="396ac-107">Remarks</span></span>  
 <span data-ttu-id="396ac-108">L'handle recuperato è di proprietà dell'interfaccia di debug.</span><span class="sxs-lookup"><span data-stu-id="396ac-108">The retrieved handle is owned by the debugging interface.</span></span> <span data-ttu-id="396ac-109">Il debugger deve duplicare l'handle prima di utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="396ac-109">The debugger should duplicate the handle before using it.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="396ac-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="396ac-110">Requirements</span></span>  
 <span data-ttu-id="396ac-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="396ac-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="396ac-112">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="396ac-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="396ac-113">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="396ac-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="396ac-114">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="396ac-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
