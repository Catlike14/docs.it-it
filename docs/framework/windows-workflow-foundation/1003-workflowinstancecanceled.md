---
title: 1003 - WorkflowInstanceCanceled
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 64754dc2-c160-4bf3-869a-13d56694e2dc
caps.latest.revision: "4"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 7b287c99453724f855a51e9a1b8068337dd5e373
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="1003---workflowinstancecanceled"></a><span data-ttu-id="b6296-102">1003 - WorkflowInstanceCanceled</span><span class="sxs-lookup"><span data-stu-id="b6296-102">1003 - WorkflowInstanceCanceled</span></span>
## <a name="properties"></a><span data-ttu-id="b6296-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b6296-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="b6296-104">ID</span><span class="sxs-lookup"><span data-stu-id="b6296-104">ID</span></span>|<span data-ttu-id="b6296-105">1003</span><span class="sxs-lookup"><span data-stu-id="b6296-105">1003</span></span>|  
|<span data-ttu-id="b6296-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="b6296-106">Keywords</span></span>|<span data-ttu-id="b6296-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="b6296-107">WFRuntime</span></span>|  
|<span data-ttu-id="b6296-108">Livello</span><span class="sxs-lookup"><span data-stu-id="b6296-108">Level</span></span>|<span data-ttu-id="b6296-109">Informazioni</span><span class="sxs-lookup"><span data-stu-id="b6296-109">Information</span></span>|  
|<span data-ttu-id="b6296-110">Canale</span><span class="sxs-lookup"><span data-stu-id="b6296-110">Channel</span></span>|<span data-ttu-id="b6296-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="b6296-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="b6296-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6296-112">Description</span></span>  
 <span data-ttu-id="b6296-113">Indica che un'istanza del flusso di lavoro è stata completata nello stato Canceled.</span><span class="sxs-lookup"><span data-stu-id="b6296-113">Indicates a workflow instance has completed in the Canceled state.</span></span>  
  
## <a name="message"></a><span data-ttu-id="b6296-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="b6296-114">Message</span></span>  
 <span data-ttu-id="b6296-115">WorkflowInstance con ID: '%1' completata nello stato Canceled.</span><span class="sxs-lookup"><span data-stu-id="b6296-115">WorkflowInstance Id: '%1' has completed in the Canceled state.</span></span>  
  
## <a name="details"></a><span data-ttu-id="b6296-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b6296-116">Details</span></span>  
  
|<span data-ttu-id="b6296-117">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="b6296-117">Data Item Name</span></span>|<span data-ttu-id="b6296-118">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="b6296-118">Data Item Type</span></span>|<span data-ttu-id="b6296-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b6296-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="b6296-120">WorkflowInstanceId</span><span class="sxs-lookup"><span data-stu-id="b6296-120">WorkflowInstanceId</span></span>|`xs:string`|<span data-ttu-id="b6296-121">ID istanza del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b6296-121">The instance id for the workflow</span></span>|  
|<span data-ttu-id="b6296-122">AppDomain</span><span class="sxs-lookup"><span data-stu-id="b6296-122">AppDomain</span></span>|`xs:string`|<span data-ttu-id="b6296-123">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="b6296-123">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
