---
title: 'Mitigazione: Costruttore ClaimsIdentity'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 946903f1-0fbf-4f67-805b-1eb48352024d
caps.latest.revision: 5
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: a50cbd69aa1f2c72adc9fc4d10a070f5faa0cf54
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="mitigation-claimsidentity-constructor"></a>Mitigazione: Costruttore ClaimsIdentity
A partire da [!INCLUDE[net_v462](../../../includes/net-v462-md.md)] è stato modificato il modo in cui il costruttore <xref:System.Security.Claims.ClaimsIdentity.%23ctor%28System.Security.Principal.IIdentity%29?displayProperty=fullName> imposta la proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=fullName>. Se l'argomento <xref:System.Security.Principal.IIdentity> è un oggetto <xref:System.Security.Claims.ClaimsIdentity> e la proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A> di tale oggetto <xref:System.Security.Claims.ClaimsIdentity> non è `null`, la proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A> viene allegata usando il metodo <xref:System.Security.Claims.ClaimsIdentity.Clone%2A?displayProperty=fullName>. Nell'oggetto [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] la proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A> è allegata come riferimento esistente.  
  
## <a name="impact"></a>Impatto  
 A partire da [!INCLUDE[net_v462](../../../includes/net-v462-md.md)], la proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=fullName> del nuovo oggetto <xref:System.Security.Claims.ClaimsIdentity> non è uguale alla proprietà <xref:System.Security.Claims.ClaimsIdentity.Actor%2A?displayProperty=fullName> dell'argomento <xref:System.Security.Principal.IIdentity> del costruttore. In [!INCLUDE[net_v461](../../../includes/net-v461-md.md)] e versioni precedenti, invece, è uguale.  
  
## <a name="mitigation"></a>Attenuazione  
 Se questo comportamento è inaccettabile, è possibile ripristinare il comportamento precedente impostando il commutatore `Switch.System.Security.ClaimsIdentity.SetActorAsReferenceWhenCopyingClaimsIdentity` nel file di configurazione dell'applicazione su `true`. A questo scopo è necessario aggiungere il codice seguente alla sezione [\<runtime>](../../../docs/framework/configure-apps/file-schema/runtime/runtime-element.md) del file web.config:  
  
```xml  
<configuration>  
   <runtime>  
      <AppContextSwitchOverrides value="Switch.System.Security.ClaimsIdentity.SetActorAsReferenceWhenCopyingClaimsIdentity=true" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Modifiche di reindirizzamento](../../../docs/framework/migration-guide/retargeting-changes-in-the-net-framework-4-6.md)

