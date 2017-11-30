---
title: Metodo ICorProfilerInfo3::GetStringLayout2
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerInfo3.GetStringLayout2 Method
api_location: Mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerInfo3::GetStringLayout2
helpviewer_keywords:
- ICorProfilerInfo3::GetStringLayout2 method [.NET Framework profiling]
- GetStringLayout2 method [.NET Framework profiling]
ms.assetid: 1a268496-ee51-4d84-8700-ee56fd0c499d
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: de89776c6208ec7e3434fa747057edbf818ec013
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerinfo3getstringlayout2-method"></a><span data-ttu-id="ca4db-102">Metodo ICorProfilerInfo3::GetStringLayout2</span><span class="sxs-lookup"><span data-stu-id="ca4db-102">ICorProfilerInfo3::GetStringLayout2 Method</span></span>
<span data-ttu-id="ca4db-103">Ottiene informazioni sul layout di un oggetto stringa.</span><span class="sxs-lookup"><span data-stu-id="ca4db-103">Gets information about the layout of a string object.</span></span> <span data-ttu-id="ca4db-104">Questo metodo sostituisce il [ICorProfilerInfo2:: GetStringLayout](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getstringlayout-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="ca4db-104">This method supersedes the [ICorProfilerInfo2::GetStringLayout](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo2-getstringlayout-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ca4db-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca4db-105">Syntax</span></span>  
  
```  
HRESULT GetStringLayout2(  
    [out] ULONG *pStringLengthOffset,  
    [out] ULONG *pBufferOffset);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ca4db-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca4db-106">Parameters</span></span>  
 `pStringLengthOffset`  
 <span data-ttu-id="ca4db-107">[out] Un puntatore all'offset della posizione relativa al `ObjectID` puntatore, che archivia la lunghezza della stringa stessa.</span><span class="sxs-lookup"><span data-stu-id="ca4db-107">[out] A pointer to the offset of the location, relative to the `ObjectID` pointer, that stores the length of the string itself.</span></span> <span data-ttu-id="ca4db-108">La lunghezza viene archiviata come un `DWORD`.</span><span class="sxs-lookup"><span data-stu-id="ca4db-108">The length is stored as a `DWORD`.</span></span>  
  
 `pBufferOffset`  
 <span data-ttu-id="ca4db-109">[out] Un puntatore all'offset del buffer relativo al `ObjectID` puntatore, che archivia la stringa di caratteri wide.</span><span class="sxs-lookup"><span data-stu-id="ca4db-109">[out] A pointer to the offset of the buffer, relative to the `ObjectID` pointer, which stores the string of wide characters.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ca4db-110">Note</span><span class="sxs-lookup"><span data-stu-id="ca4db-110">Remarks</span></span>  
 <span data-ttu-id="ca4db-111">Le stringhe possono o non possono essere con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="ca4db-111">Strings may or may not be null-terminated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ca4db-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca4db-112">Requirements</span></span>  
 <span data-ttu-id="ca4db-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ca4db-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ca4db-114">**Intestazione:** CorProf.idl, CorProf.h</span><span class="sxs-lookup"><span data-stu-id="ca4db-114">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="ca4db-115">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="ca4db-115">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="ca4db-116">**Versioni di .NET framework:**[!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="ca4db-116">**.NET Framework Versions:** [!INCLUDE[net_current_v40plus](../../../../includes/net-current-v40plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ca4db-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ca4db-117">See Also</span></span>  
 [<span data-ttu-id="ca4db-118">ICorProfilerInfo3 (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="ca4db-118">ICorProfilerInfo3 Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo3-interface.md)  
 [<span data-ttu-id="ca4db-119">Interfacce di profilatura</span><span class="sxs-lookup"><span data-stu-id="ca4db-119">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)
