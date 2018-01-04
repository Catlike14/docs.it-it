---
title: Metodo ISymUnmanagedVariable::GetAddressField1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedVariable.GetAddressField1
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedVariable::GetAddressField1
helpviewer_keywords:
- GetAddressField1 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField1 method [.NET Framework debugging]
ms.assetid: 25788ed1-0ce3-4b97-96fc-88f8997812a3
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 8085deb0cdb0b16eddfa39663277ceecdde10341
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanagedvariablegetaddressfield1-method"></a><span data-ttu-id="dc08f-102">Metodo ISymUnmanagedVariable::GetAddressField1</span><span class="sxs-lookup"><span data-stu-id="dc08f-102">ISymUnmanagedVariable::GetAddressField1 Method</span></span>
<span data-ttu-id="dc08f-103">Ottiene il primo campo di indirizzo per la variabile.</span><span class="sxs-lookup"><span data-stu-id="dc08f-103">Gets the first address field for this variable.</span></span> <span data-ttu-id="dc08f-104">Il significato dipende dal tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dc08f-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc08f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc08f-105">Syntax</span></span>  
  
```  
HRESULT GetAddressField1(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dc08f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc08f-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="dc08f-107">[out] Un puntatore a un `ULONG32` che riceve il primo campo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="dc08f-107">[out] A pointer to a `ULONG32` that receives the first address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="dc08f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc08f-108">Return Value</span></span>  
 <span data-ttu-id="dc08f-109">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="dc08f-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="dc08f-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc08f-110">Requirements</span></span>  
 <span data-ttu-id="dc08f-111">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="dc08f-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="dc08f-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc08f-112">See Also</span></span>  
 [<span data-ttu-id="dc08f-113">Interfaccia ISymUnmanagedVariable</span><span class="sxs-lookup"><span data-stu-id="dc08f-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 [<span data-ttu-id="dc08f-114">Metodo GetAddressField2</span><span class="sxs-lookup"><span data-stu-id="dc08f-114">GetAddressField2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield2-method.md)  
 [<span data-ttu-id="dc08f-115">Metodo GetAddressField3</span><span class="sxs-lookup"><span data-stu-id="dc08f-115">GetAddressField3 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield3-method.md)  
 [<span data-ttu-id="dc08f-116">Metodo GetAddressKind</span><span class="sxs-lookup"><span data-stu-id="dc08f-116">GetAddressKind Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)
