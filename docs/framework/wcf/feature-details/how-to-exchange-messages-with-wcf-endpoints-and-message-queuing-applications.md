---
title: 'Procedura: scambiare messaggi con endpoint WCF e con applicazioni del sistema di accodamento dei messaggi'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 62210fd8-a372-4d55-ab9b-c99827d1885e
caps.latest.revision: "18"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: d09b8e662b2876fa5d5c5246ea7e7a4998cde9ea
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-exchange-messages-with-wcf-endpoints-and-message-queuing-applications"></a>Procedura: scambiare messaggi con endpoint WCF e con applicazioni del sistema di accodamento dei messaggi
Per integrare le applicazioni esistenti del sistema di accodamento dei messaggi (MSMQ) con le applicazioni di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] è possibile utilizzare l'associazione di integrazione con MSMQ per convertire i messaggi MSMQ in messaggi [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e viceversa. Ciò consente di chiamare applicazioni MSMQ riceventi tramite un client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] nonché chiamare servizi [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] tramite applicazioni MSMQ mittenti.  
  
 Contenuto della sezione viene descritto come utilizzare l'associazione <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding> per la comunicazione in coda tra (1) un client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e un'applicazione MSMQ server scritta utilizzando System.Messaging e (2) un'applicazione MSMQ client e un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
 Per un esempio completo che illustra come chiamare un'applicazione MSMQ ricevente da un [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] client, vedere il [Windows Communication Foundation a Accodamento messaggi](../../../../docs/framework/wcf/samples/wcf-to-message-queuing.md) esempio.  
  
 Per un esempio completo che illustra come chiamare un [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] del servizio da un client MSMQ, vedere il [Accodamento messaggi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/message-queuing-to-wcf.md) esempio.  
  
### <a name="to-create-a-wcf-service-that-receives-messages-from-a-msmq-client"></a>Per creare un servizio WCF che riceve messaggi da un client MSMQ  
  
1.  Creare un'interfaccia che definisca il contratto del servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] che riceve messaggi in coda da un'applicazione MSMQ mittente, come illustrato nell'esempio di codice seguente.  
  
     [!code-csharp[S_MsmqToWcf#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#1)]
     [!code-vb[S_MsmqToWcf#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#1)]  
  
2.  Implementare l'interfaccia e applicare l'attributo <xref:System.ServiceModel.ServiceBehaviorAttribute> alla classe, come mostrato nell'esempio di codice seguente.  
  
     [!code-csharp[S_MsmqToWcf#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_msmqtowcf/cs/service.cs#2)]
     [!code-vb[S_MsmqToWcf#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_msmqtowcf/vb/service.vb#2)]  
  
3.  Creare un file di configurazione che specifica l'associazione <xref:System.ServiceModel.MsmqIntegration.MsmqIntegrationBinding>.  
  
  
  
4.  Creare un'istanza di un oggetto <xref:System.ServiceModel.ServiceHost> che utilizza l'associazione configurata.  
  
  
  
### <a name="to-create-a-wcf-client-that-sends-messages-to-a-msmq-receiver-application"></a>Per creare un client WCF che invia messaggi a un'applicazione MSMQ ricevente  
  
1.  Creare un'interfaccia che definisca il contratto di servizio del client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] che invii messaggi in coda a un'applicazione MSMQ ricevente, come illustrato nell'esempio di codice seguente.  
  
     [!code-csharp[S_WcfToMsmq#6](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/proxy.cs#6)]
     [!code-vb[S_WcfToMsmq#6](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/proxy.vb#6)]  
  
2.  Definire una classe client che verrà utilizzata dal client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] per chiamare l'applicazione MSMQ ricevente.  
  
     [!code-csharp[S_WcfToMsmq#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#2)]
     [!code-vb[S_WcfToMsmq#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#2)]  
  
3.  Creare una configurazione che specifichi l'utilizzo dell'associazione MsmqIntegrationBinding.  
  
     [!code-csharp[S_WcfToMsmq#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/snippets.cs#3)]
     [!code-vb[S_WcfToMsmq#3](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/s_wcftomsmq/vb/snippets.vb#3)]  
  
4.  Creare un'istanza della classe client e chiamare il metodo definito dal servizio che riceve i messaggi.  
  
     [!code-csharp[S_WcfToMsmq#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/s_wcftomsmq/cs/client.cs#4)]  
  
## <a name="see-also"></a>Vedere anche  
 [Panoramica delle code](../../../../docs/framework/wcf/feature-details/queues-overview.md)  
 [Procedura: scambiare messaggi con endpoint WCF in coda](../../../../docs/framework/wcf/feature-details/how-to-exchange-queued-messages-with-wcf-endpoints.md)  
 [Windows Communication Foundation a Accodamento messaggi](../../../../docs/framework/wcf/samples/wcf-to-message-queuing.md)  
 [Installazione di Accodamento messaggi (MSMQ)](../../../../docs/framework/wcf/samples/installing-message-queuing-msmq.md)  
 [Accodamento messaggi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/message-queuing-to-wcf.md)  
 [Sicurezza del messaggio su Accodamento messaggi](../../../../docs/framework/wcf/samples/message-security-over-message-queuing.md)
