---
title: Messaggi di messaggistica affidabile eliminati al secondo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a11b0b80-b242-48e1-b0bb-7f756db5486b
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 64ced36369bfb44b6b0cef4af500da5e4796e64d
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="reliable-messaging-messages-dropped-per-second"></a>Messaggi di messaggistica affidabile eliminati al secondo
Nome contatore: sessioni di messaggistica affidabile rilasciate al secondo.  
  
## <a name="description"></a>Descrizione  
 Numero complessivo di messaggi di messaggistica affidabile rilasciati in questo servizio in un secondo.  
  
 Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
