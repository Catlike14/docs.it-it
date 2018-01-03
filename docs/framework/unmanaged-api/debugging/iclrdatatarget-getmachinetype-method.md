---
title: Metodo ICLRDataTarget::GetMachineType
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICLRDataTarget.GetMachineType
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICLRDataTarget::GetMachineType
helpviewer_keywords:
- ICLRDataTarget::GetMachineType method [.NET Framework debugging]
- GetMachineType method [.NET Framework debugging]
ms.assetid: 5f1f9c61-3e3b-48b2-b111-a4395f7623a7
topic_type: apiref
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 56fabfd2bb929e40c60903ad7b5e86e2b18d7d93
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iclrdatatargetgetmachinetype-method"></a><span data-ttu-id="04fbc-102">Metodo ICLRDataTarget::GetMachineType</span><span class="sxs-lookup"><span data-stu-id="04fbc-102">ICLRDataTarget::GetMachineType Method</span></span>
<span data-ttu-id="04fbc-103">Ottiene l'identificatore per il tipo di set di istruzioni che utilizza il processo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="04fbc-103">Gets the identifier for the kind of instruction set that the target process is using.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04fbc-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04fbc-104">Syntax</span></span>  
  
```  
HRESULT GetMachineType (  
    [out] ULONG32     *machineType  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="04fbc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="04fbc-105">Parameters</span></span>  
 `machineType`  
 <span data-ttu-id="04fbc-106">[out] Utilizza un puntatore a un valore che indica che il set di istruzioni che il processo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="04fbc-106">[out] A pointer to a value that indicates the instruction set that the target process is using.</span></span> <span data-ttu-id="04fbc-107">L'oggetto restituito `machineType` è una delle costanti IMAGE_FILE_MACHINE, che sono definite nel file di intestazione Winnt. H.</span><span class="sxs-lookup"><span data-stu-id="04fbc-107">The returned `machineType` is one of the IMAGE_FILE_MACHINE constants, which are defined in the WinNT.h header file.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="04fbc-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04fbc-108">Requirements</span></span>  
 <span data-ttu-id="04fbc-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="04fbc-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="04fbc-110">**Intestazione:** ClrData.idl, Clrdata. H</span><span class="sxs-lookup"><span data-stu-id="04fbc-110">**Header:** ClrData.idl, ClrData.h</span></span>  
  
 <span data-ttu-id="04fbc-111">**Libreria:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="04fbc-111">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="04fbc-112">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="04fbc-112">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="04fbc-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="04fbc-113">See Also</span></span>  
 [<span data-ttu-id="04fbc-114">Interfaccia ICLRDataTarget</span><span class="sxs-lookup"><span data-stu-id="04fbc-114">ICLRDataTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/iclrdatatarget-interface.md)
