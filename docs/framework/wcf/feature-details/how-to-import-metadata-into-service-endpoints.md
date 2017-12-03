---
title: 'Procedura: importare metadati negli endpoint del servizio'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b69dbe20-92a1-4911-89d8-ffbc3dad4663
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: afc08d08a8843460972daf259027475cbbc10b66
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="how-to-import-metadata-into-service-endpoints"></a>Procedura: importare metadati negli endpoint del servizio
In questo argomento viene descritto come importare i metadati in una raccolta di endpoint del servizio e utilizzare il servizio definito nel [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md). In questo argomento viene inoltre illustrato come creare un'applicazione client che importa metadati dal servizio e quindi chiama il metodo `Add` sul servizio.  
  
### <a name="to-import-metadata-into-service-endpoints"></a>Per importare metadati negli endpoint del servizio  
  
1.  Dichiarare un oggetto <xref:System.ServiceModel.EndpointAddress> e inizializzarlo con l'URI (Uniform Resource Identifier) per l'indirizzo di scambio dei metadati (MEX, metadata exchange) del servizio.  
  
     [!code-csharp[UE_ImportMetadata#0](../../../../samples/snippets/csharp/VS_Snippets_CFX/ue_importmetadata/cs/client.cs#0)]  
  
2.  Creare un <xref:System.ServiceModel.Description.MetadataExchangeClient>, passando l'indirizzo MEX, e chiamare <xref:System.ServiceModel.Description.MetadataExchangeClient.GetMetadata%2A>. In questo modo vengono recuperati i metadati dal servizio.  
  
     [!code-csharp[UE_ImportMetadata#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/ue_importmetadata/cs/client.cs#1)]  
  
3.  Creare un <xref:System.ServiceModel.Description.WsdlImporter>, passando i metadati precedentemente recuperati, e chiamare <xref:System.ServiceModel.Description.WsdlImporter.ImportAllContracts%2A>. In questo modo viene generata una raccolta di oggetti <xref:System.ServiceModel.Description.ContractDescription>. È anche possibile chiamare <xref:System.ServiceModel.Description.WsdlImporter.ImportAllEndpoints%2A> o <xref:System.ServiceModel.Description.WsdlImporter.ImportAllBindings%2A>, in base alle esigenze.  
  
     [!code-csharp[UE_ImportMetadata#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/ue_importmetadata/cs/client.cs#2)]  
  
    > [!NOTE]
    >  Dopo avere importato i metadati, non sarà possibile creare un canale client o esportare i metadati poiché in questa fase non è disponibile alcuna informazione sul tipo. Le informazioni sul tipo sono necessarie per interagire con il servizio o esportare i metadati. Per generare informazioni sul tipo, è necessario generare il codice mostrato nei passaggi 4 e 5. In alternativa, è possibile usare la classe di supporto <xref:System.ServiceModel.Description.MetadataResolver>. [!INCLUDE[crdefault](../../../../includes/crdefault-md.md)][Procedura: usare la classe MetadataResolver per ottenere dinamicamente i metadati di associazione](../../../../docs/framework/wcf/feature-details/how-to-use-metadataresolver-to-obtain-binding-metadata-dynamically.md).  
  
4.  Generare informazioni sul tipo per ogni contratto.  
  
     [!code-csharp[UE_ImportMetadata#3](../../../../samples/snippets/csharp/VS_Snippets_CFX/ue_importmetadata/cs/client.cs#3)]  
  
5.  A questo punto è possibile usare le informazioni. Nell'esempio seguente viene generato il codice sorgente C#.  
  
     [!code-csharp[UE_ImportMetadata#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/ue_importmetadata/cs/client.cs#4)]  
  
## <a name="see-also"></a>Vedere anche  
 [Metadati](../../../../docs/framework/wcf/feature-details/metadata.md)  
 [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md)
