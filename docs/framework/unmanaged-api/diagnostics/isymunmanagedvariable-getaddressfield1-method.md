---
title: Metodo ISymUnmanagedVariable::GetAddressField1
ms.date: 03/30/2017
api_name:
- ISymUnmanagedVariable.GetAddressField1
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedVariable::GetAddressField1
helpviewer_keywords:
- GetAddressField1 method [.NET Framework debugging]
- ISymUnmanagedVariable::GetAddressField1 method [.NET Framework debugging]
ms.assetid: 25788ed1-0ce3-4b97-96fc-88f8997812a3
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: f9e0e234a8f77ef35ad93302fe8fc676cf9dbaeb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33427490"
---
# <a name="isymunmanagedvariablegetaddressfield1-method"></a><span data-ttu-id="ff9e5-102">Metodo ISymUnmanagedVariable::GetAddressField1</span><span class="sxs-lookup"><span data-stu-id="ff9e5-102">ISymUnmanagedVariable::GetAddressField1 Method</span></span>
<span data-ttu-id="ff9e5-103">Ottiene il primo campo di indirizzo per la variabile.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-103">Gets the first address field for this variable.</span></span> <span data-ttu-id="ff9e5-104">Il significato dipende dal tipo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-104">Its meaning depends on the kind of address.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ff9e5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff9e5-105">Syntax</span></span>  
  
```  
HRESULT GetAddressField1(  
    [out, retval] ULONG32* pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ff9e5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff9e5-106">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="ff9e5-107">[out] Un puntatore a un `ULONG32` che riceve il primo campo di indirizzo.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-107">[out] A pointer to a `ULONG32` that receives the first address field.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="ff9e5-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff9e5-108">Return Value</span></span>  
 <span data-ttu-id="ff9e5-109">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ff9e5-109">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ff9e5-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff9e5-110">Requirements</span></span>  
 <span data-ttu-id="ff9e5-111">**Intestazione:** CorSym. idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ff9e5-111">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff9e5-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff9e5-112">See Also</span></span>  
 [<span data-ttu-id="ff9e5-113">Interfaccia ISymUnmanagedVariable</span><span class="sxs-lookup"><span data-stu-id="ff9e5-113">ISymUnmanagedVariable Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-interface.md)  
 [<span data-ttu-id="ff9e5-114">Metodo GetAddressField2</span><span class="sxs-lookup"><span data-stu-id="ff9e5-114">GetAddressField2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield2-method.md)  
 [<span data-ttu-id="ff9e5-115">Metodo GetAddressField3</span><span class="sxs-lookup"><span data-stu-id="ff9e5-115">GetAddressField3 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddressfield3-method.md)  
 [<span data-ttu-id="ff9e5-116">Metodo GetAddressKind</span><span class="sxs-lookup"><span data-stu-id="ff9e5-116">GetAddressKind Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedvariable-getaddresskind-method.md)
