---
title: Metodo ICLRStrongName::StrongNameTokenFromPublicKey
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
- ICLRStrongName.StrongNameTokenFromPublicKey
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey
helpviewer_keywords:
- ICLRStrongName::StrongNameTokenFromPublicKey method [.NET Framework hosting]
- StrongNameTokenFromPublicKey method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 7962ce88-7e86-4a6f-8298-621b01ffc3c2
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: b5ee9153cec51f279e08b0ac0838456645cd7ada
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iclrstrongnamestrongnametokenfrompublickey-method"></a><span data-ttu-id="4093c-102">Metodo ICLRStrongName::StrongNameTokenFromPublicKey</span><span class="sxs-lookup"><span data-stu-id="4093c-102">ICLRStrongName::StrongNameTokenFromPublicKey Method</span></span>
<span data-ttu-id="4093c-103">Ottiene un token che rappresenta una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="4093c-103">Gets a token that represents a public key.</span></span> <span data-ttu-id="4093c-104">Un token con nome sicuro è la forma abbreviata di una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="4093c-104">A strong name token is the shortened form of a public key.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4093c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4093c-105">Syntax</span></span>  
  
```  
HRESULT StrongNameTokenFromPublicKey (   
    [in]  BYTE    *pbPublicKeyBlob,  
    [in]  ULONG   cbPublicKeyBlob,  
    [out] BYTE    **ppbStrongNameToken,  
    [out] ULONG   *pcbStrongNameToken  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4093c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4093c-106">Parameters</span></span>  
 `pbPublicKeyBlob`  
 <span data-ttu-id="4093c-107">[in] Una struttura di tipo [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) che contiene la parte pubblica della coppia di chiavi usata per generare la firma nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="4093c-107">[in] A structure of type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="4093c-108">[in] Le dimensioni, in byte, di `pbPublicKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="4093c-108">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="4093c-109">[out] Il token con nome sicuro corrispondente alla chiave passata `pbPublicKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="4093c-109">[out] The strong name token corresponding to the key passed in `pbPublicKeyBlob`.</span></span> <span data-ttu-id="4093c-110">Common language runtime alloca la memoria nel quale restituire il token.</span><span class="sxs-lookup"><span data-stu-id="4093c-110">The common language runtime allocates the memory in which to return the token.</span></span> <span data-ttu-id="4093c-111">Il chiamante deve liberare la memoria utilizzando il [ICLRStrongName:: StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="4093c-111">The caller must free this memory by using the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="4093c-112">[out] Le dimensioni in byte, del token restituito con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="4093c-112">[out] The size, in bytes, of the returned strong name token.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4093c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4093c-113">Return Value</span></span>  
 <span data-ttu-id="4093c-114">`S_OK`Se il metodo viene completato correttamente. in caso contrario, un valore HRESULT indicante un errore (vedere [valori HRESULT comuni](http://go.microsoft.com/fwlink/?LinkId=213878) per un elenco).</span><span class="sxs-lookup"><span data-stu-id="4093c-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4093c-115">Note</span><span class="sxs-lookup"><span data-stu-id="4093c-115">Remarks</span></span>  
 <span data-ttu-id="4093c-116">Un token con nome sicuro è la forma abbreviata di una chiave pubblica utilizzata per risparmiare spazio quando si archiviano le informazioni sulla chiave nei metadati.</span><span class="sxs-lookup"><span data-stu-id="4093c-116">A strong name token is the shortened form of a public key that is used to save space when storing key information in metadata.</span></span> <span data-ttu-id="4093c-117">In particolare, vengono utilizzati i token con nome sicuro nei riferimenti ad assembly per fare riferimento all'assembly dipendenti.</span><span class="sxs-lookup"><span data-stu-id="4093c-117">Specifically, strong name tokens are used in assembly references to refer to the dependent assembly.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4093c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4093c-118">Requirements</span></span>  
 <span data-ttu-id="4093c-119">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4093c-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4093c-120">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="4093c-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="4093c-121">**Libreria:** inclusa come risorsa in mscoree.dll</span><span class="sxs-lookup"><span data-stu-id="4093c-121">**Library:** Included as a resource in mscoree.dll</span></span>  
  
 <span data-ttu-id="4093c-122">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4093c-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4093c-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4093c-123">See Also</span></span>  
 [<span data-ttu-id="4093c-124">Metodo StrongNameGetPublicKey</span><span class="sxs-lookup"><span data-stu-id="4093c-124">StrongNameGetPublicKey Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetpublickey-method.md)  
 [<span data-ttu-id="4093c-125">Struttura PublicKeyBlob</span><span class="sxs-lookup"><span data-stu-id="4093c-125">PublicKeyBlob Structure</span></span>](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md)  
 [<span data-ttu-id="4093c-126">Interfaccia ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="4093c-126">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
