---
title: Metodo ISymUnmanagedAsyncMethod::GetAsyncStepInfoCount
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 32a4e084-09b2-4946-a4a7-19a1fed9f7cc
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 6b2431662caa41c67746da7e21591c743896c161
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedasyncmethodgetasyncstepinfocount-method"></a><span data-ttu-id="d40f7-102">Metodo ISymUnmanagedAsyncMethod::GetAsyncStepInfoCount</span><span class="sxs-lookup"><span data-stu-id="d40f7-102">ISymUnmanagedAsyncMethod::GetAsyncStepInfoCount Method</span></span>
<span data-ttu-id="d40f7-103">Vedere [metodo DefineAsyncStepInfo](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span><span class="sxs-lookup"><span data-stu-id="d40f7-103">See [DefineAsyncStepInfo Method](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-defineasyncstepinfo-method.md).</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d40f7-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d40f7-104">Syntax</span></span>  
  
```idl  
HRESULT GetAsyncStepInfoCount(    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d40f7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="d40f7-105">Parameters</span></span>  
  
|<span data-ttu-id="d40f7-106">Parametro</span><span class="sxs-lookup"><span data-stu-id="d40f7-106">Parameter</span></span>|<span data-ttu-id="d40f7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d40f7-107">Description</span></span>|  
|---------------|-----------------|  
|`pRetVal`||  
  
## <a name="return-value"></a><span data-ttu-id="d40f7-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d40f7-108">Return Value</span></span>  
 <span data-ttu-id="d40f7-109">Restituisce `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="d40f7-109">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d40f7-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d40f7-110">Requirements</span></span>  
 <span data-ttu-id="d40f7-111">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="d40f7-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d40f7-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d40f7-112">See Also</span></span>  
 [<span data-ttu-id="d40f7-113">Interfaccia ISymUnmanagedAsyncMethod</span><span class="sxs-lookup"><span data-stu-id="d40f7-113">ISymUnmanagedAsyncMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethod-interface.md)
