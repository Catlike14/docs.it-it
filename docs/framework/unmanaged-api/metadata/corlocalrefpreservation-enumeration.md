---
title: Enumerazione CorLocalRefPreservation
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorLocalRefPreservation
api_location: mscoree.dll
api_type: COM
f1_keywords: CorLocalRefPreservation
helpviewer_keywords: CorLocalRefPreservation enumeration [.NET Framework metadata]
ms.assetid: 44757163-1228-4213-a4c4-d4de503cc75d
topic_type: apiref
caps.latest.revision: "5"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: eac01ce31e850eb02af84c0b84e58c1f0142242d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corlocalrefpreservation-enumeration"></a><span data-ttu-id="130ec-102">Enumerazione CorLocalRefPreservation</span><span class="sxs-lookup"><span data-stu-id="130ec-102">CorLocalRefPreservation Enumeration</span></span>
<span data-ttu-id="130ec-103">Contiene valori di flag per il trattamento dei riferimenti locali.</span><span class="sxs-lookup"><span data-stu-id="130ec-103">Contains flag values for the treatment of local references.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="130ec-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="130ec-104">Syntax</span></span>  
  
```  
typedef enum CorLocalRefPreservation  
{  
    MDPreserveLocalRefsNone     =   0x00000000,  
    MDPreserveLocalTypeRef      =   0x00000001,  
    MDPreserveLocalMemberRef    =   0x00000002  
} CorLocalRefPreservation;  
```  
  
## <a name="members"></a><span data-ttu-id="130ec-105">Membri</span><span class="sxs-lookup"><span data-stu-id="130ec-105">Members</span></span>  
  
|<span data-ttu-id="130ec-106">Membro</span><span class="sxs-lookup"><span data-stu-id="130ec-106">Member</span></span>|<span data-ttu-id="130ec-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="130ec-107">Description</span></span>|  
|------------|-----------------|  
|`MDPreserveLocalRefsNone`|<span data-ttu-id="130ec-108">Non mantenere i riferimenti locali.</span><span class="sxs-lookup"><span data-stu-id="130ec-108">Preserve no local references.</span></span>|  
|`MDPreserveLocalTypeRef`|<span data-ttu-id="130ec-109">Mantenere i riferimenti al tipo locale.</span><span class="sxs-lookup"><span data-stu-id="130ec-109">Preserve local type references.</span></span>|  
|`MDPreserveLocalMemberRef`|<span data-ttu-id="130ec-110">Mantenere i riferimenti membro locale.</span><span class="sxs-lookup"><span data-stu-id="130ec-110">Preserve local member references.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="130ec-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="130ec-111">Requirements</span></span>  
 <span data-ttu-id="130ec-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="130ec-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="130ec-113">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="130ec-113">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="130ec-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="130ec-114">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="130ec-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="130ec-115">See Also</span></span>  
 [<span data-ttu-id="130ec-116">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="130ec-116">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
