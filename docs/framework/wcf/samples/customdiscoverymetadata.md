---
title: CustomDiscoveryMetadata
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c42455fd-3652-4b7e-b698-ab3a2bb52e48
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4b4a68204d8ae5d2a338d60498522810a557e575
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="customdiscoverymetadata"></a>CustomDiscoveryMetadata
In questo esempio viene illustrato come inserire metadati XML personalizzati nei metadati di individuazione per un endpoint individuabile esposto da un servizio. Nell'esempio viene quindi illustrato come un client può eseguire la ricerca del servizio ed estrarre questi dati personalizzati. Questo esempio è costituito da due progetti, ovvero il servizio e il client.  
  
## <a name="service"></a>Servizio  
 Nel metodo `main` dell'esempio un oggetto di tipo <xref:System.Xml.Linq.XElement> viene popolato con i campi desiderati e aggiunto a <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior>. Questo <xref:System.ServiceModel.Discovery.EndpointDiscoveryBehavior> viene aggiunto a un particolare endpoint. Nel momento in cui viene individuato quel particolare endpoint, i metadati di individuazione contengono i dati personalizzati aggiunti.  
  
## <a name="client"></a>Client  
 Nell'esempio viene illustrato il metodo <xref:System.ServiceModel.Discovery.DiscoveryClient.Find%2A> chiamato su un oggetto <xref:System.ServiceModel.Discovery.DiscoveryClient>. Sull'oggetto <xref:System.ServiceModel.Discovery.FindResponse> risultante viene eseguita una query per individuare gli elementi XML appropriati e previsti. Questi elementi vengono quindi stampati sulla console.  
  
#### <a name="to-use-this-sample"></a>Per usare questo esempio  
  
1.  Caricare la soluzione del progetto in [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] e compilare il progetto.  
  
2.  Eseguire innanzitutto l'applicazione del servizio, generata in [directory soluzione di base]\service\bin\debug, quindi eseguire l'applicazione client, generata in [directory soluzione di base]\Client\bin\debug  
  
3.  Si noti che il servizio viene portato online, il client individua il servizio e stampa i metadati pubblicati nell'endpoint.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] . Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Extensibility\DiscoveryExtensibility\CustomDiscoveryMetadata`  
  
## <a name="see-also"></a>Vedere anche
