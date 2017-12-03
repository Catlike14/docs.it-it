---
title: Applicazioni client di livello intermedio
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: f9714a64-d0ae-4a98-bca0-5d370fdbd631
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b73641fcbc881e57465f722d3a0f647938a5e12e
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="middle-tier-client-applications"></a>Applicazioni client di livello intermedio
In questo argomento vengono analizzati alcuni aspetti specifici delle applicazioni client di livello intermedio che usano [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)].  
  
## <a name="increasing-middle-tier-client-performance"></a>Miglioramento delle prestazioni dei client di livello intermedio  
 Paragonata alle tecnologie di comunicazione precedenti, ad esempio i servizi Web che usano [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)], la creazione di un'istanza client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] può essere più complessa a causa del vasto set di funzionalità di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Ad esempio, quando un oggetto <xref:System.ServiceModel.ChannelFactory%601> viene aperto può stabilire una sessione protetta con il servizio, una procedura che aumenta il tempo di avvio per l'istanza client. In genere queste funzionalità aggiuntive non influiscono significativamente sulle applicazioni client in quanto il client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] effettua più chiamate e quindi viene chiuso.  
  
 Le applicazioni client di livello intermedio possono tuttavia creare rapidamente molti oggetti client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e devono quindi soddisfare maggiori requisiti di inizializzazione. Per migliorare le prestazioni delle applicazioni di livello intermedio durante le chiamate ai servizi è possibile seguire principalmente due diversi approcci:  
  
-   Memorizzare nella cache l'oggetto client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e riutilizzarlo, se possibile, per chiamate successive.  
  
-   Creare un oggetto <xref:System.ServiceModel.ChannelFactory%601> e usarlo per creare nuovi oggetti di canale client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] per ogni chiamata.  
  
 Quando si seguono queste procedure è opportuno considerare gli aspetti seguenti:  
  
-   Se il servizio gestisce uno stato specifico del client usando una sessione, non è possibile riutilizzare il client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] di livello intermedio con richieste di client di vari livelli poiché lo stato del servizio è associato allo stato del client di livello intermedio.  
  
-   Se il servizio deve eseguire l'autenticazione per ogni singolo client, è necessario creare un nuovo client per ogni richiesta in ingresso nel livello intermedio anziché riutilizzare il client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] di livello intermedio (o l'oggetto di canale client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] ) perché le credenziali client del livello intermedio non possono essere modificate dopo che il client (o [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]) <xref:System.ServiceModel.ChannelFactory%601> è stato creato.  
  
-   Sebbene i canali e i client creati dai canali siano thread-safe, è possibile che non supportino la scrittura di più messaggi in rete contemporaneamente. Se vengono inviati messaggi di grandi dimensioni, in particolare se viene eseguito il flusso, l'operazione di invio potrebbe bloccarsi in attesa del completamento di un'altra operazione di invio. Ciò causa due tipi di problemi: la mancanza di concorrenza e la possibilità di deadlock se il flusso di controllo torna al servizio riutilizzando il canale (ovvero, il client condiviso chiama un servizio il cui percorso di codice comporta un callback al client condiviso). Questa situazione si verifica indipendentemente dal tipo di client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] che si riutilizza.  
  
-   È necessario gestire i canali in stato di errore indipendentemente dal fatto che si condivida o meno il canale. Quando i canali vengono riutilizzati, un canale in stato di errore può tuttavia annullare più richieste o operazioni di invio in sospeso.  
  
 Per un esempio che illustra le procedure consigliate per il riutilizzo di un client di più richieste, vedere [Data Binding in un Client ASP.NET](../../../../docs/framework/wcf/samples/data-binding-in-an-aspnet-client.md).  
  
 È anche possibile migliorare le prestazioni di avvio per i client che usano tipi di dati serializzabili usando la classe <xref:System.Xml.Serialization.XmlSerializer> per generare e compilare il codice di serializzazione per questi tipi di dati in fase di esecuzione. Questa procedura può comportare una riduzione delle prestazioni di avvio. Il [strumento ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) può migliorare le prestazioni di avvio per queste applicazioni per la generazione del codice di serializzazione necessari dagli assembly compilati per l'applicazione. Per ulteriori informazioni, vedere [procedura: migliorare l'avvio del tempo di applicazioni Client WCF usando XmlSerializer](../../../../docs/framework/wcf/feature-details/startup-time-of-wcf-client-applications-using-the-xmlserializer.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Accesso ai servizi tramite client WCF](../../../../docs/framework/wcf/feature-details/accessing-services-using-a-client.md)
