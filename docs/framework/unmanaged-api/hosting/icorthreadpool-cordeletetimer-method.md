---
title: Metodo ICorThreadpool::CorDeleteTimer
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
- ICorThreadpool.CorDeleteTimer
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorDeleteTimer
helpviewer_keywords:
- ICorThreadpool::CorDeleteTimer method [.NET Framework hosting]
- CorDeleteTimer method [.NET Framework hosting]
ms.assetid: 74847c35-7ca1-466a-b750-b25e7b03d100
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: d562e4b5b348c6e980780e1162ece74d8c20c46d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorthreadpoolcordeletetimer-method"></a><span data-ttu-id="06342-102">Metodo ICorThreadpool::CorDeleteTimer</span><span class="sxs-lookup"><span data-stu-id="06342-102">ICorThreadpool::CorDeleteTimer Method</span></span>
<span data-ttu-id="06342-103">Questo metodo supporta l'infrastruttura .NET Framework e non può essere utilizzato direttamente dal codice.</span><span class="sxs-lookup"><span data-stu-id="06342-103">This method supports the .NET Framework infrastructure and is not intended to be used directly from your code.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="06342-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06342-104">Syntax</span></span>  
  
```  
HRESULT CorDeleteTimer (  
    [in]  HANDLE Timer,  
    [in]  HANDLE CompletionEvent,  
    [out] BOOL*  result  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="06342-105">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06342-105">Requirements</span></span>  
 <span data-ttu-id="06342-106">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="06342-106">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="06342-107">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="06342-107">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="06342-108">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="06342-108">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="06342-109">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="06342-109">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="06342-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="06342-110">See Also</span></span>  
 [<span data-ttu-id="06342-111">Interfaccia ICorThreadpool</span><span class="sxs-lookup"><span data-stu-id="06342-111">ICorThreadpool Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/icorthreadpool-interface.md)
