---
title: Struttura BucketParameters
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: BucketParameters
api_location: mscoree.dll
api_type: COM
f1_keywords: BucketParameters
helpviewer_keywords: BucketParameters structure [.NET Framework hosting]
ms.assetid: 9432487e-f276-45d6-9a13-9a68024dbd46
topic_type: apiref
caps.latest.revision: "8"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 7626ce6b2b6278be7cd9989718c13f7c98e4ace3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="bucketparameters-structure"></a>Struttura BucketParameters
Archivia il nome del tipo di un evento e i parametri per l'eccezione corrente viene associato all'evento.  
  
## <a name="syntax"></a>Sintassi  
  
```  
typedef struct _BucketParameters {  
    BOOL  fInited;                    
    WCHAR pszEventTypeName[255];      
    WCHAR pszParams[10][255];         
} BucketParameters;  
```  
  
## <a name="members"></a>Membri  
  
|Membro|Descrizione|  
|------------|-----------------|  
|`fInited`|`true`, se il resto di questa struttura è valido. in caso contrario, `false`.|  
|`pszEventTypeName`|Nome del tipo di evento.|  
|`pszParams`|Matrice di stringhe, ognuna delle quali specifica un parametro per l'eccezione corrente associato all'evento.|  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Mscoree  
  
 **Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Strutture di hosting](../../../../docs/framework/unmanaged-api/hosting/hosting-structures.md)
