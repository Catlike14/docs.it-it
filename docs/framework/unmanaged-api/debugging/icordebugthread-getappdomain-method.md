---
title: Metodo ICorDebugThread::GetAppDomain
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
- ICorDebugThread.GetAppDomain
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugThread::GetAppDomain
helpviewer_keywords:
- GetAppDomain method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetAppDomain method [.NET Framework debugging]
ms.assetid: 415b3d34-8b35-4b60-a318-140646cc83f8
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: c235bc0294b967e26766a095b85c5acf0f27cff9
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugthreadgetappdomain-method"></a><span data-ttu-id="0074f-102">Metodo ICorDebugThread::GetAppDomain</span><span class="sxs-lookup"><span data-stu-id="0074f-102">ICorDebugThread::GetAppDomain Method</span></span>
<span data-ttu-id="0074f-103">Ottiene un puntatore a interfaccia per il dominio applicazione in cui è attualmente in esecuzione ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="0074f-103">Gets an interface pointer to the application domain in which this ICorDebugThread is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="0074f-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0074f-104">Syntax</span></span>  
  
```  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0074f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="0074f-105">Parameters</span></span>  
 `ppAppDomain`  
 <span data-ttu-id="0074f-106">[out] Un puntatore a un oggetto ICorDebugAppDomain che rappresenta il dominio applicazione in cui il thread attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0074f-106">[out] A pointer to an ICorDebugAppDomain object that represents the application domain in which this thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="0074f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0074f-107">Requirements</span></span>  
 <span data-ttu-id="0074f-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="0074f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="0074f-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="0074f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="0074f-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="0074f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="0074f-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="0074f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
