---
title: Metodo IMetaDataAssemblyImport::FindManifestResourceByName
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataAssemblyImport.FindManifestResourceByName
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataAssemblyImport::FindManifestResourceByName
helpviewer_keywords:
- FindManifestResourceByName method [.NET Framework metadata]
- IMetaDataAssemblyImport::FindManifestResourceByName method [.NET Framework metadata]
ms.assetid: 7b72fa11-3866-402b-bdea-2b966b77cfe0
topic_type: apiref
caps.latest.revision: "10"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 492f8a50c421df56d1b2f79d15d86ef3251b401e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="imetadataassemblyimportfindmanifestresourcebyname-method"></a>Metodo IMetaDataAssemblyImport::FindManifestResourceByName
Ottiene un puntatore alla risorsa di manifesto con il nome specificato.  
  
## <a name="syntax"></a>Sintassi  
  
```  
HRESULT FindManifestResourceByName (  
    [in]  LPCWSTR                szName,   
    [out] mdManifestResource     *ptkManifestResource  
);   
```  
  
#### <a name="parameters"></a>Parametri  
 `szName`  
 [in] Il nome della risorsa.  
  
 `ptkManifestResource`  
 [out] Matrice utilizzata per archiviare il `mdManifestResource` i token di metadati, ognuno dei quali rappresenta una risorsa di manifesto.  
  
## <a name="remarks"></a>Note  
 Il `FindManifestResourceByName` metodo utilizza le regole standard utilizzate da common language runtime per la risoluzione dei riferimenti.  
  
## <a name="requirements"></a>Requisiti  
 **Piattaforma:** vedere [requisiti di sistema](../../../../docs/framework/get-started/system-requirements.md).  
  
 **Intestazione:** Cor. h  
  
 **Libreria:** usata come risorsa in MsCorEE.dll  
  
 **Versioni di .NET framework:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [IMetaDataAssemblyImport (interfaccia)](../../../../docs/framework/unmanaged-api/metadata/imetadataassemblyimport-interface.md)  
 [Come il runtime individua gli assembly](../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
