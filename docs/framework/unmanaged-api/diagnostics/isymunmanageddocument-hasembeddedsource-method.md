---
title: Metodo ISymUnmanagedDocument::HasEmbeddedSource
ms.date: 03/30/2017
api_name:
- ISymUnmanagedDocument.HasEmbeddedSource
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedDocument::HasEmbeddedSource
helpviewer_keywords:
- HasEmbeddedSource method [.NET Framework debugging]
- ISymUnmanagedDocument::HasEmbeddedSource method [.NET Framework debugging]
ms.assetid: 385fc4d3-365c-4645-b7b0-6c4c5344b79f
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 350aecb9f9c99c9aa44ae6df6d31c7cb69ae5760
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33430345"
---
# <a name="isymunmanageddocumenthasembeddedsource-method"></a><span data-ttu-id="7d0bf-102">Metodo ISymUnmanagedDocument::HasEmbeddedSource</span><span class="sxs-lookup"><span data-stu-id="7d0bf-102">ISymUnmanagedDocument::HasEmbeddedSource Method</span></span>
<span data-ttu-id="7d0bf-103">Restituisce `true` se il documento di origine è incorporata nei simboli di debug; in caso contrario, restituisce `false`.</span><span class="sxs-lookup"><span data-stu-id="7d0bf-103">Returns `true` if the document has source embedded in the debugging symbols; otherwise, returns `false`.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7d0bf-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d0bf-104">Syntax</span></span>  
  
```  
HRESULT HasEmbeddedSource(  
   [out, retval]  BOOL  *pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7d0bf-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d0bf-105">Parameters</span></span>  
 `pRetVal`  
 <span data-ttu-id="7d0bf-106">[out] Un puntatore a una variabile che indica se il documento di origine è incorporata nei simboli di debug.</span><span class="sxs-lookup"><span data-stu-id="7d0bf-106">[out] A pointer to a variable that indicates whether the document has source embedded in the debugging symbols.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="7d0bf-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7d0bf-107">Return Value</span></span>  
 <span data-ttu-id="7d0bf-108">S_OK se il metodo ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7d0bf-108">S_OK if the method succeeds.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d0bf-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7d0bf-109">See Also</span></span>  
 [<span data-ttu-id="7d0bf-110">Interfaccia ISymUnmanagedDocument</span><span class="sxs-lookup"><span data-stu-id="7d0bf-110">ISymUnmanagedDocument Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanageddocument-interface.md)
