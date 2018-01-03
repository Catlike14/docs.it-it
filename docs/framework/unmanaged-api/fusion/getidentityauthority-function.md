---
title: Funzione GetIdentityAuthority
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetIdentityAuthority
api_location:
- fusion.dll
- clr.dll
api_type: COM
f1_keywords: GetIdentityAuthority
helpviewer_keywords: GetIdentityAuthority function [.NET Framework fusion]
ms.assetid: 843cd5ab-d2b7-4ff6-86bd-e68c7a91c098
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 5fab6fa7c8e58dcd2fdece05572242230847f62f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="getidentityauthority-function"></a><span data-ttu-id="10ae8-102">Funzione GetIdentityAuthority</span><span class="sxs-lookup"><span data-stu-id="10ae8-102">GetIdentityAuthority Function</span></span>
<span data-ttu-id="10ae8-103">Ottiene un puntatore a un [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) che gestisce le chiavi per gli oggetti di codice.</span><span class="sxs-lookup"><span data-stu-id="10ae8-103">Gets a pointer to an [IIdentityAuthority](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md) instance that manages keys for code objects.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="10ae8-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="10ae8-104">Syntax</span></span>  
  
```  
HRESULT GetIdentityAuthority (  
    [out] IIdentityAuthority   **ppIIdentityAuthority  
 );  
```  
  
#### <a name="parameters"></a><span data-ttu-id="10ae8-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="10ae8-105">Parameters</span></span>  
 `ppIIdentityAuthority`  
 <span data-ttu-id="10ae8-106">[out] L'oggetto restituito `IIdentityAuthority` puntatore.</span><span class="sxs-lookup"><span data-stu-id="10ae8-106">[out] The returned `IIdentityAuthority` pointer.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="10ae8-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10ae8-107">Requirements</span></span>  
 <span data-ttu-id="10ae8-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="10ae8-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="10ae8-109">**Intestazione:** Isolation. h</span><span class="sxs-lookup"><span data-stu-id="10ae8-109">**Header:** Isolation.h</span></span>  
  
 <span data-ttu-id="10ae8-110">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="10ae8-110">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="10ae8-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="10ae8-111">See Also</span></span>  
 [<span data-ttu-id="10ae8-112">Interfaccia IIdentityAuthority</span><span class="sxs-lookup"><span data-stu-id="10ae8-112">IIdentityAuthority Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iidentityauthority-interface.md)  
 [<span data-ttu-id="10ae8-113">Funzioni statiche globali Fusion</span><span class="sxs-lookup"><span data-stu-id="10ae8-113">Fusion Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-global-static-functions.md)
