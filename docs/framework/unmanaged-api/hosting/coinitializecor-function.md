---
title: Funzione CoInitializeCor
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91315e8af0cc46a3450a7515b885988cffe34927
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429988"
---
# <a name="coinitializecor-function"></a><span data-ttu-id="52177-102">Funzione CoInitializeCor</span><span class="sxs-lookup"><span data-stu-id="52177-102">CoInitializeCor Function</span></span>
<span data-ttu-id="52177-103">`CoInitializeCor` è obsoleto.</span><span class="sxs-lookup"><span data-stu-id="52177-103">`CoInitializeCor` is obsolete.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="52177-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52177-104">Syntax</span></span>  
  
```  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="52177-105">Note</span><span class="sxs-lookup"><span data-stu-id="52177-105">Remarks</span></span>  
 <span data-ttu-id="52177-106">Per inizializzare common language runtime, utilizzare [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) o [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span><span class="sxs-lookup"><span data-stu-id="52177-106">To initialize the common language runtime, use either [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) or [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="52177-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52177-107">Requirements</span></span>  
 <span data-ttu-id="52177-108">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="52177-108">**Header:** Cor.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52177-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="52177-109">See Also</span></span>  
 [<span data-ttu-id="52177-110">Funzioni statiche globali dei metadati</span><span class="sxs-lookup"><span data-stu-id="52177-110">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
