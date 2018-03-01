---
title: Funzione GetHashFromFile
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
- GetHashFromFile
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- GetHashFromFile
helpviewer_keywords:
- GetHashFromFile function [.NET Framework strong naming]
ms.assetid: b3c526a4-8fb4-4ad6-b6af-42ce9c06492e
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: be7979eb0f7d32e02257cc0b3cb400263350f0bd
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="gethashfromfile-function"></a><span data-ttu-id="32bfc-102">Funzione GetHashFromFile</span><span class="sxs-lookup"><span data-stu-id="32bfc-102">GetHashFromFile Function</span></span>
<span data-ttu-id="32bfc-103">Genera un hash per il contenuto del file specificato.</span><span class="sxs-lookup"><span data-stu-id="32bfc-103">Generates a hash over the contents of the specified file.</span></span>  
  
 <span data-ttu-id="32bfc-104">Questa funzione è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="32bfc-104">This function has been deprecated.</span></span> <span data-ttu-id="32bfc-105">Utilizzare il [ICLRStrongName:: GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) metodo invece.</span><span class="sxs-lookup"><span data-stu-id="32bfc-105">Use the [ICLRStrongName::GetHashFromFile](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="32bfc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32bfc-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromFile (  
    [in]  LPCSTR   szFilePath,  
    [in, out] unsigned int   *piHashAlg,   
    [out] BYTE     *pbHash,      
    [in]  DWORD    cchHash,      
    [out] DWORD    *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="32bfc-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="32bfc-107">Parameters</span></span>  
 `szFilePath`  
 <span data-ttu-id="32bfc-108">[in] Il nome del file con hash.</span><span class="sxs-lookup"><span data-stu-id="32bfc-108">[in] The name of the file to hash.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="32bfc-109">[in, out] L'algoritmo da utilizzare durante la generazione di hash.</span><span class="sxs-lookup"><span data-stu-id="32bfc-109">[in, out] The algorithm to use when generating the hash.</span></span> <span data-ttu-id="32bfc-110">Gli algoritmi validi sono quelli definiti in CryptoAPI Win32.</span><span class="sxs-lookup"><span data-stu-id="32bfc-110">Valid algorithms are those defined by the Win32 CryptoAPI.</span></span> <span data-ttu-id="32bfc-111">Se `piHashAlg` è impostato su 0, l'algoritmo predefinito CALG_SHA-1 viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="32bfc-111">If `piHashAlg` is set to 0, the default algorithm CALG_SHA-1 is used.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="32bfc-112">[out] Matrice di byte contenente il valore hash generato.</span><span class="sxs-lookup"><span data-stu-id="32bfc-112">[out] A byte array containing the generated hash.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="32bfc-113">[in] La dimensione massima del buffer che `pbHash` punta a.</span><span class="sxs-lookup"><span data-stu-id="32bfc-113">[in] The maximum size of the buffer that `pbHash` points to.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="32bfc-114">[out] Le dimensioni, in byte, dell'oggetto restituito `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="32bfc-114">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="32bfc-115">Note</span><span class="sxs-lookup"><span data-stu-id="32bfc-115">Remarks</span></span>  
 <span data-ttu-id="32bfc-116">Questa funzione è analoga [GetHashFromFileW](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfilew-function.md), ad eccezione del fatto che la specifica del nome file è ANSI anziché Unicode.</span><span class="sxs-lookup"><span data-stu-id="32bfc-116">This function is the same as [GetHashFromFileW](../../../../docs/framework/unmanaged-api/strong-naming/gethashfromfilew-function.md), except that the file name specification is ANSI instead of Unicode.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="32bfc-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32bfc-117">Requirements</span></span>  
 <span data-ttu-id="32bfc-118">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="32bfc-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="32bfc-119">**Intestazione:** StrongName. H</span><span class="sxs-lookup"><span data-stu-id="32bfc-119">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="32bfc-120">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="32bfc-120">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="32bfc-121">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="32bfc-121">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32bfc-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32bfc-122">See Also</span></span>  
 [<span data-ttu-id="32bfc-123">Metodo GetHashFromFile</span><span class="sxs-lookup"><span data-stu-id="32bfc-123">GetHashFromFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfile-method.md)  
 [<span data-ttu-id="32bfc-124">Metodo GetHashFromFileW</span><span class="sxs-lookup"><span data-stu-id="32bfc-124">GetHashFromFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromfilew-method.md)  
 [<span data-ttu-id="32bfc-125">Interfaccia ICLRStrongName</span><span class="sxs-lookup"><span data-stu-id="32bfc-125">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
