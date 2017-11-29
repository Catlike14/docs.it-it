---
title: Architettura client
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 02624403-0d77-41cb-9a86-ab55e98c7966
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: acd2263fddf4b045cd7efc93ca85d1ed1b2e6dd0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="client-architecture"></a>Architettura client
Per richiamare operazioni del servizio, le applicazioni utilizzano oggetti client [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)]. In questo argomento vengono descritti gli oggetti client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)], i canali client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e le relative relazioni con l'architettura del canale sottostante. Per una panoramica di base di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] oggetti del client, vedere [panoramica dei Client WCF](../../../../docs/framework/wcf/wcf-client-overview.md). [!INCLUDE[crabout](../../../../includes/crabout-md.md)]il livello del canale, vedere [estendendo il livello del canale](../../../../docs/framework/wcf/extending/extending-the-channel-layer.md).  
  
## <a name="overview"></a>Panoramica  
 Il runtime del modello di servizi crea client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] costituiti dagli elementi seguenti:  
  
-   Un'implementazione client di un contratto di servizio generata automaticamente, che trasforma le chiamate del codice dell'applicazione in messaggi in uscita e i messaggi di risposta in parametri di output e valori restituiti che possono essere recuperati dall'applicazione.  
  
-   Un'implementazione di un'interfaccia di controllo (<xref:System.ServiceModel.IClientChannel?displayProperty=nameWithType>), che raggruppa le varie interfacce e fornisce accesso alle funzionalità di controllo, tra cui la possibilità di chiudere la sessione client ed eliminare il canale.  
  
-   Un canale client creato in base alle impostazioni di configurazione specificate dall'associazione utilizzata.  
  
 Applicazioni possono creare tali client su richiesta, tramite un <xref:System.ServiceModel.ChannelFactory?displayProperty=nameWithType> o creando un'istanza di un <xref:System.ServiceModel.ClientBase%601> classe derivata, viene generato dal [strumento ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md). Queste classi client generate incapsulano e delegano a un'implementazione del canale client che viene costruita dinamicamente da una classe <xref:System.ServiceModel.ChannelFactory>. Il canale client e la channel factory che le producono costituiscono pertanto il punto centrale d'interesse di questo argomento.  
  
## <a name="client-objects-and-client-channels"></a>Oggetti client e canali client  
 L'interfaccia di base dei client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] è l'interfaccia <xref:System.ServiceModel.IClientChannel?displayProperty=nameWithType>, che espone la funzionalità client principale, nonché la funzionalità dell'oggetto di comunicazione di base di <xref:System.ServiceModel.ICommunicationObject?displayProperty=nameWithType>, la funzionalità di contesto di <xref:System.ServiceModel.IContextChannel?displayProperty=nameWithType> e il comportamento estensibile di <xref:System.ServiceModel.IExtensibleObject%601?displayProperty=nameWithType>.  
  
 L'interfaccia <xref:System.ServiceModel.IClientChannel>, tuttavia, non definisce contratti di servizio. Quelli dichiarati dall'interfaccia del contratto di servizio (in genere generato dai metadati del servizio utilizzando uno strumento come il [strumento ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)). I tipi di client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] estendono sia <xref:System.ServiceModel.IClientChannel> sia l'interfaccia del contratto di servizio di destinazione per consentire alle applicazioni di chiamare direttamente le operazioni e avere accesso alla funzionalità di runtime lato client. Con la creazione di un client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] vengono fornite agli oggetti della classe [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]<xref:System.ServiceModel.ChannelFactory?displayProperty=nameWithType> le informazioni necessarie per creare un run-time in grado di connettersi e interagire con l'endpoint del servizio configurato.  
  
 Come indicato in precedenza, è necessario configurare i due tipi di client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] prima di poterli utilizzare. I tipi di client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] più semplici sono oggetti che derivano da <xref:System.ServiceModel.ClientBase%601> (o da <xref:System.ServiceModel.DuplexClientBase%601> se il contratto del servizio è un contratto duplex). Per creare questi tipi, è possibile utilizzare un costruttore configurato a livello di codice o un file di configurazione che viene quindi chiamato direttamente per richiamare le operazioni del servizio. Per una panoramica di base di <xref:System.ServiceModel.ClientBase%601> degli oggetti, vedere [panoramica dei Client WCF](../../../../docs/framework/wcf/wcf-client-overview.md).  
  
 Il secondo tipo di client è quello generato in fase di esecuzione da una chiamata al metodo <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A>. Nelle applicazioni interessate a livello di controllo delle specifiche di comunicazione in genere utilizzano questo tipo di client, chiamato un *oggetto canale client*, poiché consente un'interazione più diretta rispetto al valore sottostante client in fase di esecuzione e il canale System.  
  
