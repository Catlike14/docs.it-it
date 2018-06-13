---
title: Funzione CoInitializeCor
ms.date: 03/30/2017
api_name:
- CoInitializeCor
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- CoInitializeCor
helpviewer_keywords:
- CoInitializeCor function [.NET Framework hosting]
ms.assetid: 9b9079fb-579e-4141-b3f0-791072dd40dc
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 91315e8af0cc46a3450a7515b885988cffe34927
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33429988"
---
# <a name="coinitializecor-function"></a>Funzione CoInitializeCor
`CoInitializeCor` è obsoleto.  
  
## <a name="syntax"></a>Sintassi  
  
```  
STDAPI CoInitializeCor (  
    DWORD fFlags  
);  
```  
  
## <a name="remarks"></a>Note  
 Per inizializzare common language runtime, utilizzare [CorBindToRuntimeEx](../../../../docs/framework/unmanaged-api/hosting/corbindtoruntimeex-function.md) o [CorBindToCurrentRuntime](../../../../docs/framework/unmanaged-api/hosting/corbindtocurrentruntime-function.md).  
  
## <a name="requirements"></a>Requisiti  
 **Intestazione:** Cor. h  
  
## <a name="see-also"></a>Vedere anche  
 [Funzioni statiche globali dei metadati](../../../../docs/framework/unmanaged-api/metadata/metadata-global-static-functions.md)
