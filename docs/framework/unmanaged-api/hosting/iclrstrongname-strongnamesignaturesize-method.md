---
title: Metodo ICLRStrongName::StrongNameSignatureSize
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRStrongName.StrongNameSignatureSize
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRStrongName::StrongNameSignatureSize
helpviewer_keywords:
- ICLRStrongName::StrongNameSignatureSize method [.NET Framework hosting]
- StrongNameSignatureSize method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 76d4f93a-5e25-4399-abcc-a1389549481d
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 91a420e520a48f3a33c4ac8c127ccefc064c23bb
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iclrstrongnamestrongnamesignaturesize-method"></a><span data-ttu-id="60979-102">Metodo ICLRStrongName::StrongNameSignatureSize</span><span class="sxs-lookup"><span data-stu-id="60979-102">ICLRStrongName::StrongNameSignatureSize Method</span></span>
<span data-ttu-id="60979-103">Restituisce la dimensione della firma con nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="60979-103">Returns the size of the strong name signature.</span></span> <span data-ttu-id="60979-104">Questo metodo viene in genere utilizzato dai compilatori per determinare la quantità di spazio da riservare nel file durante la creazione di un assembly con firma ritardata.</span><span class="sxs-lookup"><span data-stu-id="60979-104">This method is typically used by compilers to determine how much space to reserve in the file when creating a delay-signed assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60979-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60979-105">Syntax</span></span>  
  
```  
HRESULT StrongNameSignatureSize (   
    [in]  BYTE   *pbPublicKeyBlob,  
    [in]  ULONG  cbPublicKeyBlob,   
    [in]  DWORD  *pcbSize  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="60979-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60979-106">Parameters</span></span>  
 `pbPublicKeyBlob`  
 <span data-ttu-id="60979-107">[in] Una struttura di tipo [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) che contiene la parte pubblica della coppia di chiavi usata per generare la firma nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="60979-107">[in] A structure of type [PublicKeyBlob](../../../../docs/framework/unmanaged-api/strong-naming/publickeyblob-structure.md) that contains the public portion of the key pair used to generate the strong name signature.</span></span>  
  
 `cbPublicKeyBlob`  
 <span data-ttu-id="60979-108">[in] Le dimensioni, in byte, di `pbPublicKeyBlob`.</span><span class="sxs-lookup"><span data-stu-id="60979-108">[in] The size, in bytes, of `pbPublicKeyBlob`.</span></span>  
  
 `pcbSize`  
 <span data-ttu-id="60979-109">[in] Il numero di byte necessari per archiviare la firma nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="60979-109">[in] The number of bytes required to store the strong name signature.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="60979-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60979-110">Return Value</span></span>  
 <span data-ttu-id="60979-111">`S_OK`Se il metodo viene completato correttamente. in caso contrario, un valore HRESULT indicante un errore (vedere [valori HRESULT comuni](http://go.microsoft.com/fwlink/?LinkId=213878) per un elenco).</span><span class="sxs-lookup"><span data-stu-id="60979-111">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](http://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60979-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60979-112">Requirements</span></span>  
 <span data-ttu-id="60979-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="60979-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60979-114">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="60979-114">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="60979-115">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="60979-115">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="60979-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60979-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60979-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="60979-117">See Also</span></span>  
 [<span data-ttu-id="60979-118">ICLRStrongName (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="60979-118">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
