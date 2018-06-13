---
title: Transazioni propagate al secondo
ms.date: 03/30/2017
ms.assetid: b9f661e1-576c-48fc-9fdf-91853e0749e8
ms.openlocfilehash: a71095b9fdd16d7e220be8a0aeb0a746bb50527e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33472918"
---
# <a name="transactions-flowed-per-second"></a><span data-ttu-id="a69fc-102">Transazioni propagate al secondo</span><span class="sxs-lookup"><span data-stu-id="a69fc-102">Transactions Flowed Per Second</span></span>
<span data-ttu-id="a69fc-103">Nome contatore: transazioni propagate al secondo.</span><span class="sxs-lookup"><span data-stu-id="a69fc-103">Counter Name:  Transactions Flowed Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="a69fc-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a69fc-104">Description</span></span>  
 <span data-ttu-id="a69fc-105">Numero di transazioni propagate a questa operazione in un secondo.</span><span class="sxs-lookup"><span data-stu-id="a69fc-105">Number of transactions flowed to this operation in a second.</span></span> <span data-ttu-id="a69fc-106">Questo contatore viene incrementato ogni volta che è presente un ID di transazione in un messaggio inviato all'operazione.</span><span class="sxs-lookup"><span data-stu-id="a69fc-106">This counter is incremented any time a transaction ID is present in a message that is sent to the operation.</span></span>  
  
 <span data-ttu-id="a69fc-107">Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="a69fc-107">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="a69fc-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="a69fc-108">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
