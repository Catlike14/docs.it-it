---
title: Funzione GetHashFromAssemblyFileW
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetHashFromAssemblyFileW
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: GetHashFromAssemblyFileW
helpviewer_keywords: GetHashFromAssemblyFileW function [.NET Framework strong naming]
ms.assetid: d1b2b172-5353-42af-a877-cf653c68ece0
topic_type: apiref
caps.latest.revision: "15"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: aa88de90f831e1faaca2624a77a556d6a2b566c2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="gethashfromassemblyfilew-function"></a><span data-ttu-id="e50b8-102">Funzione GetHashFromAssemblyFileW</span><span class="sxs-lookup"><span data-stu-id="e50b8-102">GetHashFromAssemblyFileW Function</span></span>
<span data-ttu-id="e50b8-103">Ottiene un hash del file di assembly specificato, usando l'algoritmo hash specificato.</span><span class="sxs-lookup"><span data-stu-id="e50b8-103">Gets a hash of the specified assembly file, using the specified hash algorithm.</span></span> <span data-ttu-id="e50b8-104">Il percorso del file di assembly deve essere specificato come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="e50b8-104">The path to the assembly file must be specified as a Unicode string.</span></span>  
  
 <span data-ttu-id="e50b8-105">Questa funzione è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="e50b8-105">This function has been deprecated.</span></span> <span data-ttu-id="e50b8-106">Utilizzare il [:: GetHashFromAssemblyFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md) metodo invece.</span><span class="sxs-lookup"><span data-stu-id="e50b8-106">Use the [ICLRStrongName::GetHashFromAssemblyFileW](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e50b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e50b8-107">Syntax</span></span>  
  
```  
HRESULT GetHashFromAssemblyFileW (  
    [in]  LPCWSTR   wszFilePath,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE      *pbHash,  
    [in]  DWORD     cchHash,  
    [out] DWORD     *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e50b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e50b8-108">Parameters</span></span>  
 `wszFilePath`  
 <span data-ttu-id="e50b8-109">[in] Il percorso del file di cui eseguire l'hashing.</span><span class="sxs-lookup"><span data-stu-id="e50b8-109">[in] The path to the file to be hashed.</span></span> <span data-ttu-id="e50b8-110">Questo parametro deve essere una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="e50b8-110">This parameter must be a Unicode string.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="e50b8-111">[in, out] Costante che specifica l'algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="e50b8-111">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="e50b8-112">Utilizzare zero per l'algoritmo hash predefinito.</span><span class="sxs-lookup"><span data-stu-id="e50b8-112">Use zero for the default hash algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="e50b8-113">[out] Il buffer di hash restituito.</span><span class="sxs-lookup"><span data-stu-id="e50b8-113">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="e50b8-114">[in] La dimensione massima richiesta del `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="e50b8-114">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="e50b8-115">[out] La dimensione restituita, in byte, di `pbHash`.</span><span class="sxs-lookup"><span data-stu-id="e50b8-115">[out] The returned size, in bytes, of `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e50b8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e50b8-116">Requirements</span></span>  
 <span data-ttu-id="e50b8-117">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e50b8-117">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e50b8-118">**Intestazione:** StrongName. H</span><span class="sxs-lookup"><span data-stu-id="e50b8-118">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="e50b8-119">**Libreria:** inclusa come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="e50b8-119">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e50b8-120">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e50b8-120">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e50b8-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e50b8-121">See Also</span></span>  
 [<span data-ttu-id="e50b8-122">GetHashFromAssemblyFileW (metodo)</span><span class="sxs-lookup"><span data-stu-id="e50b8-122">GetHashFromAssemblyFileW Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfilew-method.md)  
 [<span data-ttu-id="e50b8-123">GetHashFromAssemblyFile (metodo)</span><span class="sxs-lookup"><span data-stu-id="e50b8-123">GetHashFromAssemblyFile Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromassemblyfile-method.md)  
 [<span data-ttu-id="e50b8-124">ICLRStrongName (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="e50b8-124">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
