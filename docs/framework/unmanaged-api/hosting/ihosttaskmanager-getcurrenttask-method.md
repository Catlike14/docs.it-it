---
title: Metodo IHostTaskManager::GetCurrentTask
ms.date: 03/30/2017
api_name:
- IHostTaskManager.GetCurrentTask
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- IHostTaskManager::GetCurrentTask
helpviewer_keywords:
- GetCurrentTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::GetCurrentTask method [.NET Framework hosting]
ms.assetid: f17bca49-90bd-4dee-a5e1-b9a57ea46f85
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2420ddb5cf9be2cfb08f89d27d9aa277305e7ffb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33442692"
---
# <a name="ihosttaskmanagergetcurrenttask-method"></a>Metodo IHostTaskManager::GetCurrentTask
Ottiene un puntatore a interfaccia per l'attività attualmente in esecuzione sul thread del sistema operativo da cui viene effettuata la chiamata.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetCurrentTask (  
    [out] IHostTask **pTask  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pTask`  
 [out] Un puntatore all'indirizzo di un [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) istanza che rappresenta l'attività attualmente in esecuzione, o null, se nessuna attività è in esecuzione.  
  
## <a name="return-value"></a>Valore restituito  
  
|HRESULT|Descrizione|  
|-------------|-----------------|  
|S_OK|`GetCurrentTask` stato restituito correttamente.|  
|HOST_E_CLRNOTAVAILABLE|Common language runtime (CLR) non è stato caricato in un processo oppure si trova in uno stato in cui non può eseguire codice gestito o elaborare correttamente la chiamata.|  
|HOST_E_TIMEOUT|Timeout della chiamata.|  
|HOST_E_NOT_OWNER|Il chiamante non dispone del blocco.|  
|HOST_E_ABANDONED|Un evento è stato annullato mentre un thread bloccato o fiber era in attesa su di esso.|  
|E_FAIL|Si è verificato un errore irreversibile sconosciuto. Quando un metodo viene restituito E_FAIL, Common Language Runtime non è più utilizzabile all'interno del processo. Le chiamate successive ai metodi di hosting restituiranno HOST_E_CLRNOTAVAILABLE.|  
|HOST_E_INVALIDOPERATION|`GetCurrentTask` è stato chiamato su un thread del sistema operativo all'esterno del controllo dell'host.|  
  
## <a name="remarks"></a>Note  
 L'host può anche impostare il `pTask` parametro su null per impedire che un'attività che non rientrano nel CLR.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Mscoree. H  
  
 **Libreria:** inclusa come risorsa in Mscoree. dll  
  
 **Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Interfaccia ICLRTask](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [Interfaccia ICLRTaskManager](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [Interfaccia IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [Interfaccia IHostTaskManager](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)
