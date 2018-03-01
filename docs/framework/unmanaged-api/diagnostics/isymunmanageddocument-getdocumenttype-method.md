---
title: Metodo ISymUnmanagedDocument::GetDocumentType
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name:
- ISymUnmanagedDocument.GetDocumentType
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::GetDocumentType
helpviewer_keywords:
- ISymUnmanagedDocument::GetDocumentType method [.NET Framework debugging]
- GetDocumentType method [.NET Framework debugging]
ms.assetid: 2d381ab1-7e7c-4281-af2b-e54d879b3ef8
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 3b6e2d81680c2aa5973c0095a6a3ba7cfa158031
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="isymunmanageddocumentgetdocumenttype-method"></a><span data-ttu-id="7f9cf-102">Metodo ISymUnmanagedDocument::GetDocumentType</span><span class="sxs-lookup"><span data-stu-id="7f9cf-102">ISymUnmanagedDocument::GetDocumentType Method</span></span>
<span data-ttu-id="7f9cf-103">Ottiene il tipo di questo documento.</span><span class="sxs-lookup"><span data-stu-id="7f9cf-103">Gets the document type of this document.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7f9cf-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f9cf-104">Syntax</span></span>  
  
```  
HRESULT GetDocumentType(  
    [out, retval] GUID*  pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7f9cf-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f9cf-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="7f9cf-106">[out] Puntatore a una variabile che riceve il tipo di documento.</span><span class="sxs-lookup"><span data-stu-id="7f9cf-106">[out] Pointer to a variable that receives the document type.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7f9cf-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f9cf-107">Return Value</span></span>  
 <span data-ttu-id="7f9cf-108">S_OK se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7f9cf-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7f9cf-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7f9cf-109">See Also</span></span>  
 [<span data-ttu-id="7f9cf-110">Interfaccia ISymUnmanagedDocument</span><span class="sxs-lookup"><span data-stu-id="7f9cf-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
