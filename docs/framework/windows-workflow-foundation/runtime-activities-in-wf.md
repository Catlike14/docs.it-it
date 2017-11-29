---
title: "Attività di runtime in WF"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e5ae8c31-19bc-4655-88b3-6b75cd6a1bd5
caps.latest.revision: "11"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: f3aca3fcdd4fa8d73bf3412d7c20697847d0a699
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="runtime-activities-in-wf"></a><span data-ttu-id="7e168-102">Attività di runtime in WF</span><span class="sxs-lookup"><span data-stu-id="7e168-102">Runtime Activities in WF</span></span>
<span data-ttu-id="7e168-103">In [!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] sono disponibili diverse attività fornite dal sistema per l'accesso alle funzionalità di esecuzione del flusso di lavoro, ad esempio la persistenza e la chiusura.</span><span class="sxs-lookup"><span data-stu-id="7e168-103">[!INCLUDE[netfx_current_short](../../../includes/netfx-current-short-md.md)] provides several system-provided activities for accessing the features of the workflow runtime, such as persistence and termination.</span></span>  
  
|<span data-ttu-id="7e168-104">Attività</span><span class="sxs-lookup"><span data-stu-id="7e168-104">Activity</span></span>|<span data-ttu-id="7e168-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e168-105">Description</span></span>|  
|--------------|-----------------|  
|<xref:System.Activities.Statements.Persist>|<span data-ttu-id="7e168-106">Richiede in modo esplicito la persistenza dello stato del flusso di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e168-106">Explicitly requests that the workflow persist its state.</span></span>|  
|<xref:System.Activities.Statements.TerminateWorkflow>|<span data-ttu-id="7e168-107">Termina l'istanza del flusso di lavoro in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e168-107">Terminates the running workflow instance.</span></span>|  
|<xref:System.Activities.Statements.NoPersistScope>|<span data-ttu-id="7e168-108">Attività contenitore che impedisce la persistenza delle attività figlio.</span><span class="sxs-lookup"><span data-stu-id="7e168-108">A container activity that prevents child activities from persisting.</span></span>|
