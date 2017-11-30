---
title: Funzione GetRealProcAddress
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetRealProcAddress
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: GetRealProcAddress
helpviewer_keywords: GetRealProcAddress function [.NET Framework hosting]
ms.assetid: f1f2fab1-400b-488f-95f2-d49c4fca3556
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 53e51bcf72f1a59f5c471564022d0d8c415381a6
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="getrealprocaddress-function"></a><span data-ttu-id="41040-102">Funzione GetRealProcAddress</span><span class="sxs-lookup"><span data-stu-id="41040-102">GetRealProcAddress Function</span></span>
<span data-ttu-id="41040-103">Ottiene l'indirizzo della funzione specificata esportata dall'ultima versione installata di common language runtime (CLR).</span><span class="sxs-lookup"><span data-stu-id="41040-103">Gets the address of the specified function that is exported from the latest installed version of the common language runtime (CLR).</span></span>  
  
 <span data-ttu-id="41040-104">Questa funzione è stata deprecata nel [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span><span class="sxs-lookup"><span data-stu-id="41040-104">This function has been deprecated in the [!INCLUDE[net_v40_long](../../../../includes/net-v40-long-md.md)].</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41040-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41040-105">Syntax</span></span>  
  
```  
HRESULT GetRealProcAddress (  
    [in]  LPCSTR  pwszProcName,   
    [out] VOID  **ppv  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="41040-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="41040-106">Parameters</span></span>  
 `pwszProcName`  
 <span data-ttu-id="41040-107">[in] Il nome della funzione.</span><span class="sxs-lookup"><span data-stu-id="41040-107">[in] The name of the function.</span></span>  
  
 `ppv`  
 <span data-ttu-id="41040-108">[out] Posizione che riceve un puntatore all'indirizzo della funzione.</span><span class="sxs-lookup"><span data-stu-id="41040-108">[out] The location that receives a pointer to the address of the function.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="41040-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41040-109">Return Value</span></span>  
 <span data-ttu-id="41040-110">Questo metodo restituisce codici di errore standard del modello COM (Component Object), come definito nel file Winerror. H, oltre ai seguenti valori definiti in CorError.</span><span class="sxs-lookup"><span data-stu-id="41040-110">This method returns standard Component Object Model (COM) error codes, as defined in WinError.h, in addition to the following values defined in CorError.h.</span></span>  
  
|<span data-ttu-id="41040-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="41040-111">Return code</span></span>|<span data-ttu-id="41040-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41040-112">Description</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="41040-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="41040-113">S_OK</span></span>|<span data-ttu-id="41040-114">Metodo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="41040-114">The method completed successfully.</span></span>|  
|<span data-ttu-id="41040-115">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="41040-115">E_POINTER</span></span>|<span data-ttu-id="41040-116">`ppv` non è valido.</span><span class="sxs-lookup"><span data-stu-id="41040-116">`ppv` is not valid.</span></span>|  
|<span data-ttu-id="41040-117">CLR_E_SHIM_RUNTIMEEXPORT</span><span class="sxs-lookup"><span data-stu-id="41040-117">CLR_E_SHIM_RUNTIMEEXPORT</span></span>|<span data-ttu-id="41040-118">La funzione non viene esportata dal runtime.</span><span class="sxs-lookup"><span data-stu-id="41040-118">The function is not exported from the runtime.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="41040-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41040-119">Requirements</span></span>  
 <span data-ttu-id="41040-120">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="41040-120">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="41040-121">**Intestazione:** Mscoree. H</span><span class="sxs-lookup"><span data-stu-id="41040-121">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="41040-122">**Libreria:** MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="41040-122">**Library:** MSCorEE.dll</span></span>  
  
 <span data-ttu-id="41040-123">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="41040-123">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="41040-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="41040-124">See Also</span></span>  
 [<span data-ttu-id="41040-125">Funzioni di Hosting CLR deprecate</span><span class="sxs-lookup"><span data-stu-id="41040-125">Deprecated CLR Hosting Functions</span></span>](../../../../docs/framework/unmanaged-api/hosting/deprecated-clr-hosting-functions.md)
