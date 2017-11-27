---
title: Metodo IMetaDataAssemblyEmit::DefineAssembly
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataAssemblyEmit.DefineAssembly
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataAssemblyEmit::DefineAssembly
helpviewer_keywords:
- IMetaDataAssemblyEmit::DefineAssembly method [.NET Framework metadata]
- DefineAssembly method [.NET Framework metadata]
ms.assetid: a0637d66-74bf-4f2d-8137-9ff838bccece
topic_type: apiref
caps.latest.revision: "18"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 86002eb38d72ee628dbf54d0b5691f0816e6f996
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="imetadataassemblyemitdefineassembly-method"></a><span data-ttu-id="11f38-102">Metodo IMetaDataAssemblyEmit::DefineAssembly</span><span class="sxs-lookup"><span data-stu-id="11f38-102">IMetaDataAssemblyEmit::DefineAssembly Method</span></span>
<span data-ttu-id="11f38-103">Crea un `Assembly` struttura che contiene i metadati per l'assembly specificato e restituisce il token di metadati associato.</span><span class="sxs-lookup"><span data-stu-id="11f38-103">Creates an `Assembly` structure containing metadata for the specified assembly and returns the associated metadata token.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="11f38-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11f38-104">Syntax</span></span>  
  
```  
HRESULT DefineAssembly (  
    [in]  void                 *pbPublicKey,  
    [in]  ULONG                cbPublicKey,  
    [in]  ULONG                uHashAlgId,  
    [in]  LPCWSTR              szName,   
    [in]  ASSEMBLYMETADATA     *pMetaData,  
    [in]  DWORD                dwAssemblyFlags,  
    [out] mdAssembly           *pmda  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="11f38-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="11f38-105">Parameters</span></span>  
 `pbPublicKey`  
 <span data-ttu-id="11f38-106">[in] La chiave pubblica che identifica l'autore dell'assembly, o NULL se l'assembly non è sicuro.</span><span class="sxs-lookup"><span data-stu-id="11f38-106">[in] The public key that identifies the publisher of the assembly, or NULL if the assembly is not strongly named.</span></span>  
  
 `cbPublicKey`  
 <span data-ttu-id="11f38-107">[in] Le dimensioni in byte di `pbPublicKey`.</span><span class="sxs-lookup"><span data-stu-id="11f38-107">[in] The size in bytes of `pbPublicKey`.</span></span>  
  
 `uHashAlgId`  
 <span data-ttu-id="11f38-108">[in] Identificatore dell'algoritmo hash da utilizzare per crittografare i file nell'assembly, o NULL per specificare l'algoritmo SHA-1.</span><span class="sxs-lookup"><span data-stu-id="11f38-108">[in] The identifier of the hashing algorithm to use to encrypt the files in the assembly, or NULL to specify the SHA-1 algorithm.</span></span>  
  
 `szName`  
 <span data-ttu-id="11f38-109">[in] Il nome di un testo leggibile dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="11f38-109">[in] The human-readable text name of the assembly.</span></span> <span data-ttu-id="11f38-110">Questo valore non deve superare i 1024 caratteri.</span><span class="sxs-lookup"><span data-stu-id="11f38-110">This value must not exceed 1024 characters.</span></span>  
  
 `pMetaData`  
 <span data-ttu-id="11f38-111">[in] Un puntatore a un'istanza ASSEMBLYMETADATA che contiene le informazioni sulla versione, piattaforma e delle impostazioni locali per l'assembly.</span><span class="sxs-lookup"><span data-stu-id="11f38-111">[in] A pointer to an ASSEMBLYMETADATA instance that contains the version, platform, and locale information for the assembly.</span></span>  
  
 `dwAssemblyFlags`  
 <span data-ttu-id="11f38-112">[in] Una combinazione di [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) valori che descrivono le funzionalità dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="11f38-112">[in] A combination of [CorAssemblyFlags](../../../../docs/framework/unmanaged-api/metadata/corassemblyflags-enumeration.md) values that describe features of the assembly.</span></span>  
  
 `pmda`  
 <span data-ttu-id="11f38-113">[out] Puntatore al token di metadati.</span><span class="sxs-lookup"><span data-stu-id="11f38-113">[out] A pointer to the metadata token.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="11f38-114">Note</span><span class="sxs-lookup"><span data-stu-id="11f38-114">Remarks</span></span>  
 <span data-ttu-id="11f38-115">Un solo `Assembly` struttura dei metadati può essere definito all'interno di un manifesto.</span><span class="sxs-lookup"><span data-stu-id="11f38-115">Only one `Assembly` metadata structure can be defined within a manifest.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="11f38-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11f38-116">Requirements</span></span>  
 <span data-ttu-id="11f38-117">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="11f38-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="11f38-118">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="11f38-118">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="11f38-119">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="11f38-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="11f38-120">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="11f38-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11f38-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="11f38-121">See Also</span></span>  
 [<span data-ttu-id="11f38-122">Interfaccia IMetaDataAssemblyEmit</span><span class="sxs-lookup"><span data-stu-id="11f38-122">IMetaDataAssemblyEmit Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyemit-interface.md)
