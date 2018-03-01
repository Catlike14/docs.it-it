---
title: Enumerazione CorLinkerOptions
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
- CorLinkerOptions
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorLinkerOptions
helpviewer_keywords:
- CorLinkerOptions enumeration [.NET Framework metadata]
ms.assetid: a656aad6-cc7e-4994-8251-004a6a45e18f
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 65914e52228bf55a35d48bfbf036c8bb78b29c2d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="corlinkeroptions-enumeration"></a><span data-ttu-id="d3076-102">Enumerazione CorLinkerOptions</span><span class="sxs-lookup"><span data-stu-id="d3076-102">CorLinkerOptions Enumeration</span></span>
<span data-ttu-id="d3076-103">Specifica i flag per selezionare le opzioni per il linker dei metadati.</span><span class="sxs-lookup"><span data-stu-id="d3076-103">Specifies flags to select options for the metadata linker.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d3076-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3076-104">Syntax</span></span>  
  
```  
typedef enum CorLinkerOptions {  
    MDAssembly          = 0x00000000,  
    MDNetModule         = 0x00000001,  
} CorLinkerOptions;  
```  
  
## <a name="members"></a><span data-ttu-id="d3076-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d3076-105">Members</span></span>  
  
|<span data-ttu-id="d3076-106">Membro</span><span class="sxs-lookup"><span data-stu-id="d3076-106">Member</span></span>|<span data-ttu-id="d3076-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3076-107">Description</span></span>|  
|------------|-----------------|  
|`MDAssembly`|<span data-ttu-id="d3076-108">Le funzioni globali e i tipi privati non vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="d3076-108">The private types and global functions are not preserved.</span></span>|  
|`MDNetModule`|<span data-ttu-id="d3076-109">I tipi privati e funzioni globali vengono mantenute.</span><span class="sxs-lookup"><span data-stu-id="d3076-109">The private types and global functions are preserved.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="d3076-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3076-110">Requirements</span></span>  
 <span data-ttu-id="d3076-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d3076-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d3076-112">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="d3076-112">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="d3076-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d3076-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3076-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d3076-114">See Also</span></span>  
 [<span data-ttu-id="d3076-115">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="d3076-115">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
