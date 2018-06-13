---
title: 'Servizio: chiamate non riuscite al secondo'
ms.date: 03/30/2017
ms.assetid: 5a2c7939-107d-4f0c-b43c-e02e079e8a9d
ms.openlocfilehash: 6af8f79d1fe163967a5c6e8220697aa11bee66c7
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33473827"
---
# <a name="service-calls-failed-per-second"></a><span data-ttu-id="ef0c3-102">Servizio: chiamate non riuscite al secondo</span><span class="sxs-lookup"><span data-stu-id="ef0c3-102">Service: Calls Failed Per Second</span></span>
<span data-ttu-id="ef0c3-103">Nome contatore: chiamate non riuscite al secondo</span><span class="sxs-lookup"><span data-stu-id="ef0c3-103">Counter Name: Calls Failed Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="ef0c3-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef0c3-104">Description</span></span>  
 <span data-ttu-id="ef0c3-105">Numero di chiamate al secondo ricevute dal servizio aventi eccezioni non gestite.</span><span class="sxs-lookup"><span data-stu-id="ef0c3-105">Number of calls that have unhandled exceptions, and are received by this service in a second.</span></span>  
  
 <span data-ttu-id="ef0c3-106">Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="ef0c3-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="ef0c3-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="ef0c3-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>  
  
 <span data-ttu-id="ef0c3-108">Nel codice gestito, vengono generate eccezioni quando si verificano condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="ef0c3-108">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="ef0c3-109">Nel codice gestito, vengono generate eccezioni quando si verificano condizioni di errore.</span><span class="sxs-lookup"><span data-stu-id="ef0c3-109">In managed code, exceptions are thrown when error conditions occur.</span></span>  
  
 <span data-ttu-id="ef0c3-110">Questo contatore viene incrementato ogni volta che si verifica un'eccezione non gestita in questo servizio.</span><span class="sxs-lookup"><span data-stu-id="ef0c3-110">This counter is incremented every time there is an unhandled exception in this service.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef0c3-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ef0c3-111">See Also</span></span>  
 [<span data-ttu-id="ef0c3-112">Specifica e gestione degli errori in contratti e servizi</span><span class="sxs-lookup"><span data-stu-id="ef0c3-112">Specifying and Handling Faults in Contracts and Services</span></span>](../../../../../docs/framework/wcf/specifying-and-handling-faults-in-contracts-and-services.md)
