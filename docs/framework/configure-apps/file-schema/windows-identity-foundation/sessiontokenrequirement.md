---
title: '&lt;sessionTokenRequirement&gt;'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 496a1735-cbb7-49d5-a6aa-dd5550462073
caps.latest.revision: "3"
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.workload: dotnet
ms.openlocfilehash: 5a141dd83cb7ef1271906871097eb68da174d22f
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="ltsessiontokenrequirementgt"></a><span data-ttu-id="a7999-102">&lt;sessionTokenRequirement&gt;</span><span class="sxs-lookup"><span data-stu-id="a7999-102">&lt;sessionTokenRequirement&gt;</span></span>
<span data-ttu-id="a7999-103">Fornisce la configurazione per il <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> classe o classi derivate.</span><span class="sxs-lookup"><span data-stu-id="a7999-103">Provides configuration for the <xref:System.IdentityModel.Tokens.SessionSecurityTokenHandler> class or derived classes.</span></span>  
  
 <span data-ttu-id="a7999-104">\<System. IdentityModel ></span><span class="sxs-lookup"><span data-stu-id="a7999-104">\<system.identityModel></span></span>  
<span data-ttu-id="a7999-105">\<identityConfiguration ></span><span class="sxs-lookup"><span data-stu-id="a7999-105">\<identityConfiguration></span></span>  
<span data-ttu-id="a7999-106">\<securityTokenHandlers ></span><span class="sxs-lookup"><span data-stu-id="a7999-106">\<securityTokenHandlers></span></span>  
<span data-ttu-id="a7999-107">\<add></span><span class="sxs-lookup"><span data-stu-id="a7999-107">\<add></span></span>  
<span data-ttu-id="a7999-108">\<sessionTokenRequirement ></span><span class="sxs-lookup"><span data-stu-id="a7999-108">\<sessionTokenRequirement></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a7999-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7999-109">Syntax</span></span>  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">  
        <sessionTokenRequirement lifetime=TimeSpan >  
        </sessionTokenRequirement>  
      </add>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="a7999-110">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="a7999-110">Attributes and Elements</span></span>  
 <span data-ttu-id="a7999-111">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="a7999-111">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="a7999-112">Attributi</span><span class="sxs-lookup"><span data-stu-id="a7999-112">Attributes</span></span>  
  
|<span data-ttu-id="a7999-113">Attributo</span><span class="sxs-lookup"><span data-stu-id="a7999-113">Attribute</span></span>|<span data-ttu-id="a7999-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7999-114">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="a7999-115">durata</span><span class="sxs-lookup"><span data-stu-id="a7999-115">lifetime</span></span>|<span data-ttu-id="a7999-116">Specifica la durata del token di sessione.</span><span class="sxs-lookup"><span data-stu-id="a7999-116">Specifies the lifetime of session tokens.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="a7999-117">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a7999-117">Child Elements</span></span>  
 <span data-ttu-id="a7999-118">None</span><span class="sxs-lookup"><span data-stu-id="a7999-118">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="a7999-119">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="a7999-119">Parent Elements</span></span>  
  
|<span data-ttu-id="a7999-120">Elemento</span><span class="sxs-lookup"><span data-stu-id="a7999-120">Element</span></span>|<span data-ttu-id="a7999-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a7999-121">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="a7999-122">\<add></span><span class="sxs-lookup"><span data-stu-id="a7999-122">\<add></span></span>](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/add.md)|<span data-ttu-id="a7999-123">Aggiunge il gestore di token di sicurezza specificato alla raccolta di gestori di token.</span><span class="sxs-lookup"><span data-stu-id="a7999-123">Adds the specified security token handler to the token handler collection.</span></span>|  
  
## <a name="example"></a><span data-ttu-id="a7999-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="a7999-124">Example</span></span>  
  
```xml  
<add type="System.IdentityModel.Tokens.SessionSecurityTokenHandler, System.IdentityModel">           
    <sessionTokenRequirement lifetime="10:00" />  
</add>  
```
