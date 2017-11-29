---
title: Meccanismi del controllo di accesso
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- WCF security
- access control [WCF]
ms.assetid: 9d576122-3f55-4425-9acf-b23d0781e966
caps.latest.revision: "13"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: f43de08a81afcf9ff6ab29b862f22c2935eca55f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="access-control-mechanisms"></a>Meccanismi del controllo di accesso
In [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] le possibilità di controllo dell'accesso sono numerose. In questo argomento vengono discussi brevemente i vari meccanismi e vengono forniti suggerimenti sulle circostanze in cui utilizzarli. L'argomento consente quindi di selezionare il meccanismo corretto da utilizzare. Le tecnologie di accesso sono elencate in ordine di complessità. La tecnologia più semplice è <xref:System.Security.Permissions.PrincipalPermissionAttribute>, la più complessa è il modello di identità.  
  
 Oltre a questi meccanismi, la rappresentazione e delega con [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è illustrato in [delega e rappresentazione](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md).  
  
## <a name="principalpermissionattribute"></a>PrincipalPermissionAttribute  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute> viene utilizzato per limitare l'accesso a un metodo del servizio. Quando l'attributo è applicato a un metodo, può essere utilizzato per richiedere l'identità o l'appartenenza di un chiamante specifico in un gruppo di Windows o in un ruolo [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]. Se il client viene autenticato utilizzando un certificato X.509, acquisisce un'identità primaria costituita dal nome del soggetto e dall'identificazione personale del certificato.  
  
 Utilizzare <xref:System.Security.Permissions.PrincipalPermissionAttribute> per controllare l'accesso alle risorse del computer in cui il servizio è in esecuzione e se gli utenti del servizio faranno sempre parte dello stesso dominio Windows nel quale il servizio è in esecuzione. È possibile creare facilmente gruppi di Windows che presentano livelli di accesso specifici (ad esempio nessuno, sola lettura o lettura e scrittura).  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]utilizzo dell'attributo, vedere [procedura: limitare l'accesso con la classe PrincipalPermissionAttribute](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md). [!INCLUDE[crabout](../../../../includes/crabout-md.md)]identità, vedere [autenticazione e identità del servizio](../../../../docs/framework/wcf/feature-details/service-identity-and-authentication.md).  
  
## <a name="aspnet-membership-provider"></a>Provider di appartenenze ASP.NET  
 Una funzionalità di [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] è il provider di appartenenza. Anche se tecnicamente il provider di appartenenza non è un meccanismo per il controllo dell'accesso, consente di controllare l'accesso al servizio limitando il set di possibili identità che possono accedere all'endpoint del servizio. La funzionalità di appartenenza comprende un database che può essere popolato con combinazioni nome utente/password che consentono agli utenti di un sito Web di creare account nel sito. Per accedere a un servizio che utilizza il provider di appartenenza, è necessario che l'utente esegua la procedura di accesso indicando nome utente e password.  
  
> [!NOTE]
>  È necessario innanzitutto popolare il database con la funzionalità [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], quindi è possibile per un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] utilizzare tale database a scopo di autorizzazione.  
  
 È inoltre possibile utilizzare la funzionalità di appartenenza se si dispone già di un database di appartenenza di un sito Web [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] esistente e si desidera consentire agli stessi utenti di utilizzare il servizio, autorizzandoli con lo stesso nome utente e password.  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]utilizzando la funzionalità di appartenenza in un [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] del servizio, vedere [procedura: utilizzare il Provider di appartenenze ASP.NET](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-membership-provider.md).  
  
## <a name="aspnet-role-provider"></a>Provider di ruoli ASP.NET  
 Un'altra funzionalità di [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] consiste nella possibilità di gestire l'autorizzazione mediante ruoli. Il provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] consente a uno sviluppatore di creare ruoli per gli utenti e di assegnare ogni utente a uno o più ruoli. Come per il provider di appartenenza, i ruoli e le assegnazioni sono archiviati in un database e possono essere popolati mediante strumenti forniti da una particolare implementazione del provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)]. Come per la funzionalità di appartenenza, gli sviluppatori di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] possono utilizzare le informazioni contenute nel database per autorizzare gli utenti del servizio in base ai ruoli. Essi, ad esempio, possono utilizzare il provider di ruoli in combinazione con il meccanismo di controllo dell'accesso `PrincipalPermissionAttribute` descritto in precedenza.  
  
 È inoltre possibile utilizzare il provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] se si dispone già di un database del provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] esistente e si desidera utilizzare lo stesso set di regole e assegnazioni utente nel servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]tramite la funzionalità di provider di ruoli, vedere [procedura: utilizzare il Provider di ruoli ASP.NET con un servizio](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md).  
  
