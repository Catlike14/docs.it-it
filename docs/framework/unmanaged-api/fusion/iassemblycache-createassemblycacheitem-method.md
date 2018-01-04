---
title: Metodo IAssemblyCache::CreateAssemblyCacheItem
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyCache.CreateAssemblyCacheItem
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyCache::CreateAssemblyCacheItem
helpviewer_keywords:
- IAssemblyCache::CreateAssemblyCacheItem method [.NET Framework fusion]
- CreateAssemblyCacheItem method [.NET Framework fusion]
ms.assetid: 017a7ba5-aaaf-44e2-9cbe-ceebef259df0
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 65431425afb6a666679d29f9c1bbc9691caa0afb
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iassemblycachecreateassemblycacheitem-method"></a><span data-ttu-id="9b693-102">Metodo IAssemblyCache::CreateAssemblyCacheItem</span><span class="sxs-lookup"><span data-stu-id="9b693-102">IAssemblyCache::CreateAssemblyCacheItem Method</span></span>
<span data-ttu-id="9b693-103">Ottiene un riferimento a un nuovo [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) oggetto.</span><span class="sxs-lookup"><span data-stu-id="9b693-103">Gets a reference to a new [IAssemblyCacheItem](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md) object.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="9b693-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b693-104">Syntax</span></span>  
  
```  
HRESULT CreateAssemblyCacheItem (  
    [in]  DWORD dwFlags,  
    [in]  PVOID pvReserved,  
    [out] IAssemblyCacheItem **ppAsmItem,  
    [in, optional] LPCWSTR pszAssemblyName  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="9b693-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b693-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="9b693-106">[in] Flag definiti in Fusion.</span><span class="sxs-lookup"><span data-stu-id="9b693-106">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="9b693-107">Sono supportati i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="9b693-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="9b693-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0X00000001)</span><span class="sxs-lookup"><span data-stu-id="9b693-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span></span>  
  
-   <span data-ttu-id="9b693-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0X00000002)</span><span class="sxs-lookup"><span data-stu-id="9b693-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span></span>  
  
 `pvReserved`  
 <span data-ttu-id="9b693-110">[in] Riservato per l'estensibilità futura.</span><span class="sxs-lookup"><span data-stu-id="9b693-110">[in] Reserved for future extensibility.</span></span> <span data-ttu-id="9b693-111">`pvReserved`deve essere un riferimento null.</span><span class="sxs-lookup"><span data-stu-id="9b693-111">`pvReserved` must be a null reference.</span></span>  
  
 `ppAsmItem`  
 <span data-ttu-id="9b693-112">[out] L'oggetto restituito `IAssemblyCacheItem` puntatore.</span><span class="sxs-lookup"><span data-stu-id="9b693-112">[out] The returned `IAssemblyCacheItem` pointer.</span></span>  
  
 `pszAssemblyName`  
 <span data-ttu-id="9b693-113">[in, facoltativo] Coppie, separati da virgola `name=value` coppie.</span><span class="sxs-lookup"><span data-stu-id="9b693-113">[in, optional] Uncanonicalized, comma-separated `name=value` pairs.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="9b693-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b693-114">Requirements</span></span>  
 <span data-ttu-id="9b693-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="9b693-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="9b693-116">**Intestazione:** Fusion. h</span><span class="sxs-lookup"><span data-stu-id="9b693-116">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="9b693-117">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="9b693-117">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9b693-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9b693-118">See Also</span></span>  
 [<span data-ttu-id="9b693-119">Interfaccia IAssemblyCache</span><span class="sxs-lookup"><span data-stu-id="9b693-119">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)  
 [<span data-ttu-id="9b693-120">Interfaccia IAssemblyCacheItem</span><span class="sxs-lookup"><span data-stu-id="9b693-120">IAssemblyCacheItem Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycacheitem-interface.md)
