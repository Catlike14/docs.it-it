---
title: '&lt;persistableType&gt;'
ms.date: 03/30/2017
ms.assetid: e5425fe6-523a-4076-aab4-2c2515b1d830
ms.openlocfilehash: 23724957398ed1ade2c81a3932e9773d7cf4c642
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/03/2018
ms.locfileid: "32747073"
---
# <a name="ltpersistabletypegt"></a><span data-ttu-id="91532-102">&lt;persistableType&gt;</span><span class="sxs-lookup"><span data-stu-id="91532-102">&lt;persistableType&gt;</span></span>
<span data-ttu-id="91532-103">Specifica tutti i tipi persistenti.</span><span class="sxs-lookup"><span data-stu-id="91532-103">Specifies all the persistable types.</span></span>  
  
 <span data-ttu-id="91532-104">\<system.ServiceModel></span><span class="sxs-lookup"><span data-stu-id="91532-104">\<system.ServiceModel></span></span>  
<span data-ttu-id="91532-105">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="91532-105">\<comContracts></span></span>  
<span data-ttu-id="91532-106">\<comContract ></span><span class="sxs-lookup"><span data-stu-id="91532-106">\<comContract></span></span>  
  
## <a name="syntax"></a><span data-ttu-id="91532-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="91532-107">Syntax</span></span>  
  
```xml  
<comContracts>  
  <comContract>  
      <persistableTypes>  
         <persistableType id="string"  
            name="string">  
         </persistableType>  
      </persistableTypes>  
  </comContract>  
</comContracts>  
```  
  
## <a name="type"></a><span data-ttu-id="91532-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="91532-108">Type</span></span>  
 `Type`  
  
## <a name="attributes-and-elements"></a><span data-ttu-id="91532-109">Attributi ed elementi</span><span class="sxs-lookup"><span data-stu-id="91532-109">Attributes and Elements</span></span>  
 <span data-ttu-id="91532-110">Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="91532-110">The following sections describe attributes, child elements, and parent elements.</span></span>  
  
### <a name="attributes"></a><span data-ttu-id="91532-111">Attributi</span><span class="sxs-lookup"><span data-stu-id="91532-111">Attributes</span></span>  
  
|<span data-ttu-id="91532-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="91532-112">Attribute</span></span>|<span data-ttu-id="91532-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91532-113">Description</span></span>|  
|---------------|-----------------|  
|<span data-ttu-id="91532-114">id</span><span class="sxs-lookup"><span data-stu-id="91532-114">id</span></span>|<span data-ttu-id="91532-115">Un attributo obbligatorio che contiene una stringa che specifica un identificatore univoco per un tipo persistente.</span><span class="sxs-lookup"><span data-stu-id="91532-115">A required attribute that contains a string that specifies a unique identifier for a persistable type.</span></span>|  
|<span data-ttu-id="91532-116">name</span><span class="sxs-lookup"><span data-stu-id="91532-116">name</span></span>|<span data-ttu-id="91532-117">Attributo facoltativo contenente una stringa che specifica il nome del tipo persistente.</span><span class="sxs-lookup"><span data-stu-id="91532-117">An optional attribute that contains a string that specifies the name of the persistable type.</span></span>|  
  
### <a name="child-elements"></a><span data-ttu-id="91532-118">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="91532-118">Child Elements</span></span>  
 <span data-ttu-id="91532-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="91532-119">None</span></span>  
  
### <a name="parent-elements"></a><span data-ttu-id="91532-120">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="91532-120">Parent Elements</span></span>  
  
|<span data-ttu-id="91532-121">Elemento</span><span class="sxs-lookup"><span data-stu-id="91532-121">Element</span></span>|<span data-ttu-id="91532-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91532-122">Description</span></span>|  
|-------------|-----------------|  
|[<span data-ttu-id="91532-123">\<persistableTypes ></span><span class="sxs-lookup"><span data-stu-id="91532-123">\<persistableTypes></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/persistabletypes.md)|<span data-ttu-id="91532-124">Raccolta di elementi `persistableType`.</span><span class="sxs-lookup"><span data-stu-id="91532-124">A collection of `persistableType` elements.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="91532-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="91532-125">See Also</span></span>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElementCollection>  
 <xref:System.ServiceModel.Configuration.ComPersistableTypeElement>  
 [<span data-ttu-id="91532-126">\<comContracts></span><span class="sxs-lookup"><span data-stu-id="91532-126">\<comContracts></span></span>](../../../../../docs/framework/configure-apps/file-schema/wcf/comcontracts.md)  
 [<span data-ttu-id="91532-127">Integrazione con applicazioni COM+</span><span class="sxs-lookup"><span data-stu-id="91532-127">Integrating with COM+ Applications</span></span>](../../../../../docs/framework/wcf/feature-details/integrating-with-com-plus-applications.md)  
 [<span data-ttu-id="91532-128">Procedura: Configurare le impostazioni del servizio COM+</span><span class="sxs-lookup"><span data-stu-id="91532-128">How to: Configure COM+ Service Settings</span></span>](../../../../../docs/framework/wcf/feature-details/how-to-configure-com-service-settings.md)
