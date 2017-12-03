---
title: 1016 - CompleteCompletionWorkItem
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 246929fb-6f14-440a-814b-cd8349350644
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b01706f6e84987ea20f52c131139e243e8184c51
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="1016---completecompletionworkitem"></a><span data-ttu-id="50af3-102">1016 - CompleteCompletionWorkItem</span><span class="sxs-lookup"><span data-stu-id="50af3-102">1016 - CompleteCompletionWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="50af3-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="50af3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="50af3-104">ID</span><span class="sxs-lookup"><span data-stu-id="50af3-104">ID</span></span>|<span data-ttu-id="50af3-105">1016</span><span class="sxs-lookup"><span data-stu-id="50af3-105">1016</span></span>|  
|<span data-ttu-id="50af3-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="50af3-106">Keywords</span></span>|<span data-ttu-id="50af3-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="50af3-107">WFRuntime</span></span>|  
|<span data-ttu-id="50af3-108">Livello</span><span class="sxs-lookup"><span data-stu-id="50af3-108">Level</span></span>|<span data-ttu-id="50af3-109">Dettagliato</span><span class="sxs-lookup"><span data-stu-id="50af3-109">Verbose</span></span>|  
|<span data-ttu-id="50af3-110">Canale</span><span class="sxs-lookup"><span data-stu-id="50af3-110">Channel</span></span>|<span data-ttu-id="50af3-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="50af3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="50af3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50af3-112">Description</span></span>  
 <span data-ttu-id="50af3-113">Indica che CompletionWorkItem è completato.</span><span class="sxs-lookup"><span data-stu-id="50af3-113">Indicates a CompletionWorkItem has completed.</span></span>  
  
## <a name="message"></a><span data-ttu-id="50af3-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="50af3-114">Message</span></span>  
 <span data-ttu-id="50af3-115">CompletionWorkItem completato per l'attività padre '%1', DisplayName: '%2', InstanceId: '%3'.</span><span class="sxs-lookup"><span data-stu-id="50af3-115">A CompletionWorkItem has completed for parent Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span> <span data-ttu-id="50af3-116">Attività '%4', DisplayName: '%5', InstanceId: '%6' completata.</span><span class="sxs-lookup"><span data-stu-id="50af3-116">Completed Activity '%4', DisplayName: '%5', InstanceId: '%6'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="50af3-117">Dettagli</span><span class="sxs-lookup"><span data-stu-id="50af3-117">Details</span></span>  
  
|<span data-ttu-id="50af3-118">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="50af3-118">Data Item Name</span></span>|<span data-ttu-id="50af3-119">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="50af3-119">Data Item Type</span></span>|<span data-ttu-id="50af3-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50af3-120">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="50af3-121">ParentActivity</span><span class="sxs-lookup"><span data-stu-id="50af3-121">ParentActivity</span></span>|<span data-ttu-id="50af3-122">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-122">xs:string</span></span>|<span data-ttu-id="50af3-123">Nome tipo dell'attività padre.</span><span class="sxs-lookup"><span data-stu-id="50af3-123">The type name of the parent activity.</span></span>|  
|<span data-ttu-id="50af3-124">ParentDisplayName</span><span class="sxs-lookup"><span data-stu-id="50af3-124">ParentDisplayName</span></span>|<span data-ttu-id="50af3-125">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-125">xs:string</span></span>|<span data-ttu-id="50af3-126">Nome visualizzato dell'attività padre.</span><span class="sxs-lookup"><span data-stu-id="50af3-126">The display name of the parent activity.</span></span>|  
|<span data-ttu-id="50af3-127">ParentInstanceId</span><span class="sxs-lookup"><span data-stu-id="50af3-127">ParentInstanceId</span></span>|<span data-ttu-id="50af3-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-128">xs:string</span></span>|<span data-ttu-id="50af3-129">ID dell'istanza dell'attività padre.</span><span class="sxs-lookup"><span data-stu-id="50af3-129">The instance id of the parent activity.</span></span>|  
|<span data-ttu-id="50af3-130">CompletedActivity</span><span class="sxs-lookup"><span data-stu-id="50af3-130">CompletedActivity</span></span>|<span data-ttu-id="50af3-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-131">xs:string</span></span>|<span data-ttu-id="50af3-132">Nome tipo dell'attività completata.</span><span class="sxs-lookup"><span data-stu-id="50af3-132">The type name of the completed activity.</span></span>|  
|<span data-ttu-id="50af3-133">CompletedActivityDisplayName</span><span class="sxs-lookup"><span data-stu-id="50af3-133">CompletedActivityDisplayName</span></span>|<span data-ttu-id="50af3-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-134">xs:string</span></span>|<span data-ttu-id="50af3-135">Nome visualizzato dell'attività completata.</span><span class="sxs-lookup"><span data-stu-id="50af3-135">The display name of the completed activity.</span></span>|  
|<span data-ttu-id="50af3-136">CompletedActivityInstanceId</span><span class="sxs-lookup"><span data-stu-id="50af3-136">CompletedActivityInstanceId</span></span>|<span data-ttu-id="50af3-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-137">xs:string</span></span>|<span data-ttu-id="50af3-138">L'ID dell'istanza dell'attività completata.</span><span class="sxs-lookup"><span data-stu-id="50af3-138">The instance id of the completed activity.</span></span>|  
|<span data-ttu-id="50af3-139">AppDomain</span><span class="sxs-lookup"><span data-stu-id="50af3-139">AppDomain</span></span>|<span data-ttu-id="50af3-140">xs:string</span><span class="sxs-lookup"><span data-stu-id="50af3-140">xs:string</span></span>|<span data-ttu-id="50af3-141">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="50af3-141">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
