---
title: Metodo IGCHostControl::RequestVirtualMemLimit
ms.date: 03/30/2017
api_name:
- IGCHostControl.RequestVirtualMemLimit
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- RequestVirtualMemLimit
helpviewer_keywords:
- IGCHostControl::RequestVirtualMemLimit method [.NET Framework hosting]
- RequestVirtualMemLimit method [.NET Framework hosting]
ms.assetid: f4984a8c-4c0e-4460-9aa1-d022b3621228
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2df33e3edebbf558bf78986e737c4f7bb9b2f0f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33437157"
---
# <a name="igchostcontrolrequestvirtualmemlimit-method"></a><span data-ttu-id="df7c6-102">Metodo IGCHostControl::RequestVirtualMemLimit</span><span class="sxs-lookup"><span data-stu-id="df7c6-102">IGCHostControl::RequestVirtualMemLimit Method</span></span>
<span data-ttu-id="df7c6-103">Richiede all'host di modificare i limiti di memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="df7c6-103">Requests the host to change the limits of virtual memory.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df7c6-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df7c6-104">Syntax</span></span>  
  
```  
HRESULT RequestVirtualMemLimit (  
    [in] SIZE_T       sztMaxVirtualMemMB,  
    [in, out] SIZE_T* psztNewMaxVirtualMemMB  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="df7c6-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="df7c6-105">Parameters</span></span>  
 `sztMaxVirtualMemMB`  
 <span data-ttu-id="df7c6-106">[in] La dimensione richiesta di memoria da allocare.</span><span class="sxs-lookup"><span data-stu-id="df7c6-106">[in] The requested size of memory to be allocated.</span></span>  
  
 `psztNewMaxVirtualMemMB`  
 <span data-ttu-id="df7c6-107">[in, out] Un puntatore alla dimensione effettiva di memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="df7c6-107">[in, out] A pointer to the actual size of memory allocated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="df7c6-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df7c6-108">Requirements</span></span>  
 <span data-ttu-id="df7c6-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="df7c6-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="df7c6-110">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="df7c6-110">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="df7c6-111">**Libreria:** inclusa come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="df7c6-111">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="df7c6-112">**Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="df7c6-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="df7c6-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="df7c6-113">See Also</span></span>  
 [<span data-ttu-id="df7c6-114">Interfaccia IGCHostControl</span><span class="sxs-lookup"><span data-stu-id="df7c6-114">IGCHostControl Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/igchostcontrol-interface.md)
