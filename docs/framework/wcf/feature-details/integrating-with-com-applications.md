---
title: Integrazione con applicazioni COM
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Windows Communication Foundation, COM integration
- COM [WCF], Windows Communication Foundation integration
- WCF, reusing code
- Windows Communication Foundation, reusing code
- COM [WCF]
- WCF, COM integration
ms.assetid: c98bda3e-6779-419e-8e6d-9aa94053026d
caps.latest.revision: "9"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: a0e625beaf20f6445099d8fb15cb175d3d71a860
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="integrating-with-com-applications"></a>Integrazione con applicazioni COM
I servizi [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] possono essere integrati direttamente nel codice esistente usando il moniker servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)]. Il moniker servizio può essere usato da un'ampia gamma di ambienti di sviluppo basati su COM, ad esempio Office VBA, Visual Basic 6.0 o Visual C++ 6.0.  
  
## <a name="in-this-section"></a>Contenuto della sezione  
 [L'integrazione con panoramica delle applicazioni COM](../../../../docs/framework/wcf/feature-details/integrating-with-com-applications-overview.md)  
 Fornisce una panoramica delle parti principali del processo di integrazione.  
  
 [Procedura: registrare e configurare un Moniker di servizio](../../../../docs/framework/wcf/feature-details/how-to-register-and-configure-a-service-moniker.md)  
 Per usare il moniker servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] all'interno di un'applicazione COM, registrare i tipi con attributi necessari con COM e configurare l'applicazione COM e il moniker con la configurazione dell'associazione necessaria.  
  
 [Procedura: usare il Moniker del servizio Windows Communication Foundation senza registrazione](../../../../docs/framework/wcf/feature-details/use-the-wcf-service-moniker-without-registration.md)  
 Illustra come ottenere la definizione del contratto in forma di documento WSDL (Web Services Definition Language) o da un endpoint WS-MetadataExchange.  
  
 [Procedura: usare un Moniker servizio con i contratti WSDL](../../../../docs/framework/wcf/feature-details/how-to-use-a-service-moniker-with-wsdl-contracts.md)  
 Descrive come chiamare un esempio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] usando un moniker WSDL [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)].  
  
 [Procedura: usare un Moniker servizio con contratti di scambio di metadati](../../../../docs/framework/wcf/feature-details/how-to-use-a-service-moniker-with-metadata-exchange-contracts.md)  
 Descrive come chiamare un esempio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] usando un moniker [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] che specifica un endpoint MEX.  
  
 [Procedura: specificare le credenziali di sicurezza del canale](../../../../docs/framework/wcf/feature-details/how-to-specify-channel-security-credentials.md)  
 Il moniker servizio [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] supporta l'interfaccia `IChannelCredentials` che consente un intervallo di metodi alternativi per la specifica di credenziali del canale.  
  
## <a name="reference"></a>Riferimento  
 <xref:System.ServiceModel>  
  
## <a name="see-also"></a>Vedere anche  
 [L'integrazione con applicazioni COM+](../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)
