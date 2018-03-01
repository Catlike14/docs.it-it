---
title: Metodo ICLRRuntimeInfo::IsStarted
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
- ICLRRuntimeInfo.IsStarted
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICLRRuntimeInfo::IsStarted
helpviewer_keywords:
- IsStarted method [.NET Framework hosting]
- ICLRRuntimeInfo::IsStarted method [.NET Framework hosting]
ms.assetid: ef6f2662-323b-4534-aa82-6d1afb7b9309
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 991470ca0df3e0cf0470a8c40d3e8e4c40d96026
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iclrruntimeinfoisstarted-method"></a><span data-ttu-id="c2d26-102">Metodo ICLRRuntimeInfo::IsStarted</span><span class="sxs-lookup"><span data-stu-id="c2d26-102">ICLRRuntimeInfo::IsStarted Method</span></span>
<span data-ttu-id="c2d26-103">Indica se il runtime è stato avviato (ovvero, se il [ICLRRuntimeHost::](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) è stato chiamato e ha avuto esito positivo).</span><span class="sxs-lookup"><span data-stu-id="c2d26-103">Indicates whether the runtime has been started (that is, whether the [ICLRRuntimeHost::Start method](../../../../docs/framework/unmanaged-api/hosting/iclrruntimehost-start-method.md) has been called and has succeeded).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c2d26-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2d26-104">Syntax</span></span>  
  
```  
HRESULT IsStarted(  
        [out] BOOL     *pbStarted,  
        [out] DWORD    *pdwStartupFlags);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c2d26-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2d26-105">Parameters</span></span>  
 `pbStarted`  
 <span data-ttu-id="c2d26-106">[out] `true` se il runtime è avviato; in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="c2d26-106">[out] `true` if this runtime is started; otherwise, `false`.</span></span>  
  
 `pdwStartupFlags`  
 <span data-ttu-id="c2d26-107">[out] Restituisce i flag utilizzati per avviare il runtime.</span><span class="sxs-lookup"><span data-stu-id="c2d26-107">[out] Returns the flags that were used to start the runtime.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c2d26-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2d26-108">Return Value</span></span>  
 <span data-ttu-id="c2d26-109">Questo metodo restituisce gli specifici HRESULT seguenti, nonché gli errori di HRESULT che indicano la mancata riuscita del metodo.</span><span class="sxs-lookup"><span data-stu-id="c2d26-109">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="c2d26-110">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c2d26-110">HRESULT</span></span>|<span data-ttu-id="c2d26-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2d26-111">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c2d26-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2d26-112">S_OK</span></span>|<span data-ttu-id="c2d26-113">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="c2d26-113">The method completed successfully.</span></span>|  
|<span data-ttu-id="c2d26-114">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="c2d26-114">E_NOTIMPL</span></span>|<span data-ttu-id="c2d26-115">La versione di common language runtime (CLR) è precedente alla versione CLR nel [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2d26-115">The common language runtime (CLR) version is earlier than the CLR version in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c2d26-116">Note</span><span class="sxs-lookup"><span data-stu-id="c2d26-116">Remarks</span></span>  
 <span data-ttu-id="c2d26-117">Questo metodo non funziona con le versioni CLR precedenti alla versione di CLR nel [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c2d26-117">This method does not work with CLR versions earlier than the CLR version in the [!INCLUDE[net_v40_short](../../../../includes/net-v40-short-md.md)].</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c2d26-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2d26-118">Requirements</span></span>  
 <span data-ttu-id="c2d26-119">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c2d26-119">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c2d26-120">**Intestazione:** Metahost. H</span><span class="sxs-lookup"><span data-stu-id="c2d26-120">**Header:** MetaHost.h</span></span>  
  
 <span data-ttu-id="c2d26-121">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="c2d26-121">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c2d26-122">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c2d26-122">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c2d26-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c2d26-123">See Also</span></span>  
 [<span data-ttu-id="c2d26-124">Interfaccia ICLRRuntimeInfo</span><span class="sxs-lookup"><span data-stu-id="c2d26-124">ICLRRuntimeInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrruntimeinfo-interface.md)  
 [<span data-ttu-id="c2d26-125">Interfacce di hosting</span><span class="sxs-lookup"><span data-stu-id="c2d26-125">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)  
 [<span data-ttu-id="c2d26-126">Hosting</span><span class="sxs-lookup"><span data-stu-id="c2d26-126">Hosting</span></span>](../../../../docs/framework/unmanaged-api/hosting/index.md)
