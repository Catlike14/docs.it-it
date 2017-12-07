---
title: Interfaccia IHostMalloc
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostMAlloc
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostMAlloc
helpviewer_keywords: IHostMAlloc interface [.NET Framework hosting]
ms.assetid: e3c6643b-6fc7-4a99-959d-4b7b4e63fdee
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: f788456065a5508441b9fec38ad4a7f531f9f303
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ihostmalloc-interface"></a><span data-ttu-id="874cc-102">Interfaccia IHostMalloc</span><span class="sxs-lookup"><span data-stu-id="874cc-102">IHostMalloc Interface</span></span>
<span data-ttu-id="874cc-103">Fornisce metodi che consentono a common language runtime (CLR) per richiedere di allocare dall'heap tramite l'host.</span><span class="sxs-lookup"><span data-stu-id="874cc-103">Provides methods that allow the common language runtime (CLR) to request fine-grained allocations from the heap through the host.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="874cc-104">Metodi</span><span class="sxs-lookup"><span data-stu-id="874cc-104">Methods</span></span>  
  
|<span data-ttu-id="874cc-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="874cc-105">Method</span></span>|<span data-ttu-id="874cc-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="874cc-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="874cc-107">Alloc (metodo)</span><span class="sxs-lookup"><span data-stu-id="874cc-107">Alloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-alloc-method.md)|<span data-ttu-id="874cc-108">Richieste all'host di allocare la quantità di memoria richiesta dall'heap.</span><span class="sxs-lookup"><span data-stu-id="874cc-108">Requests that the host allocate the requested amount of memory from the heap.</span></span>|  
|[<span data-ttu-id="874cc-109">DebugAlloc (metodo)</span><span class="sxs-lookup"><span data-stu-id="874cc-109">DebugAlloc Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-debugalloc-method.md)|<span data-ttu-id="874cc-110">Richiede che l'host di alloca la quantità di memoria richiesta dall'heap e inoltre tenere traccia in cui è stata allocata la memoria.</span><span class="sxs-lookup"><span data-stu-id="874cc-110">Requests that the host allocate the requested amount of memory from the heap, and additionally track where the memory was allocated.</span></span>|  
|[<span data-ttu-id="874cc-111">Free (metodo)</span><span class="sxs-lookup"><span data-stu-id="874cc-111">Free Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmalloc-free-method.md)|<span data-ttu-id="874cc-112">Libera la memoria allocata tramite il `Alloc` metodo.</span><span class="sxs-lookup"><span data-stu-id="874cc-112">Frees memory that was allocated by using the `Alloc` method.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="874cc-113">Note</span><span class="sxs-lookup"><span data-stu-id="874cc-113">Remarks</span></span>  
 <span data-ttu-id="874cc-114">CLR ottiene un puntatore a interfaccia a un `IHostMalloc` istanza chiamando il [IHostMemoryManager::](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="874cc-114">The CLR gets an interface pointer to an `IHostMalloc` instance by calling the [IHostMemoryManager::CreateMalloc](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-createmalloc-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="874cc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="874cc-115">Requirements</span></span>  
 <span data-ttu-id="874cc-116">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="874cc-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="874cc-117">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="874cc-117">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="874cc-118">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="874cc-118">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="874cc-119">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="874cc-119">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="874cc-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="874cc-120">See Also</span></span>  
 [<span data-ttu-id="874cc-121">IHostMemoryManager (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="874cc-121">IHostMemoryManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostmemorymanager-interface.md)  
 [<span data-ttu-id="874cc-122">Interfacce di hosting</span><span class="sxs-lookup"><span data-stu-id="874cc-122">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)