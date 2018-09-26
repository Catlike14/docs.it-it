---
title: Operazioni transazionali in dubbio al secondo
ms.date: 03/30/2017
ms.assetid: 7e6b0716-c107-42e5-a21d-31d988e7a691
ms.openlocfilehash: f7365c4e5f03711129916c8c6964f7e25e9b553e
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/25/2018
ms.locfileid: "47169905"
---
# <a name="transacted-operations-in-doubt-per-second"></a><span data-ttu-id="9bf7a-102">Operazioni transazionali in dubbio al secondo</span><span class="sxs-lookup"><span data-stu-id="9bf7a-102">Transacted Operations In Doubt Per Second</span></span>
<span data-ttu-id="9bf7a-103">Nome contatore: operazioni transazionali in dubbio al secondo</span><span class="sxs-lookup"><span data-stu-id="9bf7a-103">Counter Name: Transacted Operations In Doubt Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="9bf7a-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bf7a-104">Description</span></span>  
 <span data-ttu-id="9bf7a-105">Numero di operazioni transazionali con un risultato dubbio nel servizio al secondo.</span><span class="sxs-lookup"><span data-stu-id="9bf7a-105">Number of transactional operations with an in-doubt outcome in this service in a second.</span></span>  
  
 <span data-ttu-id="9bf7a-106">Questo contatore è di tipo di contatore delle prestazioni [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato utilizzando la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="9bf7a-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](https://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="9bf7a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="9bf7a-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
