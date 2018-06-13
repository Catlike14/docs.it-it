---
title: Metodo IAssemblyName::IsEqual
ms.date: 03/30/2017
api_name:
- IAssemblyName.IsEqual
api_location:
- fusion.dll
api_type:
- COM
f1_keywords:
- IAssemblyName::IsEqual
helpviewer_keywords:
- IsEqual method [.NET Framework fusion]
- IAssemblyName::IsEqual method [.NET Framework fusion]
ms.assetid: 6dfc220f-d0d4-45b3-bfce-5829f817766f
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 043394541f5ed91b85a57f4cb13c61cca442bfec
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33431841"
---
# <a name="iassemblynameisequal-method"></a><span data-ttu-id="c8fe7-102">Metodo IAssemblyName::IsEqual</span><span class="sxs-lookup"><span data-stu-id="c8fe7-102">IAssemblyName::IsEqual Method</span></span>
<span data-ttu-id="c8fe7-103">Determina se un oggetto [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) è uguale all'oggetto `IAssemblyName`, in base ai flag di confronto specificati.</span><span class="sxs-lookup"><span data-stu-id="c8fe7-103">Determines whether a specified [IAssemblyName](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md) object is equal to this `IAssemblyName`, based on the specified comparison flags.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8fe7-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8fe7-104">Syntax</span></span>  
  
```  
HRESULT IsEqual (  
    [in] IAssemblyName  *pName,  
    [in] DWORD          dwCmpFlags  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c8fe7-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8fe7-105">Parameters</span></span>  
 `pName`  
 <span data-ttu-id="c8fe7-106">[in] Il `IAssemblyName` oggetto con cui confrontare questa `IAssemblyName`.</span><span class="sxs-lookup"><span data-stu-id="c8fe7-106">[in] The `IAssemblyName` object to which to compare this `IAssemblyName`.</span></span>  
  
 `dwCmpFlags`  
 <span data-ttu-id="c8fe7-107">[in] Combinazione bit per bit di [ASM_CMP_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md) valori che influenzano il confronto.</span><span class="sxs-lookup"><span data-stu-id="c8fe7-107">[in] A bitwise combination of [ASM_CMP_FLAGS](../../../../docs/framework/unmanaged-api/fusion/asm-cmp-flags-enumeration.md) values that influence the comparison.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c8fe7-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8fe7-108">Requirements</span></span>  
 <span data-ttu-id="c8fe7-109">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="c8fe7-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c8fe7-110">**Intestazione:** Fusion. h</span><span class="sxs-lookup"><span data-stu-id="c8fe7-110">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="c8fe7-111">**Versioni di .NET Framework:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c8fe7-111">**NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c8fe7-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c8fe7-112">See Also</span></span>  
 [<span data-ttu-id="c8fe7-113">Interfaccia IAssemblyName</span><span class="sxs-lookup"><span data-stu-id="c8fe7-113">IAssemblyName Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblyname-interface.md)  
 [<span data-ttu-id="c8fe7-114">Enumerazioni Fusion</span><span class="sxs-lookup"><span data-stu-id="c8fe7-114">Fusion Enumerations</span></span>](../../../../docs/framework/unmanaged-api/fusion/fusion-enumerations.md)
