---
title: Enumerazione CorDebugCreateProcessFlags
ms.date: 03/30/2017
api_name:
- CorDebugCreateProcessFlags
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- CorDebugCreateProcessFlags
helpviewer_keywords:
- CorDebugCreateProcessFlags enumeration [.NET Framework debugging]
ms.assetid: e709acce-6a17-4346-b38a-467dba567358
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fdc37676bfae8ac90fde0a7a5b11037b8357e25
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33403757"
---
# <a name="cordebugcreateprocessflags-enumeration"></a><span data-ttu-id="79ccc-102">Enumerazione CorDebugCreateProcessFlags</span><span class="sxs-lookup"><span data-stu-id="79ccc-102">CorDebugCreateProcessFlags Enumeration</span></span>
<span data-ttu-id="79ccc-103">Fornisce opzioni di debug aggiuntive che possono essere utilizzate in una chiamata al [ICorDebug:: CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="79ccc-103">Provides additional debugging options that can be used in a call to the [ICorDebug::CreateProcess](../../../../docs/framework/unmanaged-api/debugging/icordebug-createprocess-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79ccc-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79ccc-104">Syntax</span></span>  
  
```  
typedef enum CorDebugCreateProcessFlags {  
    DEBUG_NO_SPECIAL_OPTIONS    = 0x0000  
} CorDebugCreateProcessFlags;  
```  
  
## <a name="members"></a><span data-ttu-id="79ccc-105">Membri</span><span class="sxs-lookup"><span data-stu-id="79ccc-105">Members</span></span>  
  
|<span data-ttu-id="79ccc-106">Membro</span><span class="sxs-lookup"><span data-stu-id="79ccc-106">Member</span></span>|<span data-ttu-id="79ccc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79ccc-107">Description</span></span>|  
|------------|-----------------|  
|`DEBUG_NO_SPECIAL_OPTIONS`|<span data-ttu-id="79ccc-108">Non vengono impostati opzioni speciali.</span><span class="sxs-lookup"><span data-stu-id="79ccc-108">No special options are set.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="79ccc-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79ccc-109">Requirements</span></span>  
 <span data-ttu-id="79ccc-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79ccc-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79ccc-111">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="79ccc-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="79ccc-112">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="79ccc-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79ccc-113">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79ccc-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79ccc-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="79ccc-114">See Also</span></span>  
 [<span data-ttu-id="79ccc-115">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="79ccc-115">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
