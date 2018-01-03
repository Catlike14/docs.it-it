---
title: Metodo ICorDebugRegisterSet::SetThreadContext
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugRegisterSet.SetThreadContext
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugRegisterSet::SetThreadContext
helpviewer_keywords:
- ICorDebugRegisterSet::SetThreadContext method [.NET Framework debugging]
- SetThreadContext method, ICorDebugRegisterSet interface [.NET Framework debugging]
ms.assetid: 73afa930-32cb-4c40-81f8-83e8e6fbe213
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 1ac081cbd1fef0ca46750d8d7a74a22f23dbf0bc
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugregistersetsetthreadcontext-method"></a><span data-ttu-id="4ed7f-102">Metodo ICorDebugRegisterSet::SetThreadContext</span><span class="sxs-lookup"><span data-stu-id="4ed7f-102">ICorDebugRegisterSet::SetThreadContext Method</span></span>
<span data-ttu-id="4ed7f-103">`SetThreadContext`non è implementata in .NET Framework versione 2.0.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-103">`SetThreadContext` is not implemented in the .NET Framework version 2.0.</span></span> <span data-ttu-id="4ed7f-104">Non chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-104">Do not call this method.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4ed7f-105">Utilizzare l'operazione di livello superiore [ICorDebugNativeFrame:: SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) per impostare il contesto di un thread.</span><span class="sxs-lookup"><span data-stu-id="4ed7f-105">Use the higher-level operation [ICorDebugNativeFrame::SetIP](../../../../docs/framework/unmanaged-api/debugging/icordebugnativeframe-setip-method.md) to set the context of a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4ed7f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ed7f-106">Syntax</span></span>  
  
```  
HRESULT SetThreadContext (  
    [in] ULONG32 contextSize,  
    [in, length_is(contextSize),  
         size_is(contextSize)] BYTE context[]  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="4ed7f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ed7f-107">Requirements</span></span>  
 <span data-ttu-id="4ed7f-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4ed7f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4ed7f-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="4ed7f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4ed7f-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4ed7f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4ed7f-111">**Versioni di .NET framework:** 1.1, 1.0</span><span class="sxs-lookup"><span data-stu-id="4ed7f-111">**.NET Framework Versions:** 1.1, 1.0</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ed7f-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4ed7f-112">See Also</span></span>  
 [<span data-ttu-id="4ed7f-113">Interfaccia ICorDebugRegisterSet</span><span class="sxs-lookup"><span data-stu-id="4ed7f-113">ICorDebugRegisterSet Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset-interface.md)  
 [<span data-ttu-id="4ed7f-114">Interfaccia ICorDebugRegisterSet2</span><span class="sxs-lookup"><span data-stu-id="4ed7f-114">ICorDebugRegisterSet2 Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugregisterset2-interface.md)
