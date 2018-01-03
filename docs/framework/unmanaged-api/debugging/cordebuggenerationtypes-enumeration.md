---
title: Enumerazione CorDebugGenerationTypes
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorDebugGenerationTypes
api_location: mscordbi.dll
api_type: COM
f1_keywords: CorDebugGenerationTypes
helpviewer_keywords: CorDebugGenerationTypes enumeration [.NET Framework debugging]
ms.assetid: 9f25b64f-eedd-4ae5-8b0e-cfdfb9b6c5d8
topic_type: apiref
caps.latest.revision: "3"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c9b5126958b17ee2d1de5394ed07d78c3ffe29b5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="cordebuggenerationtypes-enumeration"></a><span data-ttu-id="b0708-102">Enumerazione CorDebugGenerationTypes</span><span class="sxs-lookup"><span data-stu-id="b0708-102">CorDebugGenerationTypes Enumeration</span></span>
<span data-ttu-id="b0708-103">Specifica la generazione di un'area di memoria nell'heap gestito.</span><span class="sxs-lookup"><span data-stu-id="b0708-103">Specifies the generation of a region of memory on the managed heap.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b0708-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b0708-104">Syntax</span></span>  
  
```  
typedef enum CorDebugGenerationTypes {  
    CorDebug_Gen0 = 0,  
    CorDebug_Gen1 = 1,  
    CorDebug_Gen2 = 2,  
    CorDebug_LOH  = 3,  
} CorDebugRegionTypes;  
```  
  
## <a name="members"></a><span data-ttu-id="b0708-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b0708-105">Members</span></span>  
  
|<span data-ttu-id="b0708-106">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="b0708-106">Member name</span></span>|<span data-ttu-id="b0708-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0708-107">Description</span></span>|  
|-----------------|-----------------|  
|`CorDebug_Gen0`|<span data-ttu-id="b0708-108">Generazione 0.</span><span class="sxs-lookup"><span data-stu-id="b0708-108">Generation 0.</span></span>|  
|`CorDebug_Gen1`|<span data-ttu-id="b0708-109">Generazione 1.</span><span class="sxs-lookup"><span data-stu-id="b0708-109">Generation 1.</span></span>|  
|`CorDebug_Gen2`|<span data-ttu-id="b0708-110">Generazione 2.</span><span class="sxs-lookup"><span data-stu-id="b0708-110">Generation 2.</span></span>|  
|`CorDebug_LOH`|<span data-ttu-id="b0708-111">L'heap oggetti grandi.</span><span class="sxs-lookup"><span data-stu-id="b0708-111">The large object heap.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="b0708-112">Note</span><span class="sxs-lookup"><span data-stu-id="b0708-112">Remarks</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="b0708-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0708-113">Requirements</span></span>  
 <span data-ttu-id="b0708-114">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b0708-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b0708-115">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="b0708-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="b0708-116">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b0708-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b0708-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b0708-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b0708-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b0708-118">See Also</span></span>  
 [<span data-ttu-id="b0708-119">Enumerazioni di debug</span><span class="sxs-lookup"><span data-stu-id="b0708-119">Debugging Enumerations</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-enumerations.md)
