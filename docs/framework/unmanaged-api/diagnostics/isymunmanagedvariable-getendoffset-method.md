---
title: Metodo ISymUnmanagedVariable::GetEndOffset
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedVariable.GetEndOffset
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedVariable::GetEndOffset
helpviewer_keywords:
- ISymUnmanagedVariable::GetEndOffset method [.NET Framework debugging]
- GetEndOffset method, ISymUnmanagedVariable interface [.NET Framework debugging]
ms.assetid: e5d777c5-d450-4c0f-999c-b3953ee22cfb
topic_type: apiref
caps.latest.revision: "8"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: f91c2b0f4ecb4cc901a0389d15f4d69e926cf8f6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedvariablegetendoffset-method"></a><span data-ttu-id="16975-102">Metodo ISymUnmanagedVariable::GetEndOffset</span><span class="sxs-lookup"><span data-stu-id="16975-102">ISymUnmanagedVariable::GetEndOffset Method</span></span>
<span data-ttu-id="16975-103">Ottiene l'offset finale di questa variabile all'interno del relativo padre.</span><span class="sxs-lookup"><span data-stu-id="16975-103">Gets the end offset of this variable within its parent.</span></span> <span data-ttu-id="16975-104">Se si tratta di una variabile locale all'interno di un ambito, l'offset finale rientrerà negli offset definiti per l'ambito.</span><span class="sxs-lookup"><span data-stu-id="16975-104">If this is a local variable within a scope, the end offset will fall within the offsets defined for the scope.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="16975-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16975-105">Syntax</span></span>  
  
```  
HRESULT GetEndOffset(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="16975-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16975-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="16975-107">[out] Un puntatore a un `ULONG32` che riceve l'offset finale.</span><span class="sxs-lookup"><span data-stu-id="16975-107">[out] A pointer to a `ULONG32` that receives the end offset.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="16975-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16975-108">Return Value</span></span>  
 <span data-ttu-id="16975-109">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="16975-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="16975-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16975-110">Requirements</span></span>  
 <span data-ttu-id="16975-111">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="16975-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="16975-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="16975-112">See Also</span></span>  
 [<span data-ttu-id="16975-113">Interfaccia ISymUnmanagedVariable</span><span class="sxs-lookup"><span data-stu-id="16975-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 [<span data-ttu-id="16975-114">Metodo GetStartOffset</span><span class="sxs-lookup"><span data-stu-id="16975-114">GetStartOffset Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getstartoffset-method.md)
