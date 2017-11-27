---
title: System.ServiceModel.Channels.FailedAcceptFromPool
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d535b1b5-ee58-45e8-b400-7d9570f4eb9a
caps.latest.revision: "6"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: e50e104816567927f53673f9b1da9c3c5beac3d0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="systemservicemodelchannelsfailedacceptfrompool"></a>System.ServiceModel.Channels.FailedAcceptFromPool
Tentativo di riutilizzare una connessione in pool non riuscito. Verrà effettuato un altro tentativo entro il periodo di timeout specificato.  
  
## <a name="description"></a>Descrizione  
 Questa traccia informativa indica che si è verificato un errore durante il tentativo di riutilizzare una connessione in pool. Ciò è dovuto al fatto che la connessione in pool non era compatibile o pronta oppure era ancora attiva. Verranno eseguiti ulteriori tentativi di riutilizzo della connessione in pool entro un determinato periodo di tempo. Nel caso in cui non verranno trovate connessioni utilizzabili, verrà creata una nuova connessione.  
  
## <a name="see-also"></a>Vedere anche  
 [Traccia](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [Utilizzo delle tracce per risolvere i problemi dell'applicazione](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [Amministrazione e diagnostica](../../../../../docs/framework/wcf/diagnostics/index.md)
