---
title: Metodo ICeeGen::GetSectionDataLen
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICeeGen.GetSectionDataLen
api_location: mscoree.dll
api_type: COM
f1_keywords: ICeeGen::GetSectionDataLen
helpviewer_keywords:
- ICeeGen::GetSectionDataLen method [.NET Framework metadata]
- GetSectionDataLen method [.NET Framework metadata]
ms.assetid: e2a06ee4-b8ee-49c7-935a-c1031a29eef2
topic_type: apiref
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 7d119fdfe5c0202d08ca78026a6917bb4ef51422
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="iceegengetsectiondatalen-method"></a><span data-ttu-id="60938-102">Metodo ICeeGen::GetSectionDataLen</span><span class="sxs-lookup"><span data-stu-id="60938-102">ICeeGen::GetSectionDataLen Method</span></span>
<span data-ttu-id="60938-103">Ottiene la lunghezza della sezione specificata.</span><span class="sxs-lookup"><span data-stu-id="60938-103">Gets the length of the specified section.</span></span>  
  
 <span data-ttu-id="60938-104">Questo metodo è obsoleto e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="60938-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="60938-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60938-105">Syntax</span></span>  
  
```  
HRESULT GetSectionDataLen (  
    [in]  HCEESECTION  section,  
    [out] ULONG        *dataLen  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="60938-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60938-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="60938-107">[in] La sezione di dati la cui lunghezza verrà recuperata.</span><span class="sxs-lookup"><span data-stu-id="60938-107">[in] The data section whose length will be retrieved.</span></span>  
  
 `dataLen`  
 <span data-ttu-id="60938-108">[out] La lunghezza restituita della sezione specificata.</span><span class="sxs-lookup"><span data-stu-id="60938-108">[out] The returned length of the specified section.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="60938-109">Note</span><span class="sxs-lookup"><span data-stu-id="60938-109">Remarks</span></span>  
 <span data-ttu-id="60938-110">Chiamare `GetSectionDataLen` solo se sono necessari requisiti speciali di sezione che non sono gestiti da altri metodi.</span><span class="sxs-lookup"><span data-stu-id="60938-110">Call `GetSectionDataLen` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="60938-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60938-111">Requirements</span></span>  
 <span data-ttu-id="60938-112">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="60938-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="60938-113">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="60938-113">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="60938-114">**Libreria:** usata come risorsa in MsCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="60938-114">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="60938-115">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="60938-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="60938-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="60938-116">See Also</span></span>  
 [<span data-ttu-id="60938-117">ICeeGen (interfaccia)</span><span class="sxs-lookup"><span data-stu-id="60938-117">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
