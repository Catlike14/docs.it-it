---
title: Metodo ICorDebugFunction2::EnumerateNativeCode
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugFunction2.EnumerateNativeCode
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugFunction2::EnumerateNativeCode
helpviewer_keywords:
- ICorDebugFunction2::EnumerateNativeCode method [.NET Framework debugging]
- EnumerateNativeCode method [.NET Framework debugging]
ms.assetid: d383f5cc-1144-4b6d-b57a-db34d9134ab2
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2553c8d5e2d2e5b27f56487250c5d3f54c2786d9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugfunction2enumeratenativecode-method"></a>Metodo ICorDebugFunction2::EnumerateNativeCode
Ottiene un puntatore a interfaccia a un oggetto ICorDebugCodeEnum che contiene le istruzioni di codice nativo nella funzione a cui fa riferimento questo oggetto ICorDebugFunction2.  
  
> [!NOTE]
>  `EnumerateNativeCode`non è implementata nella versione corrente di .NET Framework.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT EnumerateNativeCode (  
    [out] ICorDebugCodeEnum   **ppCodeEnum  
);  
```  
  
## <a name="requirements"></a>Requisiti  
 **Intestazione:** CorDebug.idl, Cordebug. H
