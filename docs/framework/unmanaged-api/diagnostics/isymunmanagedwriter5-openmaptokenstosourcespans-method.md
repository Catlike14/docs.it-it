---
title: Metodo ISymUnmanagedWriter5::OpenMapTokensToSourceSpans
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 93ad2517-b0dc-464c-8688-a58a30eda18d
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f226a71ac6381c8ca04093beb1d9772d6e6c75e3
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="isymunmanagedwriter5openmaptokenstosourcespans-method"></a><span data-ttu-id="a98b7-102">Metodo ISymUnmanagedWriter5::OpenMapTokensToSourceSpans</span><span class="sxs-lookup"><span data-stu-id="a98b7-102">ISymUnmanagedWriter5::OpenMapTokensToSourceSpans Method</span></span>
<span data-ttu-id="a98b7-103">Aprire una sezione di dati personalizzati speciali per generare informazioni di mapping span token all'origine in.</span><span class="sxs-lookup"><span data-stu-id="a98b7-103">Open a special custom data section to emit token-to-source span mapping information into.</span></span> <span data-ttu-id="a98b7-104">Apertura di questa sezione quando un metodo è già aperto, o viceversa, è un errore.</span><span class="sxs-lookup"><span data-stu-id="a98b7-104">Opening this section when a method is already open, or vice versa, is an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a98b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a98b7-105">Syntax</span></span>  
  
```idl  
HRESULT OpenMapTokensToSourceSpans();  
```  
  
## <a name="return-value"></a><span data-ttu-id="a98b7-106">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a98b7-106">Return Value</span></span>  
 <span data-ttu-id="a98b7-107">Restituisce `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="a98b7-107">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="a98b7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a98b7-108">Requirements</span></span>  
 <span data-ttu-id="a98b7-109">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="a98b7-109">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a98b7-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a98b7-110">See Also</span></span>  
 [<span data-ttu-id="a98b7-111">Interfaccia ISymUnmanagedWriter5</span><span class="sxs-lookup"><span data-stu-id="a98b7-111">ISymUnmanagedWriter5 Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter5-interface.md)
