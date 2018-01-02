---
title: '&lt;appDomainManagerType&gt; elemento'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- appDomainManagerType element
- <appDomainManagerType> element
ms.assetid: ae8d5a7e-e7f7-47f7-98d9-455cc243a322
caps.latest.revision: "7"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: fcfdd9bcd1aa458aad705d4ab129646e746d63b2
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="ltappdomainmanagertypegt-element"></a><span data-ttu-id="70ecf-102">&lt;appDomainManagerType&gt; elemento</span><span class="sxs-lookup"><span data-stu-id="70ecf-102">&lt;appDomainManagerType&gt; Element</span></span>
<span data-ttu-id="70ecf-103">Specifica il tipo che funge da gestore di dominio dell'applicazione per il dominio applicazione predefinito.</span><span class="sxs-lookup"><span data-stu-id="70ecf-103">Specifies the type that serves as the application domain manager for the default application domain.</span></span>  
  
 <span data-ttu-id="70ecf-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="70ecf-104">\<configuration></span></span>  
<span data-ttu-id="70ecf-105">\<runtime ></span><span class="sxs-lookup"><span data-stu-id="70ecf-105">\<runtime></span></span>  
<span data-ttu-id="70ecf-106">\<appDomainManagerType ></span><span class="sxs-lookup"><span data-stu-id="70ecf-106">\<appDomainManagerType></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="70ecf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70ecf-107">Syntax</span></span>  
  
