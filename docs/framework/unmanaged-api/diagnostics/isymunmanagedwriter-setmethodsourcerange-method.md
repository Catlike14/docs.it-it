---
title: Metodo ISymUnmanagedWriter::SetMethodSourceRange
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedWriter.SetMethodSourceRange
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedWriter::SetMethodSourceRange
helpviewer_keywords:
- SetMethodSourceRange method [.NET Framework debugging]
- ISymUnmanagedWriter::SetMethodSourceRange method [.NET Framework debugging]
ms.assetid: c698b86e-ace7-4b21-9549-f52d6a034959
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 85ed0a73b4862702895e737f2df639b8da7f7679
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedwritersetmethodsourcerange-method"></a><span data-ttu-id="9602e-102">Metodo ISymUnmanagedWriter::SetMethodSourceRange</span><span class="sxs-lookup"><span data-stu-id="9602e-102">ISymUnmanagedWriter::SetMethodSourceRange Method</span></span>
<span data-ttu-id="9602e-103">Specifica l'inizio e fine di un metodo all'interno di un file di origine.</span><span class="sxs-lookup"><span data-stu-id="9602e-103">Specifies the true start and end of a method within a source file.</span></span> <span data-ttu-id="9602e-104">Utilizzare questo metodo per specificare l'estensione di un metodo in modo indipendente da punti di sequenza che esiste all'interno del metodo.</span><span class="sxs-lookup"><span data-stu-id="9602e-104">Use this method to specify the extent of a method independently of the sequence points that exist within the method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9602e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9602e-105">Syntax</span></span>  
  
```  
HRESULT SetMethodSourceRange(  
    [in] ISymUnmanagedDocumentWriter  *startDoc,  
    [in] ULONG32                      startLine,  
    [in] ULONG32                      startColumn,  
    [in] ISymUnmanagedDocumentWriter  *endDoc,  
    [in] ULONG32                      endLine,  
    [in] ULONG32                      endColumn);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9602e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9602e-106">Parameters</span></span>  
 `startDoc`  
 <span data-ttu-id="9602e-107">[in] Puntatore al documento contenente la posizione iniziale.</span><span class="sxs-lookup"><span data-stu-id="9602e-107">[in] A pointer to the document containing the starting position.</span></span>  
  
 `startLine`  
 <span data-ttu-id="9602e-108">[in] Il numero di riga iniziale.</span><span class="sxs-lookup"><span data-stu-id="9602e-108">[in] The starting line number.</span></span>  
  
 `startColumn`  
 <span data-ttu-id="9602e-109">[in] Colonna iniziale.</span><span class="sxs-lookup"><span data-stu-id="9602e-109">[in] The starting column.</span></span>  
  
 `endDoc`  
 <span data-ttu-id="9602e-110">[in] Puntatore al documento contenente la posizione finale.</span><span class="sxs-lookup"><span data-stu-id="9602e-110">[in] A pointer to the document containing the ending position.</span></span>  
  
 `endLine`  
 <span data-ttu-id="9602e-111">[in] Numero di riga finale.</span><span class="sxs-lookup"><span data-stu-id="9602e-111">[in] The ending line number.</span></span>  
  
 `endColumn`  
 <span data-ttu-id="9602e-112">[in] Numero di colonna finale.</span><span class="sxs-lookup"><span data-stu-id="9602e-112">[in] The ending column number.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="9602e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9602e-113">Return Value</span></span>  
 <span data-ttu-id="9602e-114">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="9602e-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9602e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9602e-115">Requirements</span></span>  
 <span data-ttu-id="9602e-116">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="9602e-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9602e-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9602e-117">See Also</span></span>  
 [<span data-ttu-id="9602e-118">ISymUnmanagedWriter (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="9602e-118">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)