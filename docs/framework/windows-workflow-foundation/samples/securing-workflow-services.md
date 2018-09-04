---
title: Protezione di servizi flusso di lavoro
ms.date: 03/30/2017
ms.assetid: 53f84ad5-1ed1-4114-8d0d-b12e8a021c6e
ms.openlocfilehash: 28c34ecf7d6d781bfa461b2737cb9325a657f47e
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43524335"
---
# <a name="securing-workflow-services"></a>Protezione di servizi flusso di lavoro
Nell'esempio di servizio flusso di lavoro protetto vengono illustrate le procedure riportate di seguito:  
  
-   Creazione di un servizio flusso di lavoro di base usando le attività <xref:System.ServiceModel.Activities.Receive> e <xref:System.ServiceModel.Activities.SendReply>.  
  
-   Utilizzo della configurazione di Windows Communication Foundation (WCF) per definire endpoint sicuri per l'utilizzo dal servizio del flusso di lavoro.  
  
-   Creazione di richieste all'interno di criteri personalizzati e utilizzo di <xref:System.ServiceModel.ServiceAuthorizationManager> per convalidare richieste.  
  
## <a name="demonstrates"></a>Dimostrazione  
 Utilizzo della sicurezza WCF per proteggere la comunicazione tra client e servizio flusso di lavoro,con autorizzazione basata sulle attestazioni  
  
## <a name="discussion"></a>Discussione  
 In questo esempio illustra l'uso dell'infrastruttura di sicurezza WCF per proteggere un servizio del flusso di lavoro come si farebbe con un normale servizio WCF. In particolare, viene usata una richiesta personalizzata per l'autorizzazione. In questo caso, viene usato <xref:System.ServiceModel.WSHttpBinding> e la sicurezza in modalità messaggio con credenziali di Windows.  
  
 L'oggetto personalizzato <xref:System.IdentityModel.Policy.IAuthorizationPolicy> (`CustomNameCheckerPolicy`) esegue il controllo del nome utente di Windows del client e di un carattere specifico. Se tale carattere è presente, la richiesta viene creata e aggiunta a <xref:System.IdentityModel.Policy.EvaluationContext>. In questo modo, i criteri personalizzati dichiarano che il client dispone di questo carattere nel nome utente. È possibile eseguire query su questa richiesta per tutta la durata della chiamata. È possibile trovare il carattere in `Constants.cs`.  
  
 I criteri di autorizzazione cercano la richiesta in `SecureWorkFlowAuthZManager`. Se viene trovata, viene restituito `true` e al flusso di lavoro è consentito procedere. In caso contrario, viene restituito `false` che causa la restituzione al client di un messaggio 'Accesso negato'. Nel contesto sono presenti altre richieste che possono essere esaminate in `SecureWorkFlowAuthZManager`.  
  
#### <a name="to-run-this-sample"></a>Per eseguire l'esempio  
  
1.  Eseguire [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] con privilegi di amministratore.  
  
2.  Caricare SecuringWorkflowServices.sln in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
3.  Per compilare la soluzione, premere CTRL+MAIUSC+B.  
  
4.  Impostare il progetto Service come progetto di avvio per la soluzione.  
  
5.  Per avviare l'esempio senza debug, premere CTRL+F5.  
  
6.  Impostare il progetto Client come progetto di avvio per la soluzione.  
  
7.  Premere CTRL+F5 per avviare l'esempio senza debug.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare al [Windows Communication Foundation (WCF) e gli esempi di Windows Workflow Foundation (WF) per .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti i Windows Communication Foundation (WCF) e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] esempi. Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\Services\SecuringWorkflowServices`
