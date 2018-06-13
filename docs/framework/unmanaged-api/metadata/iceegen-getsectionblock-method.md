---
title: Metodo ICeeGen::GetSectionBlock
ms.date: 03/30/2017
api_name:
- ICeeGen.GetSectionBlock
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- ICeeGen::GetSectionBlock
helpviewer_keywords:
- GetSectionBlock method [.NET Framework metadata]
- ICeeGen::GetSectionBlock method [.NET Framework metadata]
ms.assetid: 05c78aaf-5bbd-497e-9ae2-55f4fae0c5fb
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 5da2936a46dcf3d8f69acc3367db64712165b0cb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33444061"
---
# <a name="iceegengetsectionblock-method"></a><span data-ttu-id="f1245-102">Metodo ICeeGen::GetSectionBlock</span><span class="sxs-lookup"><span data-stu-id="f1245-102">ICeeGen::GetSectionBlock Method</span></span>
<span data-ttu-id="f1245-103">Ottiene un blocco di sezione di base di codice.</span><span class="sxs-lookup"><span data-stu-id="f1245-103">Gets a section block of the code base.</span></span>  
  
 <span data-ttu-id="f1245-104">Questo metodo è obsoleto e non deve essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f1245-104">This method is obsolete and should not be used.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f1245-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1245-105">Syntax</span></span>  
  
```  
HRESULT GetSectionBlock (  
    [in]  HCEESECTION    section,     
    [in]  ULONG          len,  
    [in]  ULONG          align     = 1,  
    [out] void           **ppBytes = 0  
);   
```  
  
#### <a name="parameters"></a><span data-ttu-id="f1245-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1245-106">Parameters</span></span>  
 `section`  
 <span data-ttu-id="f1245-107">[in] La sezione da cui recuperare un blocco di base di codice.</span><span class="sxs-lookup"><span data-stu-id="f1245-107">[in] The section from which to retrieve a block of the code base.</span></span>  
  
 `len`  
 <span data-ttu-id="f1245-108">[in] La lunghezza del blocco da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f1245-108">[in] The length of the block to be retrieved.</span></span>  
  
 `align`  
 <span data-ttu-id="f1245-109">[in] Byte, relativo all'inizio della sezione, con la quale allineare il primo byte del blocco.</span><span class="sxs-lookup"><span data-stu-id="f1245-109">[in] The byte, relative to the beginning of the section, with which to align the first byte of the block.</span></span> <span data-ttu-id="f1245-110">Questa è la posizione del blocco all'interno della sezione.</span><span class="sxs-lookup"><span data-stu-id="f1245-110">This is the position of the block within the section.</span></span>  
  
 `ppBytes`  
 <span data-ttu-id="f1245-111">[out] Puntatore a una posizione che riceve l'indirizzo del blocco recuperato.</span><span class="sxs-lookup"><span data-stu-id="f1245-111">[out] A pointer to a location that receives the address of the retrieved block.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f1245-112">Note</span><span class="sxs-lookup"><span data-stu-id="f1245-112">Remarks</span></span>  
 <span data-ttu-id="f1245-113">Chiamare `GetSectionBlock` solo se sono necessari requisiti speciali di sezione che non sono gestiti da altri metodi.</span><span class="sxs-lookup"><span data-stu-id="f1245-113">Call `GetSectionBlock` only if you have special section requirements that are not handled by other methods.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f1245-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1245-114">Requirements</span></span>  
 <span data-ttu-id="f1245-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="f1245-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f1245-116">**Intestazione:** Cor. h</span><span class="sxs-lookup"><span data-stu-id="f1245-116">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="f1245-117">**Libreria:** usata come risorsa in Mscoree. dll</span><span class="sxs-lookup"><span data-stu-id="f1245-117">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="f1245-118">**Versioni di .NET framework:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f1245-118">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f1245-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f1245-119">See Also</span></span>  
 [<span data-ttu-id="f1245-120">Interfaccia ICeeGen</span><span class="sxs-lookup"><span data-stu-id="f1245-120">ICeeGen Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/iceegen-interface.md)
