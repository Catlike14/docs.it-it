---
title: Scenari di distribuzione supportati
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 3399f208-3504-4c70-a22e-a7c02a8b94a6
caps.latest.revision: "20"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 3e6039567e4fad7fe4c014665dd3ae0c3082a9d0
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="supported-deployment-scenarios"></a>Scenari di distribuzione supportati
Il sottoinsieme delle funzionalità [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] supportate da utilizzare in applicazioni parzialmente attendibili è progettato per soddisfare i requisiti di alcuni scenari, ma non di tutti, per l'utilizzo di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Nel server, [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] soddisfa i requisiti di provider di hosting condiviso a livello di Internet che eseguono applicazioni di terze parti nell'autorizzazione di Attendibilità media di [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] impostata per ragioni di sicurezza. Nel client il supporto dell'attendibilità parziale di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è progettato per soddisfare i requisiti di tecnologie di distribuzione come la [distribuzione ClickOnce](http://go.microsoft.com/fwlink/?LinkId=83712) o la tecnologia Applicazione browser XAML di [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)], che consentono la distribuzione sicura e uniforme di applicazioni desktop da siti non attendibili.  
  
## <a name="minimum-permission-requirements"></a>Requisiti di autorizzazione minimi  
 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] supporta un sottoinsieme di funzionalità in applicazioni in esecuzione con uno dei set di autorizzazioni denominati standard seguenti:  
  
-   Autorizzazioni Attendibilità media  
  
-   Autorizzazioni Area Internet  
  
 Il tentativo di utilizzare [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] in applicazioni parzialmente attendibili con le autorizzazioni più restrittive può generare eccezioni di sicurezza in fase di esecuzione.  
  
 Per altre informazioni sulle funzionalità supportate in questi set di autorizzazioni, vedere [Partial Trust Feature Compatibility](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md).  
  
## <a name="partial-trust-on-the-server"></a>Attendibilità parziale nel server  
 Numerosi provider commerciali di servizi host di applicazioni Web [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] richiedono che le applicazioni che sono in esecuzione nei loro server vengano eseguite nel set di autorizzazioni di Attendibilità media [!INCLUDE[vstecasplong](../../../../includes/vstecasplong-md.md)] . [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]servizi possono essere eseguiti in questi ambienti a condizione che utilizzino il <xref:System.ServiceModel.BasicHttpBinding>, <xref:System.ServiceModel.WebHttpBinding>, o <<!--zz xref:System.ServiceModel.WsHttpBinding --> `xref:System.ServiceModel.WsHttpBinding`> con la sicurezza a livello di trasporto.  
  
 I servizi[!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] in esecuzione in ambienti host ad Attendibilità media possono fungere anche da servizi di livello intermedio inviando messaggi ad altri server in risposta alle richieste del client. Gli scenari di livello medio nel server sono supportati se l'ambiente host ha concesso all'applicazione la <xref:System.Net.WebPermission> appropriata per effettuare richieste in uscita al server desiderato.  
  
 Oltre alla messaggistica SOAP, l'utilizzo di una delle associazioni SOAP supportate, [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] supporta <xref:System.ServiceModel.WebHttpBinding> per creare servizi in stile Web in applicazioni parzialmente attendibili. Il [modello di programmazione HTTP Web WCF](../../../../docs/framework/wcf/feature-details/wcf-web-http-programming-model.md), [diffusione WCF](../../../../docs/framework/wcf/feature-details/wcf-syndication.md), e [integrazione AJAX e supporto JSON](../../../../docs/framework/wcf/feature-details/ajax-integration-and-json-support.md) le funzionalità di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] sono tutte supportate nell'attendibilità parziale.  
  
 I servizi flussi di lavoro richiedono autorizzazioni di attendibilità totale e non possono essere utilizzati in applicazioni parzialmente attendibili.  
  
 [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)] [Procedura: Usare l'attendibilità media in ASP.NET 2.0](http://go.microsoft.com/fwlink/?LinkId=84603).  
  
## <a name="partial-trust-on-the-client"></a>Attendibilità parziale nel client  
 Quando si scarica ed esegue codice dai siti Internet non attendibili, è necessario adottare determinate precauzioni di sicurezza. La [distribuzione ClickOnce](http://go.microsoft.com/fwlink/?LinkId=83712) e la tecnologia Applicazione browser XAML (XBAP) di [!INCLUDE[avalon2](../../../../includes/avalon2-md.md)]usano entrambe l'attendibilità parziale per concedere autorizzazioni limitate (area Internet) al codice non attendibile.  
  
 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] può essere usato per comunicare con server remoti da applicazioni parzialmente attendibili distribuite tramite la [distribuzione ClickOnce](http://go.microsoft.com/fwlink/?LinkId=83712) o XBAP. Il set di autorizzazioni dell'area Internet include <xref:System.Net.WebPermission> per l'host di origine, in modo da consentire a queste applicazioni di comunicare con il proprio server di origine usando una qualsiasi delle associazioni di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] supportate descritte in [Partial Trust Feature Compatibility](../../../../docs/framework/wcf/feature-details/partial-trust-feature-compatibility.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Sicurezza dall'accesso di codice](http://go.microsoft.com/fwlink/?LinkId=83717)  
 [Panoramica di Windows Presentation Foundation ospitate da Browser](http://go.microsoft.com/fwlink/?LinkId=98397)  
 [Attendibilità parziale](../../../../docs/framework/wcf/feature-details/partial-trust.md)  
 [Attendibilità media ASP.Net](http://go.microsoft.com/fwlink/?LinkId=69328)
