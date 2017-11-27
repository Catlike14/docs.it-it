---
title: Metodo ISymUnmanagedWriter::CloseMethod
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedWriter.CloseMethod
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedWriter::CloseMethod
helpviewer_keywords:
- ISymUnmanagedWriter::CloseMethod method [.NET Framework debugging]
- CloseMethod method [.NET Framework debugging]
ms.assetid: b8025e04-f0e5-40c8-849c-8cd51323420e
topic_type: apiref
caps.latest.revision: "7"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: ea4f917a5e553eb2541f20ce08d403adc7d86d44
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="isymunmanagedwriterclosemethod-method"></a><span data-ttu-id="4121c-102">Metodo ISymUnmanagedWriter::CloseMethod</span><span class="sxs-lookup"><span data-stu-id="4121c-102">ISymUnmanagedWriter::CloseMethod Method</span></span>
<span data-ttu-id="4121c-103">Chiude il metodo corrente.</span><span class="sxs-lookup"><span data-stu-id="4121c-103">Closes the current method.</span></span> <span data-ttu-id="4121c-104">Dopo un metodo è stato chiuso, non vi sono ulteriori simboli possono essere definiti all'interno di esso.</span><span class="sxs-lookup"><span data-stu-id="4121c-104">Once a method is closed, no more symbols can be defined within it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4121c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4121c-105">Syntax</span></span>  
  
```  
HRESULT CloseMethod();  
```  
  
## <a name="return-value"></a><span data-ttu-id="4121c-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4121c-106">Return Value</span></span>  
 <span data-ttu-id="4121c-107">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4121c-107">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4121c-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4121c-108">Requirements</span></span>  
 <span data-ttu-id="4121c-109">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="4121c-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4121c-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4121c-110">See Also</span></span>  
 [<span data-ttu-id="4121c-111">ISymUnmanagedWriter (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="4121c-111">ISymUnmanagedWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)  
 [<span data-ttu-id="4121c-112">OpenMethod (metodo)</span><span class="sxs-lookup"><span data-stu-id="4121c-112">OpenMethod Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-openmethod-method.md)
