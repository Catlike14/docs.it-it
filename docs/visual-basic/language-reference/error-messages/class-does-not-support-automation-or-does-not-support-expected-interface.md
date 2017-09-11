---
title: Classe non supporta l&quot;automazione o non supporta l&quot;interfaccia prevista | Documenti di Microsoft
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbrID430
dev_langs:
- VB
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
caps.latest.revision: 11
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 8368ac123ce24dae41363e74c8b76773f64473b1
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="class-does-not-support-automation-or-does-not-support-expected-interface"></a><span data-ttu-id="22e95-102">La classe non supporta l'automazione o l'interfaccia prevista</span><span class="sxs-lookup"><span data-stu-id="22e95-102">Class does not support Automation or does not support expected interface</span></span>
<span data-ttu-id="22e95-103">La classe specificata nella funzione `GetObject` o `CreateObject` non ha esposto un'interfaccia di programmabilità oppure è stato modificato un progetto da .dll a .exe o viceversa.</span><span class="sxs-lookup"><span data-stu-id="22e95-103">Either the class you specified in the `GetObject` or `CreateObject` function call has not exposed a programmability interface, or you changed a project from .dll to .exe, or vice versa.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="22e95-104">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="22e95-104">To correct this error</span></span>  
  
1.  <span data-ttu-id="22e95-105">Consultare la documentazione dell'applicazione che ha creato l'oggetto per verificare l'eventuale presenza di limitazioni sull'uso dell'automazione.</span><span class="sxs-lookup"><span data-stu-id="22e95-105">Check the documentation of the application that created the object for limitations on the use of automation with this class of object.</span></span>  
  
2.  <span data-ttu-id="22e95-106">Se è stato modificato un progetto da .dll a .exe o viceversa, è necessario annullare manualmente la registrazione del precedente .dll o .exe.</span><span class="sxs-lookup"><span data-stu-id="22e95-106">If you changed a project from .dll to .exe or vice versa, you must manually unregister the old .dll or .exe.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22e95-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="22e95-107">See Also</span></span>  
 <span data-ttu-id="22e95-108">[Tipi di errore](../../../visual-basic/programming-guide/language-features/error-types.md) </span><span class="sxs-lookup"><span data-stu-id="22e95-108">[Error Types](../../../visual-basic/programming-guide/language-features/error-types.md) </span></span>  
<span data-ttu-id="22e95-109"> [Comunicazioni con Microsoft](https://docs.microsoft.com/visualstudio/ide/talk-to-us)</span><span class="sxs-lookup"><span data-stu-id="22e95-109"> [Talk to Us](https://docs.microsoft.com/visualstudio/ide/talk-to-us)</span></span>
