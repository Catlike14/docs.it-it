---
title: Metodo ICLRAssemblyIdentityManager::IsStronglyNamed
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRAssemblyIdentityManager.IsStronglyNamed
api_location: mscoree.dll
api_type: COM
f1_keywords: ICLRAssemblyIdentityManager::IsStronglyNamed
helpviewer_keywords:
- IsStronglyNamed method [.NET Framework hosting]
- ICLRAssemblyIdentityManager::IsStronglyNamed method [.NET Framework hosting]
ms.assetid: 954bd386-2076-4d00-9d46-38c728aa9cab
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d0cb0bcaf5d19ec088511e64baffff9031911b32
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iclrassemblyidentitymanagerisstronglynamed-method"></a><span data-ttu-id="0844e-102">Metodo ICLRAssemblyIdentityManager::IsStronglyNamed</span><span class="sxs-lookup"><span data-stu-id="0844e-102">ICLRAssemblyIdentityManager::IsStronglyNamed Method</span></span>
<span data-ttu-id="0844e-103">Ottiene un valore che indica se l'assembly specificato è un nome sicuro.</span><span class="sxs-lookup"><span data-stu-id="0844e-103">Gets a value that indicates whether the specified assembly is strongly named.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0844e-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0844e-104">Syntax</span></span>  
  
```  
RESULT IsStronglyNamed (  
    [in]  LPCWSTR  pwzAssemblyIdentity,  
    [out] BOOL    *pbIsStronglyNamed  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0844e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0844e-105">Parameters</span></span>  
 `pwzAssemblyIdentity`  
 <span data-ttu-id="0844e-106">[in] I dati di identità assembly canonica opaca dell'assembly da valutare.</span><span class="sxs-lookup"><span data-stu-id="0844e-106">[in] The opaque canonical assembly identity data of the assembly to be evaluated.</span></span>  
  
 `pbIsStronglyNamed`  
 <span data-ttu-id="0844e-107">[out] `true`, se l'assembly a cui fa riferimento il `pwzAssemblyIdentity` parametro è fortemente denominato; in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="0844e-107">[out] `true`, if the assembly referenced by the `pwzAssemblyIdentity` parameter is strongly named; otherwise, `false`.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="0844e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0844e-108">Return Value</span></span>  
  
|<span data-ttu-id="0844e-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="0844e-109">HRESULT</span></span>|<span data-ttu-id="0844e-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0844e-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="0844e-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="0844e-111">S_OK</span></span>|<span data-ttu-id="0844e-112">Il metodo è stato restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="0844e-112">The method returned successfully.</span></span>|  
|<span data-ttu-id="0844e-113">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="0844e-113">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="0844e-114">Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.</span><span class="sxs-lookup"><span data-stu-id="0844e-114">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="0844e-115">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="0844e-115">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="0844e-116">Timeout della chiamata.</span><span class="sxs-lookup"><span data-stu-id="0844e-116">The call timed out.</span></span>|  
|<span data-ttu-id="0844e-117">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="0844e-117">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="0844e-118">Il chiamante non dispone del blocco.</span><span class="sxs-lookup"><span data-stu-id="0844e-118">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="0844e-119">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="0844e-119">HOST_E_ABANDONED</span></span>|<span data-ttu-id="0844e-120">Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.</span><span class="sxs-lookup"><span data-stu-id="0844e-120">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="0844e-121">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="0844e-121">E_FAIL</span></span>|<span data-ttu-id="0844e-122">Si è verificato un errore irreversibile sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="0844e-122">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="0844e-123">Se un metodo restituisce E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo.</span><span class="sxs-lookup"><span data-stu-id="0844e-123">If a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="0844e-124">Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.</span><span class="sxs-lookup"><span data-stu-id="0844e-124">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="0844e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0844e-125">Requirements</span></span>  
 <span data-ttu-id="0844e-126">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0844e-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0844e-127">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="0844e-127">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="0844e-128">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="0844e-128">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="0844e-129">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0844e-129">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0844e-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0844e-130">See Also</span></span>  
 [<span data-ttu-id="0844e-131">ICLRAssemblyIdentityManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="0844e-131">ICLRAssemblyIdentityManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrassemblyidentitymanager-interface.md)
