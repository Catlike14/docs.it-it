---
title: Federazione e token emessi
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- WCF, federation
- issued tokens [WCF]
- federation [WCF], issued tokens
ms.assetid: 4c31ee7d-a820-4067-8b84-a83049021bb6
caps.latest.revision: "16"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 05a110318bbe92f18d0bc6becb453a5d7851821c
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="federation-and-issued-tokens"></a><span data-ttu-id="31b6a-102">Federazione e token emessi</span><span class="sxs-lookup"><span data-stu-id="31b6a-102">Federation and Issued Tokens</span></span>
<span data-ttu-id="31b6a-103">Con [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] è possibile creare client che comunicano in modo protetto con servizi che implementano le specifiche di WS-Federation e WS-Trust.</span><span class="sxs-lookup"><span data-stu-id="31b6a-103">With [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)], you can create clients that communicate securely with services that implement the WS-Federation and WS-Trust specifications.</span></span> <span data-ttu-id="31b6a-104">Le specifiche utilizzano XML, SOAP e Web Services Description Language (WSDL) per fornire meccanismi che consentano l'autenticazione e l'autorizzazione in diverse aree di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="31b6a-104">The specifications use XML, SOAP, and Web Services Description Language (WSDL) to provide mechanisms that enable authentication and authorization across different trust realms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="31b6a-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="31b6a-105">In This Section</span></span>  
 [<span data-ttu-id="31b6a-106">Federazione</span><span class="sxs-lookup"><span data-stu-id="31b6a-106">Federation</span></span>](../../../../docs/framework/wcf/feature-details/federation.md)  
 <span data-ttu-id="31b6a-107">Fornisce una panoramica della federazione.</span><span class="sxs-lookup"><span data-stu-id="31b6a-107">Provides an overview of federation.</span></span>  
  
 [<span data-ttu-id="31b6a-108">Federazione e attendibilità</span><span class="sxs-lookup"><span data-stu-id="31b6a-108">Federation and Trust</span></span>](../../../../docs/framework/wcf/feature-details/federation-and-trust.md)  
 <span data-ttu-id="31b6a-109">Elenca i problemi di progettazione da tenere in considerazione durante la creazione di servizi o di client federati.</span><span class="sxs-lookup"><span data-stu-id="31b6a-109">Lists the design issues to be aware of when creating federated services or clients.</span></span>  
  
 [<span data-ttu-id="31b6a-110">Procedura: creare un Client federato</span><span class="sxs-lookup"><span data-stu-id="31b6a-110">How to: Create a Federated Client</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-federated-client.md)  
 <span data-ttu-id="31b6a-111">Descrive le nozioni fondamentali sulla creazione di un client federato con [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="31b6a-111">Describes the basics of creating a federated client with [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].</span></span>  
  
 [<span data-ttu-id="31b6a-112">Procedura: configurare le credenziali in un servizio federativo</span><span class="sxs-lookup"><span data-stu-id="31b6a-112">How to: Configure Credentials on a Federation Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-configure-credentials-on-a-federation-service.md)  
 <span data-ttu-id="31b6a-113">Descrive i passaggi necessari per la creazione di un servizio federato.</span><span class="sxs-lookup"><span data-stu-id="31b6a-113">Describes the steps of creating a federated service.</span></span>  
  
 [<span data-ttu-id="31b6a-114">Procedura: creare una classe WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="31b6a-114">How to: Create a WSFederationHttpBinding</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-wsfederationhttpbinding.md)  
 <span data-ttu-id="31b6a-115">Descrive come configurare client e servizi che utilizzano `WSFederationHttpBinding`.</span><span class="sxs-lookup"><span data-stu-id="31b6a-115">Describes how to configure clients and services that use the `WSFederationHttpBinding`.</span></span>  
  
 [<span data-ttu-id="31b6a-116">Procedura: creare un servizio Token di sicurezza</span><span class="sxs-lookup"><span data-stu-id="31b6a-116">How to: Create a Security Token Service</span></span>](../../../../docs/framework/wcf/feature-details/how-to-create-a-security-token-service.md)  
 <span data-ttu-id="31b6a-117">Descrive i passaggi necessari per la creazione di un servizio token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="31b6a-117">Describes the steps of creating a security token service.</span></span>  
  
 [<span data-ttu-id="31b6a-118">Attestazioni e token di sicurezza asserzioni Markup Language (SAML)</span><span class="sxs-lookup"><span data-stu-id="31b6a-118">Security Assertions Markup Language (SAML) Tokens and Claims</span></span>](../../../../docs/framework/wcf/feature-details/saml-tokens-and-claims.md)  
 <span data-ttu-id="31b6a-119">Descrive i token Security Assertions Markup Language (SAML) che sono flessibili e consentono di creare tipi di attestazione dettagliati.</span><span class="sxs-lookup"><span data-stu-id="31b6a-119">Describes Security Assertions Markup Language (SAML) tokens, which are extensible and enable you to create rich claim types.</span></span>  
  
 [<span data-ttu-id="31b6a-120">Procedura: configurare un emittente locale</span><span class="sxs-lookup"><span data-stu-id="31b6a-120">How to: Configure a Local Issuer</span></span>](../../../../docs/framework/wcf/feature-details/how-to-configure-a-local-issuer.md)  
 <span data-ttu-id="31b6a-121">Descrive come creare un emittente locale di token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="31b6a-121">Describes how to create a local issuer of security tokens.</span></span>  
  
 [<span data-ttu-id="31b6a-122">Procedura: disattivare sessioni protette in una classe WSFederationHttpBinding</span><span class="sxs-lookup"><span data-stu-id="31b6a-122">How to: Disable Secure Sessions on a WSFederationHttpBinding</span></span>](../../../../docs/framework/wcf/feature-details/how-to-disable-secure-sessions-on-a-wsfederationhttpbinding.md)  
 <span data-ttu-id="31b6a-123">Descrive come disattivare sessioni protette in `WSFederationHttpBinding`.</span><span class="sxs-lookup"><span data-stu-id="31b6a-123">Describes how to disable secure sessions on a `WSFederationHttpBinding`.</span></span> <span data-ttu-id="31b6a-124">La disattivazione di sessioni protette è necessaria in caso di creazione di una Web farm che richiede una sessione per ogni client.</span><span class="sxs-lookup"><span data-stu-id="31b6a-124">Disabling secure sessions is necessary when creating a Web farm that requires a session for each client.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="31b6a-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="31b6a-125">Reference</span></span>  
 <xref:System.IdentityModel.Claims>  
  
 <xref:System.ServiceModel.ServiceAuthorizationManager>  
  
 <xref:System.IdentityModel.Tokens.SamlSecurityToken>  
  
 <xref:System.ServiceModel.Security.IssuedTokenClientCredential>  
  
 <xref:System.ServiceModel.Security.IssuedTokenServiceCredential>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenParameters>  
  
 <xref:System.ServiceModel.Security.Tokens.IssuedSecurityTokenProvider>  
  
 <xref:System.ServiceModel.WSFederationHttpBinding>  
  
## <a name="see-also"></a><span data-ttu-id="31b6a-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31b6a-126">See Also</span></span>  
 [<span data-ttu-id="31b6a-127">Autorizzazione</span><span class="sxs-lookup"><span data-stu-id="31b6a-127">Authorization</span></span>](../../../../docs/framework/wcf/feature-details/authorization-in-wcf.md)  
 [<span data-ttu-id="31b6a-128">Token personalizzati</span><span class="sxs-lookup"><span data-stu-id="31b6a-128">Custom Tokens</span></span>](../../../../docs/framework/wcf/extending/custom-tokens.md)  
 [<span data-ttu-id="31b6a-129">Modello di sicurezza per Windows Server AppFabric</span><span class="sxs-lookup"><span data-stu-id="31b6a-129">Security Model for Windows Server App Fabric</span></span>](http://go.microsoft.com/fwlink/?LinkID=201279&clcid=0x409)
