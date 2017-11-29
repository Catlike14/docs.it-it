---
title: Metodo IAssemblyCache::InstallAssembly
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAssemblyCache.InstallAssembly
api_location: fusion.dll
api_type: COM
f1_keywords: IAssemblyCache::InstallAssembly
helpviewer_keywords:
- InstallAssembly method [.NET Framework fusion]
- IAssemblyCache::InstallAssembly method [.NET Framework fusion]
ms.assetid: 33c1d269-c85e-4cb1-b0e6-1c510c8fb5fa
topic_type: apiref
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: d1207c2dc5b29b8de084ccb9145e886f34e8144b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iassemblycacheinstallassembly-method"></a><span data-ttu-id="f57ab-102">Metodo IAssemblyCache::InstallAssembly</span><span class="sxs-lookup"><span data-stu-id="f57ab-102">IAssemblyCache::InstallAssembly Method</span></span>
<span data-ttu-id="f57ab-103">Installa l'assembly specificato nella global assembly cache.</span><span class="sxs-lookup"><span data-stu-id="f57ab-103">Installs the specified assembly in the global assembly cache.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f57ab-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f57ab-104">Syntax</span></span>  
  
```  
HRESULT InstallAssembly (  
    [in] DWORD dwFlags,  
    [in] LPCWSTR pszManifestFilePath,  
    [in] LPCFUSION_INSTALL_REFERENCE pRefData  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f57ab-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f57ab-105">Parameters</span></span>  
 `dwFlags`  
 <span data-ttu-id="f57ab-106">[in] Flag definiti in Fusion.</span><span class="sxs-lookup"><span data-stu-id="f57ab-106">[in] Flags defined in Fusion.idl.</span></span> <span data-ttu-id="f57ab-107">Sono supportati i seguenti valori:</span><span class="sxs-lookup"><span data-stu-id="f57ab-107">The following values are supported:</span></span>  
  
-   <span data-ttu-id="f57ab-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0X00000001)</span><span class="sxs-lookup"><span data-stu-id="f57ab-108">IASSEMBLYCACHE_INSTALL_FLAG_REFRESH (0x00000001)</span></span>  
  
-   <span data-ttu-id="f57ab-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0X00000002)</span><span class="sxs-lookup"><span data-stu-id="f57ab-109">IASSEMBLYCACHE_INSTALL_FLAG_FORCE_REFRESH (0x00000002)</span></span>  
  
 `pszManifestFilePath`  
 <span data-ttu-id="f57ab-110">[in] Il percorso al manifesto dell'assembly da installare.</span><span class="sxs-lookup"><span data-stu-id="f57ab-110">[in] The path to the manifest for the assembly to install.</span></span>  
  
 `pRefData`  
 <span data-ttu-id="f57ab-111">[in] Oggetto [FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md) struttura che contiene dati per l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f57ab-111">[in] A [FUSION_INSTALL_REFERENCE](../../../../docs/framework/unmanaged-api/fusion/fusion-install-reference-structure.md) structure that contains data for the installation.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f57ab-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f57ab-112">Requirements</span></span>  
 <span data-ttu-id="f57ab-113">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f57ab-113">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f57ab-114">**Intestazione:** Fusion. h</span><span class="sxs-lookup"><span data-stu-id="f57ab-114">**Header:** Fusion.h</span></span>  
  
 <span data-ttu-id="f57ab-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f57ab-115">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f57ab-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f57ab-116">See Also</span></span>  
 [<span data-ttu-id="f57ab-117">IAssemblyCache (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="f57ab-117">IAssemblyCache Interface</span></span>](../../../../docs/framework/unmanaged-api/fusion/iassemblycache-interface.md)
