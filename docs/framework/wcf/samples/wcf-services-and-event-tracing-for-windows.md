---
title: Servizi WCF e traccia eventi per Windows
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: eda4355d-0bd0-4dc9-80a2-d2c832152272
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: ed3b7b370ed6b1d9a900579ff0e6f1b0a22290c3
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="wcf-services-and-event-tracing-for-windows"></a>Servizi WCF e traccia eventi per Windows
In questo esempio viene descritto come usare la traccia analitica in [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] per generare eventi in Traccia eventi per Windows (ETW). Le tracce analitiche sono eventi generati in corrispondenza di punti chiave nello stack [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] che consentono risolvere i problemi relativi ai servizi [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] in un ambiente di produzione.  
  
 La funzionalità di tracci analitica nei servizi [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] consiste in una traccia che può essere attivata in un ambiente di produzione con impatto minimo sulle prestazioni. Queste tracce vengono inviate come eventi a una sessione ETW.  
  
 In questo esempio è incluso un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] di base in cui gli eventi vengono inviati dal servizio al registro eventi che può essere visualizzato tramite Visualizzatore eventi. È inoltre possibile avviare una sessione ETW dedicata che rimanga in ascolto degli eventi generati dal servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Nell'esempio è incluso uno script che consente di creare una sessione ETW dedicata che archivia gli eventi in un file binario che può essere letto tramite Visualizzatore eventi.  
  
#### <a name="to-use-this-sample"></a>Per usare questo esempio  
  
1.  In [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] aprire il file della soluzione EtwAnalyticTraceSample.sln.  
  
2.  Per compilare la soluzione, premere CTRL+MAIUSC+B.  
  
3.  Per eseguire la soluzione, premere CTRL+F5.  
  
     Nel Web browser, fare clic su **Calculator.svc**. L'URI del documento WSDL per il servizio viene visualizzato nel browser. Copiare l'URI.  
  
     Per impostazione predefinita, il servizio si pone in ascolto delle richieste sulla porta 1378 (http://localhost:1378/Calculator.svc).  
  
4.  Eseguire il client di prova [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] (WcfTestClient.exe).  
  
     Il [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] client di prova (WcfTestClient.exe) si trova nella \< [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] directory di installazione > \Common7\IDE\ WcfTestClient.exe (impostazione predefinita [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] è c:\Programmi\Microsoft Visual Studio 10.0).  
  
5.  All'interno di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] client di prova, aggiungere il servizio selezionando **File**e quindi **Aggiungi servizio**.  
  
     Aggiungere l'indirizzo dell'endpoint nella casella di input. L'indirizzo predefinito è http://localhost:1378/Calculator.svc.  
  
6.  Aprire l'applicazione Visualizzatore eventi.  
  
     Prima di richiamare il servizio, avviare Visualizzatore eventi e verificare che il registro eventi sia in ascolto per rilevare gli eventi generati dal servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
7.  Dal **avviare** dal menu **strumenti di amministrazione**e quindi **Visualizzatore eventi**.  Abilitare il **analitico** e **Debug** log.  
  
8.  Nella visualizzazione struttura ad albero in Visualizzatore eventi, passare a **Visualizzatore eventi**, **registri applicazioni e servizi**, **Microsoft**, **Windows**e quindi **Server applicazioni-applicazioni**. Fare doppio clic su **Server applicazioni-applicazioni**selezionare **vista**e quindi **Visualizza registri analitici e Debug**.  
  
     Verificare che il **Visualizza registri analitici e Debug** opzione è selezionata.  
  
9. Abilitare il **analitico** log.  
  
     Nella visualizzazione struttura ad albero in Visualizzatore eventi, passare a **Visualizzatore eventi**, **registri applicazioni e servizi**, **Microsoft**, **Windows**e quindi **Server applicazioni-applicazioni**. Fare doppio clic su **analitico** e selezionare **Attiva registro**.  
  
#### <a name="to-test-the-service"></a>Per eseguire il test del servizio  
  
1.  Tornare a client di prova [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)], fare doppio clic su `Divide` e mantenere i valori predefiniti che specificano un valore per il denominatore pari a 0.  
  
     Se il valore del denominatore è 0, il servizio genererà un errore.  
  
2.  Osservare gli eventi creati dal servizio.  
  
     Tornare a Visualizzatore eventi e passare a **Visualizzatore eventi**, **registri applicazioni e servizi**, **Microsoft**, **Windows**e quindi **Server applicazioni-applicazioni**. Fare doppio clic su **analitico** e selezionare **aggiornamento**.  
  
     Gli eventi di traccia analitici di WCF verranno visualizzati nel Visualizzatore eventi. Si noti che poiché un errore è stato generato dal servizio, nel Visualizzatori eventi viene visualizzato un evento traccia di errore.  
  
3.  Ripetere i passaggi 1 e 2 con valori di input validi. Il valore del parametro `N2` deve essere un numero diverso da 0.  
  
     Aggiornare il canale analitico per visualizzare gli eventi WCF e osservare come non includano alcun evento di errore.  
  
 Nell'esempio vengono illustrati gli eventi di traccia analitici creati da un servizio WCF.  
  
#### <a name="to-cleanup-optional"></a>Per eseguire la pulizia (facoltativo)  
  
1.  Aprire Visualizzatore eventi.  
  
2.  Passare a **Visualizzatore eventi**, **registri applicazioni e servizi**, **Microsoft**, **Windows**e quindi  **Server applicazioni-applicazioni**. Fare doppio clic su **analitico** e selezionare **Disattiva registro**.  
  
3.  Passare a **Visualizzatore eventi**, **registri applicazioni e servizi**, **Microsoft**, **Windows**e quindi  **Server applicazioni-applicazioni**. Fare doppio clic su **analitico** e selezionare **Cancella Log**.  
  
4.  Scegliere il **deselezionare** opzione per cancellare gli eventi.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] . Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Management\ETWTracing`  
  
## <a name="see-also"></a>Vedere anche  
 [Esempi di monitoraggio di AppFabric](http://go.microsoft.com/fwlink/?LinkId=193959)
