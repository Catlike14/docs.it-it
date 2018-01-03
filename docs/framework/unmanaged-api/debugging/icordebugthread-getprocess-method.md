---
title: Metodo ICorDebugThread::GetProcess
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread.GetProcess
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread::GetProcess
helpviewer_keywords:
- ICorDebugThread::GetProcess method [.NET Framework debugging]
- GetProcess method, ICorDebugThread interface [.NET Framework debugging]
ms.assetid: 163816e7-0739-4566-b3df-cd256be8b8a4
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 04410024dfe145b7df96dc0f3d8df6fab230f2c8
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugthreadgetprocess-method"></a><span data-ttu-id="04c8f-102">Metodo ICorDebugThread::GetProcess</span><span class="sxs-lookup"><span data-stu-id="04c8f-102">ICorDebugThread::GetProcess Method</span></span>
<span data-ttu-id="04c8f-103">Ottiene un puntatore a interfaccia per il processo di cui ICorDebugThread costituisce una parte.</span><span class="sxs-lookup"><span data-stu-id="04c8f-103">Gets an interface pointer to the process of which this ICorDebugThread forms a part.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04c8f-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04c8f-104">Syntax</span></span>  
  
```  
HRESULT GetProcess (  
    [out] ICorDebugProcess   **ppProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="04c8f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="04c8f-105">Parameters</span></span>  
 `ppProcess`  
 <span data-ttu-id="04c8f-106">[out] Un puntatore all'indirizzo di un oggetto di interfaccia ICorDebugProcess che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="04c8f-106">[out] A pointer to the address of an ICorDebugProcess interface object that represents the process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04c8f-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04c8f-107">Requirements</span></span>  
 <span data-ttu-id="04c8f-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04c8f-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04c8f-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="04c8f-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="04c8f-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="04c8f-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="04c8f-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04c8f-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
