---
title: MSMQ
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: d9fca29f-fa44-4ec4-bb48-b10800694500
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: e72d3e400440b830b689f476753a7c8c40fe2586
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="msmq"></a><span data-ttu-id="5063f-102">MSMQ</span><span class="sxs-lookup"><span data-stu-id="5063f-102">MSMQ</span></span>
<span data-ttu-id="5063f-103">In un'applicazione MSMQ, non viene trasferita alcuna attività aggiuntiva dal canale in coda a MSMQ e da MSMQ al canale in coda.</span><span class="sxs-lookup"><span data-stu-id="5063f-103">In an MSMQ application, no additional activity is transferred from the queued channel to MSMQ and from MSMQ to the queued channel.</span></span>  
  
 <span data-ttu-id="5063f-104">Inoltre, l'ID messaggio MSMQ e l'ID messaggio SOAP, insieme all'ID attività, se esistente, vengono analizzati come parte delle tracce del canale in coda in un'operazione di invio.</span><span class="sxs-lookup"><span data-stu-id="5063f-104">In addition, MSMQ Message ID and SOAP message ID (along with Activity ID, if one exists) are traced as part of queued channel traces on a Send operation.</span></span>  
  
 <span data-ttu-id="5063f-105">l'ID messaggio MSMQ e l'ID messaggio SOAP, insieme all'ID attività, se esistente, vengono analizzati come parte delle tracce del canale in coda in un'operazione di ricezione.</span><span class="sxs-lookup"><span data-stu-id="5063f-105">MSMQ Message ID and SOAP message ID (along with activity ID, if one exists) are traced as part of queued channel traces on a Receive operation.</span></span>  
  
 <span data-ttu-id="5063f-106">I trasferimenti necessari per l'operazione di ricezione vengono eseguiti in modo simile per qualsiasi altro trasporto (operazione di ricezione byte->elaborazione messaggio->).</span><span class="sxs-lookup"><span data-stu-id="5063f-106">The required transfers on the Receive operation are executed similarly to any other transport (receive bytes->Process message-> operation).</span></span>
