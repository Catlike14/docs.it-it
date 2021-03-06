---
title: Enumerazione EMemoryCriticalLevel
ms.date: 03/30/2017
api_name:
- EMemoryCriticalLevel
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- EMemoryCriticalLevel
helpviewer_keywords:
- EMemoryCriticalLevel enumeration [.NET Framework hosting]
ms.assetid: 2ca8a7a2-7b54-4ba3-8e73-277c7df485f3
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: acf4f3f582e417c5e7b814622986427f996796ce
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33432527"
---
# <a name="ememorycriticallevel-enumeration"></a>Enumerazione EMemoryCriticalLevel
Contiene valori che indicano l'impatto di un errore quando un'allocazione di memoria specifico è stato richiesto ma non può essere soddisfatta.  
  
## <a name="syntax"></a>Sintassi  
  
```  
typedef enum {  
    eTaskCritical      = 0,  
    eAppDomainCritical = 1,  
    eProcessCritical   = 2  
} EMemoryCriticalLevel;  
```  
  
## <a name="members"></a>Membri  
  
|Membro|Descrizione|  
|------------|-----------------|  
|`eAppDomainCritical`|Indica che l'allocazione è critica per l'esecuzione di codice gestito nel dominio che ha richiesto l'allocazione. Se la memoria non può essere allocata, Common Language Runtime non garantisce che il dominio è ancora utilizzabile. L'host decide l'azione da intraprendere quando non è possibile soddisfare l'allocazione. È possibile indicare a CLR di interrompere il `AppDomain` , automaticamente o consentire di continuare l'esecuzione chiamando metodi sulla [ICLRPolicyManager](../../../../docs/framework/unmanaged-api/hosting/iclrpolicymanager-interface.md).|  
|`eProcessCritical`|Indica che l'allocazione è fondamentale per l'esecuzione di codice gestito nel processo. Questo valore viene utilizzato durante l'avvio e durante l'esecuzione dei finalizzatori. Se la memoria non può essere allocata, Common Language Runtime non può operare nel processo. Se l'allocazione ha esito negativo, CLR è disabilitato. Tutte le chiamate successive a CLR esito negativo con HOST_E_CLRNOTAVAILABLE.|  
|`eTaskCritical`|Indica che l'allocazione è fondamentale per l'esecuzione dell'attività che ha richiesto l'allocazione. Se la memoria non può essere allocata, Common Language Runtime non garantisce che l'attività può essere eseguita. In caso di errore, CLR genera un <xref:System.Threading.ThreadAbortException> sul thread del sistema operazione fisica.|  
  
## <a name="remarks"></a>Note  
 I metodi di allocazione di memoria definiti nel [IHostMemoryManager](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md) e [IHostMAlloc](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-interface.md) interfacce accettano un parametro di questo tipo. In base alla gravità dell'errore, un host può decidere se eseguire immediatamente la richiesta di allocazione o attendere finché può essere soddisfatta.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Mscoree. H  
  
 **Libreria:** Mscoree. dll  
  
 **Versioni di .NET framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Interfaccia ICLRMemoryNotificationCallback](../../../../docs/framework/unmanaged-api/hosting/iclrmemorynotificationcallback-interface.md)  
 [Enumerazioni di hosting](../../../../docs/framework/unmanaged-api/hosting/hosting-enumerations.md)
