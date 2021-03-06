---
title: Metodo ICorDebugFunction2::SetJMCStatus
ms.date: 03/30/2017
api_name:
- ICorDebugFunction2.SetJMCStatus
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugFunction2::SetJMCStatus
helpviewer_keywords:
- ICorDebugFunction2::SetJMCStatus method [.NET Framework debugging]
- SetJMCStatus method, ICorDebugFunction2 interface [.NET Framework debugging]
ms.assetid: 22c27b01-2869-4214-b840-5921f7c874fc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 15b102be5a792f982edeb320199576bdddbd859a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33412360"
---
# <a name="icordebugfunction2setjmcstatus-method"></a>Metodo ICorDebugFunction2::SetJMCStatus
Contrassegna la funzione rappresentata da ICorDebugFunction2 per Just My Code l'esecuzione di istruzioni.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT SetJMCStatus (  
    [in] BOOL   bIsJustMyCode  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `bIsJustMyCode`  
 [in] Impostare su `true` per contrassegnare la funzione come codice utente; in caso contrario, impostato su `false`.  
  
## <a name="return-values"></a>Valori restituiti  
  
|HRESULT|Descrizione|  
|-------------|-----------------|  
|`S_OK`|La funzione è stata contrassegnata.|  
|`CORDBG_E_FUNCTION_NOT_DEBUGGABLE`|Impossibile contrassegnare la funzione come codice utente perché è Impossibile eseguire il debug.|  
  
## <a name="remarks"></a>Note  
 Un Just My Code ignorerà il codice non utente. Il codice utente deve essere un subset di debug.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Cordebug. idl, Cordebug. H  
  
 **Libreria:** CorGuids. lib  
  
 **Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
