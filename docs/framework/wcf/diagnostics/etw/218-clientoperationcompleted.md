---
title: 218 - ClientOperationCompleted
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: b069bced-7bb2-4e01-8227-e5dbda17af09
caps.latest.revision: "5"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: ea826aa99e847f74c5a44113f2ae16d7322873f9
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="218---clientoperationcompleted"></a><span data-ttu-id="c9531-102">218 - ClientOperationCompleted</span><span class="sxs-lookup"><span data-stu-id="c9531-102">218 - ClientOperationCompleted</span></span>
## <a name="properties"></a><span data-ttu-id="c9531-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9531-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="c9531-104">ID</span><span class="sxs-lookup"><span data-stu-id="c9531-104">ID</span></span>|<span data-ttu-id="c9531-105">218</span><span class="sxs-lookup"><span data-stu-id="c9531-105">218</span></span>|  
|<span data-ttu-id="c9531-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="c9531-106">Keywords</span></span>|<span data-ttu-id="c9531-107">Troubleshooting, ServiceModel</span><span class="sxs-lookup"><span data-stu-id="c9531-107">Troubleshooting, ServiceModel</span></span>|  
|<span data-ttu-id="c9531-108">Livello</span><span class="sxs-lookup"><span data-stu-id="c9531-108">Level</span></span>|<span data-ttu-id="c9531-109">Informazioni</span><span class="sxs-lookup"><span data-stu-id="c9531-109">Information</span></span>|  
|<span data-ttu-id="c9531-110">Canale</span><span class="sxs-lookup"><span data-stu-id="c9531-110">Channel</span></span>|<span data-ttu-id="c9531-111">Microsoft-Windows-Application Server-Applications/Analytic</span><span class="sxs-lookup"><span data-stu-id="c9531-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="c9531-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9531-112">Description</span></span>  
 <span data-ttu-id="c9531-113">Questo evento viene generato dai client al termine di un'operazione.</span><span class="sxs-lookup"><span data-stu-id="c9531-113">This event is emitted by clients just after an operation completes.</span></span> <span data-ttu-id="c9531-114">Per le operazioni unidirezionali, si tratta del momento successivo all'invio di un messaggio.</span><span class="sxs-lookup"><span data-stu-id="c9531-114">For one-way operations, this is just after the message is sent successfully.</span></span> <span data-ttu-id="c9531-115">Per le operazioni request-response, si tratta del momento successivo alla ricezione della risposta.</span><span class="sxs-lookup"><span data-stu-id="c9531-115">For request-response operations this is after the response is received.</span></span>  
  
## <a name="message"></a><span data-ttu-id="c9531-116">Messaggio</span><span class="sxs-lookup"><span data-stu-id="c9531-116">Message</span></span>  
 <span data-ttu-id="c9531-117">L'azione client '%1' associata al contratto '%2' è completa.</span><span class="sxs-lookup"><span data-stu-id="c9531-117">The Client completed executing Action '%1' associated with the '%2' contract.</span></span> <span data-ttu-id="c9531-118">Il messaggio è stato inviato a '%3'.</span><span class="sxs-lookup"><span data-stu-id="c9531-118">The message was sent to '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="c9531-119">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c9531-119">Details</span></span>  
  
|<span data-ttu-id="c9531-120">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="c9531-120">Data Item Name</span></span>|<span data-ttu-id="c9531-121">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="c9531-121">Data Item Type</span></span>|<span data-ttu-id="c9531-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9531-122">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="c9531-123">Operazione</span><span class="sxs-lookup"><span data-stu-id="c9531-123">Action</span></span>|<span data-ttu-id="c9531-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="c9531-124">xs:string</span></span>|<span data-ttu-id="c9531-125">Intestazione dell'azione SOAP del messaggio in uscita.</span><span class="sxs-lookup"><span data-stu-id="c9531-125">The SOAP action header of the outgoing message.</span></span>|  
|<span data-ttu-id="c9531-126">Nome contratto</span><span class="sxs-lookup"><span data-stu-id="c9531-126">Contract Name</span></span>|`xs:string`|<span data-ttu-id="c9531-127">Nome del contratto.</span><span class="sxs-lookup"><span data-stu-id="c9531-127">The name of the contract.</span></span> <span data-ttu-id="c9531-128">Esempio: ICalculator.</span><span class="sxs-lookup"><span data-stu-id="c9531-128">Example: ICalculator.</span></span>|  
|<span data-ttu-id="c9531-129">Destinazione</span><span class="sxs-lookup"><span data-stu-id="c9531-129">Destination</span></span>|`xs:string`|<span data-ttu-id="c9531-130">Indirizzo dell'endpoint servizio a cui è stato inviato il messaggio.</span><span class="sxs-lookup"><span data-stu-id="c9531-130">The address of the service endpoint that the message was sent to.</span></span>|  
|<span data-ttu-id="c9531-131">HostReference</span><span class="sxs-lookup"><span data-stu-id="c9531-131">HostReference</span></span>|`xs:string`|<span data-ttu-id="c9531-132">Per i servizi ospitati su Web, questo campo identifica in modo univoco il servizio nella gerarchia Web.</span><span class="sxs-lookup"><span data-stu-id="c9531-132">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="c9531-133">Il formato viene definito come ' nome sito Web dell'applicazione virtuale percorso &#124; Percorso virtuale servizio &#124; ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="c9531-133">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="c9531-134">Esempio: ' Default Web Site/CalculatorApplication &#124;/CalculatorService.svc &#124; CalculatorService'.</span><span class="sxs-lookup"><span data-stu-id="c9531-134">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="c9531-135">AppDomain</span><span class="sxs-lookup"><span data-stu-id="c9531-135">AppDomain</span></span>|`xs:string`|<span data-ttu-id="c9531-136">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="c9531-136">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
