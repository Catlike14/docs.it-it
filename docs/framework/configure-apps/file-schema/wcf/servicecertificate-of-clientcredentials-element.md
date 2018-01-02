---
title: Elemento &lt;serviceCertificate&gt; di &lt;clientCredentials&gt;
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e50c0ac5-f0df-4c90-b54b-fc602c1f84ea
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 5f6f52eae3ed9ac3236f54c62ce8712656392f0f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="ltservicecertificategt-of-ltclientcredentialsgt-element"></a>Elemento &lt;serviceCertificate&gt; di &lt;clientCredentials&gt;
Specifica un certificato da usare per l'autenticazione di un servizio presso il client.  
  
 \<System. ServiceModel >  
\<i comportamenti >  
\<endpointBehaviors >  
\<comportamento >  
\<clientCredentials >  
\<serviceCertificate >  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<serviceCertificate />  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
 Nessuno.  
  
### <a name="child-elements"></a>Elementi figlio  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<defaultCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/defaultcertificate-element.md)|Specifica un certificato X.509 da usare quando un servizio o STS non ne fornisce uno tramite un protocollo di negoziazione.|  
|[\<scopedCertificates >](../../../../../docs/framework/configure-apps/file-schema/wcf/scopedcertificates-element.md)|Rappresenta una raccolta di certificati X.509 fornita da servizi specifici (con ambito) per l'autenticazione. Questa raccolta è usata in genere per specificare i certificati di servizio per i servizi dei token di sicurezza in un scenario federato.|  
|[\<autenticazione >](../../../../../docs/framework/configure-apps/file-schema/wcf/authentication-of-servicecertificate-element.md)|Specifica i comportamenti di autenticazione per i certificati di servizio usati da un client.|  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[\<clientCredentials >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcredentials.md)|Specifica le credenziali usate per autenticare il client presso un servizio.|  
  
## <a name="remarks"></a>Note  
 Questo elemento di configurazione specifica le impostazioni usate dal client per convalidare il certificato presentato dal servizio usando l'autenticazione SSL. Contiene inoltre i certificati usati dal servizio configurato in modo esplicito nel client per crittografare i messaggi al servizio usando la sicurezza dei messaggi.  
  
 Gli attributi del `serviceCertificate` sono identici agli attributi dell'elemento di [ \<clientCertificate >](../../../../../docs/framework/configure-apps/file-schema/wcf/clientcertificate-of-clientcredentials-element.md).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement>  
 <xref:System.ServiceModel.Configuration.ClientCredentialsElement.ServiceCertificate%2A>  
 <xref:System.ServiceModel.Description.ClientCredentials>  
 <xref:System.ServiceModel.Description.ClientCredentials.ServiceCertificate%2A>  
 <xref:System.ServiceModel.Configuration.X509RecipientCertificateClientElement>  
 <xref:System.ServiceModel.Security.X509CertificateRecipientClientCredential>  
 [Comportamenti di sicurezza](../../../../../docs/framework/wcf/feature-details/security-behaviors-in-wcf.md)  
 [Protezione di client](../../../../../docs/framework/wcf/securing-clients.md)  
 [Uso di certificati](../../../../../docs/framework/wcf/feature-details/working-with-certificates.md)  
 [Protezione di servizi e client](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)
