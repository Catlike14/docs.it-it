---
title: Metodo ICorDebugStaticFieldSymbol::GetAddress
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 5a6c9a5a-ec72-4c40-a9c3-cee7baa63687
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 20c0c934772625d27057957d00e53fb4b485c4fd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugstaticfieldsymbolgetaddress-method"></a><span data-ttu-id="e78ad-102">Metodo ICorDebugStaticFieldSymbol::GetAddress</span><span class="sxs-lookup"><span data-stu-id="e78ad-102">ICorDebugStaticFieldSymbol::GetAddress Method</span></span>
<span data-ttu-id="e78ad-103">Ottiene l'indirizzo di un campo statico.</span><span class="sxs-lookup"><span data-stu-id="e78ad-103">Gets the address of a static field.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e78ad-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e78ad-104">Syntax</span></span>  
  
```  
HRESULT GetAddress(  
   [out] CORDB_ADDRESS *pRVA  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e78ad-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="e78ad-105">Parameters</span></span>  
 <span data-ttu-id="e78ad-106">pRVA</span><span class="sxs-lookup"><span data-stu-id="e78ad-106">pRVA</span></span>  
 <span data-ttu-id="e78ad-107">[out] Puntatore all'indirizzo RVA (Relative Virtual Address) del campo statico.</span><span class="sxs-lookup"><span data-stu-id="e78ad-107">[out] A pointer to the relative virtual address (RVA) of the static field.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e78ad-108">Note</span><span class="sxs-lookup"><span data-stu-id="e78ad-108">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e78ad-109">Questo metodo è disponibile solo con .NET Native.</span><span class="sxs-lookup"><span data-stu-id="e78ad-109">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e78ad-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e78ad-110">Requirements</span></span>  
 <span data-ttu-id="e78ad-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="e78ad-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e78ad-112">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="e78ad-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="e78ad-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="e78ad-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="e78ad-114">**Versioni di .NET framework:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e78ad-114">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e78ad-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e78ad-115">See Also</span></span>  
 [<span data-ttu-id="e78ad-116">Interfaccia ICorDebugStaticFieldSymbol</span><span class="sxs-lookup"><span data-stu-id="e78ad-116">ICorDebugStaticFieldSymbol Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstaticfieldsymbol-interface.md)  
 [<span data-ttu-id="e78ad-117">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="e78ad-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
