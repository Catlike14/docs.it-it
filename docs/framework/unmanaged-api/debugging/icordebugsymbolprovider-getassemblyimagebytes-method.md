---
title: Metodo ICorDebugSymbolProvider::GetAssemblyImageBytes
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
ms.assetid: 3db215aa-e180-4f70-8d23-6d5a0ffbc8e5
caps.latest.revision: "4"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 127ebe82c32e9bf3d06c171d6cbf426d508eacaa
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugsymbolprovidergetassemblyimagebytes-method"></a><span data-ttu-id="4a27c-102">Metodo ICorDebugSymbolProvider::GetAssemblyImageBytes</span><span class="sxs-lookup"><span data-stu-id="4a27c-102">ICorDebugSymbolProvider::GetAssemblyImageBytes Method</span></span>
<span data-ttu-id="4a27c-103">Legge i dati da un assembly sottoposto a merge tramite un indirizzo RVA (Relative Virtual Address) specificato nell'assembly sottoposto a merge.</span><span class="sxs-lookup"><span data-stu-id="4a27c-103">Reads data from a merged assembly given a relative virtual address (RVA) in the merged assembly.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4a27c-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a27c-104">Syntax</span></span>  
  
```  
HRESULT GetAssemblyImageBytes(  
   [in] CORDB_ADDRESS rva,   
   [in] ULONG32 length,   
   [out] ICorDebugMemoryBuffer** ppMemoryBuffer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4a27c-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a27c-105">Parameters</span></span>  
 `rva`  
 <span data-ttu-id="4a27c-106">[in] Indirizzo RVA (Relative Virtual Address) in un assembly sottoposto a merge.</span><span class="sxs-lookup"><span data-stu-id="4a27c-106">[in] A relative virtual address (RVA) in a merged assembly.</span></span>  
  
 `length`  
 <span data-ttu-id="4a27c-107">Numero di byte da leggere dall'assembly sottoposto a merge.</span><span class="sxs-lookup"><span data-stu-id="4a27c-107">The number of bytes to read from the merged assembly.</span></span>  
  
 `ppMemoryBuffer`  
 <span data-ttu-id="4a27c-108">Un puntatore all'indirizzo di un [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) oggetto che contiene informazioni sul buffer di memoria con i metadati dell'assembly sottoposto a merge.</span><span class="sxs-lookup"><span data-stu-id="4a27c-108">A pointer to the address of an [ICorDebugMemoryBuffer](../../../../docs/framework/unmanaged-api/debugging/icordebugmemorybuffer-interface.md) object that contains information about the memory buffer with merged assembly metadata.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="4a27c-109">Note</span><span class="sxs-lookup"><span data-stu-id="4a27c-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="4a27c-110">Questo metodo è disponibile solo con .NET Native.</span><span class="sxs-lookup"><span data-stu-id="4a27c-110">This method is available with .NET Native only.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4a27c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a27c-111">Requirements</span></span>  
 <span data-ttu-id="4a27c-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4a27c-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4a27c-113">**Intestazione:** CorDebug.idl, Cordebug. H</span><span class="sxs-lookup"><span data-stu-id="4a27c-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4a27c-114">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4a27c-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4a27c-115">**Versioni di .NET framework:**[!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4a27c-115">**.NET Framework Versions:** [!INCLUDE[net_46_native](../../../../includes/net-46-native-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4a27c-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4a27c-116">See Also</span></span>  
 [<span data-ttu-id="4a27c-117">Interfaccia ICorDebugSymbolProvider</span><span class="sxs-lookup"><span data-stu-id="4a27c-117">ICorDebugSymbolProvider Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugsymbolprovider-interface.md)  
 [<span data-ttu-id="4a27c-118">Interfacce di debug</span><span class="sxs-lookup"><span data-stu-id="4a27c-118">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)
