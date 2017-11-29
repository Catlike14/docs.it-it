---
title: '&lt;persistenceProvider&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a37049c5-a7ea-4519-94f2-912eeb010380
caps.latest.revision: "5"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: b506b8ef14246ee954adb0a16102f4bb208106b0
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ltpersistenceprovidergt"></a><span data-ttu-id="4aa6d-102">&lt;persistenceProvider&gt;</span><span class="sxs-lookup"><span data-stu-id="4aa6d-102">&lt;persistenceProvider&gt;</span></span>
<span data-ttu-id="4aa6d-103">Specifica il tipo di implementazione del provider di persistenza da usare, nonché il timeout da usare per le operazioni di persistenza.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-103">Specifies the type of the persistence provider implementation to use, as well as the time-out to use for persistence operations.</span></span>  
  
 <span data-ttu-id="4aa6d-104">\<System. ServiceModel ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="4aa6d-105">\<i comportamenti ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-105">\<behaviors></span></span>  
<span data-ttu-id="4aa6d-106">\<serviceBehaviors ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-106">\<serviceBehaviors></span></span>  
<span data-ttu-id="4aa6d-107">\<comportamento ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-107">\<behavior></span></span>  
<span data-ttu-id="4aa6d-108">\<persistenceProvider ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-108">\<persistenceProvider></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4aa6d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4aa6d-109">Syntax</span></span>  
  
```xml  
<persistenceProvider persistenceOperationTimeout="TimeSpan"  
   type="String" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="4aa6d-110">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="4aa6d-110">Attributes and Elements</span></span>  
 <span data-ttu-id="4aa6d-111">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="4aa6d-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="4aa6d-112">Attributes</span></span>  
  
|<span data-ttu-id="4aa6d-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-113">Attribute</span></span>|<span data-ttu-id="4aa6d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aa6d-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="4aa6d-115">persistenceOperationTimeout</span><span class="sxs-lookup"><span data-stu-id="4aa6d-115">persistenceOperationTimeout</span></span>|<span data-ttu-id="4aa6d-116">Valore di tipo <xref:System.TimeSpan> che specifica il timeout usato per le operazioni di persistenza.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-116">A <xref:System.TimeSpan> value that specifies the time-out used for persistence operations.</span></span> <span data-ttu-id="4aa6d-117">Il valore predefinito è "00: 00:30".</span><span class="sxs-lookup"><span data-stu-id="4aa6d-117">The default is "00:00:30".</span></span>|  
|<span data-ttu-id="4aa6d-118">tipo</span><span class="sxs-lookup"><span data-stu-id="4aa6d-118">type</span></span>|<span data-ttu-id="4aa6d-119">Stringa che specifica il tipo della factory del provider di persistenza da usare.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-119">A string that specifies the type of the persistence provider factory to use.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="4aa6d-120">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="4aa6d-120">Child Elements</span></span>  
 <span data-ttu-id="4aa6d-121">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-121">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="4aa6d-122">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="4aa6d-122">Parent Elements</span></span>  
  
|<span data-ttu-id="4aa6d-123">Elemento</span><span class="sxs-lookup"><span data-stu-id="4aa6d-123">Element</span></span>|<span data-ttu-id="4aa6d-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4aa6d-124">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="4aa6d-125">\<comportamento ></span><span class="sxs-lookup"><span data-stu-id="4aa6d-125">\<behavior></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/behavior-of-endpointbehaviors.md)|<span data-ttu-id="4aa6d-126">Specifica un elemento di comportamento.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-126">Specifies a behavior element.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4aa6d-127">Note</span><span class="sxs-lookup"><span data-stu-id="4aa6d-127">Remarks</span></span>  
 <span data-ttu-id="4aa6d-128">Questo elemento specifica il provider di persistenza da usare per serializzare lo stato di un servizio WCF.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-128">This element specifies the persistence provider to be used to serialize the state of a WCF service.</span></span> <span data-ttu-id="4aa6d-129">È necessario usarlo insieme a `wsHttpContextBinding`, che consente di passare le informazioni sullo stato nelle intestazioni HTTP.</span><span class="sxs-lookup"><span data-stu-id="4aa6d-129">It should be used together with the `wsHttpContextBinding` which passes state information in HTTP headers.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4aa6d-130">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4aa6d-130">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.PersistenceProviderElement>  
 <xref:System.ServiceModel.Persistence.PersistenceProvider>
