---
title: Panoramica dell'architettura dei metadati
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: metadata [WCF], overview
ms.assetid: 1d37645e-086d-4d68-a358-f3c5b6e8205e
caps.latest.revision: "24"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: cc42aa130ce5da05739af43d287441d1644d55c3
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="metadata-architecture-overview"></a>Panoramica dell'architettura dei metadati
[!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] fornisce un'infrastruttura avanzata per esportare, pubblicare, recuperare e importare metadati di servizio. I servizi di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] utilizzano i metadati per descrivere come interagire con gli endpoint del servizio affinché strumenti quali Svcutil.exe possano generare automaticamente il codice client per accedere al servizio.  
  
 La maggior parte dei tipi che costituiscono l'infrastruttura dei metadati di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] risiede nello spazio dei nomi <xref:System.ServiceModel.Description>.  
  
 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] utilizza la classe <xref:System.ServiceModel.Description.ServiceEndpoint> per descrivere endpoint in un servizio. È possibile utilizzare [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] per generare metadati per endpoint del servizio o importare metadati del servizio per generare istanze di <xref:System.ServiceModel.Description.ServiceEndpoint>.  
  
 [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] rappresenta i metadati per un servizio come istanza del tipo <xref:System.ServiceModel.Description.MetadataSet>, la cui struttura dipende strettamente dal formato di serializzazione dei metadati definito in WS-MetadataExchange. Il tipo <xref:System.ServiceModel.Description.MetadataSet> raggruppa i metadati effettivi del servizio, ad esempio i documenti Web Services Description Language (WSDL), i documenti di XML Schema o le espressioni WS-Policy, come raccolta di istanze di <xref:System.ServiceModel.Description.MetadataSection>. Ogni istanza di <xref:System.ServiceModel.Description.MetadataSection?displayProperty=nameWithType> contiene un sottolinguaggio dei metadati specifici e un identificatore. Una <xref:System.ServiceModel.Description.MetadataSection?displayProperty=nameWithType> può contenere gli elementi seguenti nella proprietà <xref:System.ServiceModel.Description.MetadataSection.Metadata%2A?displayProperty=nameWithType>:  
  
-   Metadati non elaborati.  
  
-   Istanza di <xref:System.ServiceModel.Description.MetadataReference>.  
  
-   Istanza di <xref:System.ServiceModel.Description.MetadataLocation>.  
  
 Le istanze di <xref:System.ServiceModel.Description.MetadataReference?displayProperty=nameWithType> puntano a un altro endpoint di scambio di metadati (MEX) e le istanze di <xref:System.ServiceModel.Description.MetadataLocation?displayProperty=nameWithType> puntano a un documento di metadati utilizzando un URL HTTP. [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] supporta l'utilizzo di documenti WSDL per descrivere endpoint di servizio, contratti di servizio, associazioni, modelli di scambio di messaggi, messaggi e messaggi di errore implementati da un servizio. I tipi di dati utilizzati dal servizio sono descritti nei documenti WSDL utilizzando XML Schema. [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][Schema importazione ed esportazione](../../../../docs/framework/wcf/feature-details/schema-import-and-export.md). È possibile utilizzare [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] per esportare e importare estensioni WSDL per il comportamento del servizio, i comportamenti del contratto e gli elementi di associazione che estendono la funzionalità di un servizio. [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][Esportazione di metadati personalizzati per un'estensione WCF](../../../../docs/framework/wcf/extending/exporting-custom-metadata-for-a-wcf-extension.md).  
  
