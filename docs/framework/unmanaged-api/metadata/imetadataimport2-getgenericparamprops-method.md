---
title: Metodo IMetaDataImport2::GetGenericParamProps
ms.date: 03/30/2017
api_name:
- IMetaDataImport2.GetGenericParamProps
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IMetaDataImport2::GetGenericParamProps
helpviewer_keywords:
- IMetaDataImport2::GetGenericParamProps method [.NET Framework metadata]
- GetGenericParamProps method [.NET Framework metadata]
ms.assetid: dbb21e67-712b-49e7-a27c-a1e73ffd46c5
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: b9ded6b4e0ac8f3e70fd0145ab6e2410c3b38e02
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33448674"
---
# <a name="imetadataimport2getgenericparamprops-method"></a><span data-ttu-id="162b3-102">Metodo IMetaDataImport2::GetGenericParamProps</span><span class="sxs-lookup"><span data-stu-id="162b3-102">IMetaDataImport2::GetGenericParamProps Method</span></span>
<span data-ttu-id="162b3-103">Ottiene i metadati associati al parametro generico rappresentato dal token specificato.</span><span class="sxs-lookup"><span data-stu-id="162b3-103">Gets the metadata associated with the generic parameter represented by the specified token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="162b3-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="162b3-104">Syntax</span></span>  
  
```  
HRESULT GetGenericParamProps (  
   [in]  mdGenericParam  gp,  
   [out] ULONG           *pulParamSeq,  
   [out] DWORD           *pdwParamFlags,  
   [out] mdToken         *ptOwner,  
   [out] DWORD           *reserved,  
   [out] LPWSTR          wzName,  
   [in]  ULONG           cchName,  
   [out] ULONG           *pchName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="162b3-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="162b3-105">Parameters</span></span>  
 `gp`  
 <span data-ttu-id="162b3-106">[in] Token che rappresenta il parametro generico per il quale restituire i metadati.</span><span class="sxs-lookup"><span data-stu-id="162b3-106">[in] The token that represents the generic parameter for which to return metadata.</span></span>  
  
 `pulParamSeq`  
 <span data-ttu-id="162b3-107">[out] La posizione ordinale del `Type` parametro nel metodo o nel costruttore padre.</span><span class="sxs-lookup"><span data-stu-id="162b3-107">[out] The ordinal position of the `Type` parameter in the parent constructor or method.</span></span>  
  
 `pdwParamFlags`  
 <span data-ttu-id="162b3-108">[out] Il valore di [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumerazione che descrive il `Type` per il parametro generico.</span><span class="sxs-lookup"><span data-stu-id="162b3-108">[out] A value of the [CorGenericParamAttr](../../../../docs/framework/unmanaged-api/metadata/corgenericparamattr-enumeration.md) enumeration that describes the `Type` for the generic parameter.</span></span>  
  
 `ptOwner`  
 <span data-ttu-id="162b3-109">[out] Token TypeDef o MethodDef che rappresenta il proprietario del parametro.</span><span class="sxs-lookup"><span data-stu-id="162b3-109">[out] A TypeDef or MethodDef token that represents the owner of the parameter.</span></span>  
  
 `reserved`  
 <span data-ttu-id="162b3-110">[out] Riservato per l'estensibilità futura.</span><span class="sxs-lookup"><span data-stu-id="162b3-110">[out] Reserved for future extensibility.</span></span>  
  
 `wzName`  
 <span data-ttu-id="162b3-111">[out] Il nome del parametro generico.</span><span class="sxs-lookup"><span data-stu-id="162b3-111">[out] The name of the generic parameter.</span></span>  
  
 `cchName`  
 <span data-ttu-id="162b3-112">[in] Le dimensioni del `wzName` buffer.</span><span class="sxs-lookup"><span data-stu-id="162b3-112">[in] The size of the `wzName` buffer.</span></span>  
  
 `pchName`  
 <span data-ttu-id="162b3-113">[out] Le dimensioni restituite del nome, in caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="162b3-113">[out] The returned size of the name, in wide characters.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="162b3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="162b3-114">Requirements</span></span>  
 <span data-ttu-id="162b3-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="162b3-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="162b3-116">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="162b3-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="162b3-117">**Libreria:** usata come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="162b3-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="162b3-118">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="162b3-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="162b3-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="162b3-119">See Also</span></span>  
 [<span data-ttu-id="162b3-120">Interfaccia IMetaDataImport2</span><span class="sxs-lookup"><span data-stu-id="162b3-120">IMetaDataImport2 Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport2-interface.md)  
 [<span data-ttu-id="162b3-121">Interfaccia IMetaDataImport</span><span class="sxs-lookup"><span data-stu-id="162b3-121">IMetaDataImport Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataimport-interface.md)
