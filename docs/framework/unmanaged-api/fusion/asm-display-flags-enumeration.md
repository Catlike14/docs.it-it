---
title: Enumerazione ASM_DISPLAY_FLAGS
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ASM_DISPLAY_FLAGS
api_location: fusion.dll
api_type: COM
f1_keywords: ASM_DISPLAY_FLAGS
helpviewer_keywords: ASM_DISPLAY_FLAGS enumeration [.NET Framework fusion]
ms.assetid: dbade6c9-9d26-4a79-9fd2-46108edd12d7
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5e9fcd6cc8c1a352567f635e848d49e322a35ea6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="asmdisplayflags-enumeration"></a><span data-ttu-id="4c3d2-102">Enumerazione ASM_DISPLAY_FLAGS</span><span class="sxs-lookup"><span data-stu-id="4c3d2-102">ASM_DISPLAY_FLAGS Enumeration</span></span>
<span data-ttu-id="4c3d2-103">Indica la versione, compilazione, le impostazioni cultura, firma e così via, dell'assembly il cui nome visualizzato verrà recuperato dal [IAssemblyName:: GetDisplayName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="4c3d2-103">Indicates the version, build, culture, signature, and so on, of the assembly whose display name will be retrieved by the [IAssemblyName::GetDisplayName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-getdisplayname-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4c3d2-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c3d2-104">Syntax</span></span>  
  
```  
typedef enum {  
  
    ASM_DISPLAYF_VERSION                 = 0x01,  
    ASM_DISPLAYF_CULTURE                 = 0x02,  
    ASM_DISPLAYF_PUBLIC_KEY_TOKEN        = 0x04,  
    ASM_DISPLAYF_PUBLIC_KEY              = 0x08,  
    ASM_DISPLAYF_CUSTOM                  = 0x10,  
    ASM_DISPLAYF_PROCESSORARCHITECTURE   = 0x20,  
    ASM_DISPLAYF_LANGUAGEID              = 0x40,  
    ASM_DISPLAYF_RETARGET                = 0x80,  
    ASM_DISPLAYF_CONFIG_MASK             = 0x100,  
    ASM_DISPLAYF_MVID                    = 0x200,  
    ASM_DISPLAYF_FULL                    =   
                      ASM_DISPLAYF_VERSION           |   
                      ASM_DISPLAYF_CULTURE           |   
                      ASM_DISPLAYF_PUBLIC_KEY_TOKEN  |   
                      ASM_DISPLAYF_RETARGET          |   
                      ASM_DISPLAYF_PROCESSORARCHITECTURE  
  
} ASM_DISPLAY_FLAGS;  
```  
  
## <a name="remarks"></a><span data-ttu-id="4c3d2-105">Note</span><span class="sxs-lookup"><span data-stu-id="4c3d2-105">Remarks</span></span>  
 <span data-ttu-id="4c3d2-106">`ASM_DISPLAYF_FULL`riflette le modifiche apportate alla versione di [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) oggetto.</span><span class="sxs-lookup"><span data-stu-id="4c3d2-106">`ASM_DISPLAYF_FULL` reflects any changes made to the version of the [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object.</span></span> <span data-ttu-id="4c3d2-107">Non presupporre che il valore restituito non è modificabile.</span><span class="sxs-lookup"><span data-stu-id="4c3d2-107">Do not assume that the returned value is immutable.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4c3d2-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c3d2-108">Requirements</span></span>  
 <span data-ttu-id="4c3d2-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4c3d2-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4c3d2-110">**Intestazione:** Fusion. h</span><span class="sxs-lookup"><span data-stu-id="4c3d2-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="4c3d2-111">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="4c3d2-111">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="4c3d2-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4c3d2-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4c3d2-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4c3d2-113">See Also</span></span>  
 [<span data-ttu-id="4c3d2-114">IAssemblyName (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="4c3d2-114">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="4c3d2-115">Enumerazioni Fusion</span><span class="sxs-lookup"><span data-stu-id="4c3d2-115">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
