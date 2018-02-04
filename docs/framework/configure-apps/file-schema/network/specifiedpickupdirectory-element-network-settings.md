---
title: '&lt;specifiedPickupDirectory&gt; elemento (impostazioni di rete)'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#specifiedPickupDirectory
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp/specifiedPickupDirectory
helpviewer_keywords:
- specifiedPickupDirectory element
- <specifiedPickupDirectory> element
ms.assetid: 0121f49d-bff2-4bc6-af06-f1628dcd61f1
caps.latest.revision: 
author: mcleblanc
ms.author: markl
manager: markl
ms.workload:
- dotnet
ms.openlocfilehash: e68ce8cac4048ee2df89d0241cc50242e20391a2
ms.sourcegitcommit: cf22b29db780e532e1090c6e755aa52d28273fa6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/01/2018
---
# <a name="ltspecifiedpickupdirectorygt-element-network-settings"></a><span data-ttu-id="df4ab-102">&lt;specifiedPickupDirectory&gt; elemento (impostazioni di rete)</span><span class="sxs-lookup"><span data-stu-id="df4ab-102">&lt;specifiedPickupDirectory&gt; Element (Network Settings)</span></span>
<span data-ttu-id="df4ab-103">Configura la directory locale per un server SMTP Simple Mail Transport Protocol ().</span><span class="sxs-lookup"><span data-stu-id="df4ab-103">Configures the local directory for a Simple Mail Transport Protocol (SMTP) server.</span></span>  
  
 <span data-ttu-id="df4ab-104">\<configuration></span><span class="sxs-lookup"><span data-stu-id="df4ab-104">\<configuration></span></span>  
<span data-ttu-id="df4ab-105">\<system.net></span><span class="sxs-lookup"><span data-stu-id="df4ab-105">\<system.net></span></span>  
<span data-ttu-id="df4ab-106">\<mailSettings></span><span class="sxs-lookup"><span data-stu-id="df4ab-106">\<mailSettings></span></span>  
<span data-ttu-id="df4ab-107">\<smtp></span><span class="sxs-lookup"><span data-stu-id="df4ab-107">\<smtp></span></span>  
<span data-ttu-id="df4ab-108">\<specifiedPickupDirectory></span><span class="sxs-lookup"><span data-stu-id="df4ab-108">\<specifiedPickupDirectory></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="df4ab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df4ab-109">Syntax</span></span>  
  
```xml  
<specifiedPickupDirectory  
  pickupDirectoryLocation="directory"   
/>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="df4ab-110">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="df4ab-110">Attributes and Elements</span></span>  
 <span data-ttu-id="df4ab-111">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="df4ab-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="df4ab-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="df4ab-112">Attributes</span></span>  
  
|<span data-ttu-id="df4ab-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="df4ab-113">Attribute</span></span>|<span data-ttu-id="df4ab-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df4ab-114">Description</span></span>|  
|---------------|-----------------|  
|`pickupDirectoryLocation`|<span data-ttu-id="df4ab-115">La directory in cui le applicazioni salvano posta elettronica per l'elaborazione successiva per il server SMTP.</span><span class="sxs-lookup"><span data-stu-id="df4ab-115">The directory where applications save email for later processing by the SMTP server.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="df4ab-116">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="df4ab-116">Child Elements</span></span>  
 <span data-ttu-id="df4ab-117">Nessuno.</span><span class="sxs-lookup"><span data-stu-id="df4ab-117">None.</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="df4ab-118">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="df4ab-118">Parent Elements</span></span>  
  
|<span data-ttu-id="df4ab-119">Elemento</span><span class="sxs-lookup"><span data-stu-id="df4ab-119">Element</span></span>|<span data-ttu-id="df4ab-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df4ab-120">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="df4ab-121">\<SMTP > elemento (impostazioni di rete)</span><span class="sxs-lookup"><span data-stu-id="df4ab-121">\<smtp> Element (Network Settings)</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|<span data-ttu-id="df4ab-122">Configura posta elettronica SMTP Simple Mail Transport Protocol (), le opzioni di invio.</span><span class="sxs-lookup"><span data-stu-id="df4ab-122">Configures Simple Mail Transport Protocol (SMTP) mail sending options.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="df4ab-123">Note</span><span class="sxs-lookup"><span data-stu-id="df4ab-123">Remarks</span></span>  
 <span data-ttu-id="df4ab-124">Con l'attributo `specifiedPickupDirectory` viene impostata la directory in cui nelle applicazioni vengono salvati i messaggi di posta elettronica da elaborare mediante il server SMTP.</span><span class="sxs-lookup"><span data-stu-id="df4ab-124">The `specifiedPickupDirectory` attribute sets the directory where applications save mail messages to be processed by the SMTP server.</span></span>  
  
## <a name="example"></a><span data-ttu-id="df4ab-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="df4ab-125">Example</span></span>  
 <span data-ttu-id="df4ab-126">Nell'esempio seguente specifica c:\maildrop come la directory di prelievo della posta.</span><span class="sxs-lookup"><span data-stu-id="df4ab-126">The following example specifies c:\maildrop as the mail pickup directory.</span></span>  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="specifiedPickupDirectory">  
        <specifiedPickupDirectory  
          pickupDirectoryLocation="c:\maildrop"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a><span data-ttu-id="df4ab-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="df4ab-127">See Also</span></span>  
 <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSpecifiedPickupDirectoryElement?displayProperty=nameWithType>  
 [<span data-ttu-id="df4ab-128">Schema delle impostazioni di rete</span><span class="sxs-lookup"><span data-stu-id="df4ab-128">Network Settings Schema</span></span>](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
