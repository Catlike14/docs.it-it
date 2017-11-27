---
title: Annidamento di TransactionScope all'interno di un servizio
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e7e1ba64-1384-4eba-add8-415636e2d6d0
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 475da3f9204764a2585bd7a50381db7ad72c2b1e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="nesting-of-transactionscope-within-a-service"></a>Annidamento di TransactionScope all'interno di un servizio
Questo esempio è costituito da due scenari che vengono eseguiti per illustrare come gestire le istanze dell'attività <xref:System.Activities.Statements.TransactionScope> all'interno di un servizio. Innanzitutto viene iniziata la transazione usando l'attività <xref:System.Activities.Statements.TransactionScope> per creare una nuova transazione nel client e l'attività <xref:System.ServiceModel.Activities.TransactedReceiveScope> per ricevere e definire l'ambito della durata della transazione sul server. Il primo scenario all'interno del servizio esegue un'attività <xref:System.Activities.Statements.TransactionScope> secondaria per dimostrare l'annidamento delle attività <xref:System.Activities.Statements.TransactionScope> all'interno del servizio. Nel secondo scenario viene illustrato il rispetto dei timeout all'interno delle attività <xref:System.Activities.Statements.TransactionScope> annidate.  
  
## <a name="client-application"></a>Applicazione client  
 L'applicazione client esegue un flusso di lavoro che avvia un'attività <xref:System.Activities.Statements.TransactionScope>, stampa l'ID della transazione distribuita, invia un messaggio al server, propaga la transazione, riceve la risposta, stampa nuovamente l'ID della transazione distribuita e viene completato. Queste operazioni vengono eseguite una volta per ogni scenario del servizio.  
  
## <a name="server-application"></a>Applicazione server  
 Il progetto server è ospitato nell'oggetto <xref:System.ServiceModel.Activities.WorkflowServiceHost> che crea l'endpoint per restare in ascolto del messaggio dal client. Il flusso di lavoro si basa sull'oggetto <xref:System.ServiceModel.Activities.TransactedReceiveScope> che riceve la transazione propagata dal client, stampa l'ID della transazione distribuita, quindi esegue una seconda attività <xref:System.Activities.Statements.TransactionScope>. Nel primo scenario, la transazione viene completata correttamente. Nel secondo scenario, il corpo dell'attività <xref:System.Activities.Statements.TransactionScope> ha un ritardo di cinque secondi e il timeout per la transazione è impostato su due secondi. Quando la transazione scade, viene interrotta.  
  
#### <a name="to-run-the-sample"></a>Per eseguire l'esempio  
  
1.  Aprire la soluzione TransactionServiceExample.sln in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].  
  
2.  Per compilare la soluzione, premere CTRL + MAIUSC + B o scegliere **Compila soluzione** dal **compilare** menu.  
  
3.  Una volta completata la compilazione, la soluzione e scegliere **Imposta progetti di avvio**. Nella finestra di dialogo, selezionare **più progetti di avvio** e assicurarsi che l'azione per entrambi i progetti sia **avviare**.  
  
4.  Premere F5 o scegliere **Avvia debug** dal **Debug** menu. In alternativa, è possibile premere CTRL + F5 o selezionare **Avvia senza eseguire debug** dal **Debug** menu per l'esecuzione senza debug.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] . Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Transactions\TRSComposability`
