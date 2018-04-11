---
title: Elemento personalizzato per SingleTagSectionHandler
ms.date: 05/01/2017
ms.prod: .net-framework
ms.technology:
- dotnet-clr
ms.topic: article
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/sectionName
helpviewer_keywords:
- custom element
ms.assetid: e62056c6-b351-40eb-afc0-cc13fc44e45e
author: guardrex
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 8ee722c7d5db9d58ab1a91f4b1299912981510af
ms.sourcegitcommit: b750a8e3979749b214e7e10c82efb0a0524dfcb1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/10/2018
---
# <a name="custom-element-for-singletagsectionhandler"></a><span data-ttu-id="bdc7b-102">Elemento personalizzato per SingleTagSectionHandler</span><span class="sxs-lookup"><span data-stu-id="bdc7b-102">Custom element for SingleTagSectionHandler</span></span>

<span data-ttu-id="bdc7b-103">Definisce le impostazioni in una sezione di configurazione personalizzato definito da un</span><span class="sxs-lookup"><span data-stu-id="bdc7b-103">Defines settings in a custom configuration section that is defined by a</span></span> <section> <span data-ttu-id="bdc7b-104">elemento e viene utilizzato il <xref:System.Configuration.SingleTagSectionHandler> classe.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-104">element and uses the <xref:System.Configuration.SingleTagSectionHandler> class.</span></span>

<span data-ttu-id="bdc7b-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="bdc7b-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="bdc7b-106">&nbsp;&nbsp;*\<sectionName>*</span><span class="sxs-lookup"><span data-stu-id="bdc7b-106">&nbsp;&nbsp;*\<sectionName>*</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc7b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdc7b-107">Syntax</span></span>

```xml
<sectionName key="value" key2="value2" ... />
```

## <a name="attributes"></a><span data-ttu-id="bdc7b-108">Attributi</span><span class="sxs-lookup"><span data-stu-id="bdc7b-108">Attributes</span></span>

<span data-ttu-id="bdc7b-109">Gli attributi e valori di attributo sono definiti dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-109">Attributes and attribute values are user defined.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bdc7b-110">Elemento padre</span><span class="sxs-lookup"><span data-stu-id="bdc7b-110">Parent element</span></span>

|     | <span data-ttu-id="bdc7b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdc7b-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="bdc7b-112">**\<configuration>**</span><span class="sxs-lookup"><span data-stu-id="bdc7b-112">**\<configuration>**</span></span>](~/docs/framework/configure-apps/file-schema/configuration-element.md) | <span data-ttu-id="bdc7b-113">Elemento radice in ciascun file di configurazione usato in Common Language Runtime e nelle applicazioni .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-113">The root element in every configuration file used by the common language runtime and .NET Framework applications.</span></span> |

## <a name="child-elements"></a><span data-ttu-id="bdc7b-114">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="bdc7b-114">Child elements</span></span>

<span data-ttu-id="bdc7b-115">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bdc7b-115">None</span></span>

## <a name="remarks"></a><span data-ttu-id="bdc7b-116">Note</span><span class="sxs-lookup"><span data-stu-id="bdc7b-116">Remarks</span></span>

<span data-ttu-id="bdc7b-117">Il  **\<sectionName >** è un elemento personalizzato definito da un [  **\<sezione >** ](~/docs/framework/configure-apps/file-schema/section-element.md) tag il [  **\<configSections >** ](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) elemento.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-117">The **\<sectionName>** element is a custom element defined by a [**\<section>**](~/docs/framework/configure-apps/file-schema/section-element.md) tag in the [**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) element.</span></span> <span data-ttu-id="bdc7b-118">Il sistema di configurazione restituisce un <xref:System.Collections.IDictionary> oggetto quando si chiama <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-118">The configuration system returns a <xref:System.Collections.IDictionary> object when you call <xref:System.Configuration.Configuration.GetSection(System.String)?displayProperty=nameWithType>.</span></span>

## <a name="example"></a><span data-ttu-id="bdc7b-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="bdc7b-119">Example</span></span>

<span data-ttu-id="bdc7b-120">Nell'esempio seguente dichiara un elemento personalizzato denominato  **\<sampleSection >** che contiene le impostazioni di lettura per il <xref:System.Configuration.SingleTagSectionHandler> classe:</span><span class="sxs-lookup"><span data-stu-id="bdc7b-120">The following example declares a custom element called **\<sampleSection>** that contains settings read by the <xref:System.Configuration.SingleTagSectionHandler> class:</span></span>

```xml
<configuration>
  <configSections>
    <section name="sampleSection" 
             type="System.Configuration.SingleTagSectionHandler" />
  </configSections>
  <sampleSection setting1="Value1" 
                 setting2="value two" 
                 setting3="third value" />
</configuration>
```

## <a name="configuration-file"></a><span data-ttu-id="bdc7b-121">File di configurazione</span><span class="sxs-lookup"><span data-stu-id="bdc7b-121">Configuration file</span></span>

<span data-ttu-id="bdc7b-122">Questo elemento può essere usato nel file di configurazione dell'applicazione, i file di configurazione macchina (*Machine. config*), e *Web. config* file che non sono a livello di directory dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bdc7b-122">This element can be used in the application configuration file, machine configuration file (*Machine.config*), and *Web.config* files that are not at the application directory level.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdc7b-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bdc7b-123">See also</span></span>

[<span data-ttu-id="bdc7b-124">Schema di file di configurazione per .NET Framework</span><span class="sxs-lookup"><span data-stu-id="bdc7b-124">Configuration file schema for the .NET Framework</span></span>](~/docs/framework/configure-apps/file-schema/index.md)
