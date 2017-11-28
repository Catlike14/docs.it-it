---
title: Metodo ICorDebugMutableDataTarget::SetThreadContext
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 8c0d01d5-67e5-4522-9ccf-c8f3a78cb4fd
caps.latest.revision: "5"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 8c43ef5405ed582cc55af69d7f41887c0615965f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmutabledatatargetsetthreadcontext-method"></a><span data-ttu-id="b5c4c-102">Metodo ICorDebugMutableDataTarget::SetThreadContext</span><span class="sxs-lookup"><span data-stu-id="b5c4c-102">ICorDebugMutableDataTarget::SetThreadContext Method</span></span>
<span data-ttu-id="b5c4c-103">Imposta il contesto (valori del registro) per un thread.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-103">Sets the context (register values) for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b5c4c-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5c4c-104">Syntax</span></span>  
  
```  
HRESULT SetThreadContext(  
   [in] DWORD dwThreadID,  
   [in] ULONG32 contextSize,   [in, size_is(contextSize)] const BYTE * pContext);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b5c4c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5c4c-105">Parameters</span></span>  
 `dwThreadID`  
 <span data-ttu-id="b5c4c-106">[in] Identificatore del thread definito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-106">[in] The operating system-defined thread identifier.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="b5c4c-107">[in] Dimensioni del buffer `pContext` da scrivere.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-107">[in] The size of the `pContext` buffer to be written.</span></span>  
  
 `pContext`  
 <span data-ttu-id="b5c4c-108">[in] Puntatore ai byte da scrivere.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-108">[in] A pointer to the bytes to be written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b5c4c-109">Note</span><span class="sxs-lookup"><span data-stu-id="b5c4c-109">Remarks</span></span>  
 <span data-ttu-id="b5c4c-110">Il metodo `SetThreadContext` aggiorna il contesto corrente per il thread specificato dall'argomento `dwThreadID` definito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-110">The `SetThreadContext` method updates the current context for the thread specified by the operating system-defined `dwThreadID` argument.</span></span> <span data-ttu-id="b5c4c-111">Il formato del record di contesto è determinato dalla piattaforma indicata dal [ICorDebugDataTarget:: GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-111">The format of the context record is determined by the platform indicated by the [ICorDebugDataTarget::GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="b5c4c-112">In Windows, si tratta di un [contesto](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx) struttura.</span><span class="sxs-lookup"><span data-stu-id="b5c4c-112">On Windows, this is a [CONTEXT](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b5c4c-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5c4c-113">Requirements</span></span>  
 <span data-ttu-id="b5c4c-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b5c4c-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b5c4c-115">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b5c4c-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b5c4c-116">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b5c4c-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b5c4c-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b5c4c-117">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5c4c-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b5c4c-118">See Also</span></span>  
 [<span data-ttu-id="b5c4c-119">Interfaccia ICorDebugMutableDataTarget</span><span class="sxs-lookup"><span data-stu-id="b5c4c-119">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)  
 [<span data-ttu-id="b5c4c-120">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="b5c4c-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
