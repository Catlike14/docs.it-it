---
title: '&lt;messageSenderAuthentication&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ea62fc06-55fb-42e0-aa2b-8867bdf4b415
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 734deddc2924814b081ce80b8504fb77e78c095c
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="ltmessagesenderauthenticationgt"></a><span data-ttu-id="d38de-102">&lt;messageSenderAuthentication&gt;</span><span class="sxs-lookup"><span data-stu-id="d38de-102">&lt;messageSenderAuthentication&gt;</span></span>
<span data-ttu-id="d38de-103">Specifica impostazioni di autenticazione per certificato peer usato dal mittente di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d38de-103">Specifies authentication settings for peer certificate used by a message sender.</span></span>  
  
 <span data-ttu-id="d38de-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="d38de-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="d38de-105">\<i comportamenti ></span><span class="sxs-lookup"><span data-stu-id="d38de-105">\<behaviors></span></span>  
<span data-ttu-id="d38de-106">\<serviceBehaviors></span><span class="sxs-lookup"><span data-stu-id="d38de-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="d38de-107">\<behavior></span><span class="sxs-lookup"><span data-stu-id="d38de-107">\<behavior></span></span>  
<span data-ttu-id="d38de-108">\<serviceCredentials></span><span class="sxs-lookup"><span data-stu-id="d38de-108">\<serviceCredentials></span></span>  
<span data-ttu-id="d38de-109">\<peer></span><span class="sxs-lookup"><span data-stu-id="d38de-109">\<peer></span></span>  
<span data-ttu-id="d38de-110">\<messageSenderAuthentication></span><span class="sxs-lookup"><span data-stu-id="d38de-110">\<messageSenderAuthentication></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d38de-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d38de-111">Syntax</span></span>  
  
