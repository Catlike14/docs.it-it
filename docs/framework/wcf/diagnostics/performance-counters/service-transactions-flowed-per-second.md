---
title: 'Servizio: transazioni propagate al secondo'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: ec72eb49-2942-4811-91df-d6e5dad81fd8
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 9172075294de8431216540b06aec542753c94621
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="service-transactions-flowed-per-second"></a>Servizio: transazioni propagate al secondo
Nome contatore: transazioni propagate al secondo.  
  
## <a name="description"></a>Descrizione  
 Numero di transazioni propagate alle operazioni in questo servizio al secondo.  
  
 Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
