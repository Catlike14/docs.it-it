---
title: Metodo ICorProfilerInfo::GetAppDomainInfo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo.GetAppDomainInfo
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo::GetAppDomainInfo
helpviewer_keywords:
- ICorProfilerInfo::GetAppDomainInfo method [.NET Framework profiling]
- GetAppDomainInfo method [.NET Framework profiling]
ms.assetid: a6bf5a04-e03e-44f0-917a-96f6a6d3cc96
topic_type: apiref
caps.latest.revision: "23"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c31d3c61a868bf741213f6e505d91524cc925207
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfogetappdomaininfo-method"></a><span data-ttu-id="79ed1-102">Metodo ICorProfilerInfo::GetAppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="79ed1-102">ICorProfilerInfo::GetAppDomainInfo Method</span></span>
<span data-ttu-id="79ed1-103">Accetta un ID del dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79ed1-103">Accepts an application domain ID.</span></span> <span data-ttu-id="79ed1-104">Restituisce il nome di un domino applicazione e l'ID del processo che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="79ed1-104">Returns an application domain name and the ID of the process that contains it.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79ed1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79ed1-105">Syntax</span></span>  
  
```  
HRESULT GetAppDomainInfo(  
    [in]  AppDomainID appDomainId,  
    [in]  ULONG       cchName,  
    [out] ULONG       *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]  
          WCHAR       szName[] ,  
    [out] ProcessID   *pProcessId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="79ed1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="79ed1-106">Parameters</span></span>  
 `appDomainId`  
 <span data-ttu-id="79ed1-107">[in] ID del dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79ed1-107">[in] The ID of the application domain.</span></span>  
  
 `cchName`  
 <span data-ttu-id="79ed1-108">[in] Lunghezza, espressa in caratteri, del buffer restituito `szName`.</span><span class="sxs-lookup"><span data-stu-id="79ed1-108">[in] The length, in characters, of the `szName` return buffer.</span></span>  
  
 `pcchName`  
 <span data-ttu-id="79ed1-109">[out] Puntatore ai caratteri totali del nome del dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79ed1-109">[out] A pointer to the total character length of the application domain name.</span></span>  
  
 `szName`  
 <span data-ttu-id="79ed1-110">[out] Buffer per caratteri di tipo "wide" fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="79ed1-110">[out] A caller-provided wide character buffer.</span></span> <span data-ttu-id="79ed1-111">Una volta completato il metodo, il parametro `szName` conterrà il nome del dominio dell'applicazione completo o parziale.</span><span class="sxs-lookup"><span data-stu-id="79ed1-111">When the method returns, `szName` will contain the full or partial application domain name.</span></span>  
  
 `pProcessId`  
 <span data-ttu-id="79ed1-112">[out] Puntatore all'ID del processo che contiene il dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79ed1-112">[out] A pointer to the ID of the process that contains the application domain.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79ed1-113">Note</span><span class="sxs-lookup"><span data-stu-id="79ed1-113">Remarks</span></span>  
 <span data-ttu-id="79ed1-114">Dopo il completamento del metodo, è necessario verificare che il buffer `szName` sia abbastanza grande per contenere il nome completo del dominio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="79ed1-114">After this method returns, you must verify that the `szName` buffer was large enough to contain the full name of the application domain.</span></span> <span data-ttu-id="79ed1-115">A tale scopo, confrontare il valore a cui punta `pcchName` con il valore del parametro `cchName`.</span><span class="sxs-lookup"><span data-stu-id="79ed1-115">To do this, compare the value that `pcchName` points to with the value of the `cchName` parameter.</span></span> <span data-ttu-id="79ed1-116">Se `pcchName` punta a un valore maggiore di `cchName`, allocare un buffer `szName` più grande, aggiornare `cchName` con la nuova dimensione e chiamare nuovamente `GetAppDomainInfo`.</span><span class="sxs-lookup"><span data-stu-id="79ed1-116">If `pcchName` points to a value that is larger than `cchName`, allocate a larger `szName` buffer, update `cchName` with the new, larger size, and call `GetAppDomainInfo` again.</span></span>  
  
 <span data-ttu-id="79ed1-117">In alternativa, è possibile chiamare innanzitutto `GetAppDomainInfo` con un buffer `szName` di lunghezza zero per ottenere le dimensioni del buffer corrette.</span><span class="sxs-lookup"><span data-stu-id="79ed1-117">Alternatively, you can first call `GetAppDomainInfo` with a zero-length `szName` buffer to obtain the correct buffer size.</span></span> <span data-ttu-id="79ed1-118">È quindi possibile impostare le dimensioni del buffer sul valore restituito nel parametro `pcchName` e chiamare nuovamente `GetAppDomainInfo`.</span><span class="sxs-lookup"><span data-stu-id="79ed1-118">You can then set the buffer size to the value returned in `pcchName` and call `GetAppDomainInfo` again.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="79ed1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="79ed1-119">Requirements</span></span>  
 <span data-ttu-id="79ed1-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="79ed1-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="79ed1-121">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="79ed1-121">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="79ed1-122">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="79ed1-122">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="79ed1-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="79ed1-123">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="79ed1-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="79ed1-124">See Also</span></span>  
 [<span data-ttu-id="79ed1-125">Interfaccia ICorProfilerInfo</span><span class="sxs-lookup"><span data-stu-id="79ed1-125">ICorProfilerInfo Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo-interface.md)  
 [<span data-ttu-id="79ed1-126">Interfacce di profilatura</span><span class="sxs-lookup"><span data-stu-id="79ed1-126">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)  
 [<span data-ttu-id="79ed1-127">Profilatura</span><span class="sxs-lookup"><span data-stu-id="79ed1-127">Profiling</span></span>](../../../../docs/framework/unmanaged-api/profiling/index.md)