```xml  
<messageSenderAuthentication  
   customCertificateValidatorType="namespace.typeName, [,AssemblyName] [,Version=version number] [,Culture=culture] [,PublicKeyToken=token]"  
   certificateValidationMode="ChainTrust/None/PeerTrust/PeerOrChainTrust/Custom"  
   revocationMode="NoCheck/Online/Offline"  
   trustedStoreLocation="CurrentUser/LocalMachine"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="d38de-112">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="d38de-112">Attributes and Elements</span></span>  
 <span data-ttu-id="d38de-113">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="d38de-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="d38de-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="d38de-114">Attributes</span></span>  
  
|<span data-ttu-id="d38de-115">Attributo</span><span class="sxs-lookup"><span data-stu-id="d38de-115">Attribute</span></span>|<span data-ttu-id="d38de-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d38de-116">Description</span></span>|  
|---------------|-----------------|  
|`certificateValidationMode`|<span data-ttu-id="d38de-117">Enumerazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d38de-117">Optional enumeration.</span></span> <span data-ttu-id="d38de-118">Specifica una delle cinque modalità usate per convalidare credenziali.</span><span class="sxs-lookup"><span data-stu-id="d38de-118">Specifies one of five modes used to validate credentials.</span></span> <span data-ttu-id="d38de-119">L'attributo è di tipo <xref:System.ServiceModel.Security.X509CertificateValidationMode>.</span><span class="sxs-lookup"><span data-stu-id="d38de-119">This attribute is of type <xref:System.ServiceModel.Security.X509CertificateValidationMode>.</span></span> <span data-ttu-id="d38de-120">Se impostato su `Custom`, è necessario fornire anche un `customCertificateValidator`.</span><span class="sxs-lookup"><span data-stu-id="d38de-120">If set to `Custom`, then a `customCertificateValidator` must also be supplied.</span></span>|  
|`customCertificateValidatorType`|<span data-ttu-id="d38de-121">Stringa facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d38de-121">Optional string.</span></span> <span data-ttu-id="d38de-122">Specifica un tipo e un assembly usati per convalidare un tipo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d38de-122">Specifies a type and assembly used to validate a custom type.</span></span> <span data-ttu-id="d38de-123">Questo attributo deve essere impostato quando `certificateValidationMode` è impostato su `Custom`.</span><span class="sxs-lookup"><span data-stu-id="d38de-123">This attribute must be set when `certificateValidationMode` is set to `Custom`.</span></span> <span data-ttu-id="d38de-124">L'attributo è di tipo <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span><span class="sxs-lookup"><span data-stu-id="d38de-124">This attribute is of type <xref:System.IdentityModel.Selectors.X509CertificateValidator>.</span></span> [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)]<span data-ttu-id="d38de-125"> fornisce un validator del certificato peer predefinita che verifica il certificato peer a fronte dell'archivio Persone attendibili.</span><span class="sxs-lookup"><span data-stu-id="d38de-125"> provides a default peer certificate validator that verifies the peer certificate against the trusted people store.</span></span> <span data-ttu-id="d38de-126">Verifica inoltre che il certificato sia concatenato a una radice valida.</span><span class="sxs-lookup"><span data-stu-id="d38de-126">It also verifies that the certificate chains up to a valid root.</span></span> <span data-ttu-id="d38de-127">È possibile implementare una convalida personalizzata per specificare un comportamento diverso e usare questo attributo per puntare alla convalida personalizzata.</span><span class="sxs-lookup"><span data-stu-id="d38de-127">You can implement a custom validator to specify a different behavior and use this attribute to point to the custom validator.</span></span>|  
|`revocationMode`|<span data-ttu-id="d38de-128">Enumerazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d38de-128">Optional enumeration.</span></span> <span data-ttu-id="d38de-129">Specifica la modalità di revoca dei certificati.</span><span class="sxs-lookup"><span data-stu-id="d38de-129">Specifies the certificate revocation mode.</span></span> <span data-ttu-id="d38de-130">L'attributo è di tipo <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>.</span><span class="sxs-lookup"><span data-stu-id="d38de-130">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.X509RevocationMode>.</span></span> <span data-ttu-id="d38de-131">Il sistema verifica che il certificato peer non sia stato revocato cercandolo nell'elenco dei certificati revocati.</span><span class="sxs-lookup"><span data-stu-id="d38de-131">The system verifies that the peer certificate has not been revoked by looking it up in the revoked certificate list.</span></span> <span data-ttu-id="d38de-132">Questo controllo può essere eseguito controllando in linea o in un elenco di revoche memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="d38de-132">This check can be performed either by checking online or against a cached revocation list.</span></span> <span data-ttu-id="d38de-133">È possibile disattivare il controllo di revoca impostando l'attributo su NoCheck.</span><span class="sxs-lookup"><span data-stu-id="d38de-133">Revocation checking can be turned off by setting this attribute to NoCheck.</span></span>|  
|`trustedStoreLocation`|<span data-ttu-id="d38de-134">Enumerazione facoltativa.</span><span class="sxs-lookup"><span data-stu-id="d38de-134">Optional enumeration.</span></span> <span data-ttu-id="d38de-135">Specifica il percorso dell'archivio dati attendibile in cui il certificato peer viene convalidato dal sistema di sicurezza [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d38de-135">Specifies the trusted store location where the peer certificate is validated by the [!INCLUDE[indigo2](../../../../../includes/indigo2-md.md)] security system.</span></span> <span data-ttu-id="d38de-136">L'attributo è di tipo <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span><span class="sxs-lookup"><span data-stu-id="d38de-136">This attribute is of type <xref:System.Security.Cryptography.X509Certificates.StoreLocation>.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="d38de-137">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="d38de-137">Child Elements</span></span>  
 <span data-ttu-id="d38de-138">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="d38de-138">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="d38de-139">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="d38de-139">Parent Elements</span></span>  
  
|<span data-ttu-id="d38de-140">Elemento</span><span class="sxs-lookup"><span data-stu-id="d38de-140">Element</span></span>|<span data-ttu-id="d38de-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d38de-141">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="d38de-142">\<peer></span><span class="sxs-lookup"><span data-stu-id="d38de-142">\<peer></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/peer-of-servicecredentials.md)|<span data-ttu-id="d38de-143">Specifica le credenziali correnti per un nodo peer.</span><span class="sxs-lookup"><span data-stu-id="d38de-143">Specifies the current credentials for a peer node.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d38de-144">Note</span><span class="sxs-lookup"><span data-stu-id="d38de-144">Remarks</span></span>  
 <span data-ttu-id="d38de-145">Se è stata scelta l'autenticazione dei messaggi, sarà necessario configurare questo elemento.</span><span class="sxs-lookup"><span data-stu-id="d38de-145">This element must be configured if message authentication is chosen.</span></span> <span data-ttu-id="d38de-146">Per i canali di output, ogni messaggio viene firmato utilizzando il certificato fornito dal [ \<certificato >](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md).</span><span class="sxs-lookup"><span data-stu-id="d38de-146">For output channels, each message is signed using the certificate provided by [\<certificate>](../../../../../docs/framework/configure-apps/file-schema/wcf/certificate-element.md).</span></span> <span data-ttu-id="d38de-147">Prima che vengano recapitati all'applicazione, tutti i messaggi vengono controllati a fronte delle credenziali del messaggio usando la convalida specificata dall'attributo `customCertificateValidatorType` di questo elemento.</span><span class="sxs-lookup"><span data-stu-id="d38de-147">All messages, before delivered to the application, are checked against the message credential using the validator specified by the `customCertificateValidatorType` attribute of this element.</span></span> <span data-ttu-id="d38de-148">La convalida può accettare o rifiutare la credenziale.</span><span class="sxs-lookup"><span data-stu-id="d38de-148">The validator can either accept or reject the credential.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d38de-149">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d38de-149">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.X509PeerCertificateAuthenticationElement>  
 <xref:System.ServiceModel.Security.X509PeerCertificateAuthentication>  
 <xref:System.ServiceModel.Security.PeerCredential.MessageSenderAuthentication%2A>  
 <xref:System.ServiceModel.Configuration.PeerCredentialElement.MessageSenderAuthentication%2A>  
 [<span data-ttu-id="d38de-150">Uso di certificati</span><span class="sxs-lookup"><span data-stu-id="d38de-150">Working with Certificates</span></span>](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [<span data-ttu-id="d38de-151">Reti peer-to-peer</span><span class="sxs-lookup"><span data-stu-id="d38de-151">Peer-to-Peer Networking</span></span>](../../../../../docs/framework/wcf/feature-details/peer-to-peer-networking.md)  
 [<span data-ttu-id="d38de-152">Autenticazione dei messaggi del canale peer</span><span class="sxs-lookup"><span data-stu-id="d38de-152">Peer Channel Message Authentication</span></span>](http://msdn.microsoft.com/library/80e73386-514e-4c30-9e4a-b9ca8c173a95)  
 [<span data-ttu-id="d38de-153">Autenticazione personalizzata canale peer</span><span class="sxs-lookup"><span data-stu-id="d38de-153">Peer Channel Custom Authentication</span></span>](http://msdn.microsoft.com/library/4aa8a82e-41a8-48e2-8621-7e1cbabdca7c)  
 [<span data-ttu-id="d38de-154">Protezione di applicazioni del canale peer</span><span class="sxs-lookup"><span data-stu-id="d38de-154">Securing Peer Channel Applications</span></span>](../../../../../docs/framework/wcf/feature-details/securing-peer-channel-applications.md)
