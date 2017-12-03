---
title: Operazioni transazionali interrotte ogni secondo
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 19fc993f-2b3d-4898-852e-3b98ec2153a5
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: a54b84f2fa0ab9c7531a17e69b10f78c725255ef
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="transacted-operations-aborted-per-second"></a><span data-ttu-id="e9509-102">Operazioni transazionali interrotte ogni secondo</span><span class="sxs-lookup"><span data-stu-id="e9509-102">Transacted Operations Aborted Per Second</span></span>
<span data-ttu-id="e9509-103">Nome contatorte: operazioni transazionali interrotte ogni secondo.</span><span class="sxs-lookup"><span data-stu-id="e9509-103">Counter Name: Transacted Operations Aborted Per Second.</span></span>  
  
## <a name="description"></a><span data-ttu-id="e9509-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9509-104">Description</span></span>  
 <span data-ttu-id="e9509-105">Numero di operazioni transazionali interrotte in questo servizio in un secondo.</span><span class="sxs-lookup"><span data-stu-id="e9509-105">Number of transactional operations that have been aborted in this service in a second.</span></span>  
  
 <span data-ttu-id="e9509-106">Questo contatore è di tipo di contatore prestazioni [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), il cui valore viene calcolato usando la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="e9509-106">This counter is of performance counter type [PERF_COUNTER_COUNTER](http://go.microsoft.com/fwlink/?LinkID=94649), whose value is calculated using the following formula.</span></span>  
  
 <span data-ttu-id="e9509-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span><span class="sxs-lookup"><span data-stu-id="e9509-107">(N 1 - N 0 ) / ( (D 1 -D 0 ) / F)</span></span>
