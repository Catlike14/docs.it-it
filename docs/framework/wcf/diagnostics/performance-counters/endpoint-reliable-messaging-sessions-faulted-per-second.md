---
title: 'Endpoint: sessioni di messaggistica affidabile non riuscite al secondo'
ms.date: 03/30/2017
ms.assetid: e9ae808a-7e1f-46b0-9560-d5a866be6d6e
ms.openlocfilehash: f6b48ec4c37c28588dd874a5bfa94a01a2f43b0c
ms.sourcegitcommit: 76a304c79a32aa13889ebcf4b9789a4542b48e3e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/14/2018
ms.locfileid: "45560805"
---
# <a name="endpoint-reliable-messaging-sessions-faulted-per-second"></a>Endpoint: sessioni di messaggistica affidabile non riuscite al secondo
Nome contatore: sessioni di messaggistica affidabile con errori al secondo.  
  
## <a name="description"></a>Descrizione  
 Numero di sessioni di messaggistica affidabile con errori per l'endpoint al secondo.  
  
 Questo contatore è di tipo di contatore delle prestazioni [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato utilizzando la formula seguente.  
  
 (N 1 - N 0 ) / ( (D 1 -D 0 ) / F)
