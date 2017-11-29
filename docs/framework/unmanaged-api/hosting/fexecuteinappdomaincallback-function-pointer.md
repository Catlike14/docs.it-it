---
title: Puntatore alla funzione FExecuteInAppDomainCallback
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: FExecuteInAppDomainCallback
api_location: mscoree.dll
api_type: COM
f1_keywords: FExecuteInAppDomainCallback
helpviewer_keywords: FExecuteInAppDomainCallback function pointer [.NET Framework hosting]
ms.assetid: 2709f18f-3eee-497f-bc33-3ab7a485599b
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 5e6c04a964b50357dc3687f3faf5710505bae364
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="fexecuteinappdomaincallback-function-pointer"></a><span data-ttu-id="05132-102">Puntatore alla funzione FExecuteInAppDomainCallback</span><span class="sxs-lookup"><span data-stu-id="05132-102">FExecuteInAppDomainCallback Function Pointer</span></span>
<span data-ttu-id="05132-103">Punta a una funzione che viene chiamato da common language runtime (CLR) per eseguire codice gestito.</span><span class="sxs-lookup"><span data-stu-id="05132-103">Points to a function that is called by the common language runtime (CLR) to execute managed code.</span></span>  
  
 <span data-ttu-id="05132-104">Questo puntatore a funzione è stato deprecato nel [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="05132-104">This function pointer has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="05132-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05132-105">Syntax</span></span>  
  
```  
typedef HRESULT (__stdcall *FExecuteInAppDomainCallback) (  
    [in] void  *cookie  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="05132-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="05132-106">Parameters</span></span>  
 `cookie`  
 <span data-ttu-id="05132-107">[in] Puntatore alla memoria allocata dal chiamante opaca che contiene il codice gestito deve essere eseguito.</span><span class="sxs-lookup"><span data-stu-id="05132-107">[in] A pointer to opaque caller-allocated memory that contains the managed code to be executed.</span></span>  
  
 <span data-ttu-id="05132-108">L'allocazione e la durata della memoria sono controllate dal chiamante (CLR).</span><span class="sxs-lookup"><span data-stu-id="05132-108">The allocation and lifetime of this memory are controlled by the caller (that is, the CLR).</span></span> <span data-ttu-id="05132-109">Non si tratta della memoria heap gestito di CLR.</span><span class="sxs-lookup"><span data-stu-id="05132-109">This is not CLR managed-heap memory.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="05132-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05132-110">Requirements</span></span>  
 <span data-ttu-id="05132-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="05132-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="05132-112">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="05132-112">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="05132-113">**Libreria:** MSCorWks.dll</span><span class="sxs-lookup"><span data-stu-id="05132-113">**Library:** MSCorWks.dll</span></span>  
  
 <span data-ttu-id="05132-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="05132-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="05132-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="05132-115">See Also</span></span>  
 [<span data-ttu-id="05132-116">Funzioni di Hosting CLR deprecate</span><span class="sxs-lookup"><span data-stu-id="05132-116">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
