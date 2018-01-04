---
title: Struttura COR_PRF_FUNCTION_ARGUMENT_RANGE
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: COR_PRF_FUNCTION_ARGUMENT_RANGE
api_location: mscorwks.dll
api_type: COM
f1_keywords: COR_PRF_FUNCTION_ARGUMENT_RANGE
helpviewer_keywords: COR_PRF_FUNCTION_ARGUMENT_RANGE structure [.NET Framework profiling'
ms.assetid: 9f469eac-ac66-419b-8668-fe705bc1a51f
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 7f61d23fc3ee3c6c8adb46c0deecdd72d155ae65
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="corprffunctionargumentrange-structure"></a><span data-ttu-id="b78ac-102">Struttura COR_PRF_FUNCTION_ARGUMENT_RANGE</span><span class="sxs-lookup"><span data-stu-id="b78ac-102">COR_PRF_FUNCTION_ARGUMENT_RANGE Structure</span></span>
<span data-ttu-id="b78ac-103">Rappresenta un blocco di argomenti della funzione archiviati in modo contiguo da sinistra a destra in memoria.</span><span class="sxs-lookup"><span data-stu-id="b78ac-103">Represents a block of function arguments stored contiguously in left-to-right order in memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b78ac-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b78ac-104">Syntax</span></span>  
  
```  
typedef struct _COR_PRF_FUNCTION_ARGUMENT_RANGE {  
    UINT_PTR startAddress;  
    ULONG length;  
} COR_PRF_FUNCTION_ARGUMENT_RANGE;  
```  
  
## <a name="members"></a><span data-ttu-id="b78ac-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b78ac-105">Members</span></span>  
  
|<span data-ttu-id="b78ac-106">Membri</span><span class="sxs-lookup"><span data-stu-id="b78ac-106">Members</span></span>|<span data-ttu-id="b78ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b78ac-107">Description</span></span>|  
|-------------|-----------------|  
|`startAddress`|<span data-ttu-id="b78ac-108">L'indirizzo iniziale del blocco.</span><span class="sxs-lookup"><span data-stu-id="b78ac-108">The starting address of the block.</span></span>|  
|`length`|<span data-ttu-id="b78ac-109">La lunghezza del blocco contiguo.</span><span class="sxs-lookup"><span data-stu-id="b78ac-109">The length of the contiguous block.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b78ac-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b78ac-110">Requirements</span></span>  
 <span data-ttu-id="b78ac-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b78ac-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b78ac-112">**Intestazione:** CorProf.idl</span><span class="sxs-lookup"><span data-stu-id="b78ac-112">**Header:** CorProf.idl</span></span>  
  
 <span data-ttu-id="b78ac-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="b78ac-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="b78ac-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b78ac-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b78ac-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b78ac-115">See Also</span></span>  
 [<span data-ttu-id="b78ac-116">Strutture di profilatura</span><span class="sxs-lookup"><span data-stu-id="b78ac-116">Profiling Structures</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-structures.md)