## <a name="authorization-manager"></a>Gestione autorizzazioni  
 Un'altra funzionalità riunisce la Gestione autorizzazioni (AzMan) e il provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] per l'autorizzazione dei client. Quando [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] ospita un servizio Web, AzMan può essere integrato nell'applicazione per fare in modo che l'autorizzazione al servizio venga eseguita tramite AzMan. La funzionalità di Gestione ruoli di [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] fornisce un'API per gestire ruoli applicazione, aggiungere e rimuovere utenti dai ruoli e controllare l'appartenenza al ruolo. Con questa API non è tuttavia possibile eseguire una query per appurare se un utente è autorizzato a eseguire una determinata attività o operazione. AzMan consente di definire operazioni singole e di riunirle in attività. Con AZMan, oltre a controlli del ruolo è inoltre possibile verificare se un utente è autorizzato a eseguire un'attività. L'assegnazione del ruolo e l'autorizzazione all'esecuzione dell'attività possono essere configurate esternamente all'applicazione o eseguite a livello di programmazione all'interno dell'applicazione. Lo snap-in MMC (Microsoft Management Console) per l'amministrazione di AzMan consente agli amministratori di modificare le attività che un ruolo può eseguire in fase di esecuzione e di gestire l'appartenenza di ogni utente ai ruoli.  
  
 È inoltre possibile utilizzare AzMan e il provider di ruoli [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] se si dispone già dell'accesso a un'installazione di AzMan esistente e si desidera autorizzare gli utenti del servizio utilizzando le funzionalità della combinazione AzMan/provider di ruoli.  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]AzMan e [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] provider di ruoli, vedere [procedura: utilizzare Gestione autorizzazioni (AzMan) con ASP.NET 2.0](http://go.microsoft.com/fwlink/?LinkId=88951). [!INCLUDE[crabout](../../../../includes/crabout-md.md)]con AzMan e il provider di ruoli per [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] servizi, vedere [procedura: utilizzare il Provider di ruoli ASP.NET di gestione autorizzazioni con un servizio](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md).  
  
## <a name="identity-model"></a>Modello di identità  
 Il modello di identità è un set di API che consentono di gestire attestazioni e criteri per autorizzare client. Con il modello di identità, è possibile esaminare ogni attestazione contenuta in credenziali che il chiamante ha utilizzato per autenticarsi nel servizio, confrontare le attestazioni con il set di criteri per il servizio e concedere o negare l'accesso in base al confronto.  
  
 Utilizzare il modello di identità se sono necessari un controllo preciso e la possibilità di impostare criteri specifici prima di concedere l'accesso. Quando si utilizza <xref:System.Security.Permissions.PrincipalPermissionAttribute>, ad esempio, il criterio consiste semplicemente nel fatto che l'identità dell'utente viene autenticata e appartiene a un ruolo specifico. Con il modello di identità, al contrario, è possibile creare un criterio in base al quale l'utente deve avere più di 18 anni ed essere in possesso di patente di guida valida perché gli sia consentito visualizzare un documento.  
  
 Un esempio della possibilità di avvalersi del controllo dell'accesso basato su attestazioni del modello di identità consiste nell'utilizzo di credenziali federate nello scenario del token rilasciato. [!INCLUDE[crabout](../../../../includes/crabout-md.md)]federazione e i token emessi, vedere [federazione e i token emessi](../../../../docs/framework/wcf/feature-details/federation-and-issued-tokens.md).  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]il modello di identità, vedere [gestione attestazioni e autorizzazioni con il modello di identità](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Security.Permissions.PrincipalPermissionAttribute>  
 [Procedura: Limitare l'accesso con la classe PrincipalPermissionAttribute](../../../../docs/framework/wcf/how-to-restrict-access-with-the-principalpermissionattribute-class.md)  
 [Procedura: utilizzare il Provider di ruoli ASP.NET con un servizio](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-role-provider-with-a-service.md)  
 [Procedura: utilizzare il Provider di ruoli ASP.NET di gestione autorizzazioni con un servizio](../../../../docs/framework/wcf/feature-details/how-to-use-the-aspnet-authorization-manager-role-provider-with-a-service.md)  
 [Gestione attestazioni e autorizzazioni con il modello di identità](../../../../docs/framework/wcf/feature-details/managing-claims-and-authorization-with-the-identity-model.md)  
 [Delega e rappresentazione](../../../../docs/framework/wcf/feature-details/delegation-and-impersonation-with-wcf.md)
