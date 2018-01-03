---
title: Enumerazione CorDebugCreateProcessFlags
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugCreateProcessFlags
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugCreateProcessFlags
helpviewer_keywords: CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 9e35aa2656a1e950cead94480eb06cde96e4c811
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="bad3d-102">Enumerazione CorDebugCreateProcessFlags</span><span class="sxs-lookup"><span data-stu-id="bad3d-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="bad3d-103">Fornisce opzioni di debug aggiuntive che possono essere utilizzate in una chiamata al [ICorDebug:: CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="bad3d-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="bad3d-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bad3d-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="bad3d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="bad3d-105">Members</span></span>  
  
|<span data-ttu-id="bad3d-106">Membro</span><span class="sxs-lookup"><span data-stu-id="bad3d-106">Member</span></span>|<span data-ttu-id="bad3d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bad3d-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="bad3d-108">Non vengono impostati opzioni speciali.</span><span class="sxs-lookup"><span data-stu-id="bad3d-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="bad3d-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bad3d-109">Requirements</span></span>  
 <span data-ttu-id="bad3d-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="bad3d-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="bad3d-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="bad3d-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="bad3d-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="bad3d-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="bad3d-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="bad3d-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bad3d-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bad3d-114">See Also</span></span>  
 [<span data-ttu-id="bad3d-115">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="bad3d-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
