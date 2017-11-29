---
title: Metodo IMetaDataImport::EnumMembers
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.EnumMembers
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::EnumMembers
helpviewer_keywords:
- IMetaDataImport::EnumMembers method [.NET Framework metadata]
- EnumMembers method [.NET Framework metadata]
ms.assetid: 3fb8e178-342b-4c89-9bcf-f7f834e6cb77
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: cc17437c18dd7a2cdc2fdabdc714b12f8d91cc7a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportenummembers-method"></a><span data-ttu-id="d0c06-102">Metodo IMetaDataImport::EnumMembers</span><span class="sxs-lookup"><span data-stu-id="d0c06-102">IMetaDataImport::EnumMembers Method</span></span>
<span data-ttu-id="d0c06-103">Enumera i token MemberDef che rappresentano i membri del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="d0c06-103">Enumerates MemberDef tokens representing members of the specified type.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d0c06-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0c06-104">Syntax</span></span>  
  
```  
HRESULT EnumMembers (   
   [in, out]  HCORENUM    *phEnum,   
   [in]  mdTypeDef   cl,   
   [out] mdToken     rMembers[],   
   [in]  ULONG       cMax,   
   [out] ULONG       *pcTokens  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d0c06-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0c06-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="d0c06-106">[in, out] Un puntatore all'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="d0c06-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `cl`  
 <span data-ttu-id="d0c06-107">[in] Token TypeDef che rappresenta il tipo i cui membri sono da enumerare.</span><span class="sxs-lookup"><span data-stu-id="d0c06-107">[in] A TypeDef token representing the type whose members are to be enumerated.</span></span>  
  
 `rMembers`  
 <span data-ttu-id="d0c06-108">[out] Matrice utilizzata per contenere i token MemberDef.</span><span class="sxs-lookup"><span data-stu-id="d0c06-108">[out] The array used to hold the MemberDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="d0c06-109">[in] Dimensione massima della matrice `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="d0c06-109">[in] The maximum size of the `rMembers` array.</span></span>  
  
 `pcTokens`  
 <span data-ttu-id="d0c06-110">[out] Il numero effettivo di token MemberDef restituiti in `rMembers`.</span><span class="sxs-lookup"><span data-stu-id="d0c06-110">[out] The actual number of MemberDef tokens returned in `rMembers`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d0c06-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0c06-111">Return Value</span></span>  
  
|<span data-ttu-id="d0c06-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0c06-112">HRESULT</span></span>|<span data-ttu-id="d0c06-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0c06-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="d0c06-114">`EnumMembers`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="d0c06-114">`EnumMembers` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="d0c06-115">Non sono presenti token MemberDef da enumerare.</span><span class="sxs-lookup"><span data-stu-id="d0c06-115">There are no MemberDef tokens to enumerate.</span></span> <span data-ttu-id="d0c06-116">In tal caso, `pcTokens` è zero.</span><span class="sxs-lookup"><span data-stu-id="d0c06-116">In that case, `pcTokens` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d0c06-117">Note</span><span class="sxs-lookup"><span data-stu-id="d0c06-117">Remarks</span></span>  
 <span data-ttu-id="d0c06-118">Durante l'enumerazione di raccolte di membri per una classe, `EnumMembers` restituisce solo i membri definiti direttamente sulla classe.</span><span class="sxs-lookup"><span data-stu-id="d0c06-118">When enumerating collections of members for a class, `EnumMembers` returns only members defined directly on the class.</span></span> <span data-ttu-id="d0c06-119">Non restituisce i membri che eredita la classe, anche se la classe fornisce un'implementazione per i membri ereditati.</span><span class="sxs-lookup"><span data-stu-id="d0c06-119">It does not return any members that the class inherits, even if the class provides an implementation for those inherited members.</span></span> <span data-ttu-id="d0c06-120">Per enumerare i membri ereditati, il chiamante deve verificare in modo esplicito la catena di ereditarietà.</span><span class="sxs-lookup"><span data-stu-id="d0c06-120">To enumerate inherited members, the caller must explicitly walk the inheritance chain.</span></span> <span data-ttu-id="d0c06-121">Si noti che le regole per la catena di ereditarietà possono variare a seconda del linguaggio o del compilatore che ha creato i metadati originali.</span><span class="sxs-lookup"><span data-stu-id="d0c06-121">Note that the rules for the inheritance chain may vary depending on the language or compiler that emitted the original metadata.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d0c06-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0c06-122">Requirements</span></span>  
 <span data-ttu-id="d0c06-123">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d0c06-123">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d0c06-124">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="d0c06-124">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="d0c06-125">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="d0c06-125">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="d0c06-126">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d0c06-126">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d0c06-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d0c06-127">See Also</span></span>  
 [<span data-ttu-id="d0c06-128">IMetaDataImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="d0c06-128">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="d0c06-129">IMetaDataImport2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="d0c06-129">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
