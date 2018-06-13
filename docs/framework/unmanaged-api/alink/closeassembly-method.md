---
title: Metodo CloseAssembly
ms.date: 03/30/2017
api_name:
- IALink.CloseAssembly
- CloseAssembly
api_location:
- alink.dll
api_type:
- COM
f1_keywords:
- CloseAssembly
helpviewer_keywords:
- CloseAssembly method
ms.assetid: f66a43bc-a5c5-4190-acbe-63fd27640634
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 68698aab0fd0872c6e6f67e4ec531ab0226e784f
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33401953"
---
# <a name="closeassembly-method"></a><span data-ttu-id="671a8-102">Metodo CloseAssembly</span><span class="sxs-lookup"><span data-stu-id="671a8-102">CloseAssembly Method</span></span>
<span data-ttu-id="671a8-103">Consente di finalizzare le operazioni di assembly.</span><span class="sxs-lookup"><span data-stu-id="671a8-103">Finalizes assembly operations.</span></span> <span data-ttu-id="671a8-104">Chiamare questo metodo prima di iniziare un nuovo assembly o il modulo non associato.</span><span class="sxs-lookup"><span data-stu-id="671a8-104">Call this method before beginning a new assembly or unbound module.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="671a8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="671a8-105">Syntax</span></span>  
  
```  
HRESULT CloseAssembly(  
    mdAssembly AssemblyID  
) PURE;  
```  
  
#### <a name="parameters"></a><span data-ttu-id="671a8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="671a8-106">Parameters</span></span>  
 `AssemblyID`  
 <span data-ttu-id="671a8-107">ID dell'assembly.</span><span class="sxs-lookup"><span data-stu-id="671a8-107">ID of the assembly.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="671a8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="671a8-108">Return Value</span></span>  
 <span data-ttu-id="671a8-109">Se il metodo ha esito positivo, restituisce S_OK.</span><span class="sxs-lookup"><span data-stu-id="671a8-109">Returns S_OK if the method succeeds.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="671a8-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="671a8-110">Requirements</span></span>  
 <span data-ttu-id="671a8-111">Richiede alink.h.</span><span class="sxs-lookup"><span data-stu-id="671a8-111">Requires alink.h.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="671a8-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="671a8-112">See Also</span></span>  
 [<span data-ttu-id="671a8-113">Interfaccia IALink</span><span class="sxs-lookup"><span data-stu-id="671a8-113">IALink Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink-interface.md)  
 [<span data-ttu-id="671a8-114">Interfaccia IALink2</span><span class="sxs-lookup"><span data-stu-id="671a8-114">IALink2 Interface</span></span>](../../../../docs/framework/unmanaged-api/alink/ialink2-interface.md)  
 [<span data-ttu-id="671a8-115">Alink (API)</span><span class="sxs-lookup"><span data-stu-id="671a8-115">ALink API</span></span>](../../../../docs/framework/unmanaged-api/alink/index.md)
