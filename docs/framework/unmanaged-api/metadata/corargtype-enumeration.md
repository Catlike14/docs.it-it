---
title: Enumerazione CorArgType
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
- CorArgType
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorArgType
helpviewer_keywords:
- CorArgType enumeration [.NET Framework metadata]
ms.assetid: 3c1cb268-57a0-4664-91c7-f6908ff29e32
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: dfc632849249c437769ce547b2b7facfd97333e5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="corargtype-enumeration"></a><span data-ttu-id="7cb33-102">Enumerazione CorArgType</span><span class="sxs-lookup"><span data-stu-id="7cb33-102">CorArgType Enumeration</span></span>
<span data-ttu-id="7cb33-103">Contiene valori che descrivono il tipo nativo di un handle di runtime.</span><span class="sxs-lookup"><span data-stu-id="7cb33-103">Contains values that describe the native type of a runtime handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7cb33-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cb33-104">Syntax</span></span>  
  
```  
typedef enum CorArgType {  
  
    IMAGE_CEE_CS_END        = 0x0,  
    IMAGE_CEE_CS_VOID       = 0x1,  
    IMAGE_CEE_CS_I4         = 0x2,  
    IMAGE_CEE_CS_I8         = 0x3,  
    IMAGE_CEE_CS_R4         = 0x4,  
    IMAGE_CEE_CS_R8         = 0x5,  
    IMAGE_CEE_CS_PTR        = 0x6,  
    IMAGE_CEE_CS_OBJECT     = 0x7,  
    IMAGE_CEE_CS_STRUCT4    = 0x8,  
    IMAGE_CEE_CS_STRUCT32   = 0x9,  
    IMAGE_CEE_CS_BYVALUE    = 0xA  
  
} CorArgType;  
```  
  
## <a name="requirements"></a><span data-ttu-id="7cb33-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cb33-105">Requirements</span></span>  
 <span data-ttu-id="7cb33-106">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7cb33-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7cb33-107">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="7cb33-107">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="7cb33-108">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7cb33-108">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7cb33-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7cb33-109">See Also</span></span>  
 [<span data-ttu-id="7cb33-110">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="7cb33-110">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
