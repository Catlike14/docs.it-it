---
title: Dispatcher di canali personalizzati
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 813acf03-9661-4d57-a3c7-eeab497321c6
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 81512576e1d26b63cf65b3a0c9992c2d273d2779
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="custom-channel-dispatcher"></a>Dispatcher di canali personalizzati
In questo esempio viene descritto come compilare lo stack di canali in modo personalizzato implementando direttamente <xref:System.ServiceModel.ServiceHostBase> e come creare un dispatcher del canale personalizzato in un ambiente host Web. Il dispatcher del canale interagisce con <xref:System.ServiceModel.Channels.IChannelListener> per accettare canali e recupera messaggi dallo stack di canali. Questo esempio fornisce anche un esempio di base che illustra come compilare uno stack di canali in un ambiente host Web tramite <xref:System.ServiceModel.Activation.VirtualPathExtension>.  
  
## <a name="custom-servicehostbase"></a>ServiceHostBase personalizzato  
 In questo esempio viene implementato il tipo di base <xref:System.ServiceModel.ServiceHostBase> invece di <xref:System.ServiceModel.ServiceHost> per dimostrare come sostituire l'implementazione di stack di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] con un livello di gestione dei messaggi personalizzato all'interno dello stack di canali. Viene eseguito l'override del metodo virtuale <xref:System.ServiceModel.ServiceHostBase.InitializeRuntime%2A> per compilare i listener del canale e il dispatcher del canale.  
  
 Per implementare un servizio ospitato sul Web, ottenere l'estensione del servizio <xref:System.ServiceModel.Activation.VirtualPathExtension> dalla raccolta <xref:System.ServiceModel.ServiceHostBase.Extensions%2A> e aggiungerla a <xref:System.ServiceModel.Channels.BindingParameterCollection> in modo che il livello di trasporto sia in grado di configurare il listener del canale in base alle impostazioni dell'ambiente host, ovvero le impostazioni Internet Information Services (IIS)/servizio di attivazione dei processi di Windows.  
  
## <a name="custom-channel-dispatcher"></a>Dispatcher di canali personalizzati  
 Il dispatcher del canale personalizzato estende il tipo <xref:System.ServiceModel.Dispatcher.ChannelDispatcherBase>. Tale tipo implementa la logica di programmazione relativa al livello del canale. In questo esempio, solo <xref:System.ServiceModel.Channels.IReplyChannel> viene supportato per il modello di scambio di messaggi request/reply, ma il dispatcher del canale personalizzato può essere esteso facilmente ad altri tipi di canale.  
  
 Il dispatcher apre innanzitutto il listener del canale, quindi accetta il canale di risposta singleton. Con il canale, inizia a inviare messaggi (richieste) in un ciclo infinito. Per ogni richiesta, crea un messaggio di risposta e lo restituisce al client.  
  
## <a name="creating-a-response-message"></a>Creazione di un messaggio di risposta  
 L'elaborazione del messaggio viene implementata nel tipo `MyServiceManager`. Nel metodo `HandleRequest`, l'intestazione `Action` del messaggio viene dapprima controllata per verificare se la richiesta è supportata. Un'azione SOAP predefinita "http://tempuri.org/HelloWorld/Hello" viene definita per fornire applicazione di filtri del messaggio, in modo analogo al concetto di contratto di servizio nell'implementazione di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] di <xref:System.ServiceModel.ServiceHost>.  
  
 Nel caso dell'azione SOAP corretta, l'esempio recupera i dati del messaggio richiesti e genera una risposta corrispondente alla richiesta in modo analogo a quanto si verifica nel caso di <xref:System.ServiceModel.ServiceHost>.  
  
 In questo caso, il verbo HTTP-GET viene gestito in modo speciale restituendo un messaggio HTML personalizzato, affinché sia possibile accedere al servizio da un browser per verificarne la corretta compilazione. Se l'azione SOAP non corrisponde, restituire un messaggio di errore per indicare che la richiesta non è supportata.  
  
 Il client di questo esempio è un client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] normale che non presuppone nulla dal servizio. Pertanto, il servizio è progettato in modo specifico per individuare una corrispondenza tra ciò che si ottiene da una normale implementazione di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] in <xref:System.ServiceModel.ServiceHost>. Di conseguenza, nel client viene richiesto solo un contratto di servizio.  
  
## <a name="using-the-sample"></a>Utilizzo dell'esempio  
 L'esecuzione dell'applicazione client in modo diretto produce l'output seguente.  
  
```Output  
Client is talking to a request/reply WCF service.   
Type what you want to say to the server: Howdy  
Server replied: You said: Howdy. Message id: 1  
Server replied: You said: Howdy. Message id: 2  
Server replied: You said: Howdy. Message id: 3  
Server replied: You said: Howdy. Message id: 4  
Server replied: You said: Howdy. Message id: 5  
```  
  
 È inoltre possibile accedere al servizio da un browser in modo che un messaggio HTTP-GET venga elaborato nel server. In questo modo, verrà restituito testo HTML formattato in modo corretto.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] . Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Extensibility\Channels\CustomChannelDispatcher`
