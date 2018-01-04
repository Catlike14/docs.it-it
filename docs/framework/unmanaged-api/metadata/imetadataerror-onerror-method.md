---
title: Metodo IMetaDataError::OnError
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataError.OnError
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataError::OnError
helpviewer_keywords:
- IMetaDataError::OnError method [.NET Framework metadata]
- OnError method, IMetaDataError interface [.NET Framework metadata]
ms.assetid: c1e744b8-a6fb-4d9c-a971-8babc875d8f0
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b6e136f3fd76b9eb2be1e49a48316dc65c481fc6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="imetadataerroronerror-method"></a><span data-ttu-id="fc967-102">Metodo IMetaDataError::OnError</span><span class="sxs-lookup"><span data-stu-id="fc967-102">IMetaDataError::OnError Method</span></span>
<span data-ttu-id="fc967-103">Fornisce la notifica degli errori che si verificano durante l'unione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="fc967-103">Provides notification of errors that occur during the metadata merge.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fc967-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fc967-104">Syntax</span></span>  
  
```  
HRESULT OnError (  
    [in] HRESULT   hrError,   
    [in] mdToken   token  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fc967-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc967-105">Parameters</span></span>  
 `hrError`  
 <span data-ttu-id="fc967-106">[in] Il valore di errore HRESULT restituito al metodo di chiamata.</span><span class="sxs-lookup"><span data-stu-id="fc967-106">[in] The HRESULT error value returned to the calling method.</span></span>  
  
 `token`  
 <span data-ttu-id="fc967-107">[in] Il token di metadati dell'oggetto di codice che è stato unito quando si è verificato l'errore.</span><span class="sxs-lookup"><span data-stu-id="fc967-107">[in] The metadata token of the code object that was being merged when the error occurred.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fc967-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc967-108">Requirements</span></span>  
 <span data-ttu-id="fc967-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="fc967-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="fc967-110">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="fc967-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="fc967-111">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="fc967-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="fc967-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="fc967-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fc967-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fc967-113">See Also</span></span>  
 [<span data-ttu-id="fc967-114">Interfaccia IMetaDataError</span><span class="sxs-lookup"><span data-stu-id="fc967-114">IMetaDataError Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadataerror-interface.md)
