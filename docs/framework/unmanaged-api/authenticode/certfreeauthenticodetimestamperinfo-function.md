---
title: Funzione CertFreeAuthenticodeTimestamperInfo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: CertFreeAuthenticodeTimestamperInfo
api_location: clr.dll
api_type: DLLExport
ms.assetid: 3eb14c49-68c2-4516-ac89-e5bd7473831c
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: b8b6392e57e641d25d07580fcb6bf630f8d983be
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="certfreeauthenticodetimestamperinfo-function"></a>Funzione CertFreeAuthenticodeTimestamperInfo
Libera le risorse allocate per il [AXL_AUTHENTICODE_TIMESTAMPER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md) struttura.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT CertFreeAuthenticodeTimestamperInfo (  
    [in, out]  PAXL_AUTHENTICODE_TIMESTAMPER_INFO   pTimestamperInfo  
);  
```  
  
#### <a name="parameters"></a>Parametri  
 `pTimestamperInfo`  
 [in, out] Informazioni relative a chi ha apposto il timestamp da rilasciare. Vedere il [AXL_AUTHENTICODE_TIMESTAMPER_INFO](../../../../docs/framework/unmanaged-api/authenticode/axl-authenticode-timestamper-info-structure.md) struttura.  
  
## <a name="return-value"></a>Valore restituito  
 `S_OK` se la funzione ha esito positivo. In caso contrario, verrà restituito un codice di errore.  
  
## <a name="see-also"></a>Vedere anche  
 [Authenticode](../../../../docs/framework/unmanaged-api/authenticode/index.md)
