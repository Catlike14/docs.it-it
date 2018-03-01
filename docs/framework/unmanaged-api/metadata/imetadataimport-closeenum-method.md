---
title: Metodo IMetaDataImport::CloseEnum
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
- IMetaDataImport.CloseEnum
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::CloseEnum
helpviewer_keywords:
- IMetaDataImport::CloseEnum method [.NET Framework metadata]
- CloseEnum method, IMetaDataImport interface [.NET Framework metadata]
ms.assetid: 727819d5-1dab-4ebb-ac25-950b4111dc72
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 013629b5a3389fcb8da9368f7875bd1977ee9e20
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataimportcloseenum-method"></a><span data-ttu-id="8f7c6-102">Metodo IMetaDataImport::CloseEnum</span><span class="sxs-lookup"><span data-stu-id="8f7c6-102">IMetaDataImport::CloseEnum Method</span></span>
<span data-ttu-id="8f7c6-103">Chiude l'enumeratore identificata dall'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="8f7c6-103">Closes the enumerator that is identified by the specified handle.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f7c6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f7c6-104">Syntax</span></span>  
  
```  
void CloseEnum (  
   [in] HCORENUM hEnum  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8f7c6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f7c6-105">Parameters</span></span>  
 `hEnum`  
 <span data-ttu-id="8f7c6-106">[in] Handle per l'enumeratore chiudere.</span><span class="sxs-lookup"><span data-stu-id="8f7c6-106">[in] The handle for the enumerator to close.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8f7c6-107">Note</span><span class="sxs-lookup"><span data-stu-id="8f7c6-107">Remarks</span></span>  
 <span data-ttu-id="8f7c6-108">L'handle specificato dal `hEnum` viene ottenuto da un precedente `Enum` *nome* chiamata (ad esempio, [IMetaDataImport:: EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span><span class="sxs-lookup"><span data-stu-id="8f7c6-108">The handle specified by `hEnum` is obtained from a previous `Enum`*Name* call (for example, [IMetaDataImport::EnumTypeDefs](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-enumtypedefs-method.md)).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f7c6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f7c6-109">Requirements</span></span>  
 <span data-ttu-id="8f7c6-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8f7c6-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8f7c6-111">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="8f7c6-111">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="8f7c6-112">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="8f7c6-112">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="8f7c6-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8f7c6-113">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f7c6-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f7c6-114">See Also</span></span>  
 [<span data-ttu-id="8f7c6-115">Interfaccia IMetaDataImport</span><span class="sxs-lookup"><span data-stu-id="8f7c6-115">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="8f7c6-116">Interfaccia IMetaDataImport2</span><span class="sxs-lookup"><span data-stu-id="8f7c6-116">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
