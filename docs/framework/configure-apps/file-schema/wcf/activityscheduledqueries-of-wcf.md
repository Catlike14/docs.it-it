---
title: '&lt;activityScheduledQueries&gt; di WCF'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e351329f-9676-4f11-9b19-f4bac82f36fc
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4fc263f0d70e7c1016bab819fb157dde6fad66d4
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="ltactivityscheduledqueriesgt-of-wcf"></a><span data-ttu-id="2f1ce-102">&lt;activityScheduledQueries&gt; di WCF</span><span class="sxs-lookup"><span data-stu-id="2f1ce-102">&lt;activityScheduledQueries&gt; of WCF</span></span>
<span data-ttu-id="2f1ce-103">Rappresenta una raccolta di query usate per rilevare un'attività pianificata per l'esecuzione da parte di un'attività padre.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-103">Represents a collection of queries that are used to track an activity scheduled for execution by a parent activity.</span></span> <span data-ttu-id="2f1ce-104">La query è necessaria affinché un partecipante del rilevamento sottoscriva i record pianificati dell'attività.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-104">The query is necessary for a tracking participant to subscribe to activity scheduled records.</span></span>  
  
 <span data-ttu-id="2f1ce-105">Per ulteriori informazioni sulla query del profilo di rilevamento, vedere [profili di rilevamento](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span><span class="sxs-lookup"><span data-stu-id="2f1ce-105">For more information on tracking profile queries, see [Tracking Profiles](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)</span></span>  
  
 <span data-ttu-id="2f1ce-106">\<System. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-106">\<system.serviceModel></span></span>  
<span data-ttu-id="2f1ce-107">\<rilevamento ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-107">\<tracking></span></span>  
<span data-ttu-id="2f1ce-108">\<trackingProfile ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-108">\<trackingProfile></span></span>  
<span data-ttu-id="2f1ce-109">\<flusso di lavoro ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-109">\<workflow></span></span>  
<span data-ttu-id="2f1ce-110">\<activityScheduledQueries ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-110">\<activityScheduledQueries></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="2f1ce-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f1ce-111">Syntax</span></span>  
  
```xml  
<tracking>     <trackingProfile name="Name">       <workflow>          <activityScheduledQueries>             <activityScheduledQuery activityName="String"                 childActivityName="String"/>          </activityScheduledQueries>       </workflow>     </trackingProfile></tracking>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="2f1ce-112">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="2f1ce-112">Attributes and Elements</span></span>  
 <span data-ttu-id="2f1ce-113">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-113">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="2f1ce-114">Attributi</span><span class="sxs-lookup"><span data-stu-id="2f1ce-114">Attributes</span></span>  
 <span data-ttu-id="2f1ce-115">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-115">None.</span></span>  
  
### <a name="child-elements"></a><span data-ttu-id="2f1ce-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="2f1ce-116">Child Elements</span></span>  
  
|<span data-ttu-id="2f1ce-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="2f1ce-117">Element</span></span>|<span data-ttu-id="2f1ce-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f1ce-118">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2f1ce-119">\<activityScheduledQuery ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-119">\<activityScheduledQuery></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/activityscheduledquery.md)|<span data-ttu-id="2f1ce-120">Query usata per rilevare un'attività pianificata per l'esecuzione da parte di un'attività padre.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-120">A query that is used to track an activity scheduled for execution by a parent activity.</span></span>|  
  
### <a name="parent-elements"></a><span data-ttu-id="2f1ce-121">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="2f1ce-121">Parent Elements</span></span>  
  
|<span data-ttu-id="2f1ce-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="2f1ce-122">Element</span></span>|<span data-ttu-id="2f1ce-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f1ce-123">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="2f1ce-124">\<flusso di lavoro ></span><span class="sxs-lookup"><span data-stu-id="2f1ce-124">\<workflow></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-workflow-foundation/workflow.md)|<span data-ttu-id="2f1ce-125">Elemento di configurazione contenente tutte le query per un flusso di lavoro specifico identificato dalla proprietà `activityDefinitionId`.</span><span class="sxs-lookup"><span data-stu-id="2f1ce-125">A configuration element that contains all queries for a specific workflow identified by the `activityDefinitionId` property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2f1ce-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2f1ce-126">See Also</span></span>  
 <span data-ttu-id="2f1ce-127"><xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection></span><span class="sxs-lookup"><span data-stu-id="2f1ce-127"><xref:System.ServiceModel.Activities.Tracking.Configuration.ActivityScheduledQueryElementCollection></span></span>     
 <span data-ttu-id="2f1ce-128"><xref:System.Activities.Tracking.ActivityScheduledQuery></span><span class="sxs-lookup"><span data-stu-id="2f1ce-128"><xref:System.Activities.Tracking.ActivityScheduledQuery></span></span>     
 [<span data-ttu-id="2f1ce-129">Rilevamento e analisi del flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="2f1ce-129">Workflow Tracking and Tracing</span></span>](../../../../../docs/framework/windows-workflow-foundation/workflow-tracking-and-tracing.md)  
 [<span data-ttu-id="2f1ce-130">Profili di rilevamento</span><span class="sxs-lookup"><span data-stu-id="2f1ce-130">Tracking Profiles</span></span>](../../../../../docs/framework/windows-workflow-foundation/tracking-profiles.md)