## <a name="channel-factories"></a>Channel factory  
 La classe responsabile della creazione del run-time sottostante che supporta le chiamate client è la classe <xref:System.ServiceModel.ChannelFactory%601?displayProperty=nameWithType>. Gli oggetti client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e gli oggetti canale client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] utilizzano un oggetto <xref:System.ServiceModel.ChannelFactory%601> per creare istanze; l'oggetto client derivato <xref:System.ServiceModel.ClientBase%601> incapsula la gestione della channel factory, ma per alcuni scenari è possibile utilizzare direttamente la channel factory. Lo scenario più comune si ha quando si desidera creare ripetutamente nuovi canali client da una factory esistente. Se si utilizza un oggetto client, è possibile ottenere la channel factory sottostante da un oggetto client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] chiamando la proprietà <xref:System.ServiceModel.ClientBase%601.ChannelFactory%2A?displayProperty=nameWithType>.  
  
 La cosa importante da ricordare a proposito delle channel factory è che creano nuove istanze di canali client per la configurazione fornita loro prima di chiamare il metodo <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A?displayProperty=nameWithType>. Una volta chiamato il metodo <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A> (o <xref:System.ServiceModel.ClientBase%601.Open%2A?displayProperty=nameWithType>, <xref:System.ServiceModel.ClientBase%601.CreateChannel%2A?displayProperty=nameWithType> oppure qualsiasi operazione su un oggetto client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]), non è possibile modificare la channel factory e aspettarsi di ottenere canali per istanze del servizio diverse, anche se si modifica soltanto l'indirizzo dell'endpoint di destinazione. Se si desidera creare un oggetto client o un canale client con una configurazione diversa, è necessario prima creare una nuova channel factory.  
  
 [!INCLUDE[crabout](../../../../includes/crabout-md.md)]problemi vari usando [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] oggetti client e [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] canali client, vedere [accesso ai servizi tramite Client WCF](../../../../docs/framework/wcf/feature-details/accessing-services-using-a-client.md).  
  
 Nelle due sezioni seguenti vengono illustrati la creazione e l'utilizzo degli oggetti canale client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
#### <a name="creating-a-new-wcf-client-channel-object"></a>Creazione di un nuovo oggetto canale client WCF  
 Per illustrare l'utilizzo di un canale client, si supponga che sia stato generato il contratto di servizio seguente.  
  
 [!code-csharp[C_GeneratedCodeFiles#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#12)]  
  
 Per eseguire la connessione a un servizio `ISampleService`, utilizzare direttamente l'interfaccia del contratto generata con una channel factory (<xref:System.ServiceModel.ChannelFactory%601>). Una volta creata e configurata una channel factory per un particolare contratto, è possibile chiamare il metodo <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A> per restituire oggetti canale client che possono essere utilizzati per comunicare con un servizio `ISampleService`.  
  
 Quando si usa la classe <xref:System.ServiceModel.ChannelFactory%601> con un'interfaccia del contratto del servizio, per aprire, chiudere o interrompere in modo esplicito il canale è necessario eseguire il cast all'interfaccia <xref:System.ServiceModel.IClientChannel>. Per semplificare l'uso, lo strumento Svcutil.exe genera inoltre un'interfaccia di supporto che implementa l'interfaccia del contratto del servizio e <xref:System.ServiceModel.IClientChannel> per consentire l'interazione con l'infrastruttura del canale client senza dovere eseguire il cast. Nel codice seguente viene illustrata la definizione di un canale client di supporto che implementa il contratto del servizio precedente.  
  
 [!code-csharp[C_GeneratedCodeFiles#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_generatedcodefiles/cs/proxycode.cs#13)]  
  
#### <a name="creating-a-new-wcf-client-channel-object"></a>Creazione di un nuovo oggetto canale client WCF  
 Per utilizzare un canale client per la connessione a un servizio `ISampleService`, è necessario utilizzare direttamente l'interfaccia del contratto generata (o la versione di supporto) con una channel factory, passando il tipo dell'interfaccia del contratto come parametro di tipo. Una volta creata e configurata una channel factory per un particolare contratto, è possibile chiamare il metodo <xref:System.ServiceModel.ChannelFactory%601.CreateChannel%2A?displayProperty=nameWithType> per restituire oggetti canale client che possono essere utilizzati per comunicare con un servizio `ISampleService`.  
  
 Quando vengono creati, gli oggetti canale client implementano <xref:System.ServiceModel.IClientChannel> e l'interfaccia del contratto. È pertanto possibile utilizzarli direttamente per chiamare operazioni che interagiscono con un servizio che supporta tale contratto.  
  
 La differenza tra l'utilizzo di oggetti client e di oggetti canale client consiste solo nel maggiore controllo e facilità di utilizzo da parte degli sviluppatori. Coloro che sono abituati a lavorare con le classi e gli oggetti preferiranno utilizzare l'oggetto client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] anziché il canale client [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] .  
  
 Per un esempio, vedere [procedura: usare ChannelFactory](../../../../docs/framework/wcf/feature-details/how-to-use-the-channelfactory.md).
