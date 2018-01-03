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
ms.workload: dotnet
ms.openlocfilehash: 264eac8be96fad0ed72177c2b497f438f08b9f2a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icordebugfunction2enumeratenativecode-method"></a><span data-ttu-id="8d1db-102">Metodo ICorDebugFunction2::EnumerateNativeCode</span><span class="sxs-lookup"><span data-stu-id="8d1db-102">ICorDebugFunction2::EnumerateNativeCode Method</span></span>
<span data-ttu-id="8d1db-103">Ottiene un puntatore a interfaccia a un oggetto ICorDebugCodeEnum che contiene le istruzioni di codice nativo nella funzione a cui fa riferimento questo oggetto ICorDebugFunction2.</span><span class="sxs-lookup"><span data-stu-id="8d1db-103">Gets an interface pointer to an ICorDebugCodeEnum object that contains the native code statements in the function referenced by this ICorDebugFunction2 object.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8d1db-104">`EnumerateNativeCode`non è implementata nella versione corrente di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="8d1db-104">`EnumerateNativeCode` is not implemented in the current version of the .NET Framework.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8d1db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d1db-105">Syntax</span></span>  
  
```  
HRESULT EnumerateNativeCode (  
    [out] ICorDebugCodeEnum   **ppCodeEnum  
);  
```  
  
## <a name="requirements"></a><span data-ttu-id="8d1db-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d1db-106">Requirements</span></span>  
 <span data-ttu-id="8d1db-107">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="8d1db-107">**Header:** CorDebug.idl, CorDebug.h</span></span>
