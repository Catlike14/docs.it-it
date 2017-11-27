---
title: '&lt;aggiungere&gt; elemento per webRequestModules (impostazioni di rete)'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/webRequestModules/add
- http://schemas.microsoft.com/.NetConfiguration/v2.0#add
helpviewer_keywords:
- <webRequestModules>, add element
- webRequestModules, add element
- add element, webRequestModules
- <add> element, webRequestModules
ms.assetid: 47ec4adc-f39f-4bcd-8680-1ec21fd26890
caps.latest.revision: "16"
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: fd407f77e75bce4bdbc37acd5f28bbe39f92d564
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ltaddgt-element-for-webrequestmodules-network-settings"></a><span data-ttu-id="6357b-102">&lt;aggiungere&gt; elemento per webRequestModules (impostazioni di rete)</span><span class="sxs-lookup"><span data-stu-id="6357b-102">&lt;add&gt; Element for webRequestModules (Network Settings)</span></span>
<span data-ttu-id="6357b-103">Aggiunge un modulo di richiesta Web personalizzato per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6357b-103">Adds a custom Web request module to the application.</span></span>  
  
 <span data-ttu-id="6357b-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="6357b-104">\<configuration></span></span>  
<span data-ttu-id="6357b-105">\<System.NET ></span><span class="sxs-lookup"><span data-stu-id="6357b-105">\<system.net></span></span>  
<span data-ttu-id="6357b-106">\<webRequestModules ></span><span class="sxs-lookup"><span data-stu-id="6357b-106">\<webRequestModules></span></span>  
<span data-ttu-id="6357b-107">\<add></span><span class="sxs-lookup"><span data-stu-id="6357b-107">\<add></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="6357b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6357b-108">Syntax</span></span>  
  
```xml  
<add   
  prefix="URI prefix"   
  type="type_fullname, assembly_fullname"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="6357b-109">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="6357b-109">Attributes and Elements</span></span>  
 <span data-ttu-id="6357b-110">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="6357b-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="6357b-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="6357b-111">Attributes</span></span>  
  
|<span data-ttu-id="6357b-112">**Attributo**</span><span class="sxs-lookup"><span data-stu-id="6357b-112">**Attribute**</span></span>|<span data-ttu-id="6357b-113">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6357b-113">**Description**</span></span>|  
|-------------------|---------------------|  
|`prefix`|<span data-ttu-id="6357b-114">Il prefisso URI per le richieste gestite da questo modulo di richiesta Web.</span><span class="sxs-lookup"><span data-stu-id="6357b-114">The URI prefix for requests handled by this Web request module.</span></span>|  
|`type`|<span data-ttu-id="6357b-115">Il nome completo del tipo (indicato dal <xref:System.Type.FullName%2A> proprietà) e il nome dell'assembly (indicato dal <xref:System.Reflection.Assembly.FullName%2A> proprietà), separati da una virgola, che implementa questo modulo di richiesta Web.</span><span class="sxs-lookup"><span data-stu-id="6357b-115">The fully qualified type name (indicated by the <xref:System.Type.FullName%2A> property) and the assembly name (indicated by the <xref:System.Reflection.Assembly.FullName%2A> property), separated by a comma, that implements this Web request module.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="6357b-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="6357b-116">Child Elements</span></span>  
 <span data-ttu-id="6357b-117">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="6357b-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="6357b-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="6357b-118">Parent Elements</span></span>  
  
|<span data-ttu-id="6357b-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6357b-119">**Element**</span></span>|<span data-ttu-id="6357b-120">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="6357b-120">**Description**</span></span>|  
|-----------------|---------------------|  
|[<span data-ttu-id="6357b-121">webRequestModules</span><span class="sxs-lookup"><span data-stu-id="6357b-121">webRequestModules</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/webrequestmodules-element-network-settings.md)|<span data-ttu-id="6357b-122">Specifica i moduli da utilizzare per richiedere informazioni agli host di rete.</span><span class="sxs-lookup"><span data-stu-id="6357b-122">Specifies modules to use to request information from network hosts.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="6357b-123">Note</span><span class="sxs-lookup"><span data-stu-id="6357b-123">Remarks</span></span>  
 <span data-ttu-id="6357b-124">Il `prefix` attributo definisce il prefisso URI che usa il modulo di richiesta Web specificato.</span><span class="sxs-lookup"><span data-stu-id="6357b-124">The `prefix` attribute defines the URI prefix that uses the specified Web request module.</span></span> <span data-ttu-id="6357b-125">Moduli di richiesta Web sono in genere registrati per gestire un protocollo specifico, ad esempio HTTP o FTP, ma possono essere registrati per gestire una richiesta di un server specifico o un percorso in un server.</span><span class="sxs-lookup"><span data-stu-id="6357b-125">Web request modules are typically registered to handle a specific protocol, such as HTTP or FTP, but can be registered to handle a request to a specific server or path on a server.</span></span>  
  
 <span data-ttu-id="6357b-126">Il modulo di richiesta Web viene creato quando viene passato un prefisso corrispondente a un URI per il <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> metodo.</span><span class="sxs-lookup"><span data-stu-id="6357b-126">The Web request module is created when a URI matching prefix is passed to the <xref:System.Net.WebRequest.Create%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="6357b-127">Il valore per il `prefix` attributo deve corrispondere ai caratteri iniziali di un URI valido, ad esempio, "http" o "http://www.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="6357b-127">The value for the `prefix` attribute should be the leading characters of a valid URI --for example, "http", or "http://www.contoso.com".</span></span>  
  
 <span data-ttu-id="6357b-128">Il valore per il `type` attributo deve essere un nome di tipo valido e un nome di assembly corrispondente, separati da una virgola.</span><span class="sxs-lookup"><span data-stu-id="6357b-128">The value for the `type` attribute should be a valid type name and corresponding assembly name, separated by a comma .</span></span>  
  
## <a name="configuration-files"></a><span data-ttu-id="6357b-129">File di configurazione</span><span class="sxs-lookup"><span data-stu-id="6357b-129">Configuration Files</span></span>  
 <span data-ttu-id="6357b-130">Questo elemento può essere usato nel file di configurazione dell'applicazione o nel file di configurazione del computer (Machine.config).</span><span class="sxs-lookup"><span data-stu-id="6357b-130">This element can be used in the application configuration file or the machine configuration file (Machine.config).</span></span>  
  
## <a name="example"></a><span data-ttu-id="6357b-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="6357b-131">Example</span></span>  
 <span data-ttu-id="6357b-132">Nell'esempio seguente viene registrato un modulo di richiesta Web personalizzato per HTTP.</span><span class="sxs-lookup"><span data-stu-id="6357b-132">The following example registers a custom Web request module for HTTP.</span></span> <span data-ttu-id="6357b-133">È necessario sostituire i valori per la versione e PublicKeyToken con i valori corretti per il modulo specificato.</span><span class="sxs-lookup"><span data-stu-id="6357b-133">You should replace the values for Version and PublicKeyToken with the correct values for the specified module.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <webRequestModules>  
      <add prefix="http"  
           type="System.Net.HttpRequestCreator, System, Version=2.0.3600.0,  
           Culture=neutral, PublicKeyToken=b77a5c561934e089"  
      />  
    </webRequestModules>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="6357b-134">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6357b-134">See Also</span></span>  
 <xref:System.Net.WebRequest>  
 [<span data-ttu-id="6357b-135">Schema delle impostazioni di rete</span><span class="sxs-lookup"><span data-stu-id="6357b-135">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
