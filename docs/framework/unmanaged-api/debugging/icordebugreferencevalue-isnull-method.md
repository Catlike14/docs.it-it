---
title: Metodo ICorDebugReferenceValue::IsNull
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugReferenceValue.IsNull
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugReferenceValue::IsNull
helpviewer_keywords:
- IsNull method, ICorDebugReferenceValue interface [.NET Framework debugging]
- ICorDebugReferenceValue::IsNull method [.NET Framework debugging]
ms.assetid: 99e8c8d7-a1c0-47c8-9dbd-03e0b2bcb4d5
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 53eaa411dc405142461de99bc787eba7a5d52db6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugreferencevalueisnull-method"></a>Metodo ICorDebugReferenceValue::IsNull
Ottiene un valore che indica se l'interfaccia ICorDebugReferenceValue è un valore null, nel qual caso il `ICorDebugReferenceValue` non punta a un oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT IsNull (  
    [out] BOOL   *pbNull  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pbNull`  
 [out] Un puntatore a un valore booleano che è `true` se `ICorDebugReferenceValue` oggetto è null; in caso contrario, `pbNull` è `false`.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** CorDebug.idl, Cordebug. H  
  
 **Libreria:** CorGuids.lib  
  
 **Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
