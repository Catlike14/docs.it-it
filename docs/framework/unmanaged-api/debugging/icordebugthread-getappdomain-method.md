---
title: Metodo ICorDebugThread::GetAppDomain
ms.date: 03/30/2017
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
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 51878f0334afe52608b60ca540e49c86fded148e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33418045"
---
# <a name="icordebugthreadgetappdomain-method"></a><span data-ttu-id="f4596-102">Metodo ICorDebugThread::GetAppDomain</span><span class="sxs-lookup"><span data-stu-id="f4596-102">ICorDebugThread::GetAppDomain Method</span></span>
<span data-ttu-id="f4596-103">Ottiene un puntatore a interfaccia per il dominio applicazione in cui è attualmente in esecuzione ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="f4596-103">Gets an interface pointer to the application domain in which this ICorDebugThread is currently executing.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f4596-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4596-104">Syntax</span></span>  
  
```  
HRESULT GetAppDomain (  
    [out] ICorDebugAppDomain  **ppAppDomain  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f4596-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4596-105">Parameters</span></span>  
 `ppAppDomain`  
 <span data-ttu-id="f4596-106">[out] Un puntatore a un oggetto ICorDebugAppDomain che rappresenta il dominio applicazione in cui il thread attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f4596-106">[out] A pointer to an ICorDebugAppDomain object that represents the application domain in which this thread is currently executing.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f4596-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4596-107">Requirements</span></span>  
 <span data-ttu-id="f4596-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f4596-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f4596-109">**Intestazione:** Cordebug. idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="f4596-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f4596-110">**Libreria:** CorGuids. lib</span><span class="sxs-lookup"><span data-stu-id="f4596-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f4596-111">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f4596-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