## <a name="exporting-service-metadata"></a>Esportazione di metadati del servizio  
 In [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)], *esportazione dei metadati* è il processo di descrivere gli endpoint del servizio e quindi proiettarli in una rappresentazione parallela standardizzata che i client possono usare per comprendere come utilizzare il servizio. Per esportare metadati da istanze di <xref:System.ServiceModel.Description.ServiceEndpoint>, utilizzare un'implementazione della classe astratta <xref:System.ServiceModel.Description.MetadataExporter>. Un'implementazione <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType> genera metadati che sono incapsulati in un'istanza di <xref:System.ServiceModel.Description.MetadataSet>.  
  
 La classe <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType> fornisce un framework per la generazione di espressioni di criteri che descrivono le funzionalità e i requisiti di un'associazione di endpoint e le operazioni, i messaggi e gli errori pertinenti. Queste espressioni di criteri vengono acquisite in un'istanza di <xref:System.ServiceModel.Description.PolicyConversionContext>. Un'implementazione di <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType> può quindi collegare tali espressioni di criteri ai metadati che genera.  
  
 <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType> chiama ogni <xref:System.ServiceModel.Channels.BindingElement?displayProperty=nameWithType> che implementa l'interfaccia <xref:System.ServiceModel.Description.IPolicyExportExtension> nell'associazione di un <xref:System.ServiceModel.Description.ServiceEndpoint> durante la generazione di un oggetto <xref:System.ServiceModel.Description.PolicyConversionContext> che deve essere utilizzato dall'implementazione di <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType>. È possibile esportare nuove asserzioni di criteri implementando l'interfaccia <xref:System.ServiceModel.Description.IPolicyExportExtension> nelle implementazioni personalizzate del tipo <xref:System.ServiceModel.Channels.BindingElement>.  
  
 Il tipo <xref:System.ServiceModel.Description.WsdlExporter> è un'implementazione della classe astratta <xref:System.ServiceModel.Description.MetadataExporter?displayProperty=nameWithType> fornita da [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Il tipo <xref:System.ServiceModel.Description.WsdlExporter> genera metadati WSDL con allegate le espressioni di criteri.  
  
 Per esportare metadati WSDL personalizzati o estensioni WSDL per i comportamenti degli endpoint, i comportamenti del contratto o elementi di associazione in un endpoint del servizio, è possibile implementare l'interfaccia <xref:System.ServiceModel.Description.IWsdlExportExtension>. <xref:System.ServiceModel.Description.WsdlExporter> cerca in un'istanza <xref:System.ServiceModel.Description.ServiceEndpoint> elementi di associazione, comportamenti dell'operazione, comportamenti del contratto e comportamenti degli endpoint che implementano l'interfaccia <xref:System.ServiceModel.Description.IWsdlExportExtension> in fase di generazione del documento WSDL.  
  
## <a name="publishing-service-metadata"></a>Pubblicazione di metadati del servizio  
 I servizi [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] pubblicano i metadati tramite l'esposizione di uno o più endpoint dei metadati. La pubblicazione dei metadati del servizio li rende disponibili utilizzando i protocolli standard, ad esempio le richieste MEX e HTTP/GET. Gli endpoint dei metadati sono accomunati ad altri endpoint del servizio dal fatto di avere un indirizzo, un'associazione e un contratto. È possibile aggiungere endpoint dei metadati a un host del servizio nella configurazione o nel codice.  
  
 Per pubblicare endpoint dei metadati per un servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)], è innanzitutto necessario aggiungere al servizio un'istanza del comportamento del servizio <xref:System.ServiceModel.Description.ServiceMetadataBehavior>. L'aggiunta di un'istanza <xref:System.ServiceModel.Description.ServiceMetadataBehavior?displayProperty=nameWithType> al servizio aggiunge a quest'ultimo la capacità di pubblicare metadati esponendo uno o più endpoint dei metadati. Dopo aver aggiunto il comportamento del servizio <xref:System.ServiceModel.Description.ServiceMetadataBehavior?displayProperty=nameWithType>, è possibile esporre gli endpoint dei metadati che supportano il protocollo MEX o quelli che rispondono alle richieste HTTP/GET.  
  
 Per aggiungere endpoint dei metadati che utilizzano il protocollo MEX, aggiungere gli endpoint del servizio all'host del servizio che utilizza il contratto di servizio denominato IMetadataExchange.[!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] definisce il <xref:System.ServiceModel.Description.IMetadataExchange> interfaccia con il nome del contratto di servizio. Endpoint WS-MetadataExchange, o endpoint MEX, possono utilizzare una delle quattro associazioni predefinite che i metodi factory statici espongono sulla classe <xref:System.ServiceModel.Description.MetadataExchangeBindings> in modo che corrispondano alle associazioni predefinite utilizzate dagli strumenti [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)], ad esempio Svcutil.exe. È inoltre possibile configurare gli endpoint dei metadati MEX utilizzando un'associazione personalizzata.  
  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> utilizza un oggetto <xref:System.ServiceModel.Description.WsdlExporter?displayProperty=nameWithType> per esportare i metadati per tutti gli endpoint nel servizio. [!INCLUDE[crabout](../../../../includes/crabout-md.md)]l'esportazione dei metadati da un servizio, vedere [di esportazione e importazione di metadati](../../../../docs/framework/wcf/feature-details/exporting-and-importing-metadata.md).  
  
 <xref:System.ServiceModel.Description.ServiceMetadataBehavior> aggiunge all'host del servizio un'istanza di <xref:System.ServiceModel.Description.ServiceMetadataExtension> come estensione. <xref:System.ServiceModel.Description.ServiceMetadataExtension?displayProperty=nameWithType> fornisce l'implementazione per i metadati che pubblicano protocolli. È inoltre possibile utilizzare <xref:System.ServiceModel.Description.ServiceMetadataExtension?displayProperty=nameWithType> per ottenere i metadati del servizio in fase di esecuzione accedendo alla proprietà <xref:System.ServiceModel.Description.ServiceMetadataExtension.Metadata%2A>.  
  
