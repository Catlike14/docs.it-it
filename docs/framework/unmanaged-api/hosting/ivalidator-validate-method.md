---
title: Metodo IValidator::Validate
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IValidator.Validate
api_location: mscoree.dll
api_type: COM
f1_keywords: Validate
helpviewer_keywords:
- IValidator::Validate method [.NET Framework hosting]
- Validate method, IValidator interface [.NET Framework hosting]
ms.assetid: 7d68666a-fb73-4455-bebd-908d49a16abc
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 722c6acc7e152a78ba28bc2730b2fdc7e0c45eb0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="ivalidatorvalidate-method"></a><span data-ttu-id="7e751-102">Metodo IValidator::Validate</span><span class="sxs-lookup"><span data-stu-id="7e751-102">IValidator::Validate Method</span></span>
<span data-ttu-id="7e751-103">Convalida lo specificato eseguibile portabile (PE) o un file Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="7e751-103">Validates the specified portable executable (PE) or Microsoft intermediate language (MSIL) file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="7e751-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e751-104">Syntax</span></span>  
  
```  
HRESULT Validate (  
    [in] IVEHandler            *veh,  
    [in] IUnknown              *pAppDomain,  
    [in] unsigned long          ulFlags,  
    [in] unsigned long          ulMaxError,  
    [in] unsigned long          token,  
    [in] LPWSTR                 fileName,  
    [in, size_is(ulSize)] BYTE *pe,  
    [in] unsigned long          ulSize  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7e751-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e751-105">Parameters</span></span>  
 `veh`  
 <span data-ttu-id="7e751-106">[in] Un puntatore a un `IVEHandler` istanza che gestisce gli errori di convalida.</span><span class="sxs-lookup"><span data-stu-id="7e751-106">[in] A pointer to an `IVEHandler` instance that handles validation errors.</span></span>  
  
 `pAppDomain`  
 <span data-ttu-id="7e751-107">[in] Un puntatore per il dominio dell'applicazione in cui viene caricato il file.</span><span class="sxs-lookup"><span data-stu-id="7e751-107">[in] A pointer to the application domain in which the file is loaded.</span></span>  
  
 `ulFlags`  
 <span data-ttu-id="7e751-108">[in] Combinazione bit per bit di [ValidatorFlags](../../../../docs/framework/unmanaged-api/hosting/validatorflags-enumeration.md) valori, che indica le convalide che devono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="7e751-108">[in] A bitwise combination of [ValidatorFlags](../../../../docs/framework/unmanaged-api/hosting/validatorflags-enumeration.md) values, indicating the validations that should be performed.</span></span>  
  
 `ulMaxError`  
 <span data-ttu-id="7e751-109">[in] Il numero massimo di errori consentiti prima di disattivare la convalida.</span><span class="sxs-lookup"><span data-stu-id="7e751-109">[in] The maximum number of errors to allow before exiting the validation.</span></span>  
  
 `token`  
 <span data-ttu-id="7e751-110">[in] Non usato.</span><span class="sxs-lookup"><span data-stu-id="7e751-110">[in] Not used.</span></span>  
  
 `fileName`  
 <span data-ttu-id="7e751-111">[in] Stringa che specifica il nome del file da convalidare.</span><span class="sxs-lookup"><span data-stu-id="7e751-111">[in] A string that specifies the name of the file to be validated.</span></span>  
  
 `pe`  
 <span data-ttu-id="7e751-112">[in] Puntatore al buffer di memoria in cui è archiviato il file.</span><span class="sxs-lookup"><span data-stu-id="7e751-112">[in] A pointer to the memory buffer in which the file is stored.</span></span>  
  
 `ulSize`  
 <span data-ttu-id="7e751-113">[in] Le dimensioni in byte, del file da convalidare.</span><span class="sxs-lookup"><span data-stu-id="7e751-113">[in] The size, in bytes, of the file to be validated.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="7e751-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e751-114">Requirements</span></span>  
 <span data-ttu-id="7e751-115">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7e751-115">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="7e751-116">**Intestazione:** IValidator. idl, IValidator.h</span><span class="sxs-lookup"><span data-stu-id="7e751-116">**Header:** IValidator.idl, IValidator.h</span></span>  
  
 <span data-ttu-id="7e751-117">**Libreria:** inclusa come risorsa in MSCorEE.dll</span><span class="sxs-lookup"><span data-stu-id="7e751-117">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="7e751-118">**Versioni di .NET framework:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="7e751-118">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7e751-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7e751-119">See Also</span></span>  
 
