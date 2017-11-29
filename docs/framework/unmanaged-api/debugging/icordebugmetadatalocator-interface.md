---
title: Interfaccia ICorDebugMetaDataLocator
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugMetaDataLocator
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugMetaDataLocator
helpviewer_keywords: ICorDebugMetaDataLocator interface [.NET Framework debugging]
ms.assetid: 287f5ecd-863f-4090-a615-077859f0257b
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 4611581bd2692d7c2be48adad1db3c495080e776
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugmetadatalocator-interface"></a><span data-ttu-id="b0fd2-102">Interfaccia ICorDebugMetaDataLocator</span><span class="sxs-lookup"><span data-stu-id="b0fd2-102">ICorDebugMetaDataLocator Interface</span></span>
<span data-ttu-id="b0fd2-103">Fornisce informazioni sui metadati al debugger.</span><span class="sxs-lookup"><span data-stu-id="b0fd2-103">Provides metadata information to the debugger.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="b0fd2-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="b0fd2-104">Methods</span></span>  
  
|<span data-ttu-id="b0fd2-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="b0fd2-105">Method</span></span>|<span data-ttu-id="b0fd2-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0fd2-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="b0fd2-107">GetMetaData (metodo)</span><span class="sxs-lookup"><span data-stu-id="b0fd2-107">GetMetaData Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmetadatalocator-getmetadata-method.md)|<span data-ttu-id="b0fd2-108">Chiede al debugger di restituire il percorso completo di un modulo i cui metadati sono necessari per completare un'operazione richiesta dal debugger.</span><span class="sxs-lookup"><span data-stu-id="b0fd2-108">Asks the debugger to return the full path to a module whose metadata is needed to complete an operation the debugger requested.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b0fd2-109">Note</span><span class="sxs-lookup"><span data-stu-id="b0fd2-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="b0fd2-110">Questa interfaccia non supporta la chiamata in modalità remota, tra computer o tra processi.</span><span class="sxs-lookup"><span data-stu-id="b0fd2-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0fd2-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0fd2-111">Requirements</span></span>  
 <span data-ttu-id="b0fd2-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b0fd2-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0fd2-113">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b0fd2-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b0fd2-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b0fd2-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b0fd2-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0fd2-115">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0fd2-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b0fd2-116">See Also</span></span>  
 [<span data-ttu-id="b0fd2-117">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="b0fd2-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="b0fd2-118">Debug</span><span class="sxs-lookup"><span data-stu-id="b0fd2-118">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
