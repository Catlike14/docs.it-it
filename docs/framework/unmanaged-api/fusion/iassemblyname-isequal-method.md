---
title: Metodo IAssemblyName::IsEqual
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyName.IsEqual
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyName::IsEqual
helpviewer_keywords:
- IsEqual method [.NET Framework fusion]
- IAssemblyName::IsEqual method [.NET Framework fusion]
ms.assetid: 6dfc220f-d0d4-45b3-bfce-5829f817766f
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 454226d45474abea67b944e8437cf53be5c8ed1f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="iassemblynameisequal-method"></a><span data-ttu-id="232ee-102">Metodo IAssemblyName::IsEqual</span><span class="sxs-lookup"><span data-stu-id="232ee-102">IAssemblyName::IsEqual Method</span></span>
<span data-ttu-id="232ee-103">Determina se un oggetto [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) è uguale all'oggetto `IAssemblyName`, in base ai flag di confronto specificati.</span><span class="sxs-lookup"><span data-stu-id="232ee-103">Determines whether a specified [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object is equal to this `IAssemblyName`, based on the specified comparison flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="232ee-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="232ee-104">Syntax</span></span>  
  
```  
HRESULT IsEqual (  
    [in] IAssemblyName  *pName,  
    [in] DWORD          dwCmpFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="232ee-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="232ee-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="232ee-106">[in] Il `IAssemblyName` oggetto con cui confrontare questa `IAssemblyName`.</span><span class="sxs-lookup"><span data-stu-id="232ee-106">[in] The `IAssemblyName` object to which to compare this `IAssemblyName`.</span></span>  
  
 `dwCmpFlags`  
 <span data-ttu-id="232ee-107">[in] Combinazione bit per bit di [ASM_CMP_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md) valori che influenzano il confronto.</span><span class="sxs-lookup"><span data-stu-id="232ee-107">[in] A bitwise combination of [ASM_CMP_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md) values that influence the comparison.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="232ee-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="232ee-108">Requirements</span></span>  
 <span data-ttu-id="232ee-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="232ee-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="232ee-110">**Intestazione:** Fusion. h</span><span class="sxs-lookup"><span data-stu-id="232ee-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="232ee-111">**Versioni di .NET Framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="232ee-111">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="232ee-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="232ee-112">See Also</span></span>  
 [<span data-ttu-id="232ee-113">Interfaccia IAssemblyName</span><span class="sxs-lookup"><span data-stu-id="232ee-113">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="232ee-114">Enumerazioni Fusion</span><span class="sxs-lookup"><span data-stu-id="232ee-114">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
