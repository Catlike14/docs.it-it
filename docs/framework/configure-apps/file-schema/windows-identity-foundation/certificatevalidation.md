---
title: '&lt;certificateValidation&gt;'
ms.date: 03/30/2017
ms.assetid: 6c54c704-b55e-4631-88ff-4d4a5621554c
author: BrucePerlerMS
ms.openlocfilehash: 29881be43f02d275ad135efd97dc8b25a7409beb
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2018
ms.locfileid: "48778169"
---
# <a name="ltcertificatevalidationgt"></a><span data-ttu-id="e9327-102">&lt;certificateValidation&gt;</span><span class="sxs-lookup"><span data-stu-id="e9327-102">&lt;certificateValidation&gt;</span></span>
<span data-ttu-id="e9327-103">Controllare le impostazioni che utilizzano i gestori di token per convalidare i certificati.</span><span class="sxs-lookup"><span data-stu-id="e9327-103">Controls the settings that token handlers use to validate certificates.</span></span> <span data-ttu-id="e9327-104">Queste impostazioni vengono ignorate se un gestore specifico è configurato con il proprio validator.</span><span class="sxs-lookup"><span data-stu-id="e9327-104">These settings are overridden if a specific handler is configured with its own validator.</span></span>  
  
 <span data-ttu-id="e9327-105">\<system.identityModel></span><span class="sxs-lookup"><span data-stu-id="e9327-105">\<system.identityModel></span></span>  
<span data-ttu-id="e9327-106">\<identityConfiguration></span><span class="sxs-lookup"><span data-stu-id="e9327-106">\<identityConfiguration></span></span>  
<span data-ttu-id="e9327-107">\<certificateValidation ></span><span class="sxs-lookup"><span data-stu-id="e9327-107">\<certificateValidation></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e9327-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9327-108">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <certificateValidation  
      certificateValidationMode="None||ChainTrust||PeerTrust||PeerOrChainTrust||Custom"  
      revocationMode="NoCheck||Offline||Online"  
      trustedStoreLocation="CurrentLocation||LocalMachine" >  
    </certificateValidation>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="e9327-109">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="e9327-109">Attributes and Elements</span></span>  
 <span data-ttu-id="e9327-110">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="e9327-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="e9327-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="e9327-111">Attributes</span></span>  
  
|<span data-ttu-id="e9327-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="e9327-112">Attribute</span></span>|<span data-ttu-id="e9327-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9327-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="e9327-114">certificateValidationMode</span><span class="sxs-lookup"><span data-stu-id="e9327-114">certificateValidationMode</span></span>|<span data-ttu-id="e9327-115">Un <xref:System.ServiceModel.Security.X509CertificateValidationMode> valore che specifica la modalità di convalida da utilizzare per il certificato X.509.</span><span class="sxs-lookup"><span data-stu-id="e9327-115">An <xref:System.ServiceModel.Security.X509CertificateValidationMode> value that specifies the validation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="e9327-116">Il valore predefinito è "PeerOrChainTrust".</span><span class="sxs-lookup"><span data-stu-id="e9327-116">The default value is "PeerOrChainTrust".</span></span> <span data-ttu-id="e9327-117">Per specificare un validator personalizzato, impostare questo attributo su "Custom" e specificare il validator mediante la [ \<certificateValidator >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="e9327-117">To specify a custom validator, set this attribute to "Custom" and specify the validator using the [\<certificateValidator>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md) element.</span></span> <span data-ttu-id="e9327-118">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9327-118">Optional.</span></span>|  
|<span data-ttu-id="e9327-119">revocationMode</span><span class="sxs-lookup"><span data-stu-id="e9327-119">revocationMode</span></span>|<span data-ttu-id="e9327-120">Un <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> valore che specifica la modalità di revoche di certificati da utilizzare per il certificato X.509.</span><span class="sxs-lookup"><span data-stu-id="e9327-120">An <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode> value that specifies the revocation mode to use for the X.509 certificate.</span></span> <span data-ttu-id="e9327-121">Il valore predefinito è "Online".</span><span class="sxs-lookup"><span data-stu-id="e9327-121">The default value is "Online".</span></span> <span data-ttu-id="e9327-122">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9327-122">Optional.</span></span>|  
|<span data-ttu-id="e9327-123">trustedStoreLocation</span><span class="sxs-lookup"><span data-stu-id="e9327-123">trustedStoreLocation</span></span>|<span data-ttu-id="e9327-124">Oggetto <xref:System.Security.Cryptography.X509Certificates.StoreLocation> valore che specifica l'archivio certificati X.509.</span><span class="sxs-lookup"><span data-stu-id="e9327-124">A <xref:System.Security.Cryptography.X509Certificates.StoreLocation> value that specifies the X.509 certificate store.</span></span> <span data-ttu-id="e9327-125">Il valore predefinito è "LocalMachine".</span><span class="sxs-lookup"><span data-stu-id="e9327-125">The default value is "LocalMachine".</span></span> <span data-ttu-id="e9327-126">Facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9327-126">Optional.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="e9327-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="e9327-127">Child Elements</span></span>  
  
|<span data-ttu-id="e9327-128">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9327-128">Element</span></span>|<span data-ttu-id="e9327-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9327-129">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e9327-130">\<certificateValidator ></span><span class="sxs-lookup"><span data-stu-id="e9327-130">\<certificateValidator></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidator.md)|<span data-ttu-id="e9327-131">Specifica un tipo personalizzato per la convalida del certificato.</span><span class="sxs-lookup"><span data-stu-id="e9327-131">Specifies a custom type for certificate validation.</span></span> <span data-ttu-id="e9327-132">Questo tipo viene usato solo se il `certificateValidationMode` attributo del [ \<certificateValidation >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) elemento è impostato su "Custom".</span><span class="sxs-lookup"><span data-stu-id="e9327-132">This type is used only if the `certificateValidationMode` attribute of the [\<certificateValidation>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/certificatevalidation.md) element is set to "Custom".</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="e9327-133">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="e9327-133">Parent Elements</span></span>  
  
