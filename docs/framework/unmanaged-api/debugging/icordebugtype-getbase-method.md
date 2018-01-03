---
title: Metodo ICorDebugType::GetBase
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugType.GetBase
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugType::GetBase
helpviewer_keywords:
- ICorDebugType::GetBase method [.NET Framework debugging]
- GetBase method [.NET Framework debugging]
ms.assetid: f24e1af9-c220-4f79-ae62-4153ec17ea81
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c28c88988155cf5e00897858d4306e4cb2ea78a3
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugtypegetbase-method"></a><span data-ttu-id="a8ede-102">Metodo ICorDebugType::GetBase</span><span class="sxs-lookup"><span data-stu-id="a8ede-102">ICorDebugType::GetBase Method</span></span>
<span data-ttu-id="a8ede-103">Ottiene un puntatore a interfaccia ICorDebugType che rappresenta il tipo di base, se presente, del tipo rappresentato da questo `ICorDebugType`.</span><span class="sxs-lookup"><span data-stu-id="a8ede-103">Gets an interface pointer to an ICorDebugType that represents the base type, if one exists, of the type represented by this `ICorDebugType`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a8ede-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a8ede-104">Syntax</span></span>  
  
```  
HRESULT GetBase (  
    [out] ICorDebugType   **pBase  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a8ede-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="a8ede-105">Parameters</span></span>  
 `pBase`  
 <span data-ttu-id="a8ede-106">[out] Un puntatore all'indirizzo di un `ICorDebugType` oggetto che rappresenta il tipo di base.</span><span class="sxs-lookup"><span data-stu-id="a8ede-106">[out] A pointer to the address of an `ICorDebugType` object that represents the base type.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a8ede-107">Note</span><span class="sxs-lookup"><span data-stu-id="a8ede-107">Remarks</span></span>  
 <span data-ttu-id="a8ede-108">Cercare il tipo di base per un tipo è utile per implementare le funzionalità comuni del debugger, ad esempio la stampa tutti i campi di un oggetto o le relative classi padre.</span><span class="sxs-lookup"><span data-stu-id="a8ede-108">Looking up the base type for a type is useful to implement common debugger functionality, such as printing out all the fields of an object or its parent classes.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a8ede-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a8ede-109">Requirements</span></span>  
 <span data-ttu-id="a8ede-110">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="a8ede-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="a8ede-111">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="a8ede-111">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="a8ede-112">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="a8ede-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="a8ede-113">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="a8ede-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>
