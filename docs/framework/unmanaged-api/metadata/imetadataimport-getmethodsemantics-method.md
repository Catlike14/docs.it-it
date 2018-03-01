---
title: Metodo IMetaDataImport::GetMethodSemantics
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
- IMetaDataImport.GetMethodSemantics
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::GetMethodSemantics
helpviewer_keywords:
- GetMethodSemantics method [.NET Framework metadata]
- IMetaDataImport::GetMethodSemantics method [.NET Framework metadata]
ms.assetid: 5e018eaa-d60e-4a0b-a2c5-8c36bd09d905
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8f8921c4f6a676c9647d4e8907a22f0d68b0b359
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataimportgetmethodsemantics-method"></a><span data-ttu-id="9f6d2-102">Metodo IMetaDataImport::GetMethodSemantics</span><span class="sxs-lookup"><span data-stu-id="9f6d2-102">IMetaDataImport::GetMethodSemantics Method</span></span>
<span data-ttu-id="9f6d2-103">Ottiene il token flag che indica la relazione tra il metodo a cui fa riferimento il token MethodDef specificato e l'associazione di proprietà ed evento a cui fa riferimento EventProp specificato.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-103">Gets flags indicating the relationship between the method referenced by the specified MethodDef token and the paired property and event referenced by the specified EventProp token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9f6d2-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f6d2-104">Syntax</span></span>  
  
```  
HRESULT GetMethodSemantics (  
   [in]  mdMethodDef   mb,  
   [in]  mdToken       tkEventProp,  
   [out] DWORD         *pdwSemanticsFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9f6d2-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f6d2-105">Parameters</span></span>  
 `mb`  
 <span data-ttu-id="9f6d2-106">[in] Token MethodDef che rappresenta il metodo per ottenere le informazioni sui ruoli semantica.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-106">[in] A MethodDef token representing the method to get the semantic role information for.</span></span>  
  
 `tkEventProp`  
 <span data-ttu-id="9f6d2-107">[in] Un token che rappresenta l'associazione di proprietà ed eventi per cui ottenere il ruolo del metodo.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-107">[in] A token representing the paired property and event for which to get the method's role.</span></span>  
  
 `pdwSemanticsFlags`  
 <span data-ttu-id="9f6d2-108">[out] Puntatore al flag di semantica associati.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-108">[out] A pointer to the associated semantics flags.</span></span> <span data-ttu-id="9f6d2-109">Questo valore è una maschera di bit di [CorMethodSemanticsAttr](../../../../docs/framework/unmanaged-api/metadata/cormethodsemanticsattr-enumeration.md) enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-109">This value is a bitmask from the [CorMethodSemanticsAttr](../../../../docs/framework/unmanaged-api/metadata/cormethodsemanticsattr-enumeration.md) enumeration.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9f6d2-110">Note</span><span class="sxs-lookup"><span data-stu-id="9f6d2-110">Remarks</span></span>  
 <span data-ttu-id="9f6d2-111">Il [IMetaDataEmit:: DefineProperty](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md) metodo imposta flag di semantica del metodo.</span><span class="sxs-lookup"><span data-stu-id="9f6d2-111">The [IMetaDataEmit::DefineProperty](../../../../docs/framework/unmanaged-api/metadata/imetadataemit-defineproperty-method.md) method sets a method's semantics flags.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9f6d2-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f6d2-112">Requirements</span></span>  
 <span data-ttu-id="9f6d2-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9f6d2-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9f6d2-114">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="9f6d2-114">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="9f6d2-115">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9f6d2-115">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="9f6d2-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9f6d2-116">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f6d2-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9f6d2-117">See Also</span></span>  
 [<span data-ttu-id="9f6d2-118">Interfaccia IMetaDataImport</span><span class="sxs-lookup"><span data-stu-id="9f6d2-118">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="9f6d2-119">Interfaccia IMetaDataImport2</span><span class="sxs-lookup"><span data-stu-id="9f6d2-119">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
