---
title: Metodo ICLRStrongName::StrongNameTokenFromAssemblyEx
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
- ICLRStrongName.StrongNameTokenFromAssemblyEx
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::StrongNameTokenFromAssemblyEx
helpviewer_keywords:
- StrongNameTokenFromAssemblyEx method, ICLRStrongName interface [.NET Framework hosting]
- ICLRStrongName::StrongNameTokenFromAssemblyEx method [.NET Framework hosting]
ms.assetid: 648ea90e-5e60-40a0-a56a-3e61bf2fba7c
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 5b8b3437d8c07cd57a4791995890cab1b06aafc6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iclrstrongnamestrongnametokenfromassemblyex-method"></a><span data-ttu-id="09ee4-102">Metodo ICLRStrongName::StrongNameTokenFromAssemblyEx</span><span class="sxs-lookup"><span data-stu-id="09ee4-102">ICLRStrongName::StrongNameTokenFromAssemblyEx Method</span></span>
<span data-ttu-id="09ee4-103">Crea un token con nome sicuro dal file di assembly specificato e restituisce la chiave pubblica che rappresenta il token.</span><span class="sxs-lookup"><span data-stu-id="09ee4-103">Creates a strong name token from the specified assembly file, and returns the public key that the token represents.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="09ee4-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="09ee4-104">Syntax</span></span>  
  
```  
HRESULT StrongNameTokenFromAssemblyEx (  
    [in]  LPCWSTR   wszFilePath,  
    [out] BYTE      **ppbStrongNameToken,  
    [out] ULONG     *pcbStrongNameToken,  
    [out] BYTE      **ppbPublicKeyBlob,  
    [out] ULONG     *pcbPublicKeyBlob  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="09ee4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="09ee4-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="09ee4-106">[in] Il percorso del file eseguibile portabile (PE) per l'assembly.</span><span class="sxs-lookup"><span data-stu-id="09ee4-106">[in] The path to the portable executable (PE) file for the assembly.</span></span>  
  
 `ppbStrongNameToken`  
 <span data-ttu-id="09ee4-107">[out] Il token restituito con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="09ee4-107">[out] The returned strong name token.</span></span>  
  
 `pcbStrongNameToken`  
 <span data-ttu-id="09ee4-108">[out] Le dimensioni in byte, del token con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="09ee4-108">[out] The size, in bytes, of the strong name token.</span></span>  
  
 `ppbPublicKeyBlob`  
 <span data-ttu-id="09ee4-109">[out] La chiave pubblica restituita.</span><span class="sxs-lookup"><span data-stu-id="09ee4-109">[out] The returned public key.</span></span>  
  
 `pcbPublicKeyBlob`  
 <span data-ttu-id="09ee4-110">[out] Le dimensioni in byte, della chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="09ee4-110">[out] The size, in bytes, of the public key.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="09ee4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="09ee4-111">Return Value</span></span>  
 <span data-ttu-id="09ee4-112">`S_OK`Se il metodo viene completato correttamente. in caso contrario, un valore HRESULT indicante un errore (vedere [valori HRESULT comuni](http://go.microsoft.com/fwlink/?LinkId=213878) per un elenco).</span><span class="sxs-lookup"><span data-stu-id="09ee4-112">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="09ee4-113">Note</span><span class="sxs-lookup"><span data-stu-id="09ee4-113">Remarks</span></span>  
 <span data-ttu-id="09ee4-114">Un token con nome sicuro è la forma abbreviata di una chiave pubblica.</span><span class="sxs-lookup"><span data-stu-id="09ee4-114">A strong name token is the shortened form of a public key.</span></span> <span data-ttu-id="09ee4-115">Il token è un hash a 64 bit che viene creato dalla chiave pubblica utilizzata per firmare l'assembly.</span><span class="sxs-lookup"><span data-stu-id="09ee4-115">The token is a 64-bit hash that is created from the public key used to sign the assembly.</span></span> <span data-ttu-id="09ee4-116">Il token fa parte del nome sicuro per l'assembly e può essere letti dai metadati dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="09ee4-116">The token is a part of the strong name for the assembly, and can be read from the assembly metadata.</span></span>  
  
 <span data-ttu-id="09ee4-117">Dopo il recupero della chiave e il token viene creato, è necessario chiamare il [ICLRStrongName:: StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) metodo per rilasciare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="09ee4-117">After the key is retrieved and the token is created, you should call the [ICLRStrongName::StrongNameFreeBuffer](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamefreebuffer-method.md) method to release the allocated memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="09ee4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="09ee4-118">Requirements</span></span>  
 <span data-ttu-id="09ee4-119">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="09ee4-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="09ee4-120">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="09ee4-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="09ee4-121">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="09ee4-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="09ee4-122">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="09ee4-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09ee4-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="09ee4-123">See Also</span></span>  
 [<span data-ttu-id="09ee4-124">Metodo StrongNameTokenFromAssembly</span><span class="sxs-lookup"><span data-stu-id="09ee4-124">StrongNameTokenFromAssembly Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnametokenfromassembly-method.md)  
 [<span data-ttu-id="09ee4-125">Interfaccia ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="09ee4-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
