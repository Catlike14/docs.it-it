---
title: '&lt;identity&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c1d2ae56-e231-4a07-9c3f-9f13381dc0d8
caps.latest.revision: "18"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: fa6bfdf72bd292599867bf7a9571ecd6b408a2c2
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ltidentitygt"></a>&lt;identity&gt;
L'elemento identity consente a uno sviluppatore di client di specificare in fase di progettazione l'identità prevista del servizio. Nel processo di handshake tra il client e il servizio, l'infrastruttura [!INCLUDE[indigo1](../../../../../includes/indigo1-md.md)] garantirà che l'identità del servizio previsto corrisponda ai valori di questo elemento consentendone pertanto l'autenticazione. Per ulteriori informazioni, vedere [autenticazione e identità del servizio](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
 \<System. ServiceModel >  
\<client >  
\<endpoint >  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<identity>  
    <certificate encodedValue="String"/>  
    <certificateReference findValue="String"   
       isChainIncluded="Boolean"  
       storeName="AddressBook/AuthRoot/CertificateAuthority/Disallowed/My/Root/TrustedPeople/TrustedPublisher"storeName="  
       storeLocation="LocalMachine/CurrentUser"  
       X509FindType= Enumeration./>  
    <dns value="String"/>  
    <rsa value="String"/>  
    <servicePrincipalName value="String"/>  
    <usePrincipalName value="String"/>  
</identity>  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
 Nessuno.  
  
### <a name="child-elements"></a>Elementi figlio  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|certificato|Specifica le impostazioni di un certificato X.509. L'elemento è di tipo <xref:System.ServiceModel.Configuration.CertificateElement>. Contiene un attributo stringa `encodedValue` che specifica il valore codificato da questo certificato.|  
|certificateReference|Specifica le impostazioni per la convalida del certificato X.509. L'elemento è di tipo <xref:System.ServiceModel.Configuration.CertificateReferenceElement>.|  
|dns|Specifica il DNS di un certificato X.509 usato per autenticare un servizio. Questo elemento contiene un attributo stringa `value` contenente l'identità effettiva.|  
|rsa|Specifica il valore del campo RSA di un certificato X.509 usato per autenticare un servizio presso un client. Questo elemento contiene un attributo stringa `value` contenente l'identità effettiva.|  
|servicePrincipalName|Specifica l'identità di un nome principale di servizio (SPN, Server Principal Name), ovvero il nome principale usato da un client per identificare in modo univoco un'istanza di un servizio. Questo elemento contiene un attributo stringa `value` contenente il nome principale effettivo. L'elemento è di tipo <xref:System.ServiceModel.Configuration.ServicePrincipalNameElement>.|  
|nomeEntitàUtente|Specifica l'identità di un nome principale dell'utente (UPN, User Principal Name), ovvero il tipo di nome che un utente usa per accedere a una rete. È costituito dal nome dell'oggetto utente usato in Active Directory seguito dal simbolo "@" e quindi, in genere, dal dominio padre DNS (Domain Name System). Jeff nell'albero di dominio Fabrikam.com sarebbe ad esempio, il nome dell'entità utente [ jeff@fabrikam.com ](mailto:jeffsmith@fabrikam.com).  Questo elemento contiene un attributo stringa `value` contenente il nome principale effettivo. L'elemento è di tipo <xref:System.ServiceModel.Configuration.UserPrincipalNameElement>.|  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<personalizzate >](../../../../../docs/framework/configure-apps/file-schema/wcf/custom.md)|Specifica un resolver peer personalizzato per un'associazione netPeerTcpBinding.|  
|[\<endpoint >](http://msdn.microsoft.com/en-us/13aa23b7-2f08-4add-8dbf-a99f8127c017)|Configura differenti tipi di endpoint.|  
|[\<autorità di certificazione >](../../../../../docs/framework/configure-apps/file-schema/wcf/issuer.md)|Specifica il servizio token di sicurezza del servizio federato.|  
|[\<issuerMetadata >](../../../../../docs/framework/configure-apps/file-schema/wcf/issuermetadata.md)|Specifica l'endpoint dei metadati del servizio token di sicurezza di un servizio federato.|  
|[\<issuedTokenParameters >](../../../../../docs/framework/configure-apps/file-schema/wcf/issuedtokenparameters.md)|Definisce i parametri di un token emesso in un'associazione personalizzata.|  
|[\<localIssuer >](../../../../../docs/framework/configure-apps/file-schema/wcf/localissuer.md)|Specifica un servizio token di sicurezza locale.|  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.ServiceModel.Configuration.IdentityElement>  
 <xref:System.ServiceModel.EndpointAddress>  
 <xref:System.ServiceModel.EndpointAddress.Identity%2A>  
 [L'autenticazione e identità del servizio](../../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md)  
 [Endpoint: Indirizzi, associazioni e contratti](../../../../../docs/framework/wcf/feature-details/endpoints-addresses-bindings-and-contracts.md)