> [!CAUTION]
>  Se si aggiunge un endpoint MEX al file di configurazione dell'applicazione e quindi si tenta di aggiungere l'oggetto <xref:System.ServiceModel.Description.ServiceMetadataBehavior> all'host del servizio nel codice, verrà generata l'eccezione seguente:  
>   
>  System.InvalidOperationException: Impossibile trovare il nome contratto 'IMetadataExchange' nell'elenco dei contratti implementati dal servizio Service1. Aggiungere un elemento ServiceMetadataBehavior al file di configurazione oppure direttamente a ServiceHost per abilitare il supporto per questo contratto.  
>   
>  Per risolvere il problema, aggiungere l'oggetto <xref:System.ServiceModel.Description.ServiceMetadataBehavior> al file di configurazione oppure aggiungere sia l'endpoint che l'oggetto <xref:System.ServiceModel.Description.ServiceMetadataBehavior> al codice.  
>   
>  Per un esempio di aggiunta <xref:System.ServiceModel.Description.ServiceMetadataBehavior> in un file di configurazione dell'applicazione, vedere il [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md). Per un esempio di aggiunta <xref:System.ServiceModel.Description.ServiceMetadataBehavior> nel codice, vedere il [indipendente](../../../../docs/framework/wcf/samples/self-host.md) esempio.  
  
> [!CAUTION]
>  Quando si pubblicano metadati per un servizio che espone due contratti di servizio diversi in cui ciascuno contiene un'operazione dello stesso nome viene generata un'eccezione. Se ad esempio è presente un servizio che espone un contratto di servizio denominato ICarService con un'operazione Get(Car c) e lo stesso servizio espone un contratto di servizio denominato IBookService con un'operazione Get(Book b), viene generata un'eccezione o viene visualizzato un messaggio di errore durante la creazione dei metadati del servizio. Per risolvere il problema, effettuare una delle operazioni seguenti:  
>   
>  -   Rinominare una delle operazioni.  
> -   Impostare <xref:System.ServiceModel.OperationContractAttribute.Name%2A> su un nome diverso.  
> -   Impostare uno degli spazi dei nomi delle operazioni su uno spazio dei nomi diverso, utilizzando la proprietà <xref:System.ServiceModel.ServiceContractAttribute.Namespace%2A>.  
  
## <a name="retrieving-service-metadata"></a>Recupero di metadati del servizio  
 In [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è possibile recuperare i metadati del servizio utilizzando protocolli standard, ad esempio WS-MetadataExchange e HTTP. Entrambi questi protocolli sono supportati dal tipo <xref:System.ServiceModel.Description.MetadataExchangeClient>. Per recuperare i metadati del servizio, utilizzare il tipo <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> fornendo un indirizzo e un'associazione facoltativa. L'associazione utilizzata da un'istanza <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> può essere una delle associazioni predefinite dalla classe statica <xref:System.ServiceModel.Description.MetadataExchangeBindings>, un'associazione fornita dall'utente o un'associazione caricata dalla configurazione dell'endpoint per il contratto `IMetadataExchange`. <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> può inoltre risolvere i riferimenti dell'URL HTTP ai metadati utilizzando il tipo <xref:System.Net.HttpWebRequest>.  
  
 Per impostazione predefinita, un'istanza di <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> è collegata a una sola istanza di <xref:System.ServiceModel.Channels.ChannelFactoryBase>. È possibile modificare o sostituire l'istanza di <xref:System.ServiceModel.Channels.ChannelFactoryBase> utilizzata da <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> eseguendo l'override del metodo virtuale <xref:System.ServiceModel.Description.MetadataExchangeClient.GetChannelFactory%2A>. Analogamente, è possibile modificare o sostituire l'istanza di <xref:System.Net.HttpWebRequest?displayProperty=nameWithType> utilizzata da <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> per le richieste HTTP/GET eseguendo l'override del metodo virtuale <xref:System.ServiceModel.Description.MetadataExchangeClient.GetWebRequest%2A?displayProperty=nameWithType>.  
  
 È possibile recuperare i metadati del servizio utilizzando richieste WS-MetadataExchange o HTTP/GET utilizzando lo strumento Svcutil.exe e passando il **/target:metadata** switch e un indirizzo. Svcutil.exe scarica i metadati all'indirizzo specificato e salva i file su disco. Svcutil.exe utilizza un'istanza di <xref:System.ServiceModel.Description.MetadataExchangeClient?displayProperty=nameWithType> internamente e carica una configurazione dell'endpoint MEX (dal file di configurazione dell'applicazione) il cui nome corrisponde allo schema dell'indirizzo passato a Svcutil.exe, se presente. In caso contrario, Svcutil.exe utilizza per impostazione predefinita una delle associazioni definite dal tipo di factory statico <xref:System.ServiceModel.Description.MetadataExchangeBindings>.  
  
