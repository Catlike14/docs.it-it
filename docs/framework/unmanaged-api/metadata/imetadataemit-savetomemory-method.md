---
title: Metodo IMetaDataEmit::SaveToMemory
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
- IMetaDataEmit.SaveToMemory
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataEmit::SaveToMemory
helpviewer_keywords:
- IMetaDataEmit::SaveToMemory method [.NET Framework metadata]
- SaveToMemory method [.NET Framework metadata]
ms.assetid: d5237628-2675-45ed-a39e-65c0731b6a56
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: b88034562701508369d6aadef8e92e31b2de438c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataemitsavetomemory-method"></a><span data-ttu-id="8e9aa-102">Metodo IMetaDataEmit::SaveToMemory</span><span class="sxs-lookup"><span data-stu-id="8e9aa-102">IMetaDataEmit::SaveToMemory Method</span></span>
<span data-ttu-id="8e9aa-103">Salva tutti i metadati nell'ambito corrente per l'area specificata di memoria.</span><span class="sxs-lookup"><span data-stu-id="8e9aa-103">Saves all metadata in the current scope to the specified area of memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8e9aa-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e9aa-104">Syntax</span></span>  
  
```  
HRESULT SaveToMemory (   
    [out]  void        *pbData,   
    [in]   ULONG       cbData   
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8e9aa-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e9aa-105">Parameters</span></span>  
 `pbData`  
 <span data-ttu-id="8e9aa-106">[out] L'indirizzo da cui iniziare la scrittura dei metadati.</span><span class="sxs-lookup"><span data-stu-id="8e9aa-106">[out] The address at which to begin writing metadata.</span></span>  
  
 `cbData`  
 <span data-ttu-id="8e9aa-107">[in] Le dimensioni in byte, della memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="8e9aa-107">[in] The size, in bytes, of the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8e9aa-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e9aa-108">Requirements</span></span>  
 <span data-ttu-id="8e9aa-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8e9aa-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8e9aa-110">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="8e9aa-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8e9aa-111">**Libreria:** usata come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8e9aa-111">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="8e9aa-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8e9aa-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8e9aa-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8e9aa-113">See Also</span></span>  
 [<span data-ttu-id="8e9aa-114">Interfaccia IMetaDataEmit</span><span class="sxs-lookup"><span data-stu-id="8e9aa-114">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="8e9aa-115">Interfaccia IMetaDataEmit2</span><span class="sxs-lookup"><span data-stu-id="8e9aa-115">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
