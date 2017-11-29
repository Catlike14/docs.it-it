---
title: Metodo ICorRuntimeHost::GetConfiguration
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorRuntimeHost.GetConfiguration
api_location: mscoree.dll
api_type: COM
f1_keywords: ICorRuntimeHost::GetConfiguration
helpviewer_keywords:
- ICorRuntimeHost::GetConfiguration method [.NET Framework hosting]
- GetConfiguration method [.NET Framework hosting]
ms.assetid: c431617a-b055-44a0-8730-48b7a86d9610
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 61c0a95df2140d2eaf771fcd8f50cd733b9133e1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icorruntimehostgetconfiguration-method"></a>Metodo ICorRuntimeHost::GetConfiguration
Ottiene un oggetto che consente all'host specificare la configurazione di callback di common language runtime (CLR).  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT GetConfiguration(  
    [out] ICorConfiguration** pConfiguration  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pConfiguration`  
 [out] Un puntatore all'indirizzo di un [ICorConfiguration](../../../../docs/framework/unmanaged-api/hosting/icorconfiguration-interface.md) oggetto che può essere usato per configurare CLR.  
  
## <a name="remarks"></a>Note  
 CLR deve essere configurato prima dell'inizializzazione; in caso contrario, il `GetConfiguration` metodo restituisce un HRESULT che indica un errore.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Mscoree. H  
  
 **Libreria:** inclusa come risorsa in MSCorEE.dll  
  
 **Versioni di .NET framework:** 1.0, 1.1  
  
## <a name="see-also"></a>Vedere anche  
 [ICorRuntimeHost (interfaccia)](../../../../docs/framework/unmanaged-api/hosting/icorruntimehost-interface.md)
