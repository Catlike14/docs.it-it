---
title: Metodo ICorDebugThread::GetUserState
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugThread.GetUserState
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugThread::GetUserState
helpviewer_keywords:
- GetUserState method, ICorDebugThread interface [.NET Framework debugging]
- ICorDebugThread::GetUserState method [.NET Framework debugging]
ms.assetid: ae0cfd73-8ead-4d36-9310-dccaac9db0bd
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 48a86317774a3ebba4ed600b880110a7adaa02a7
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugthreadgetuserstate-method"></a><span data-ttu-id="8a5b7-102">Metodo ICorDebugThread::GetUserState</span><span class="sxs-lookup"><span data-stu-id="8a5b7-102">ICorDebugThread::GetUserState Method</span></span>
<span data-ttu-id="8a5b7-103">Ottiene lo stato corrente dell'ICorDebugThread.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-103">Gets the current user state of this ICorDebugThread.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8a5b7-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a5b7-104">Syntax</span></span>  
  
```  
HRESULT GetUserState (  
    [out] CorDebugUserState   *pState  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="8a5b7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a5b7-105">Parameters</span></span>  
 `pState`  
 <span data-ttu-id="8a5b7-106">[out] Un puntatore a una combinazione bit per bit dei valori di enumerazione CorDebugUserState che descrivono lo stato utente corrente di questo thread.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-106">[out] A pointer to a bitwise combination of CorDebugUserState enumeration values that describe the current user state of this thread.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="8a5b7-107">Note</span><span class="sxs-lookup"><span data-stu-id="8a5b7-107">Remarks</span></span>  
 <span data-ttu-id="8a5b7-108">Quando viene esaminato dal programma che viene eseguito il debug, lo stato utente del thread è lo stato del thread.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-108">The user state of the thread is the state of the thread when it is examined by the program that is being debugged.</span></span> <span data-ttu-id="8a5b7-109">Un thread può avere più bit di stato impostato.</span><span class="sxs-lookup"><span data-stu-id="8a5b7-109">A thread may have multiple state bits set.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8a5b7-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8a5b7-110">Requirements</span></span>  
 <span data-ttu-id="8a5b7-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="8a5b7-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="8a5b7-112">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="8a5b7-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="8a5b7-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="8a5b7-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="8a5b7-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="8a5b7-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
