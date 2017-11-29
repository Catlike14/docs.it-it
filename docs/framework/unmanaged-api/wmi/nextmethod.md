---
title: Funzione NextMethod (riferimenti alle API non gestite)
description: La funzione NextMethod recupera il metodo successivo nell'enumerazione.
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: NextMethod
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: NextMethod
helpviewer_keywords: NextMethod function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d9b14424bb914be3ba127670e1b6490f79854d6e
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2017
---
# <a name="nextmethod-function"></a><span data-ttu-id="d6408-103">NextMethod (funzione)</span><span class="sxs-lookup"><span data-stu-id="d6408-103">NextMethod function</span></span>
<span data-ttu-id="d6408-104">Recupera un'enumerazione che inizia con una chiamata al metodo successivo [BeginMethodEnumeration](beginmethodenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d6408-104">Retrieves the next method in an enumeration that begins with a call to [BeginMethodEnumeration](beginmethodenumeration.md).</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="d6408-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6408-105">Syntax</span></span>  
  
```  
HRESULT NextMethod (
   [in] int                 vFunc, 
   [in] IWbemClassObject*   ptr, 
   [in] LONG                lFlags,
   [out] BSTR*              pName,
   [out] IWbemClassObject** ppInSignature,
   [out] IWbemClassObject** ppOutSignature   
); 
```  

## <a name="parameters"></a><span data-ttu-id="d6408-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6408-106">Parameters</span></span>

`vFunc`  
<span data-ttu-id="d6408-107">[in] Questo parametro è inutilizzato.</span><span class="sxs-lookup"><span data-stu-id="d6408-107">[in] This parameter is unused.</span></span>

`ptr`  
<span data-ttu-id="d6408-108">[in] Un puntatore a un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) istanza.</span><span class="sxs-lookup"><span data-stu-id="d6408-108">[in] A pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) instance.</span></span>

`lFlags`  
<span data-ttu-id="d6408-109">[in] Riservato.</span><span class="sxs-lookup"><span data-stu-id="d6408-109">[in] Reserved.</span></span> <span data-ttu-id="d6408-110">Questo parametro deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="d6408-110">This parameter must be 0.</span></span>

`pName`  
<span data-ttu-id="d6408-111">[out] Un puntatore che punta a `null` prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="d6408-111">[out] A pointer that points to `null` prior to the call.</span></span> <span data-ttu-id="d6408-112">Quando la funzione restituisce, l'indirizzo di un nuovo `BSTR` che contiene il nome del metodo.</span><span class="sxs-lookup"><span data-stu-id="d6408-112">When the function returns, the address of a new `BSTR` that contains the method name.</span></span> 

`ppSignatureIn`  
<span data-ttu-id="d6408-113">[out] Un puntatore che riceve un puntatore a un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) che contiene il `in` parametri per il metodo.</span><span class="sxs-lookup"><span data-stu-id="d6408-113">[out] A pointer that receives a pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) that contains the `in` parameters for the method.</span></span> 

