---
title: Metodo ICorThreadpool::CorBindIoCompletionCallback
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorThreadpool.CorBindIoCompletionCallback
api_location: mscoree.dll
api_type: COM
f1_keywords: CorBindIoCompletionCallback
helpviewer_keywords:
- CorBindIoCompletionCallback method [.NET Framework hosting]
- ICorThreadpool::CorBindIoCompletionCallback method [.NET Framework hosting]
ms.assetid: 2b159225-f09c-42f1-aa7c-44087e121249
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 28baf49fd659564f1e1e356f52be6cd9cbb9f643
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorthreadpoolcorbindiocompletioncallback-method"></a><span data-ttu-id="f4872-102">Metodo ICorThreadpool::CorBindIoCompletionCallback</span><span class="sxs-lookup"><span data-stu-id="f4872-102">ICorThreadpool::CorBindIoCompletionCallback Method</span></span>
<span data-ttu-id="f4872-103">Questo metodo supporta l'infrastruttura .NET Framework e non può essere utilizzato direttamente dal codice.</span><span class="sxs-lookup"><span data-stu-id="f4872-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4872-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4872-104">Syntax</span></span>  
  
```  
HRESULT CorBindIoCompletionCallback (  
    [in] HANDLE                          fileHandle,  
    [in] LPOVERLAPPED_COMPLETION_ROUTINE callback  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="f4872-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4872-105">Requirements</span></span>  
 <span data-ttu-id="f4872-106">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f4872-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4872-107">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="f4872-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="f4872-108">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="f4872-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="f4872-109">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4872-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f4872-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f4872-110">See Also</span></span>  
 [<span data-ttu-id="f4872-111">ICorThreadpool (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f4872-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
