---
title: Enumerazione CorMethodImpl
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
- CorMethodImpl
api_location:
- mscoree.dll
api_type:
- COM
f1_keywords:
- CorMethodImpl
helpviewer_keywords:
- CorMethodImpl enumeration [.NET Framework metadata]
ms.assetid: ffbb3caf-20da-4a4b-8983-77376e72b990
topic_type:
- apiref
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: e82eb50e4850ffbb4d5fc67d9603a3128cf8bcf6
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="cormethodimpl-enumeration"></a><span data-ttu-id="b9a0c-102">Enumerazione CorMethodImpl</span><span class="sxs-lookup"><span data-stu-id="b9a0c-102">CorMethodImpl Enumeration</span></span>
<span data-ttu-id="b9a0c-103">Contiene valori che descrivono funzionalità di implementazione dei metodi.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-103">Contains values that describe method implementation features.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="b9a0c-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9a0c-104">Syntax</span></span>  
  
```  
typedef enum CorMethodImpl {  
  
    miCodeTypeMask      =   0x0003,  
    miIL                =   0x0000,  
    miNative            =   0x0001,  
    miOPTIL             =   0x0002,  
    miRuntime           =   0x0003,  
  
    miManagedMask       =   0x0004,  
    miUnmanaged         =   0x0004,  
    miManaged           =   0x0000,  
  
    miForwardRef        =   0x0010,  
    miPreserveSig       =   0x0080,  
  
    miInternalCall      =   0x1000,  
    miSynchronized      =   0x0020,  
    miNoInlining        =   0x0008,  
    miAggressiveInlining =  0x0100,  
    miNoOptimization     =  0x0040,  
    miMaxMethodImplVal  =   0xffff  
  
} CorMethodImpl;  
```  
  
## <a name="members"></a><span data-ttu-id="b9a0c-105">Membri</span><span class="sxs-lookup"><span data-stu-id="b9a0c-105">Members</span></span>  
  
|<span data-ttu-id="b9a0c-106">Membro</span><span class="sxs-lookup"><span data-stu-id="b9a0c-106">Member</span></span>|<span data-ttu-id="b9a0c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9a0c-107">Description</span></span>|  
|------------|-----------------|  
|`miCodeTypeMask`|<span data-ttu-id="b9a0c-108">Flag che descrivono il tipo di codice.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-108">Flags that describe code type.</span></span>|  
|`miIL`|<span data-ttu-id="b9a0c-109">Specifica che l'implementazione del metodo è Microsoft intermediate language (MSIL).</span><span class="sxs-lookup"><span data-stu-id="b9a0c-109">Specifies that the method implementation is Microsoft intermediate language (MSIL).</span></span>|  
|`miNative`|<span data-ttu-id="b9a0c-110">Specifica che l'implementazione del metodo è nativa.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-110">Specifies that the method implementation is native.</span></span>|  
|`miOPTIL`|<span data-ttu-id="b9a0c-111">Specifica che l'implementazione del metodo OPTIL.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-111">Specifies that the method implementation is OPTIL.</span></span>|  
|`miRuntime`|<span data-ttu-id="b9a0c-112">Specifica che l'implementazione del metodo è fornito da common language runtime.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-112">Specifies that the method implementation is provided by the common language runtime.</span></span>|  
|`miManagedMask`|<span data-ttu-id="b9a0c-113">Flag che indicano se il codice sia gestito o meno.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-113">Flags that indicate whether the code is managed or unmanaged.</span></span>|  
|`miUnmanaged`|<span data-ttu-id="b9a0c-114">Specifica che l'implementazione del metodo non è gestito.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-114">Specifies that the method implementation is unmanaged.</span></span>|  
|`miManaged`|<span data-ttu-id="b9a0c-115">Specifica che l'implementazione del metodo gestito.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-115">Specifies that the method implementation is managed.</span></span>|  
|`miForwardRef`|<span data-ttu-id="b9a0c-116">Specifica che il metodo è definito.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-116">Specifies that the method is defined.</span></span> <span data-ttu-id="b9a0c-117">Questo flag viene utilizzato principalmente in scenari di tipo merge.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-117">This flag is used primarily in merge scenarios.</span></span>|  
|`miPreserveSig`|<span data-ttu-id="b9a0c-118">Specifica che la firma del metodo non può essere alterata per una conversione HRESULT.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-118">Specifies that the method signature cannot be mangled for an HRESULT conversion.</span></span>|  
|`miInternalCall`|<span data-ttu-id="b9a0c-119">Riservato per uso interno da common language runtime.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-119">Reserved for internal use by the common language runtime.</span></span>|  
|`miSynchronized`|<span data-ttu-id="b9a0c-120">Specifica che il metodo è a thread singolo mediante il relativo corpo.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-120">Specifies that the method is single-threaded through its body.</span></span>|  
|`miNoInlining`|<span data-ttu-id="b9a0c-121">Specifica che il metodo non può essere impostato come inline.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-121">Specifies that the method cannot be inlined.</span></span>|  
|`miAggressiveInlining`|<span data-ttu-id="b9a0c-122">Specifica che il metodo deve essere resa inline se possibile.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-122">Specifies that the method should be inlined if possible.</span></span>|  
|`miNoOptimization`|<span data-ttu-id="b9a0c-123">Specifica che il metodo non deve essere ottimizzato.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-123">Specifies that the method should not be optimized.</span></span>|  
|`miMaxMethodImplVal`|<span data-ttu-id="b9a0c-124">Il valore massimo valido per un `CorMethodImpl`.</span><span class="sxs-lookup"><span data-stu-id="b9a0c-124">The maximum valid value for a `CorMethodImpl`.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="b9a0c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9a0c-125">Requirements</span></span>  
 <span data-ttu-id="b9a0c-126">**Piattaforme:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b9a0c-126">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="b9a0c-127">**Intestazione:** CorHdr. H</span><span class="sxs-lookup"><span data-stu-id="b9a0c-127">**Header:** CorHdr.h</span></span>  
  
 <span data-ttu-id="b9a0c-128">**Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="b9a0c-128">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b9a0c-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9a0c-129">See Also</span></span>  
 [<span data-ttu-id="b9a0c-130">Enumerazioni dei metadati</span><span class="sxs-lookup"><span data-stu-id="b9a0c-130">Metadata Enumerations</span></span>](../../../../docs/framework/unmanaged-api/metadata/metadata-enumerations.md)
