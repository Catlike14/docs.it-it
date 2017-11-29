---
title: Metodo ICorDebugFrame::GetCode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugFrame.GetCode
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugFrame::GetCode
helpviewer_keywords:
- GetCode method, ICorDebugFrame interface [.NET Framework debugging]
- ICorDebugFrame::GetCode method [.NET Framework debugging]
ms.assetid: fbaa0794-a031-4015-8beb-2749e47ac340
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e4538526f0358e7fa5259e87cbdf46abdb662475
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugframegetcode-method"></a><span data-ttu-id="75f72-102">Metodo ICorDebugFrame::GetCode</span><span class="sxs-lookup"><span data-stu-id="75f72-102">ICorDebugFrame::GetCode Method</span></span>
<span data-ttu-id="75f72-103">Ottiene un puntatore per il codice associato a questo stack frame.</span><span class="sxs-lookup"><span data-stu-id="75f72-103">Gets a pointer to the code associated with this stack frame.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="75f72-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75f72-104">Syntax</span></span>  
  
```  
HRESULT GetCode (  
    [out] ICorDebugCode      **ppCode  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="75f72-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="75f72-105">Parameters</span></span>  
 `ppCode`  
 <span data-ttu-id="75f72-106">[out] Un puntatore all'indirizzo di un oggetto ICorDebugCode che rappresenta il codice associato a questo frame.</span><span class="sxs-lookup"><span data-stu-id="75f72-106">[out] A pointer to the address of an ICorDebugCode object that represents the code associated with this frame.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="75f72-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75f72-107">Requirements</span></span>  
 <span data-ttu-id="75f72-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="75f72-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="75f72-109">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="75f72-109">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="75f72-110">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="75f72-110">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="75f72-111">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="75f72-111">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>
