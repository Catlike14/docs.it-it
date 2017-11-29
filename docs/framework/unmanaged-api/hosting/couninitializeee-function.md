---
title: Funzione CoUninitializeEE
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CoUninitializeEE
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: CoUninitializeEE
helpviewer_keywords: CoUninitializeEE function [.NET Framework hosting]
ms.assetid: 5f5a311a-839a-465f-89d9-ff1c74da9736
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d64064c29d2a03578305f71a37e759907814727e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="couninitializeee-function"></a><span data-ttu-id="1093b-102">Funzione CoUninitializeEE</span><span class="sxs-lookup"><span data-stu-id="1093b-102">CoUninitializeEE Function</span></span>
<span data-ttu-id="1093b-103">`CoUninitializeEE`è obsoleto e non fornisce alcuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1093b-103">`CoUninitializeEE` is obsolete and provides no functionality.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="1093b-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1093b-104">Syntax</span></span>  
  
```  
void CoUninitializeEE (  
    BOOL fFlags  
);  
```  
  
## <a name="remarks"></a><span data-ttu-id="1093b-105">Note</span><span class="sxs-lookup"><span data-stu-id="1093b-105">Remarks</span></span>  
 <span data-ttu-id="1093b-106">Il motore di esecuzione di common language runtime non può essere scaricato da un processo.</span><span class="sxs-lookup"><span data-stu-id="1093b-106">The common language runtime execution engine cannot be unloaded from a process.</span></span> <span data-ttu-id="1093b-107">Per arrestare il motore, chiamare [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md).</span><span class="sxs-lookup"><span data-stu-id="1093b-107">To shut down the execution engine call [CorExitProcess](../../../../docs/framework/unmanaged-api/hosting/corexitprocess-function.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1093b-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1093b-108">See Also</span></span>  
 [<span data-ttu-id="1093b-109">CoInitializeEE (funzione)</span><span class="sxs-lookup"><span data-stu-id="1093b-109">CoInitializeEE Function</span></span>](../../../../docs/framework/unmanaged-api/hosting/coinitializeee-function.md)  
 [<span data-ttu-id="1093b-110">Funzioni statiche globali dei metadati</span><span class="sxs-lookup"><span data-stu-id="1093b-110">Metadata Global Static Functions</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
