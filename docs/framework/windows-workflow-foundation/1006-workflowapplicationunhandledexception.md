---
title: 1006 - WorkflowApplicationUnhandledException
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: dfe0f316-e03b-47fb-b6a3-622c56bfd753
caps.latest.revision: "3"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: a03809be5e5d61c505e295e2f769a0298f770f7f
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="1006---workflowapplicationunhandledexception"></a><span data-ttu-id="beff3-102">1006 - WorkflowApplicationUnhandledException</span><span class="sxs-lookup"><span data-stu-id="beff3-102">1006 - WorkflowApplicationUnhandledException</span></span>
## <a name="properties"></a><span data-ttu-id="beff3-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="beff3-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="beff3-104">ID</span><span class="sxs-lookup"><span data-stu-id="beff3-104">ID</span></span>|<span data-ttu-id="beff3-105">1006</span><span class="sxs-lookup"><span data-stu-id="beff3-105">1006</span></span>|  
|<span data-ttu-id="beff3-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="beff3-106">Keywords</span></span>|<span data-ttu-id="beff3-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="beff3-107">WFRuntime</span></span>|  
|<span data-ttu-id="beff3-108">Livello</span><span class="sxs-lookup"><span data-stu-id="beff3-108">Level</span></span>|<span data-ttu-id="beff3-109">Errore</span><span class="sxs-lookup"><span data-stu-id="beff3-109">Error</span></span>|  
|<span data-ttu-id="beff3-110">Canale</span><span class="sxs-lookup"><span data-stu-id="beff3-110">Channel</span></span>|<span data-ttu-id="beff3-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="beff3-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="beff3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beff3-112">Description</span></span>  
 <span data-ttu-id="beff3-113">Indica che un'applicazione flusso di lavoro ha rilevato un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="beff3-113">Indicates a workflow application has encountered an unhandled exception.</span></span>  
  
## <a name="message"></a><span data-ttu-id="beff3-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="beff3-114">Message</span></span>  
 <span data-ttu-id="beff3-115">WorkflowInstance con Id: '%1' ha rilevato un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="beff3-115">WorkflowInstance Id: '%1' has encountered an unhandled exception.</span></span>  <span data-ttu-id="beff3-116">Eccezione originata dall'attività '%2', DisplayName: '%3'.</span><span class="sxs-lookup"><span data-stu-id="beff3-116">The exception originated from Activity '%2', DisplayName: '%3'.</span></span>  <span data-ttu-id="beff3-117">Verrà effettuata l'azione seguente: %4.</span><span class="sxs-lookup"><span data-stu-id="beff3-117">The following action will be taken: %4.</span></span>  
  
## <a name="details"></a><span data-ttu-id="beff3-118">Dettagli</span><span class="sxs-lookup"><span data-stu-id="beff3-118">Details</span></span>  
  
|<span data-ttu-id="beff3-119">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="beff3-119">Data Item Name</span></span>|<span data-ttu-id="beff3-120">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="beff3-120">Data Item Type</span></span>|<span data-ttu-id="beff3-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="beff3-121">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="beff3-122">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="beff3-122">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="beff3-123">ID istanza del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="beff3-123">The instance id for the workflow</span></span>|  
|<span data-ttu-id="beff3-124">Eccezione</span><span class="sxs-lookup"><span data-stu-id="beff3-124">Exception</span></span>|`xs:string`|<span data-ttu-id="beff3-125">Dettagli dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="beff3-125">The exception details for the exception</span></span>|  
|<span data-ttu-id="beff3-126">AppDomain</span><span class="sxs-lookup"><span data-stu-id="beff3-126">AppDomain</span></span>|`xs:string`|<span data-ttu-id="beff3-127">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="beff3-127">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
