---
title: Metodo IMetaDataEmit::DeleteClassLayout
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataEmit.DeleteClassLayout
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataEmit::DeleteClassLayout
helpviewer_keywords:
- DeleteClassLayout method [.NET Framework metadata]
- IMetaDataEmit::DeleteClassLayout method [.NET Framework metadata]
ms.assetid: 65a4ad49-fa49-4b36-8ed1-76dd6a185ab4
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: a35606f85e134886addd8b30c240442800a9109e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataemitdeleteclasslayout-method"></a><span data-ttu-id="1dbae-102">Metodo IMetaDataEmit::DeleteClassLayout</span><span class="sxs-lookup"><span data-stu-id="1dbae-102">IMetaDataEmit::DeleteClassLayout Method</span></span>
<span data-ttu-id="1dbae-103">Elimina definitivamente la firma dei metadati di layout di classe per il tipo rappresentato dal token specificato.</span><span class="sxs-lookup"><span data-stu-id="1dbae-103">Destroys the class layout metadata signature for the type represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1dbae-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dbae-104">Syntax</span></span>  
  
```  
HRESULT DeleteClassLayout (  
    [in]  mdTypeDef   td  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1dbae-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dbae-105">Parameters</span></span>  
 `td`  
 <span data-ttu-id="1dbae-106">[in] Un `mdTypeDef` token di metadati che rappresenta il tipo per cui verrà eliminato il layout della classe.</span><span class="sxs-lookup"><span data-stu-id="1dbae-106">[in] An `mdTypeDef` metadata token that represents the type for which the class layout will be deleted.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="1dbae-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dbae-107">Requirements</span></span>  
 <span data-ttu-id="1dbae-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="1dbae-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="1dbae-109">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="1dbae-109">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="1dbae-110">**Libreria:** usata come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="1dbae-110">**Library:** Used as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="1dbae-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="1dbae-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1dbae-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1dbae-112">See Also</span></span>  
 [<span data-ttu-id="1dbae-113">IMetaDataEmit (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="1dbae-113">IMetaDataEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-interface.md)  
 [<span data-ttu-id="1dbae-114">Interfaccia IMetaDataEmit2</span><span class="sxs-lookup"><span data-stu-id="1dbae-114">IMetaDataEmit2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataemit2-interface.md)