|<span data-ttu-id="e9327-134">Elemento</span><span class="sxs-lookup"><span data-stu-id="e9327-134">Element</span></span>|<span data-ttu-id="e9327-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9327-135">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="e9327-136">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="e9327-136">\<identityConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)|<span data-ttu-id="e9327-137">Specifica le impostazioni di identità a livello di servizio.</span><span class="sxs-lookup"><span data-stu-id="e9327-137">Specifies service-level identity settings.</span></span>|  
|[<span data-ttu-id="e9327-138">\<securityTokenHandlerConfiguration ></span><span class="sxs-lookup"><span data-stu-id="e9327-138">\<securityTokenHandlerConfiguration></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|<span data-ttu-id="e9327-139">Fornisce la configurazione per una raccolta di sicurezza i gestori di token.</span><span class="sxs-lookup"><span data-stu-id="e9327-139">Provides configuration for a collection of security token handlers.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="e9327-140">Note</span><span class="sxs-lookup"><span data-stu-id="e9327-140">Remarks</span></span>  
 <span data-ttu-id="e9327-141">Oggetto `<certificateValidation>` elemento può essere specificato a livello di servizio con il `<identityConfiguration>` elemento o a livello di raccolta gestori di token di sicurezza nel `<securityTokenHandlerConfiguration>` elemento.</span><span class="sxs-lookup"><span data-stu-id="e9327-141">A `<certificateValidation>` element can be specified at the service level under the `<identityConfiguration>` element or on the security token handler collection level under the `<securityTokenHandlerConfiguration>` element.</span></span> <span data-ttu-id="e9327-142">Le impostazioni in una raccolta di gestori di token sostituiscono quelle specificate nel servizio.</span><span class="sxs-lookup"><span data-stu-id="e9327-142">Settings on a token handler collection override those specified on the service.</span></span> <span data-ttu-id="e9327-143">Alcuni gestori di token consentono di specificare le impostazioni di convalida di certificati nella configurazione.</span><span class="sxs-lookup"><span data-stu-id="e9327-143">Some token handlers allow you to specify certificate validation settings in configuration.</span></span> <span data-ttu-id="e9327-144">Le impostazioni ai singoli gestori di token sostituiscono quelle specificate a livello di servizio e la raccolta di gestori di token di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="e9327-144">Settings on individual token handlers override those specified both at the service level and on the security token handler collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e9327-145">Esempio</span><span class="sxs-lookup"><span data-stu-id="e9327-145">Example</span></span>  
  
```xml  
<certificateValidation certificateValidationMode="PeerOrChainTrust"  
                       revocationMode="Online"  
                       trustedStoreLocation="LocalMachine" />  
```
