---
title: Esposizione di componenti COM a .NET Framework
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- exposing COM components to .NET Framework
- interoperation with unmanaged code, exposing COM components
- COM interop, exposing COM components
ms.assetid: e78b14f1-e487-43cd-9c6d-1a07483f1730
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: c082ec115370ba60839d88e5af7df3585a8f8455
ms.sourcegitcommit: 3a96c706e4dbb4667bf3bf37edac9e1666646f93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/27/2018
---
# <a name="exposing-com-components-to-the-net-framework"></a><span data-ttu-id="e126b-102">Esposizione di componenti COM a .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e126b-102">Exposing COM Components to the .NET Framework</span></span>
<span data-ttu-id="e126b-103">Questa sezione riepiloga il processo necessario per esporre un componente COM esistente al codice gestito.</span><span class="sxs-lookup"><span data-stu-id="e126b-103">This section summarizes the process needed to expose an existing COM component to managed code.</span></span> <span data-ttu-id="e126b-104">Per informazioni dettagliate sulla scrittura di server COM strettamente integrati con .NET Framework, vedere [Considerazioni di progettazione per l'interoperabilità](https://msdn.microsoft.com/library/b59637f6-fe35-40d6-ae72-901e7a707689(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e126b-104">For details about writing COM servers that tightly integrate with the .NET Framework, see [Design Considerations for Interoperation](https://msdn.microsoft.com/library/b59637f6-fe35-40d6-ae72-901e7a707689(v=vs.100)).</span></span>
  
 <span data-ttu-id="e126b-105">I componenti COM esistenti sono risorse preziose nel codice gestito come applicazioni aziendali di livello intermedio o come funzionalità isolate.</span><span class="sxs-lookup"><span data-stu-id="e126b-105">Existing COM components are valuable resources in managed code as middle-tier business applications or as isolated functionality.</span></span> <span data-ttu-id="e126b-106">Un componente ideale ha un assembly di interoperabilità primario ed è strettamente conforme agli standard di programmazione imposti da COM.</span><span class="sxs-lookup"><span data-stu-id="e126b-106">An ideal component has a primary interop assembly and conforms tightly to the programming standards imposed by COM.</span></span>  
  
#### <a name="to-expose-com-components-to-the-net-framework"></a><span data-ttu-id="e126b-107">Per esporre i componenti COM a .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e126b-107">To expose COM components to the .NET Framework</span></span>  
  
1.  <span data-ttu-id="e126b-108">[Importare una libreria dei tipi come assembly](../../../docs/framework/interop/importing-a-type-library-as-an-assembly.md).</span><span class="sxs-lookup"><span data-stu-id="e126b-108">[Import a type library as an assembly](../../../docs/framework/interop/importing-a-type-library-as-an-assembly.md).</span></span>  
  
     <span data-ttu-id="e126b-109">Common Language Runtime richiede metadati per tutti i tipi, inclusi i tipi COM.</span><span class="sxs-lookup"><span data-stu-id="e126b-109">The common language runtime requires metadata for all types, including COM types.</span></span> <span data-ttu-id="e126b-110">Un assembly contenente tipi COM importati come metadati può essere ottenuto in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="e126b-110">There are several ways to obtain an assembly containing COM types imported as metadata.</span></span>  
  
2.  <span data-ttu-id="e126b-111">[Creare tipi COM nel codice gestito](http://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66).</span><span class="sxs-lookup"><span data-stu-id="e126b-111">[Create COM types in managed Code](http://msdn.microsoft.com/library/1a95a8ca-c8b8-4464-90b0-5ee1a1135b66).</span></span>  
  
     <span data-ttu-id="e126b-112">È possibile esaminare i tipi COM, attivare istanze e richiamare i metodi sull'oggetto COM esattamente come per gli altri tipi gestiti.</span><span class="sxs-lookup"><span data-stu-id="e126b-112">You can inspect COM types, activate instances, and invoke methods on the COM object the same way you do for any managed type.</span></span>  
  
3.  <span data-ttu-id="e126b-113">[Compilare un progetto di interoperabilità](../../../docs/framework/interop/compiling-an-interop-project.md).</span><span class="sxs-lookup"><span data-stu-id="e126b-113">[Compile an interop project](../../../docs/framework/interop/compiling-an-interop-project.md).</span></span>  
  
     <span data-ttu-id="e126b-114">[!INCLUDE[winsdklong](../../../includes/winsdklong-md.md)] fornisce i compilatori per diversi linguaggi conformi alle specifiche CLS, inclusi [!INCLUDE[vbprvblong](../../../includes/vbprvblong-md.md)], C# e C++.</span><span class="sxs-lookup"><span data-stu-id="e126b-114">The [!INCLUDE[winsdklong](../../../includes/winsdklong-md.md)] provides compilers for several languages compliant with the Common Language Specification (CLS), including [!INCLUDE[vbprvblong](../../../includes/vbprvblong-md.md)], C#, and C++.</span></span>  
  
4.  <span data-ttu-id="e126b-115">[Distribuire un'applicazione di interoperabilità](../../../docs/framework/interop/deploying-an-interop-application.md).</span><span class="sxs-lookup"><span data-stu-id="e126b-115">[Deploy an interop application](../../../docs/framework/interop/deploying-an-interop-application.md).</span></span>  
  
     <span data-ttu-id="e126b-116">Per una distribuzione ottimale delle applicazioni di interoperabilità, distribuirle come assembly firmati [con nome sicuro](../../../docs/framework/app-domains/strong-named-assemblies.md) nella Global Assembly Cache.</span><span class="sxs-lookup"><span data-stu-id="e126b-116">Interop applications are best deployed as [strong-named](../../../docs/framework/app-domains/strong-named-assemblies.md), signed assemblies in the global assembly cache.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e126b-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e126b-117">See Also</span></span>  
 [<span data-ttu-id="e126b-118">Interoperabilità con codice non gestito</span><span class="sxs-lookup"><span data-stu-id="e126b-118">Interoperating with Unmanaged Code</span></span>](../../../docs/framework/interop/index.md)  
 [<span data-ttu-id="e126b-119">Considerazioni di progettazione per l'interoperabilità</span><span class="sxs-lookup"><span data-stu-id="e126b-119">Design Considerations for Interoperation</span></span>](http://msdn.microsoft.com/library/b59637f6-fe35-40d6-ae72-901e7a707689)  
 [<span data-ttu-id="e126b-120">Esempio di interoperabilità COM: client .NET e server COM</span><span class="sxs-lookup"><span data-stu-id="e126b-120">COM Interop Sample: .NET Client and COM Server</span></span>](../../../docs/framework/interop/com-interop-sample-net-client-and-com-server.md)  
 [<span data-ttu-id="e126b-121">Indipendenza del linguaggio e componenti indipendenti dal linguaggio</span><span class="sxs-lookup"><span data-stu-id="e126b-121">Language Independence and Language-Independent Components</span></span>](../../../docs/standard/language-independence-and-language-independent-components.md)  
 [<span data-ttu-id="e126b-122">Gacutil.exe (strumento Global Assembly Cache)</span><span class="sxs-lookup"><span data-stu-id="e126b-122">Gacutil.exe (Global Assembly Cache Tool)</span></span>](../../../docs/framework/tools/gacutil-exe-gac-tool.md)
