---
title: '&lt;add&gt; di &lt;backupList&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: bc5939fc-314a-4ea4-a533-c96958da7173
caps.latest.revision: "2"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 1475983f7dc54a597198d48a2a404e431ce9c0a0
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="ltaddgt-of-ltbackuplistgt"></a><span data-ttu-id="8f201-102">&lt;add&gt; di &lt;backupList&gt;</span><span class="sxs-lookup"><span data-stu-id="8f201-102">&lt;add&gt; of &lt;backupList&gt;</span></span>
<span data-ttu-id="8f201-103">Rappresenta un elemento di configurazione che definisce un elemento dell'endpoint di backup.</span><span class="sxs-lookup"><span data-stu-id="8f201-103">Represents a configuration element that defines a backup endpoint element.</span></span>  
  
 <span data-ttu-id="8f201-104">\<System. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="8f201-104">\<system.serviceModel></span></span>  
<span data-ttu-id="8f201-105">\<routing ></span><span class="sxs-lookup"><span data-stu-id="8f201-105">\<routing></span></span>  
<span data-ttu-id="8f201-106">\<backupLists ></span><span class="sxs-lookup"><span data-stu-id="8f201-106">\<backupLists></span></span>  
<span data-ttu-id="8f201-107">\<backupList ></span><span class="sxs-lookup"><span data-stu-id="8f201-107">\<backupList></span></span>  
<span data-ttu-id="8f201-108">\<add></span><span class="sxs-lookup"><span data-stu-id="8f201-108">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f201-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f201-109">Syntax</span></span>  
  
```xml  
   <routing>  <backupLists>    <backupList name="String">      <add endpointName="String" />    </backupList>    </backupLists></routing>  
```  
  
```csharp  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="8f201-110">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="8f201-110">Attributes and Elements</span></span>  
 <span data-ttu-id="8f201-111">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="8f201-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="8f201-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="8f201-112">Attributes</span></span>  
  
|<span data-ttu-id="8f201-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="8f201-113">Attribute</span></span>|<span data-ttu-id="8f201-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f201-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="8f201-115">name</span><span class="sxs-lookup"><span data-stu-id="8f201-115">name</span></span>|<span data-ttu-id="8f201-116">Stringa che specifica il nome dell'endpoint di backup.</span><span class="sxs-lookup"><span data-stu-id="8f201-116">A string that specifies the name of the backup endpoint.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="8f201-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="8f201-117">Child Elements</span></span>  
 <span data-ttu-id="8f201-118">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="8f201-118">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="8f201-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="8f201-119">Parent Elements</span></span>  
  
|<span data-ttu-id="8f201-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="8f201-120">Element</span></span>|<span data-ttu-id="8f201-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f201-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="8f201-122">\<routing ></span><span class="sxs-lookup"><span data-stu-id="8f201-122">\<routing></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/routing.md)|<span data-ttu-id="8f201-123">Contiene un elenco di endpoint che si desidera che il servizio di Routing da utilizzare nel caso in cui l'endpoint primario non è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="8f201-123">Contains a list of endpoints that you would like the Routing Service to use in case the primary endpoint can't be reached.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8f201-124">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f201-124">See Also</span></span>  
 <xref:System.ServiceModel.Routing.Configuration.BackupEndpointElement?displayProperty=nameWithType> 
