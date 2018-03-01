---
title: Interfaccia ICorDebugExceptionObjectValue
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
- ICorDebugExceptionObjectValue
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugExceptionObjectValue
helpviewer_keywords:
- ICorDebugExceptionObjectValue interface [.NET Framework debugging]
ms.assetid: 43416dd5-8892-4106-9f59-f9143b19ddb4
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e6ee743a5e3e28b5d8b864f325239725ca6c0042
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugexceptionobjectvalue-interface"></a><span data-ttu-id="57d1f-102">Interfaccia ICorDebugExceptionObjectValue</span><span class="sxs-lookup"><span data-stu-id="57d1f-102">ICorDebugExceptionObjectValue Interface</span></span>
<span data-ttu-id="57d1f-103">Estende l'interfaccia "ICorDebugObjectValue" per fornire informazioni sull'analisi dello stack da un oggetto eccezione gestito.</span><span class="sxs-lookup"><span data-stu-id="57d1f-103">Extends the "ICorDebugObjectValue" interface to provide stack trace information from a managed exception object.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="57d1f-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="57d1f-104">Methods</span></span>  
  
|<span data-ttu-id="57d1f-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="57d1f-105">Method</span></span>|<span data-ttu-id="57d1f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57d1f-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="57d1f-107">Metodo EnumerateExceptionCallStack</span><span class="sxs-lookup"><span data-stu-id="57d1f-107">EnumerateExceptionCallStack Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugexceptionobjectvalue-enumerateexceptioncallstack-method.md)|<span data-ttu-id="57d1f-108">Ottiene un enumeratore per lo stack di chiamate incorporato in un oggetto eccezione.</span><span class="sxs-lookup"><span data-stu-id="57d1f-108">Gets an enumerator to the call stack embedded in an exception object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="57d1f-109">Note</span><span class="sxs-lookup"><span data-stu-id="57d1f-109">Remarks</span></span>  
 <span data-ttu-id="57d1f-110">La chiamata a `QueryInterface` avrà esito positivo per gli oggetti gestiti che derivano da <xref:System.Exception?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="57d1f-110">The call to `QueryInterface` will succeed for managed objects that derive from <xref:System.Exception?displayProperty=nameWithType>.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="57d1f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57d1f-111">Requirements</span></span>  
 <span data-ttu-id="57d1f-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="57d1f-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="57d1f-113">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="57d1f-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="57d1f-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="57d1f-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="57d1f-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="57d1f-115">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57d1f-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="57d1f-116">See Also</span></span>  
 [<span data-ttu-id="57d1f-117">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="57d1f-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="57d1f-118">Debug</span><span class="sxs-lookup"><span data-stu-id="57d1f-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)  
 
