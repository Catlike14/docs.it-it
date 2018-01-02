---
title: Schema delle sezioni di configurazione
ms.date: 05/02/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- configuration settings [.NET Framework], custom
- schema configuration settings
- configuration sections [.NET Framework]
- custom elements
- configuration schema [.NET Framework], custom settings in configuration files
- elements [.NET Framework], custom settings in configuration files
ms.assetid: 6e4cc793-c526-4007-b4e9-37d56295f2cb
author: guardrex
ms.author: mairaw
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: da9af8fd24f1bf6e6effd411ad37490a4ee08804
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="configuration-sections-schema"></a><span data-ttu-id="1b434-102">Schema delle sezioni di configurazione</span><span class="sxs-lookup"><span data-stu-id="1b434-102">Configuration sections schema</span></span>

<span data-ttu-id="1b434-103">Lo schema di sezioni di configurazione contiene elementi che definiscono le impostazioni personalizzate nei file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1b434-103">The configuration sections schema contains elements that define custom settings in configuration files.</span></span> <span data-ttu-id="1b434-104">Per informazioni generali sui file di configurazione e gli schemi, vedere [schema di file di configurazione per .NET Framework](~/docs/framework/configure-apps/file-schema/index.md).</span><span class="sxs-lookup"><span data-stu-id="1b434-104">For general information on configuration files and schemas, see [Configuration file schema for the .NET Framework](~/docs/framework/configure-apps/file-schema/index.md).</span></span>

<span data-ttu-id="1b434-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span><span class="sxs-lookup"><span data-stu-id="1b434-105">[**\<configuration>**](~/docs/framework/configure-apps/file-schema/configuration-element.md) </span></span>  
<span data-ttu-id="1b434-106">[**\<configSections >**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span><span class="sxs-lookup"><span data-stu-id="1b434-106">[**\<configSections>**](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) </span></span>  
<span data-ttu-id="1b434-107">[**\<Deselezionare >**](~/docs/framework/configure-apps/file-schema/clear-element-for-configsections.md) </span><span class="sxs-lookup"><span data-stu-id="1b434-107">[**\<clear>**](~/docs/framework/configure-apps/file-schema/clear-element-for-configsections.md) </span></span>  
<span data-ttu-id="1b434-108">[**\<rimuovere >**](~/docs/framework/configure-apps/file-schema/remove-element-for-configsections.md) </span><span class="sxs-lookup"><span data-stu-id="1b434-108">[**\<remove>**](~/docs/framework/configure-apps/file-schema/remove-element-for-configsections.md) </span></span>  
<span data-ttu-id="1b434-109">[**\<sezione >**](~/docs/framework/configure-apps/file-schema/section-element.md) </span><span class="sxs-lookup"><span data-stu-id="1b434-109">[**\<section>**](~/docs/framework/configure-apps/file-schema/section-element.md) </span></span>  
[<span data-ttu-id="1b434-110">**\<sectionGroup >**</span><span class="sxs-lookup"><span data-stu-id="1b434-110">**\<sectionGroup>**</span></span>](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md)

|     | <span data-ttu-id="1b434-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b434-111">Description</span></span> |
| --- | ----------- |
| [<span data-ttu-id="1b434-112">**\<Deselezionare >** per  **\<configSections >**</span><span class="sxs-lookup"><span data-stu-id="1b434-112">**\<clear>** for **\<configSections>**</span></span>](~/docs/framework/configure-apps/file-schema/clear-element-for-configsections.md) | <span data-ttu-id="1b434-113">Cancella tutte le sezioni definite in precedenza e i gruppi di sezioni.</span><span class="sxs-lookup"><span data-stu-id="1b434-113">Clears all previously defined sections and section groups.</span></span> |
| [<span data-ttu-id="1b434-114">**\<clear>**</span><span class="sxs-lookup"><span data-stu-id="1b434-114">**\<clear>**</span></span>](~/docs/framework/configure-apps/file-schema/clear-element-for-configsections.md) | <span data-ttu-id="1b434-115">Cancella tutte le sezioni definite in precedenza e i gruppi di sezioni.</span><span class="sxs-lookup"><span data-stu-id="1b434-115">Clears all previously defined sections and section groups.</span></span> |
| [<span data-ttu-id="1b434-116">**\<configSections >**</span><span class="sxs-lookup"><span data-stu-id="1b434-116">**\<configSections>**</span></span>](~/docs/framework/configure-apps/file-schema/configsections-element-for-configuration.md) | <span data-ttu-id="1b434-117">Contiene le dichiarazioni dello spazio dei nomi e di sezione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1b434-117">Contains configuration section and namespace declarations.</span></span> |
| [<span data-ttu-id="1b434-118">**\<rimuovere >** per  **\<configSections >**</span><span class="sxs-lookup"><span data-stu-id="1b434-118">**\<remove>** for **\<configSections>**</span></span>](~/docs/framework/configure-apps/file-schema/remove-element-for-configsections.md) | <span data-ttu-id="1b434-119">Rimuove una sezione predefinita o il gruppo di sezione.</span><span class="sxs-lookup"><span data-stu-id="1b434-119">Removes a predefined section or section group.</span></span> |
| [<span data-ttu-id="1b434-120">**\<sezione >** per  **\<configSections >** e  **\<sectionGroup >**</span><span class="sxs-lookup"><span data-stu-id="1b434-120">**\<section>** for **\<configSections>** and **\<sectionGroup>**</span></span>](~/docs/framework/configure-apps/file-schema/section-element.md) | <span data-ttu-id="1b434-121">Contiene una dichiarazione di sezione di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1b434-121">Contains a configuration section declaration.</span></span> |
| [<span data-ttu-id="1b434-122">**\<sectionGroup >** per  **\<configSections >**</span><span class="sxs-lookup"><span data-stu-id="1b434-122">**\<sectionGroup>** for **\<configSections>**</span></span>](~/docs/framework/configure-apps/file-schema/sectiongroup-element-for-configsections.md) | <span data-ttu-id="1b434-123">Definisce uno spazio dei nomi per le sezioni di configurazione.</span><span class="sxs-lookup"><span data-stu-id="1b434-123">Defines a namespace for configuration sections.</span></span> |