`ppSignatureOut`  
<span data-ttu-id="d6408-114">[out] Un puntatore che riceve un puntatore a un [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) che contiene il `out` parametri per il metodo.</span><span class="sxs-lookup"><span data-stu-id="d6408-114">[out] A pointer that receives a pointer to an [IWbemClassObject](https://msdn.microsoft.com/library/aa391433%28v=vs.85%29.aspx) that contains the `out` parameters for the method.</span></span> 

## <a name="return-value"></a><span data-ttu-id="d6408-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6408-115">Return value</span></span>

<span data-ttu-id="d6408-116">I seguenti valori restituiti da questa funzione sono definiti nel *WbemCli.h* file di intestazione, oppure è possibile definirli come costanti nel codice:</span><span class="sxs-lookup"><span data-stu-id="d6408-116">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="d6408-117">Costante</span><span class="sxs-lookup"><span data-stu-id="d6408-117">Constant</span></span>  |<span data-ttu-id="d6408-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d6408-118">Value</span></span>  |<span data-ttu-id="d6408-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6408-119">Description</span></span>  |
|---------|---------|---------|
| `WBEM_E_UNEXPECTED` | <span data-ttu-id="d6408-120">0x8004101d</span><span class="sxs-lookup"><span data-stu-id="d6408-120">0x8004101d</span></span> | <span data-ttu-id="d6408-121">Si è verificato alcuna chiamata al [ `BeginEnumeration` ](beginenumeration.md) (funzione).</span><span class="sxs-lookup"><span data-stu-id="d6408-121">There was no call to the [`BeginEnumeration`](beginenumeration.md) function.</span></span> |
| `WBEM_S_NO_ERROR` | <span data-ttu-id="d6408-122">0</span><span class="sxs-lookup"><span data-stu-id="d6408-122">0</span></span> | <span data-ttu-id="d6408-123">La chiamata di funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d6408-123">The function call was successful.</span></span>  |
| `WBEM_S_NO_MORE_DATA` | <span data-ttu-id="d6408-124">0x40005</span><span class="sxs-lookup"><span data-stu-id="d6408-124">0x40005</span></span> | <span data-ttu-id="d6408-125">Non esistono altre proprietà nell'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="d6408-125">There are no more properties in the enumeration.</span></span> |
  
## <a name="remarks"></a><span data-ttu-id="d6408-126">Note</span><span class="sxs-lookup"><span data-stu-id="d6408-126">Remarks</span></span>

<span data-ttu-id="d6408-127">Questa funzione esegue il wrapping di una chiamata al [IWbemClassObject::NextMethod](https://msdn.microsoft.com/library/aa391454(v=vs.85).aspx) metodo.</span><span class="sxs-lookup"><span data-stu-id="d6408-127">This function wraps a call to the [IWbemClassObject::NextMethod](https://msdn.microsoft.com/library/aa391454(v=vs.85).aspx) method.</span></span>

<span data-ttu-id="d6408-128">Il chiamante ha inizio la sequenza di enumerazione chiamando il [BeginMethodEnumeration](beginmethodenumeration.md) funzione e quindi chiama la funzione [NextMethod] fino a quando la funzione restituisce `WBEM_S_NO_MORE_DATA`.</span><span class="sxs-lookup"><span data-stu-id="d6408-128">The caller begins the enumeration sequence by calling the [BeginMethodEnumeration](beginmethodenumeration.md) function, and then calls the [NextMethod] function until the function returns `WBEM_S_NO_MORE_DATA`.</span></span> <span data-ttu-id="d6408-129">Facoltativamente, il chiamante al termine della sequenza chiamando [EndMethodEnumeration](endmethodenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="d6408-129">Optionally, the caller finishes the sequence by calling [EndMethodEnumeration](endmethodenumeration.md).</span></span> <span data-ttu-id="d6408-130">Il chiamante può terminare in anticipo l'enumerazione chiamando [EndMethodEnumeration](endmethodenumeration.md) in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="d6408-130">The caller may terminate the enumeration early by calling [EndMethodEnumeration](endmethodenumeration.md) at any time.</span></span>

## <a name="example"></a><span data-ttu-id="d6408-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="d6408-131">Example</span></span>

<span data-ttu-id="d6408-132">Per un esempio di C++, vedere il [IWbemClassObject::NextMethod](https://msdn.microsoft.com/library/aa391454(v=vs.85).aspx) metodo.</span><span class="sxs-lookup"><span data-stu-id="d6408-132">For a C++ example, see the [IWbemClassObject::NextMethod](https://msdn.microsoft.com/library/aa391454(v=vs.85).aspx) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6408-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6408-133">Requirements</span></span>  
 <span data-ttu-id="d6408-134">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="d6408-134">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d6408-135">**Intestazione:** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="d6408-135">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="d6408-136">**Versioni di .NET framework:**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="d6408-136">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d6408-137">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d6408-137">See also</span></span>  
[<span data-ttu-id="d6408-138">WMI e i contatori delle prestazioni (riferimenti alle API non gestite)</span><span class="sxs-lookup"><span data-stu-id="d6408-138">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)
