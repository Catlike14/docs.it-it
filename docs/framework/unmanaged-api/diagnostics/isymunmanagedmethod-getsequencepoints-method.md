---
title: Metodo ISymUnmanagedMethod::GetSequencePoints
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedMethod.GetSequencePoints
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedMethod::GetSequencePoints
helpviewer_keywords:
- ISymUnmanagedMethod::GetSequencePoints method [.NET Framework debugging]
- GetSequencePoints method [.NET Framework debugging]
ms.assetid: f909ac48-3d8f-49fb-a369-e3d9959151cd
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 3cde9de634534acdeafa40bd7a94c46624e49604
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedmethodgetsequencepoints-method"></a><span data-ttu-id="af005-102">Metodo ISymUnmanagedMethod::GetSequencePoints</span><span class="sxs-lookup"><span data-stu-id="af005-102">ISymUnmanagedMethod::GetSequencePoints Method</span></span>
<span data-ttu-id="af005-103">Ottiene tutti i punti di sequenza all'interno del metodo.</span><span class="sxs-lookup"><span data-stu-id="af005-103">Gets all the sequence points within this method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="af005-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af005-104">Syntax</span></span>  
  
```  
HRESULT GetSequencePoints(  
    [in]  ULONG32  cPoints,  
    [out] ULONG32  *pcPoints,  
    [in, size_is(cPoints)] ULONG32  offsets[],  
    [in, size_is(cPoints)] ISymUnmanagedDocument* documents[],  
    [in, size_is(cPoints)] ULONG32  lines[],  
    [in, size_is(cPoints)] ULONG32  columns[],  
    [in, size_is(cPoints)] ULONG32  endLines[],  
    [in, size_is(cPoints)] ULONG32  endColumns[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="af005-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="af005-105">Parameters</span></span>  
 `cPoints`  
 <span data-ttu-id="af005-106">[in] Oggetto `ULONG32` che riceve le dimensioni del `offsets`, `documents`, `lines`, `columns`, `endLines`, e `endColumns` matrici.</span><span class="sxs-lookup"><span data-stu-id="af005-106">[in] A `ULONG32` that receives the size of the `offsets`, `documents`, `lines`, `columns`, `endLines`, and `endColumns` arrays.</span></span>  
  
 `pcPoints`  
 <span data-ttu-id="af005-107">[out] Un puntatore a un `ULONG32` che riceve la lunghezza del buffer necessaria per contenere i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-107">[out] A pointer to a `ULONG32` that receives the length of the buffer required to contain the sequence points.</span></span>  
  
 `offsets`  
 <span data-ttu-id="af005-108">[in] Matrice in cui archiviare il Microsoft intermedio language (MSIL) viene eseguito l'offset dall'inizio del metodo per i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-108">[in] An array in which to store the Microsoft intermediate language (MSIL) offsets from the beginning of the method for the sequence points.</span></span>  
  
 `documents`  
 <span data-ttu-id="af005-109">[in] Matrice in cui archiviare i documenti in cui si trovano i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-109">[in] An array in which to store the documents in which the sequence points are located.</span></span>  
  
 `lines`  
 <span data-ttu-id="af005-110">[in] Matrice in cui archiviare le righe dei documenti in cui sono posizionati i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-110">[in] An array in which to store the lines in the documents at which the sequence points are located.</span></span>  
  
 `columns`  
 <span data-ttu-id="af005-111">[in] Matrice in cui archiviare le colonne dei documenti in cui sono posizionati i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-111">[in] An array in which to store the columns in the documents at which the sequence points are located.</span></span>  
  
 `endLines`  
 <span data-ttu-id="af005-112">[in] Matrice di righe dei documenti in cui terminano i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-112">[in] The array of lines in the documents at which the sequence points end.</span></span>  
  
 `endColumns`  
 <span data-ttu-id="af005-113">[in] Matrice di colonne dei documenti in cui terminano i punti di sequenza.</span><span class="sxs-lookup"><span data-stu-id="af005-113">[in] The array of columns in the documents at which the sequence points end.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="af005-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af005-114">Return Value</span></span>  
 <span data-ttu-id="af005-115">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="af005-115">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="af005-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af005-116">Requirements</span></span>  
 <span data-ttu-id="af005-117">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="af005-117">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="af005-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="af005-118">See Also</span></span>  
 [<span data-ttu-id="af005-119">ISymUnmanagedMethod (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="af005-119">ISymUnmanagedMethod Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedmethod-interface.md)
