---
title: Enumerazione CorSaveSize
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorSaveSize
api_location: mscoree.dll
api_type: COM
f1_keywords: CorSaveSize
helpviewer_keywords: CorSaveSize enumeration [.NET Framework metadata]
ms.assetid: eb95ce39-5688-43c1-a34d-578794b32faa
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 3780050285f63fa7334ec5463cd22050836dc136
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="corsavesize-enumeration"></a><span data-ttu-id="76df4-102">Enumerazione CorSaveSize</span><span class="sxs-lookup"><span data-stu-id="76df4-102">CorSaveSize Enumeration</span></span>
<span data-ttu-id="76df4-103">Contiene valori che indicano il livello di precisione richiesto quando si eseguono query relative alla dimensione di un'operazione di salvataggio.</span><span class="sxs-lookup"><span data-stu-id="76df4-103">Contains values indicating the level of precision required when querying for the size of a save operation.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="76df4-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76df4-104">Syntax</span></span>  
  
```  
typedef enum CorSaveSize {  
    cssAccurate                = 0x0000,   
    cssQuick                   = 0x0001,   
    cssDiscardTransientCAs     = 0x0002  
} CorSaveSize;  
```  
  
## <a name="members"></a><span data-ttu-id="76df4-105">Membri</span><span class="sxs-lookup"><span data-stu-id="76df4-105">Members</span></span>  
  
|<span data-ttu-id="76df4-106">Membro</span><span class="sxs-lookup"><span data-stu-id="76df4-106">Member</span></span>|<span data-ttu-id="76df4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76df4-107">Description</span></span>|  
|------------|-----------------|  
|`cssAccurate`|<span data-ttu-id="76df4-108">Specifica che il valore restituito deve essere esatto.</span><span class="sxs-lookup"><span data-stu-id="76df4-108">Specifies that the return value should be exact.</span></span>|  
|`cssQuick`|<span data-ttu-id="76df4-109">Specifica che il valore restituito deve essere stimato.</span><span class="sxs-lookup"><span data-stu-id="76df4-109">Specifies that the return value should be estimated.</span></span>|  
|`cssDiscardTransientCAs`|<span data-ttu-id="76df4-110">Specifica che i tipi eliminabili devono essere rimossi.</span><span class="sxs-lookup"><span data-stu-id="76df4-110">Specifies that discardable types should be removed.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="76df4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76df4-111">Requirements</span></span>  
 <span data-ttu-id="76df4-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="76df4-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="76df4-113">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="76df4-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="76df4-114">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="76df4-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="76df4-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="76df4-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="76df4-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="76df4-116">See Also</span></span>  
 [<span data-ttu-id="76df4-117">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="76df4-117">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
