---
title: Metodo IMetaDataImport::EnumTypeRefs
ms.date: 03/30/2017
api_name:
- IMetaDataImport.EnumTypeRefs
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport::EnumTypeRefs
helpviewer_keywords:
- EnumTypeRefs method [.NET Framework metadata]
- IMetaDataImport::EnumTypeRefs method [.NET Framework metadata]
ms.assetid: b4896b8f-8e97-469c-8089-e72a025661b5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b8a4fe2a65244156abe1bb0da4266f949ddd3df6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33447072"
---
# <a name="imetadataimportenumtyperefs-method"></a><span data-ttu-id="c4575-102">Metodo IMetaDataImport::EnumTypeRefs</span><span class="sxs-lookup"><span data-stu-id="c4575-102">IMetaDataImport::EnumTypeRefs Method</span></span>
<span data-ttu-id="c4575-103">Enumera i token TypeRef definiti nell'ambito dei metadati corrente.</span><span class="sxs-lookup"><span data-stu-id="c4575-103">Enumerates TypeRef tokens defined in the current metadata scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c4575-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4575-104">Syntax</span></span>  
  
```  
HRESULT EnumTypeRefs (  
   [in, out] HCORENUM    *phEnum,   
   [out] mdTypeRef       rTypeRefs[],  
   [in]  ULONG           cMax,   
   [out] ULONG           *pcTypeRefs  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c4575-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4575-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="c4575-106">[in, out] Un puntatore all'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="c4575-106">[in, out] A pointer to the enumerator.</span></span> <span data-ttu-id="c4575-107">Per la prima chiamata di questo metodo deve essere NULL.</span><span class="sxs-lookup"><span data-stu-id="c4575-107">This must be NULL for the first call of this method.</span></span>  
  
 `rTypeRefs`  
 <span data-ttu-id="c4575-108">[out] Matrice utilizzata per archiviare i token TypeRef.</span><span class="sxs-lookup"><span data-stu-id="c4575-108">[out] The array used to store the TypeRef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="c4575-109">[in] Dimensione massima della matrice `rTypeRefs`.</span><span class="sxs-lookup"><span data-stu-id="c4575-109">[in] The maximum size of the `rTypeRefs` array.</span></span>  
  
 `pcTypeRefs`  
 <span data-ttu-id="c4575-110">[out] Un puntatore al numero di token TypeRef restituiti nel `rTypeRefs`.</span><span class="sxs-lookup"><span data-stu-id="c4575-110">[out] A pointer to the number of TypeRef tokens returned in `rTypeRefs`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c4575-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4575-111">Return Value</span></span>  
  
|<span data-ttu-id="c4575-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c4575-112">HRESULT</span></span>|<span data-ttu-id="c4575-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4575-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="c4575-114">`EnumTypeRefs` stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="c4575-114">`EnumTypeRefs` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="c4575-115">Non sono presenti token da enumerare.</span><span class="sxs-lookup"><span data-stu-id="c4575-115">There are no tokens to enumerate.</span></span> <span data-ttu-id="c4575-116">In tal caso, `pcTypeRefs` è zero.</span><span class="sxs-lookup"><span data-stu-id="c4575-116">In that case, `pcTypeRefs` is zero.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c4575-117">Note</span><span class="sxs-lookup"><span data-stu-id="c4575-117">Remarks</span></span>  
 <span data-ttu-id="c4575-118">Un token TypeRef rappresenta un riferimento a un tipo.</span><span class="sxs-lookup"><span data-stu-id="c4575-118">A TypeRef token represents a reference to a type.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c4575-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4575-119">Requirements</span></span>  
 <span data-ttu-id="c4575-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c4575-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c4575-121">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="c4575-121">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="c4575-122">**Libreria:** inclusa come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="c4575-122">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="c4575-123">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c4575-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c4575-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c4575-124">See Also</span></span>  
 [<span data-ttu-id="c4575-125">Interfaccia IMetaDataImport</span><span class="sxs-lookup"><span data-stu-id="c4575-125">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="c4575-126">Interfaccia IMetaDataImport2</span><span class="sxs-lookup"><span data-stu-id="c4575-126">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
