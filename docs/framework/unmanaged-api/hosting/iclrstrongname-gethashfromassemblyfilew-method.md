---
title: Metodo ICLRStrongName::GetHashFromAssemblyFileW
ms.date: 03/30/2017
api_name:
- ICLRStrongName.GetHashFromAssemblyFileW
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW
helpviewer_keywords:
- ICLRStrongName::GetHashFromAssemblyFileW method [.NET Framework hosting]
- GetHashFromAssemblyFileW method, ICLRStrongName interface [.NET Framework hosting]
ms.assetid: 5d0b44a2-5a14-44a2-9a0e-e8682fd4e106
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7686a84759f8ac40a123d2c9a7b8f1b9b8096cb
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43672600"
---
# <a name="iclrstrongnamegethashfromassemblyfilew-method"></a><span data-ttu-id="124a3-102">Metodo ICLRStrongName::GetHashFromAssemblyFileW</span><span class="sxs-lookup"><span data-stu-id="124a3-102">ICLRStrongName::GetHashFromAssemblyFileW Method</span></span>
<span data-ttu-id="124a3-103">Genera un hash basato sul contenuto del file specificato da una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="124a3-103">Generates a hash over the contents of the file specified by a Unicode string.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="124a3-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="124a3-104">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="124a3-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="124a3-105">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="124a3-106">[in] Il percorso del file di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="124a3-106">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="124a3-107">Questo parametro deve essere una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="124a3-107">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="124a3-108">[in, out] Costante che specifica l'algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="124a3-108">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="124a3-109">Usa lo zero per l'algoritmo hash predefinito.</span><span class="sxs-lookup"><span data-stu-id="124a3-109">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="124a3-110">[out] Il buffer di hash restituito.</span><span class="sxs-lookup"><span data-stu-id="124a3-110">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="124a3-111">[in] La dimensione massima richiesta del `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="124a3-111">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="124a3-112">[out] La dimensione restituita, in byte, di `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="124a3-112">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="124a3-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="124a3-113">Return Value</span></span>  
 <span data-ttu-id="124a3-114">`S_OK` Se il metodo è stata completata correttamente. in caso contrario, un valore HRESULT indicante un errore (vedere [valori HRESULT comuni](https://go.microsoft.com/fwlink/?LinkId=213878) per un elenco).</span><span class="sxs-lookup"><span data-stu-id="124a3-114">`S_OK` if the method completed successfully; otherwise, an HRESULT value that indicates failure (see [Common HRESULT Values](https://go.microsoft.com/fwlink/?LinkId=213878) for a list).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="124a3-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="124a3-115">Requirements</span></span>  
 <span data-ttu-id="124a3-116">**Piattaforme:** vedere [Requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="124a3-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="124a3-117">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="124a3-117">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="124a3-118">**Libreria:** inclusa come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="124a3-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="124a3-119">**Versioni di .NET Framework:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="124a3-119">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="124a3-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="124a3-120">See Also</span></span>  
 [<span data-ttu-id="124a3-121">Metodo GetHashFromAssemblyFile</span><span class="sxs-lookup"><span data-stu-id="124a3-121">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [<span data-ttu-id="124a3-122">Interfaccia ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="124a3-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
