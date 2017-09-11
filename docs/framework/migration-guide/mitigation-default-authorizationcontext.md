---
title: 'Mitigazione: AuthorizationContext predefinito'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6cfeee63-b148-429a-a7e6-6fe9b0cb7610
caps.latest.revision: 3
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 48363d0f8e515b703e49761a763379566e217844
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="mitigation-default-authorizationcontext"></a><span data-ttu-id="fcb32-102">Mitigazione: AuthorizationContext predefinito</span><span class="sxs-lookup"><span data-stu-id="fcb32-102">Mitigation: Default AuthorizationContext</span></span>
<span data-ttu-id="fcb32-103">L'implementazione dell'oggetto <xref:System.IdentityModel.Policy.AuthorizationContext> restituito da una chiamata al metodo <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext%28System.Collections.Generic.IList%7BSystem.IdentityModel.Policy.IAuthorizationPolicy%7D%29> con un argomento `null``authorizationPolicies` è cambiata in [!INCLUDE[net_v46](../../../includes/net-v46-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fcb32-103">The implementation of the <xref:System.IdentityModel.Policy.AuthorizationContext> returned by a call to the <xref:System.IdentityModel.Policy.AuthorizationContext.CreateDefaultAuthorizationContext%28System.Collections.Generic.IList%7BSystem.IdentityModel.Policy.IAuthorizationPolicy%7D%29> with a `null``authorizationPolicies` argument has changed its implementation in the [!INCLUDE[net_v46](../../../includes/net-v46-md.md)].</span></span>  
  
## <a name="impact"></a><span data-ttu-id="fcb32-104">Impatto</span><span class="sxs-lookup"><span data-stu-id="fcb32-104">Impact</span></span>  
 <span data-ttu-id="fcb32-105">In rari casi, le app WCF che usano l'autenticazione personalizzata possono riscontrare differenze di comportamento.</span><span class="sxs-lookup"><span data-stu-id="fcb32-105">In rare cases, WCF apps that use custom authentication may see behavioral differences.</span></span>  
  
## <a name="mitigation"></a><span data-ttu-id="fcb32-106">Attenuazione</span><span class="sxs-lookup"><span data-stu-id="fcb32-106">Mitigation</span></span>  
 <span data-ttu-id="fcb32-107">È possibile ripristinare il comportamento precedente in due modi diversi:</span><span class="sxs-lookup"><span data-stu-id="fcb32-107">You can restore the previous behavior in either of two ways:</span></span>  
  
-   <span data-ttu-id="fcb32-108">Ricompilare l'app per destinarla a una versione precedente rispetto a .NET Framework 4.6.</span><span class="sxs-lookup"><span data-stu-id="fcb32-108">Recompile your app to target an earlier version of the .NET Framework than 4.6.</span></span> <span data-ttu-id="fcb32-109">Per i servizi ospitati in IIS, usare l'elemento `<httpRuntime targetFramework="x.x" />` per destinare l'app a una versione precedente di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="fcb32-109">For IIS-hosted services, use the `<httpRuntime targetFramework="x.x" />` element to target an earlier version of the .NET Framework.</span></span>  
  
-   <span data-ttu-id="fcb32-110">Aggiungere la riga seguente alla sezione `<appSettings>` del file app.config:</span><span class="sxs-lookup"><span data-stu-id="fcb32-110">Add the following line to the `<appSettings>` section of your app.config file:</span></span>  
  
    ```xml  
    <add key="appContext.SetSwitch:Switch.System.IdentityModel.EnableCachedEmptyDefaultAuthorizationContext" value="true" />  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="fcb32-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fcb32-111">See Also</span></span>  
 [<span data-ttu-id="fcb32-112">Modifiche di reindirizzamento</span><span class="sxs-lookup"><span data-stu-id="fcb32-112">Retargeting Changes</span></span>](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-6.md)

