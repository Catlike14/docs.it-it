---
title: Metodo ICorDebugMutableDataTarget::SetThreadContext
ms.date: 03/30/2017
ms.assetid: 8c0d01d5-67e5-4522-9ccf-c8f3a78cb4fd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 05f0c0d23b4885f2d6fd351fdf845a25c899228e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418418"
---
# <a name="icordebugmutabledatatargetsetthreadcontext-method"></a><span data-ttu-id="b17fa-102">Metodo ICorDebugMutableDataTarget::SetThreadContext</span><span class="sxs-lookup"><span data-stu-id="b17fa-102">ICorDebugMutableDataTarget::SetThreadContext Method</span></span>
<span data-ttu-id="b17fa-103">Imposta il contesto (valori del registro) per un thread.</span><span class="sxs-lookup"><span data-stu-id="b17fa-103">Sets the context (register values) for a thread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b17fa-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b17fa-104">Syntax</span></span>  
  
```  
HRESULT SetThreadContext(  
   [in] DWORD dwThreadID,  
   [in] ULONG32 contextSize,   [in, size_is(contextSize)] const BYTE * pContext);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b17fa-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b17fa-105">Parameters</span></span>  
 `dwThreadID`  
 <span data-ttu-id="b17fa-106">[in] Identificatore del thread definito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b17fa-106">[in] The operating system-defined thread identifier.</span></span>  
  
 `contextSize`  
 <span data-ttu-id="b17fa-107">[in] Dimensioni del buffer `pContext` da scrivere.</span><span class="sxs-lookup"><span data-stu-id="b17fa-107">[in] The size of the `pContext` buffer to be written.</span></span>  
  
 `pContext`  
 <span data-ttu-id="b17fa-108">[in] Puntatore ai byte da scrivere.</span><span class="sxs-lookup"><span data-stu-id="b17fa-108">[in] A pointer to the bytes to be written.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b17fa-109">Note</span><span class="sxs-lookup"><span data-stu-id="b17fa-109">Remarks</span></span>  
 <span data-ttu-id="b17fa-110">Il metodo `SetThreadContext` aggiorna il contesto corrente per il thread specificato dall'argomento `dwThreadID` definito dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b17fa-110">The `SetThreadContext` method updates the current context for the thread specified by the operating system-defined `dwThreadID` argument.</span></span> <span data-ttu-id="b17fa-111">Il formato del record di contesto è determinato dalla piattaforma indicata dal [ICorDebugDataTarget:: GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="b17fa-111">The format of the context record is determined by the platform indicated by the [ICorDebugDataTarget::GetPlatform](../../../../docs/framework/unmanaged-api/debugging/icordebugdatatarget-getplatform-method.md) method.</span></span> <span data-ttu-id="b17fa-112">In Windows, si tratta di un [contesto](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx) struttura.</span><span class="sxs-lookup"><span data-stu-id="b17fa-112">On Windows, this is a [CONTEXT](http://msdn.microsoft.com/library/windows/desktop/ms679284.aspx) structure.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b17fa-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b17fa-113">Requirements</span></span>  
 <span data-ttu-id="b17fa-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b17fa-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b17fa-115">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b17fa-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b17fa-116">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="b17fa-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b17fa-117">**Versioni di .NET framework:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b17fa-117">**.NET Framework Versions:** [!INCLUDE[net_current_v46plus](../../../../includes/net-current-v46plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b17fa-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b17fa-118">See Also</span></span>  
 [<span data-ttu-id="b17fa-119">Interfaccia ICorDebugMutableDataTarget</span><span class="sxs-lookup"><span data-stu-id="b17fa-119">ICorDebugMutableDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmutabledatatarget-interface.md)  
 [<span data-ttu-id="b17fa-120">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="b17fa-120">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
