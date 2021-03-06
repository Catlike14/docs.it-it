---
title: Migrazione delle applicazioni di .NET Remoting a WCF
ms.date: 03/30/2017
helpviewer_keywords:
- ',NET remoting [WCF]'
ms.assetid: 24793465-65ae-4308-8c12-dce4fd12a583
ms.openlocfilehash: 3f5556eeaf56ac48dd4f1d578ed2e66b90415677
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43503434"
---
# <a name="migrating-net-remoting-applications-to-wcf"></a>Migrazione delle applicazioni di .NET Remoting a WCF
**Questo argomento è specifico di una tecnologia legacy mantenuta per una questione di compatibilità con le applicazioni esistenti di versioni precedenti e non è consigliato per il nuovo sviluppo. Le applicazioni distribuite devono ora essere sviluppate utilizzando WCF.**  
  
 Esistono due modi per sfruttare i vantaggi di WCF con le applicazioni .NET Remoting esistenti: integrazione e la migrazione. Consente l'integrazione è necessario avere .net Remoting 2.0 e WCF in esecuzione-by-side lato, consentendo di esporre simultaneamente gli stessi oggetti business su entrambe le tecnologie senza dover modificare il .net esistenti codice .NET Remoting 2.0. L'integrazione richiede che sia in esecuzione [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 2.0 o versione successiva. Se si desidera avvalersi delle funzionalità di WCF e non è necessario compatibility wire con sistemi .NET Remoting 2.0, è possibile eseguire la migrazione dell'intero servizio a WCF. Migrazione da .NET Remoting 2.0 a WCF richiede modifiche all'interfaccia dell'oggetto remoto e relative impostazioni di configurazione. Entrambi questi argomenti vengono analizzate [da .NET Remoting a Windows Communication Foundation](https://go.microsoft.com/fwlink/?LinkId=74403).  
  
## <a name="see-also"></a>Vedere anche  
 [Panoramica dei concetti](../../../../docs/framework/wcf/conceptual-overview.md)
