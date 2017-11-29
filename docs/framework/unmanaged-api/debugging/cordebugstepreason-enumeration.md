---
title: Enumerazione CorDebugStepReason
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugStepReason
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugStepReason
helpviewer_keywords: CorDebugStepReason enumeration [.NET Framework debugging]
ms.assetid: fe248069-b33c-48e1-a777-06ac9b239c54
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 32892a14de820e8add38654cef92aa44930aec62
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="cordebugstepreason-enumeration"></a><span data-ttu-id="50785-102">Enumerazione CorDebugStepReason</span><span class="sxs-lookup"><span data-stu-id="50785-102">CorDebugStepReason Enumeration</span></span>
<span data-ttu-id="50785-103">Indica l'esito di una singola istruzione.</span><span class="sxs-lookup"><span data-stu-id="50785-103">Indicates the outcome of an individual step.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="50785-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50785-104">Syntax</span></span>  
  
```  
typedef enum CorDebugStepReason {  
    STEP_NORMAL,  
    STEP_RETURN,  
    STEP_CALL,  
    STEP_EXCEPTION_FILTER,  
    STEP_EXCEPTION_HANDLER,  
    STEP_INTERCEPT,  
    STEP_EXIT  
} CorDebugStepReason;  
```  
  
## <a name="members"></a><span data-ttu-id="50785-105">Membri</span><span class="sxs-lookup"><span data-stu-id="50785-105">Members</span></span>  
  
|<span data-ttu-id="50785-106">Membro</span><span class="sxs-lookup"><span data-stu-id="50785-106">Member</span></span>|<span data-ttu-id="50785-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50785-107">Description</span></span>|  
|------------|-----------------|  
|`STEP_NORMAL`|<span data-ttu-id="50785-108">In genere, l'esecuzione di istruzioni completata all'interno della stessa funzione.</span><span class="sxs-lookup"><span data-stu-id="50785-108">Stepping completed normally, within the same function.</span></span>|  
|`STEP_RETURN`|<span data-ttu-id="50785-109">L'avanzamento continua in genere, dopo la funzione ha restituito.</span><span class="sxs-lookup"><span data-stu-id="50785-109">Stepping continued normally, after the function returned.</span></span>|  
|`STEP_CALL`|<span data-ttu-id="50785-110">In genere, l'avanzamento continua all'inizio di una nuova funzione chiamata.</span><span class="sxs-lookup"><span data-stu-id="50785-110">Stepping continued normally, at the beginning of a newly called function.</span></span>|  
|`STEP_EXCEPTION_FILTER`|<span data-ttu-id="50785-111">È stata generata un'eccezione e il controllo è stato passato a un filtro eccezioni.</span><span class="sxs-lookup"><span data-stu-id="50785-111">An exception was generated and control was passed to an exception filter.</span></span>|  
|`STEP_EXCEPTION_HANDLER`|<span data-ttu-id="50785-112">È stata generata un'eccezione e il controllo è stato passato a un gestore di eccezioni.</span><span class="sxs-lookup"><span data-stu-id="50785-112">An exception was generated and control was passed to an exception handler.</span></span>|  
|`STEP_INTERCEPT`|<span data-ttu-id="50785-113">Il controllo è stato passato a un intercettore.</span><span class="sxs-lookup"><span data-stu-id="50785-113">Control was passed to an interceptor.</span></span>|  
|`STEP_EXIT`|<span data-ttu-id="50785-114">Il thread è stato chiuso prima del completamento dell'istruzione.</span><span class="sxs-lookup"><span data-stu-id="50785-114">The thread exited before the step was completed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="50785-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50785-115">Requirements</span></span>  
 <span data-ttu-id="50785-116">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="50785-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="50785-117">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="50785-117">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="50785-118">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="50785-118">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="50785-119">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="50785-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="50785-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="50785-120">See Also</span></span>  
 [<span data-ttu-id="50785-121">StepComplete (metodo)</span><span class="sxs-lookup"><span data-stu-id="50785-121">StepComplete Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-stepcomplete-method.md)  
 [<span data-ttu-id="50785-122">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="50785-122">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