```xml  
<appDomainManagerAssembly   
   value="type name" />  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="70ecf-108">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="70ecf-108">Attributes and Elements</span></span>  
 <span data-ttu-id="70ecf-109">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="70ecf-109">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="70ecf-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="70ecf-110">Attributes</span></span>  
  
|<span data-ttu-id="70ecf-111">Attributo</span><span class="sxs-lookup"><span data-stu-id="70ecf-111">Attribute</span></span>|<span data-ttu-id="70ecf-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70ecf-112">Description</span></span>|  
|---------------|-----------------|  
|`value`|<span data-ttu-id="70ecf-113">Attributo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="70ecf-113">Required attribute.</span></span> <span data-ttu-id="70ecf-114">Specifica il nome del tipo, incluso lo spazio dei nomi, che funge da gestore di dominio di applicazione per il dominio applicazione predefinito nel processo.</span><span class="sxs-lookup"><span data-stu-id="70ecf-114">Specifies the name of the type, including the namespace, that serves as the application domain manager for the default application domain in the process.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="70ecf-115">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="70ecf-115">Child Elements</span></span>  
 <span data-ttu-id="70ecf-116">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="70ecf-116">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="70ecf-117">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="70ecf-117">Parent Elements</span></span>  
  
|<span data-ttu-id="70ecf-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="70ecf-118">Element</span></span>|<span data-ttu-id="70ecf-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70ecf-119">Description</span></span>|  
|-------------|-----------------|  
|`configuration`|<span data-ttu-id="70ecf-120">Elemento radice in ciascun file di configurazione usato in Common Language Runtime e nelle applicazioni .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="70ecf-120">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span>|  
|`runtime`|<span data-ttu-id="70ecf-121">Contiene informazioni sull'associazione degli assembly e sull'operazione di Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="70ecf-121">Contains information about assembly binding and garbage collection.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="70ecf-122">Note</span><span class="sxs-lookup"><span data-stu-id="70ecf-122">Remarks</span></span>  
 <span data-ttu-id="70ecf-123">Per specificare il tipo del gestore di dominio di applicazione, è necessario specificare sia questo elemento e [ \<appDomainManagerAssembly >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="70ecf-123">To specify the type of the application domain manager, you must specify both this element and the [\<appDomainManagerAssembly>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) element.</span></span> <span data-ttu-id="70ecf-124">Se uno di questi elementi non è specificato, l'altro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="70ecf-124">If either of these elements is not specified, the other is ignored.</span></span>  
  
 <span data-ttu-id="70ecf-125">Quando il dominio applicazione predefinito viene caricato, <xref:System.TypeLoadException> viene generata se il tipo specificato non esiste nell'assembly specificato da di [ \<appDomainManagerAssembly >](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) elemento; e non il processo avviare.</span><span class="sxs-lookup"><span data-stu-id="70ecf-125">When the default application domain is loaded, <xref:System.TypeLoadException> is thrown if the specified type does not exist in the assembly that is specified by the [\<appDomainManagerAssembly>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md) element; and the process fails to start.</span></span>  
  
 <span data-ttu-id="70ecf-126">Quando si specifica il tipo di gestore di dominio di applicazione per il dominio applicazione predefinito, gli altri domini applicazione creati dal dominio applicazione predefinito ereditano il tipo di gestione del dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="70ecf-126">When you specify the application domain manager type for the default application domain, other application domains created from the default application domain inherit the application domain manager type.</span></span> <span data-ttu-id="70ecf-127">Utilizzare il <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> e <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> le proprietà per specificare un tipo di gestione del dominio applicazione diverso per un nuovo dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="70ecf-127">Use the <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType> and <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType> properties to specify a different application domain manager type for a new application domain.</span></span>  
  
 <span data-ttu-id="70ecf-128">Specifica il tipo di gestione del dominio applicazione richiede che l'applicazione disponga di attendibilità.</span><span class="sxs-lookup"><span data-stu-id="70ecf-128">Specifying the application domain manager type requires the application to have full trust.</span></span> <span data-ttu-id="70ecf-129">(Ad esempio, un'applicazione in esecuzione sul desktop è l'attendibilità totale.) Se l'applicazione non ha l'attendibilità totale, un <xref:System.TypeLoadException> viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="70ecf-129">(For example, an application running on the desktop has full trust.) If the application does not have full trust, a <xref:System.TypeLoadException> is thrown.</span></span>  
  
 <span data-ttu-id="70ecf-130">Il formato del tipo e spazio dei nomi è lo stesso formato utilizzato per la <xref:System.Type.FullName%2A?displayProperty=nameWithType> proprietà.</span><span class="sxs-lookup"><span data-stu-id="70ecf-130">The format of the type and namespace is the same format that is used for the <xref:System.Type.FullName%2A?displayProperty=nameWithType> property.</span></span>  
  
 <span data-ttu-id="70ecf-131">È disponibile solo in questo elemento di configurazione di [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="70ecf-131">This configuration element is available only in the [!INCLUDE[net_v40_long](../../../../../includes/net-v40-long-md.md)] and later.</span></span>  
  
## <a name="example"></a><span data-ttu-id="70ecf-132">Esempio</span><span class="sxs-lookup"><span data-stu-id="70ecf-132">Example</span></span>  
 <span data-ttu-id="70ecf-133">Nell'esempio seguente viene illustrato come specificare che il gestore di dominio di applicazione per il dominio applicazione predefinito di un processo è il `MyMgr` digitare il `AdMgrExample` assembly.</span><span class="sxs-lookup"><span data-stu-id="70ecf-133">The following example shows how to specify that the application domain manager for the default application domain of a process is the `MyMgr` type in the `AdMgrExample` assembly.</span></span>  
  
```xml  
<configuration>  
   <runtime>  
      <appDomainManagerType value="MyMgr" />  
      <appDomainManagerAssembly   
         value="AdMgrExample, Version=1.0.0.0, Culture=neutral, PublicKeyToken=6856bccf150f00b3" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="70ecf-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="70ecf-134">See Also</span></span>  
 <xref:System.AppDomainSetup.AppDomainManagerType%2A?displayProperty=nameWithType>  
 <xref:System.AppDomainSetup.AppDomainManagerAssembly%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="70ecf-135">\<appDomainManagerAssembly > elemento</span><span class="sxs-lookup"><span data-stu-id="70ecf-135">\<appDomainManagerAssembly> Element</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/appdomainmanagerassembly-element.md)  
 [<span data-ttu-id="70ecf-136">Schema delle impostazioni di runtime</span><span class="sxs-lookup"><span data-stu-id="70ecf-136">Runtime Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [<span data-ttu-id="70ecf-137">Schema dei file di configurazione</span><span class="sxs-lookup"><span data-stu-id="70ecf-137">Configuration File Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/index.md)  
 [<span data-ttu-id="70ecf-138">Metodo SetAppDomainManagerType</span><span class="sxs-lookup"><span data-stu-id="70ecf-138">SetAppDomainManagerType Method</span></span>](../../../../../docs/framework/unmanaged-api/hosting/iclrcontrol-setappdomainmanagertype-method.md)
