---
title: Metodo IMetaDataImport::EnumInterfaceImpls
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataImport.EnumInterfaceImpls
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataImport::EnumInterfaceImpls
helpviewer_keywords:
- IMetaDataImport::EnumInterfaceImpls method [.NET Framework metadata]
- EnumInterfaceImpls method [.NET Framework metadata]
ms.assetid: ba6e178f-128b-4e47-a13c-b4be73eb106c
topic_type: apiref
caps.latest.revision: "11"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 1d9f2883c32daafd8938bd1c80c035a3527cc6a1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataimportenuminterfaceimpls-method"></a><span data-ttu-id="ab88a-102">Metodo IMetaDataImport::EnumInterfaceImpls</span><span class="sxs-lookup"><span data-stu-id="ab88a-102">IMetaDataImport::EnumInterfaceImpls Method</span></span>
<span data-ttu-id="ab88a-103">Enumera i token MethodDef che rappresentano le implementazioni dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="ab88a-103">Enumerates MethodDef tokens representing interface implementations.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ab88a-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab88a-104">Syntax</span></span>  
  
```  
HRESULT EnumInterfaceImpls (  
   [in, out]  HCORENUM       *phEnum,   
   [in]   mdTypeDef          td,  
   [out]  mdInterfaceImpl    rImpls[],   
   [in]   ULONG              cMax,  
   [out]  ULONG*             pcImpls  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ab88a-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab88a-105">Parameters</span></span>  
 `phEnum`  
 <span data-ttu-id="ab88a-106">[in, out] Un puntatore all'enumeratore.</span><span class="sxs-lookup"><span data-stu-id="ab88a-106">[in, out] A pointer to the enumerator.</span></span>  
  
 `td`  
 <span data-ttu-id="ab88a-107">[in] Il token di TypeDef con token MethodDef che rappresentano le implementazioni di interfaccia sono da enumerare.</span><span class="sxs-lookup"><span data-stu-id="ab88a-107">[in] The token of the TypeDef whose MethodDef tokens representing interface implementations are to be enumerated.</span></span>  
  
 `rImpls`  
 <span data-ttu-id="ab88a-108">[out] Matrice utilizzata per archiviare i token MethodDef.</span><span class="sxs-lookup"><span data-stu-id="ab88a-108">[out] The array used to store the MethodDef tokens.</span></span>  
  
 `cMax`  
 <span data-ttu-id="ab88a-109">[in] Dimensione massima della matrice `rImpls`.</span><span class="sxs-lookup"><span data-stu-id="ab88a-109">[in] The maximum size of the `rImpls` array.</span></span>  
  
 `pcImpls`  
 <span data-ttu-id="ab88a-110">[out] Il numero effettivo di token restituiti in `rImpls`.</span><span class="sxs-lookup"><span data-stu-id="ab88a-110">[out] The actual number of tokens returned in `rImpls`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ab88a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab88a-111">Return Value</span></span>  
  
|<span data-ttu-id="ab88a-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="ab88a-112">HRESULT</span></span>|<span data-ttu-id="ab88a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab88a-113">Description</span></span>|  
|-------------|-----------------|  
|`S_OK`|<span data-ttu-id="ab88a-114">`EnumInterfaceImpls`stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ab88a-114">`EnumInterfaceImpls` returned successfully.</span></span>|  
|`S_FALSE`|<span data-ttu-id="ab88a-115">Non sono presenti token MethodDef da enumerare.</span><span class="sxs-lookup"><span data-stu-id="ab88a-115">There are no MethodDef tokens to enumerate.</span></span> <span data-ttu-id="ab88a-116">In tal caso, `pcImpls` è impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="ab88a-116">In that case, `pcImpls` is set to zero.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="ab88a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab88a-117">Requirements</span></span>  
 <span data-ttu-id="ab88a-118">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ab88a-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ab88a-119">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="ab88a-119">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="ab88a-120">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="ab88a-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="ab88a-121">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ab88a-121">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab88a-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ab88a-122">See Also</span></span>  
 [<span data-ttu-id="ab88a-123">IMetaDataImport (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="ab88a-123">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)  
 [<span data-ttu-id="ab88a-124">IMetaDataImport2 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="ab88a-124">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)
