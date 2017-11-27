---
title: Chiamate al secondo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 0efb5a94-d83b-4793-b529-6fcbedb65c43
caps.latest.revision: "11"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 54e8b60679c7e7106f5b2e28abfebe5adc589174
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="calls-per-second"></a><span data-ttu-id="8af92-102">Chiamate al secondo</span><span class="sxs-lookup"><span data-stu-id="8af92-102">Calls Per Second</span></span>
<span data-ttu-id="8af92-103">Nome contatore: chiamate al secondo</span><span class="sxs-lookup"><span data-stu-id="8af92-103">Counter Name: Calls Per Second</span></span>  
  
## <a name="description"></a><span data-ttu-id="8af92-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8af92-104">Description</span></span>  
 <span data-ttu-id="8af92-105">Numero di chiamate all'operazione al secondo.</span><span class="sxs-lookup"><span data-stu-id="8af92-105">Number of calls to this operation in a second.</span></span>  
  
 <span data-ttu-id="8af92-106">Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="8af92-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="8af92-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="8af92-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
