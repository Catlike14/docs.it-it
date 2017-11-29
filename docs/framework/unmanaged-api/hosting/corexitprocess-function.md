---
title: Funzione CorExitProcess
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CorExitProcess
api_location:
- mscoree.dll
- clr.dll
- mscorwks.dll
- mscoreei.dll
api_type: DLLExport
f1_keywords: CorExitProcess
helpviewer_keywords: CorExitProcess function [.NET Framework hosting]
ms.assetid: a5cab4c6-990e-47f3-8798-cf422b791015
topic_type: apiref
caps.latest.revision: "21"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 75b35631bad5de46d48ed818c6f929f25a5f7e66
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="corexitprocess-function"></a><span data-ttu-id="9be25-102">Funzione CorExitProcess</span><span class="sxs-lookup"><span data-stu-id="9be25-102">CorExitProcess Function</span></span>
<span data-ttu-id="9be25-103">Arresta il processo corrente non gestito.</span><span class="sxs-lookup"><span data-stu-id="9be25-103">Shuts down the current unmanaged process.</span></span>  
  
 <span data-ttu-id="9be25-104">Questa funzione è stata deprecata nel [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="9be25-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span> <span data-ttu-id="9be25-105">Utilizzare il [ICLRMetaHost:: ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) metodo invece.</span><span class="sxs-lookup"><span data-stu-id="9be25-105">Use the [ICLRMetaHost::ExitProcess](../../../../docs/framework/unmanaged-api/hosting/iclrmetahost-exitprocess-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9be25-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9be25-106">Syntax</span></span>  
  
```  
void STDMETHODCALLTYPE CorExitProcess (   
  int  exitCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9be25-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9be25-107">Parameters</span></span>  
 `exitCode`  
 <span data-ttu-id="9be25-108">Valore intero che specifica il codice di uscita del processo.</span><span class="sxs-lookup"><span data-stu-id="9be25-108">An integer that specifies the process exit code.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9be25-109">Note</span><span class="sxs-lookup"><span data-stu-id="9be25-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="9be25-110">A partire dal [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` chiude ogni runtime avviato il processo, non solo il runtime a cui sono state associate le API legacy.</span><span class="sxs-lookup"><span data-stu-id="9be25-110">Beginning with the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)], `CorExitProcess` exits every started runtime in the process, not just the runtime to which the legacy APIs have been bound.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9be25-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9be25-111">Requirements</span></span>  
 <span data-ttu-id="9be25-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9be25-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9be25-113">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="9be25-113">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="9be25-114">**Libreria:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="9be25-114">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="9be25-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9be25-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9be25-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9be25-116">See Also</span></span>  
 [<span data-ttu-id="9be25-117">Funzioni di Hosting CLR deprecate</span><span class="sxs-lookup"><span data-stu-id="9be25-117">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
