---
title: Metodo ICorDebugProcess::EnableLogMessages
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcess.EnableLogMessages
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcess::EnableLogMessages
helpviewer_keywords:
- ICorDebugProcess::EnableLogMessages method [.NET Framework debugging]
- EnableLogMessages method [.NET Framework debugging]
ms.assetid: 14a4e5a3-3eaf-4f53-9dd1-762726963a23
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: e7aecb0c72b58d1d46c3fd4d1137d6c303453706
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugprocessenablelogmessages-method"></a>Metodo ICorDebugProcess::EnableLogMessages
Abilita e disabilita la trasmissione dei messaggi di log al debugger.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT EnableLogMessages([in]BOOL fOnOff);  
```  
  
#### <a name="parameters"></a>Parametri  
 `fOnOff`  
 [in] `true` consente la trasmissione di messaggi di log. `false` disabilita la trasmissione.  
  
## <a name="remarks"></a>Note  
 Questo metodo è valido solo dopo il [ICorDebugManagedCallback::](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-createprocess-method.md) callback si verifica.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** CorDebug.idl, Cordebug. H  
  
 **Libreria:** CorGuids.lib  
  
 **Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]
