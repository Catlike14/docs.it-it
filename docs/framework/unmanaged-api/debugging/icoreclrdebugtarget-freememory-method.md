---
title: Metodo ICoreClrDebugTarget::FreeMemory
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
- ICoreDebugTarget.FreeMemory
api_location:
- mscordbi_macx86.dll
api_type:
- COM
f1_keywords:
- ICoreClrDebugTarget::FreeMemory
helpviewer_keywords:
- remote debugging API [Silverlight]
- FreeMemory method, ICoreClrDebugTarget interface [Silverlight debugging]
- ICorClrDebugTarget::FreeMemory method [Silverlight debugging]
- Silverlight, remote debugging
ms.assetid: 98f2a0db-a6ec-4f9b-861d-f82485237d08
topic_type:
- apiref
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 2079d0363e962d0423623c7c0261cc64fc4b3237
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="icoreclrdebugtargetfreememory-method"></a><span data-ttu-id="ccdad-102">Metodo ICoreClrDebugTarget::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="ccdad-102">ICoreClrDebugTarget::FreeMemory Method</span></span>
<span data-ttu-id="ccdad-103">Libera la memoria allocata per il [ICoreClrDebugTarget:: EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) e [ICoreClrDebugTarget:: EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) metodi.</span><span class="sxs-lookup"><span data-stu-id="ccdad-103">Frees the memory allocated by the [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) and [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) methods.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="ccdad-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccdad-104">Syntax</span></span>  
  
```  
void FreeMemory (  
     [in] void*pMemory);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ccdad-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccdad-105">Parameters</span></span>  
 `pMemory`  
 <span data-ttu-id="ccdad-106">[in] Un puntatore alla matrice restituita dal [ICoreClrDebugTarget:: EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) o [ICoreClrDebugTarget:: EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="ccdad-106">[in] A pointer to the array that is returned by either the [ICoreClrDebugTarget::EnumProcesses](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumprocesses-method.md) or the [ICoreClrDebugTarget::EnumRuntimes](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-enumruntimes-method.md) method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="ccdad-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccdad-107">Requirements</span></span>  
 <span data-ttu-id="ccdad-108">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="ccdad-108">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="ccdad-109">**Intestazione:** coreclrremotedebugginginterfaces. H</span><span class="sxs-lookup"><span data-stu-id="ccdad-109">**Header:** CoreClrRemoteDebuggingInterfaces.h</span></span>  
  
 <span data-ttu-id="ccdad-110">**Libreria:** mscordbi_macx86.dll</span><span class="sxs-lookup"><span data-stu-id="ccdad-110">**Library:** mscordbi_macx86.dll</span></span>  
  
 <span data-ttu-id="ccdad-111">**Versioni di .NET framework:** 3.5 SP1</span><span class="sxs-lookup"><span data-stu-id="ccdad-111">**.NET Framework Versions:** 3.5 SP1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ccdad-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ccdad-112">See Also</span></span>  
 [<span data-ttu-id="ccdad-113">Interfaccia ICoreClrDebugTarget</span><span class="sxs-lookup"><span data-stu-id="ccdad-113">ICoreClrDebugTarget Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icoreclrdebugtarget-interface.md)
