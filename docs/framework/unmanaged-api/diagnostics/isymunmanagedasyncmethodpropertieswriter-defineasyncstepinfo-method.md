---
title: Metodo ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo
ms.date: 03/30/2017
ms.assetid: f738a6ed-7cd9-4106-a5cd-355481e5771c
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 3ebd4bb1d674a27785ccbe5460a65fed764638ea
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33435877"
---
# <a name="isymunmanagedasyncmethodpropertieswriterdefineasyncstepinfo-method"></a><span data-ttu-id="ad1a3-102">Metodo ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo</span><span class="sxs-lookup"><span data-stu-id="ad1a3-102">ISymUnmanagedAsyncMethodPropertiesWriter::DefineAsyncStepInfo Method</span></span>
<span data-ttu-id="ad1a3-103">Definire un gruppo di async await operazioni nel metodo corrente.</span><span class="sxs-lookup"><span data-stu-id="ad1a3-103">Define a group of async await operations in the current method.</span></span>  
  
 <span data-ttu-id="ad1a3-104">Istruzione return di un await, che identifica un potenziale rendimento corrisponde a ogni offset yield.</span><span class="sxs-lookup"><span data-stu-id="ad1a3-104">Each yield offset matches an await's return instruction, identifying a potential yield.</span></span> <span data-ttu-id="ad1a3-105">Ogni `breakpointMethod` / `breakpointOffset` coppia indica dove verrà ripreso l'operazione asincrona, (che può essere un altro metodo.</span><span class="sxs-lookup"><span data-stu-id="ad1a3-105">Each `breakpointMethod`/`breakpointOffset` pair tells us where the asynchronous operation will resume,(which could be in a different method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ad1a3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad1a3-106">Syntax</span></span>  
  
```idl  
HRESULT DefineAsyncStepInfo(    [in] ULONG32 count,    [in, size_is(count)] ULONG32 yieldOffsets[],    [in, size_is(count)] ULONG32 breakpointOffset[],     [in, size_is(count)] mdToken breakpointMethod[]);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad1a3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad1a3-107">Parameters</span></span>  
  
|<span data-ttu-id="ad1a3-108">Parametro</span><span class="sxs-lookup"><span data-stu-id="ad1a3-108">Parameter</span></span>|<span data-ttu-id="ad1a3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad1a3-109">Description</span></span>|  
|---------------|-----------------|  
|`count`||  
|`yieldOffsets`||  
|`breakpointOffset`||  
|`breakpointMethod`||  
  
## <a name="return-value"></a><span data-ttu-id="ad1a3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad1a3-110">Return Value</span></span>  
 <span data-ttu-id="ad1a3-111">Restituisce `HRESULT`.</span><span class="sxs-lookup"><span data-stu-id="ad1a3-111">Returns `HRESULT`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ad1a3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad1a3-112">Requirements</span></span>  
 <span data-ttu-id="ad1a3-113">**Intestazione:** CorSym. idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="ad1a3-113">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ad1a3-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ad1a3-114">See Also</span></span>  
 [<span data-ttu-id="ad1a3-115">Interfaccia ISymUnmanagedAsyncMethodPropertiesWriter</span><span class="sxs-lookup"><span data-stu-id="ad1a3-115">ISymUnmanagedAsyncMethodPropertiesWriter Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedasyncmethodpropertieswriter-interface.md)
