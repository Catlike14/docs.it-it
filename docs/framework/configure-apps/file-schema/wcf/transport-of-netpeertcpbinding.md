---
title: '&lt;transport&gt; di &lt;netPeerTcpBinding&gt;'
ms.date: 03/30/2017
ms.assetid: c44d86d2-1160-44d7-9c7a-297b12eccc7f
ms.openlocfilehash: 62ba3b27b10afe182623f3be0f6738940e194579
ms.sourcegitcommit: 586dbdcaef9767642436b1e4efbe88fb15473d6f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/06/2018
ms.locfileid: "48836615"
---
# <a name="lttransportgt-of-ltnetpeertcpbindinggt"></a><span data-ttu-id="78b01-102">&lt;transport&gt; di &lt;netPeerTcpBinding&gt;</span><span class="sxs-lookup"><span data-stu-id="78b01-102">&lt;transport&gt; of &lt;netPeerTcpBinding&gt;</span></span>
<span data-ttu-id="78b01-103">Specifica le impostazioni per la sicurezza a livello di trasporto quando si usa la [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="78b01-103">Specifies settings for transport level security when using the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>  
  
 <span data-ttu-id="78b01-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="78b01-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="78b01-105">\<le associazioni ></span><span class="sxs-lookup"><span data-stu-id="78b01-105">\<bindings></span></span>  
<span data-ttu-id="78b01-106">\<netPeerTcpBinding></span><span class="sxs-lookup"><span data-stu-id="78b01-106">\<netPeerTcpBinding></span></span>  
<span data-ttu-id="78b01-107">\<binding></span><span class="sxs-lookup"><span data-stu-id="78b01-107">\<binding></span></span>  
<span data-ttu-id="78b01-108">\<security></span><span class="sxs-lookup"><span data-stu-id="78b01-108">\<security></span></span>  
<span data-ttu-id="78b01-109">\<trasporto ></span><span class="sxs-lookup"><span data-stu-id="78b01-109">\<transport></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="78b01-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78b01-110">Syntax</span></span>  
  
```xml  
<netPeerTcpBinding>  
    <binding>  
        <security>  
            <transport credentialType="Certificate/Password" />  
        </security>         
    </binding>  
</netPeerTcpBinding>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="78b01-111">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="78b01-111">Attributes and Elements</span></span>  
 <span data-ttu-id="78b01-112">Nelle sezioni seguenti vengono descritti attributi, elementi figlio ed elementi padre.</span><span class="sxs-lookup"><span data-stu-id="78b01-112">The following sections describe attributes, child elements, and parent elements</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="78b01-113">Attributi</span><span class="sxs-lookup"><span data-stu-id="78b01-113">Attributes</span></span>  
  
|<span data-ttu-id="78b01-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="78b01-114">Attribute</span></span>|<span data-ttu-id="78b01-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78b01-115">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="78b01-116">credentialType</span><span class="sxs-lookup"><span data-stu-id="78b01-116">credentialType</span></span>|<span data-ttu-id="78b01-117">Parametro facoltativo.</span><span class="sxs-lookup"><span data-stu-id="78b01-117">Optional.</span></span> <span data-ttu-id="78b01-118">Specifica il tipo di credenziali usate per verificare messaggi inviati con il trasporto peer.</span><span class="sxs-lookup"><span data-stu-id="78b01-118">Specifies the type of credentials used to verify messages sent with the peer transport.</span></span> <span data-ttu-id="78b01-119">L'attributo è di tipo <xref:System.ServiceModel.PeerTransportCredentialType>.</span><span class="sxs-lookup"><span data-stu-id="78b01-119">This attribute is of type <xref:System.ServiceModel.PeerTransportCredentialType>.</span></span>|  
  
## <a name="credentialtype-attribute"></a><span data-ttu-id="78b01-120">Attributo credentialType</span><span class="sxs-lookup"><span data-stu-id="78b01-120">credentialType Attribute</span></span>  
  
|<span data-ttu-id="78b01-121">Valore</span><span class="sxs-lookup"><span data-stu-id="78b01-121">Value</span></span>|<span data-ttu-id="78b01-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78b01-122">Description</span></span>|  
|-----------|-----------------|  
|<span data-ttu-id="78b01-123">Certificato</span><span class="sxs-lookup"><span data-stu-id="78b01-123">Certificate</span></span>|<span data-ttu-id="78b01-124">L'autenticazione del trasporto del canale peer richiede un certificato X509.</span><span class="sxs-lookup"><span data-stu-id="78b01-124">Authentication of the peer channel transport requires an X509 certificate.</span></span>|  
|<span data-ttu-id="78b01-125">Password</span><span class="sxs-lookup"><span data-stu-id="78b01-125">Password</span></span>|<span data-ttu-id="78b01-126">L'autenticazione del trasporto del canale peer richiede una password corretta.</span><span class="sxs-lookup"><span data-stu-id="78b01-126">Authentication of the peer channel transport requires a correct password.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="78b01-127">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="78b01-127">Child Elements</span></span>  
 <span data-ttu-id="78b01-128">nessuno</span><span class="sxs-lookup"><span data-stu-id="78b01-128">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="78b01-129">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="78b01-129">Parent Elements</span></span>  
  
|<span data-ttu-id="78b01-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="78b01-130">Element</span></span>|<span data-ttu-id="78b01-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78b01-131">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="78b01-132">\<security></span><span class="sxs-lookup"><span data-stu-id="78b01-132">\<security></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netpeerbinding.md)|<span data-ttu-id="78b01-133">Definisce le impostazioni di sicurezza per il [ \<netPeerTcpBinding >](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span><span class="sxs-lookup"><span data-stu-id="78b01-133">Defines the security settings for the [\<netPeerTcpBinding>](../../../../../docs/framework/configure-apps/file-schema/wcf/netpeertcpbinding.md).</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="78b01-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="78b01-134">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PeerTransportSecurityElement>  
 <xref:System.ServiceModel.PeerSecuritySettings.Transport%2A>  
 <xref:System.ServiceModel.Configuration.PeerSecurityElement.Transport%2A>  
 <xref:System.ServiceModel.PeerTransportSecuritySettings>  
 [<span data-ttu-id="78b01-135">Protezione di servizi e client</span><span class="sxs-lookup"><span data-stu-id="78b01-135">Securing Services and Clients</span></span>](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [<span data-ttu-id="78b01-136">Associazioni</span><span class="sxs-lookup"><span data-stu-id="78b01-136">Bindings</span></span>](../../../../../docs/framework/wcf/bindings.md)  
 [<span data-ttu-id="78b01-137">Configurazione di associazioni fornite dal sistema</span><span class="sxs-lookup"><span data-stu-id="78b01-137">Configuring System-Provided Bindings</span></span>](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [<span data-ttu-id="78b01-138">Uso di associazioni per configurare servizi e client</span><span class="sxs-lookup"><span data-stu-id="78b01-138">Using Bindings to Configure Services and Clients</span></span>](../../../../../docs/framework/wcf/using-bindings-to-configure-services-and-clients.md)  
 [<span data-ttu-id="78b01-139">\<binding></span><span class="sxs-lookup"><span data-stu-id="78b01-139">\<binding></span></span>](../../../../../docs/framework/misc/binding.md)
