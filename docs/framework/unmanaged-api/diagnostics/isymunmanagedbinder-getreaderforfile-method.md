---
title: Metodo ISymUnmanagedBinder::GetReaderForFile
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ISymUnmanagedBinder.GetReaderForFile
api_location: diasymreader.dll
api_type: COM
f1_keywords: ISymUnmanagedBinder::GetReaderForFile
helpviewer_keywords:
- ISymUnmanagedBinder::GetReaderForFile method [.NET Framework debugging]
- GetReaderForFile method [.NET Framework debugging]
ms.assetid: 46c06258-831e-47c8-a50a-8650af6b637e
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 856f7eb506f77181d41ebd10148f321197ebfda3
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="isymunmanagedbindergetreaderforfile-method"></a><span data-ttu-id="fe653-102">Metodo ISymUnmanagedBinder::GetReaderForFile</span><span class="sxs-lookup"><span data-stu-id="fe653-102">ISymUnmanagedBinder::GetReaderForFile Method</span></span>
<span data-ttu-id="fe653-103">Dato un'interfaccia di metadati e un nome di file, restituisce la corretta <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> Struttura che verrà letti i simboli di debug associati al modulo.</span><span class="sxs-lookup"><span data-stu-id="fe653-103">Given a metadata interface and a file name, returns the correct <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> structure that will read the debugging symbols associated with the module.</span></span>  
  
 <span data-ttu-id="fe653-104">Questo metodo verrà aprire il file di programma (PDB) di database solo se si trova accanto al file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="fe653-104">This method will open the program database (PDB) file only if it is next to the executable file.</span></span> <span data-ttu-id="fe653-105">È stato modificato per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fe653-105">This change has been made for security purposes.</span></span> <span data-ttu-id="fe653-106">Se occorre una ricerca più completa per il file PDB, usare il [ISymUnmanagedBinder2:: Getreaderforfile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md) metodo.</span><span class="sxs-lookup"><span data-stu-id="fe653-106">If you need a more extensive search for the PDB file, use the [ISymUnmanagedBinder2::GetReaderForFile2](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md) method.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="fe653-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe653-107">Syntax</span></span>  
  
```  
HRESULT GetReaderForFile(  
    [in]  IUnknown     *importer,  
    [in]  const WCHAR  *fileName,  
    [in]  const WCHAR  *searchPath,  
    [out, retval] ISymUnmanagedReader  **pRetVal);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="fe653-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe653-108">Parameters</span></span>  
 `importer`  
 <span data-ttu-id="fe653-109">[in] Un puntatore all'interfaccia di importazione dei metadati.</span><span class="sxs-lookup"><span data-stu-id="fe653-109">[in] A pointer to the metadata import interface.</span></span>  
  
 `fileName`  
 <span data-ttu-id="fe653-110">[in] Puntatore al nome del file.</span><span class="sxs-lookup"><span data-stu-id="fe653-110">[in] A pointer to the file name.</span></span>  
  
 `searchPath`  
 <span data-ttu-id="fe653-111">[in] Puntatore al percorso di ricerca.</span><span class="sxs-lookup"><span data-stu-id="fe653-111">[in] A pointer to the search path.</span></span>  
  
 `pRetVal`  
 <span data-ttu-id="fe653-112">[out] Un puntatore che viene impostato sull'oggetto restituito <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fe653-112">[out] A pointer that is set to the returned <<!--zz xref:ISymUnmanagedReader --> `ISymUnmanagedReader`> interface.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="fe653-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe653-113">Return Value</span></span>  
 <span data-ttu-id="fe653-114">S_OK se il metodo ha esito positivo. in caso contrario, E_FAIL o un altro codice di errore.</span><span class="sxs-lookup"><span data-stu-id="fe653-114">S_OK if the method succeeds; otherwise, E_FAIL or some other error code.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="fe653-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe653-115">Requirements</span></span>  
 <span data-ttu-id="fe653-116">**Intestazione:** CorSym.idl, CorSym.h</span><span class="sxs-lookup"><span data-stu-id="fe653-116">**Header:** CorSym.idl, CorSym.h</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fe653-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fe653-117">See Also</span></span>  
 [<span data-ttu-id="fe653-118">Interfaccia ISymUnmanagedBinder</span><span class="sxs-lookup"><span data-stu-id="fe653-118">ISymUnmanagedBinder Interface</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder-interface.md)  
 [<span data-ttu-id="fe653-119">GetReaderForFile2 (metodo)</span><span class="sxs-lookup"><span data-stu-id="fe653-119">GetReaderForFile2 Method</span></span>](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedbinder2-getreaderforfile2-method.md)