## <a name="importing-service-metadata"></a>Importazione di metadati del servizio  
 In [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] l'importazione dei metadati consiste nella generazione di una rappresentazione astratta di un servizio o dei relativi componenti a partire dai metadati del servizio. Ad esempio, [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] può importare istanze della classe <xref:System.ServiceModel.Description.ServiceEndpoint>, della classe <xref:System.ServiceModel.Channels.Binding> o della classe <xref:System.ServiceModel.Description.ContractDescription> da un documento WSDL di un servizio. Per importare i metadati di un servizio in [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è necessario utilizzare un'implementazione della classe astratta <xref:System.ServiceModel.Description.MetadataImporter>. I tipi che derivano dalla classe <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType> implementano il supporto per l'importazione dei formati di metadati che si basano sulla logica di importazione di WS-Policy di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
 Un'implementazione di <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType> raccoglie le espressioni di criteri collegate ai metadati del servizio in un oggetto <xref:System.ServiceModel.Description.PolicyConversionContext>. <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType> elabora quindi i criteri come parte dell'importazione dei metadati chiamando le implementazioni dell'interfaccia <xref:System.ServiceModel.Description.IPolicyImportExtension> nella proprietà <xref:System.ServiceModel.Description.MetadataImporter.PolicyImportExtensions%2A>.  
  
 È possibile aggiungere il supporto per importare nuove asserzioni di criteri in un <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType> aggiungendo la propria implementazione dell'interfaccia <xref:System.ServiceModel.Description.IPolicyImportExtension> alla raccolta <xref:System.ServiceModel.Description.MetadataImporter.PolicyImportExtensions%2A> in un'istanza <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType>. In alternativa, è possibile registrare l'estensione di importazione dei criteri nel file di configurazione dell'applicazione client.  
  
 Il tipo <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType> è un'implementazione della classe astratta <xref:System.ServiceModel.Description.MetadataImporter?displayProperty=nameWithType> fornita da [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Il tipo <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType> importa metadati WSDL insieme ai relativi criteri allegati. Questi elementi vengono quindi raggruppati in un oggetto <xref:System.ServiceModel.Description.MetadataSet>.  
  
 Per aggiungere il supporto per l'importazione di estensioni WSDL, implementare l'interfaccia <xref:System.ServiceModel.Description.IWsdlImportExtension>, quindi aggiungere tale implementazione alla proprietà <xref:System.ServiceModel.Description.WsdlImporter.WsdlImportExtensions%2A> nell'istanza di <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType>. È inoltre possibile utilizzare il tipo <xref:System.ServiceModel.Description.WsdlImporter?displayProperty=nameWithType> per caricare implementazioni dell'interfaccia <xref:System.ServiceModel.Description.IWsdlImportExtension?displayProperty=nameWithType> registrate nel file di configurazione dell'applicazione client.  
  
## <a name="dynamic-bindings"></a>Associazioni dinamiche  
 È possibile aggiornare dinamicamente l'associazione utilizzata per creare un canale per un endpoint del servizio nel caso in cui l'associazione per l'endpoint cambi o si desideri creare un canale per un endpoint che utilizza lo stesso contratto ma ha un'associazione diversa. È possibile utilizzare la <xref:System.ServiceModel.Description.MetadataResolver> classe statica per recuperare e importare metadati in fase di esecuzione per endpoint del servizio che implementano un contratto specifico. È quindi possibile utilizzare gli oggetti <xref:System.ServiceModel.Description.ServiceEndpoint?displayProperty=nameWithType> importati per creare un client o una channel factory per l'endpoint desiderato.  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.ServiceModel.Description>  
 [Formati di metadati](../../../../docs/framework/wcf/feature-details/metadata-formats.md)  
 [Esportazione e importazione di metadati](../../../../docs/framework/wcf/feature-details/exporting-and-importing-metadata.md)  
 [Pubblicazione dei metadati](../../../../docs/framework/wcf/feature-details/publishing-metadata.md)  
 [Il recupero dei metadati](../../../../docs/framework/wcf/feature-details/retrieving-metadata.md)  
 [Utilizzo dei metadati](../../../../docs/framework/wcf/feature-details/using-metadata.md)  
 [Considerazioni sulla sicurezza con metadati](../../../../docs/framework/wcf/feature-details/security-considerations-with-metadata.md)  
 [Estensione del sistema di metadati](../../../../docs/framework/wcf/extending/extending-the-metadata-system.md)
