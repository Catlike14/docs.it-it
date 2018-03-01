---
title: Metodo ICorProfilerInfo::GetTokenAndMetadataFromFunction
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
- ICorProfilerInfo.GetTokenAndMetadataFromFunction
api_location:
- mscorwks.dll
api_type:
- COM
f1_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction
helpviewer_keywords:
- ICorProfilerInfo::GetTokenAndMetadataFromFunction method [.NET Framework profiling]
- GetTokenAndMetadataFromFunction method [.NET Framework profiling]
ms.assetid: e525aa16-c923-4b16-833b-36f1f0dd70fc
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 33522d55383b1137d8591c74c988903655eba5f6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icorprofilerinfogettokenandmetadatafromfunction-method"></a><span data-ttu-id="eddde-102">Metodo ICorProfilerInfo::GetTokenAndMetadataFromFunction</span><span class="sxs-lookup"><span data-stu-id="eddde-102">ICorProfilerInfo::GetTokenAndMetadataFromFunction Method</span></span>
<span data-ttu-id="eddde-103">Ottiene il token di metadati e un'istanza di interfaccia di metadati che può essere utilizzata con il token per la funzione specificata.</span><span class="sxs-lookup"><span data-stu-id="eddde-103">Gets the metadata token and a metadata interface instance that can be used against the token for the specified function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="eddde-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eddde-104">Syntax</span></span>  
  
```  
HRESULT GetTokenAndMetaDataFromFunction(  
    [in]  FunctionID functionId,  
    [in]  REFIID     riid,  
    [out] IUnknown   **ppImport,  
    [out] mdToken    *pToken);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="eddde-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="eddde-105">Parameters</span></span>  
 `functionId`  
 <span data-ttu-id="eddde-106">[in] L'ID della funzione per cui ottenere il token di metadati e l'interfaccia di metadati.</span><span class="sxs-lookup"><span data-stu-id="eddde-106">[in] The ID of the function for which to get the metadata token and metadata interface.</span></span>  
  
 `riid`  
 <span data-ttu-id="eddde-107">[in] L'ID di riferimento dell'interfaccia di metadati per l'istanza di.</span><span class="sxs-lookup"><span data-stu-id="eddde-107">[in] The reference ID of the metadata interface to get the instance of.</span></span>  
  
 `ppImport`  
 <span data-ttu-id="eddde-108">[out] Un puntatore all'indirizzo dell'istanza di interfaccia di metadati che può essere utilizzato sulla base del token per la funzione specificata.</span><span class="sxs-lookup"><span data-stu-id="eddde-108">[out] A pointer to the address of the metadata interface instance that can be used against the token for the specified function.</span></span>  
  
 `pToken`  
 <span data-ttu-id="eddde-109">[out] Puntatore al token di metadati per la funzione specificata.</span><span class="sxs-lookup"><span data-stu-id="eddde-109">[out] A pointer to the metadata token for the specified function.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="eddde-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eddde-110">Requirements</span></span>  
 <span data-ttu-id="eddde-111">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="eddde-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="eddde-112">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="eddde-112">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="eddde-113">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="eddde-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="eddde-114">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="eddde-114">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eddde-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eddde-115">See Also</span></span>  
 [<span data-ttu-id="eddde-116">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="eddde-116">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)
