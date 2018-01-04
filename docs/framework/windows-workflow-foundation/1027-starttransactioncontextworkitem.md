---
title: 1027 - StartTransactionContextWorkItem
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 116ae5ec-b9d5-4231-824e-270d00eea7b8
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: baa644cb7693b8608f119cf211b3b08ab4b1a2b8
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="1027---starttransactioncontextworkitem"></a><span data-ttu-id="87e57-102">1027 - StartTransactionContextWorkItem</span><span class="sxs-lookup"><span data-stu-id="87e57-102">1027 - StartTransactionContextWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="87e57-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="87e57-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="87e57-104">ID</span><span class="sxs-lookup"><span data-stu-id="87e57-104">ID</span></span>|<span data-ttu-id="87e57-105">1027</span><span class="sxs-lookup"><span data-stu-id="87e57-105">1027</span></span>|  
|<span data-ttu-id="87e57-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="87e57-106">Keywords</span></span>|<span data-ttu-id="87e57-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="87e57-107">WFRuntime</span></span>|  
|<span data-ttu-id="87e57-108">Livello</span><span class="sxs-lookup"><span data-stu-id="87e57-108">Level</span></span>|<span data-ttu-id="87e57-109">Dettagliato</span><span class="sxs-lookup"><span data-stu-id="87e57-109">Verbose</span></span>|  
|<span data-ttu-id="87e57-110">Canale</span><span class="sxs-lookup"><span data-stu-id="87e57-110">Channel</span></span>|<span data-ttu-id="87e57-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="87e57-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="87e57-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e57-112">Description</span></span>  
 <span data-ttu-id="87e57-113">Indica che viene avviata l'esecuzione di TransactionContextWorkItem.</span><span class="sxs-lookup"><span data-stu-id="87e57-113">Indicates a TransactionContextWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="87e57-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="87e57-114">Message</span></span>  
 <span data-ttu-id="87e57-115">Avvio dell'esecuzione di TransactionContextWorkItem per l'attività '%1', DisplayName: '%2', InstanceId: '%3'.</span><span class="sxs-lookup"><span data-stu-id="87e57-115">Starting execution of a TransactionContextWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="87e57-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="87e57-116">Details</span></span>  
  
|<span data-ttu-id="87e57-117">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="87e57-117">Data Item Name</span></span>|<span data-ttu-id="87e57-118">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="87e57-118">Data Item Type</span></span>|<span data-ttu-id="87e57-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87e57-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="87e57-120">Attività</span><span class="sxs-lookup"><span data-stu-id="87e57-120">Activity</span></span>|<span data-ttu-id="87e57-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="87e57-121">xs:string</span></span>|<span data-ttu-id="87e57-122">Il nome del tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="87e57-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="87e57-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="87e57-123">DisplayName</span></span>|<span data-ttu-id="87e57-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="87e57-124">xs:string</span></span>|<span data-ttu-id="87e57-125">Nome visualizzato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="87e57-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="87e57-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="87e57-126">InstanceId</span></span>|<span data-ttu-id="87e57-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="87e57-127">xs:string</span></span>|<span data-ttu-id="87e57-128">L'ID dell'istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="87e57-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="87e57-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="87e57-129">AppDomain</span></span>|<span data-ttu-id="87e57-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="87e57-130">xs:string</span></span>|<span data-ttu-id="87e57-131">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="87e57-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
