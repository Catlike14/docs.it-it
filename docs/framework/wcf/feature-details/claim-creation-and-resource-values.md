---
title: Creazione di attestazioni e valori delle risorse
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- claims [WCF], creation and resource values
ms.assetid: 30431f76-cbe7-4bad-bad7-8e43e23a82d4
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8afcd09e09cefcd08e3cb92aba980f599cf44d11
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="claim-creation-and-resource-values"></a><span data-ttu-id="27215-102">Creazione di attestazioni e valori delle risorse</span><span class="sxs-lookup"><span data-stu-id="27215-102">Claim Creation and Resource Values</span></span>
<span data-ttu-id="27215-103">La classe <xref:System.IdentityModel.Claims.Claim> fornisce numerosi metodi per creare istanze di tipi di attestazioni incorporati.</span><span class="sxs-lookup"><span data-stu-id="27215-103">The <xref:System.IdentityModel.Claims.Claim> class provides several methods for creating instances of built-in claims types.</span></span> <span data-ttu-id="27215-104">Il metodo seguente non esegue alcun controllo semantico o del formato sulla risorsa fornita:</span><span class="sxs-lookup"><span data-stu-id="27215-104">Of these methods, the following perform no semantic or format checking on the supplied resource:</span></span>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateDnsClaim%2A>  
  
-   <span data-ttu-id="27215-105"><xref:System.IdentityModel.Claims.Claim.CreateHashClaim%2A> (non controlla la lunghezza o il contenuto della matrice di byte)</span><span class="sxs-lookup"><span data-stu-id="27215-105"><xref:System.IdentityModel.Claims.Claim.CreateHashClaim%2A> (does not check the length or content of the byte array)</span></span>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateNameClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateSpnClaim%2A>  
  
-   <span data-ttu-id="27215-106"><xref:System.IdentityModel.Claims.Claim.CreateThumbprintClaim%2A> (non controlla la lunghezza o il contenuto della matrice di byte)</span><span class="sxs-lookup"><span data-stu-id="27215-106"><xref:System.IdentityModel.Claims.Claim.CreateThumbprintClaim%2A> (does not check the length or content of the byte array)</span></span>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateUpnClaim%2A>  
  
 <span data-ttu-id="27215-107">Al momento di chiamare i metodi riportati in precedenza, fare attenzione che i valori della risorsa passati siano nel formato corretto o contengano informazioni corrette (o entrambe le cose).</span><span class="sxs-lookup"><span data-stu-id="27215-107">Care should be taken when calling the above methods to ensure that the resource values passed in are of the correct format or contain the correct kind of information (or both).</span></span>  
  
 <span data-ttu-id="27215-108">I metodi seguenti prendono tipi specifici:</span><span class="sxs-lookup"><span data-stu-id="27215-108">The following methods take specific types:</span></span>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateDenyOnlyWindowsSidClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateMailAddressClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateRsaClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateUriClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateWindowsSidClaim%2A>  
  
-   <xref:System.IdentityModel.Claims.Claim.CreateX500DistinguishedNameClaim%2A>  
  
## <a name="see-also"></a><span data-ttu-id="27215-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="27215-109">See Also</span></span>  
 <xref:System.IdentityModel.Claims.Claim>  
 <xref:System.IdentityModel.Claims.ClaimSet>  
 [<span data-ttu-id="27215-110">Gestione delle attestazioni e dell'autorizzazione con il modello di identità</span><span class="sxs-lookup"><span data-stu-id="27215-110">Managing Claims and Authorization with the Identity Model</span></span>](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)
