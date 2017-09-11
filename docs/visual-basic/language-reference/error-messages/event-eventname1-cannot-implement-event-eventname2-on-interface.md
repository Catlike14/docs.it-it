---
title: "Evento &quot;&lt;eventname1&gt;&quot;non può implementare l&quot;evento&quot;&lt;eventname2&gt;&quot;nell&quot;interfaccia&quot;&lt;interfaccia&gt;&quot; perché i tipi di delegati&lt;delegate1&gt;&quot;e&quot;&lt;delegate2&gt;&quot; non corrispondono a | Documenti di Microsoft"
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc31423
- bc31423
dev_langs:
- VB
helpviewer_keywords:
- BC31423
ms.assetid: 2e754b66-5836-48ff-9697-b9c0d7085f18
caps.latest.revision: 6
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
ms.openlocfilehash: 340547d3673b651e988a6c1167bf7043360b04e4
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="event-39lteventname1gt39-cannot-implement-event-39lteventname2gt39-on-interface-39ltinterfacegt39-because-their-delegate-types-39ltdelegate1gt39-and-39ltdelegate2gt39-do-not-match"></a><span data-ttu-id="b2f31-102">Evento '&lt;eventname1&gt;'non può implementare l'evento'&lt;eventname2&gt;'nell'interfaccia'&lt;interfaccia&gt;' perché i tipi di delegati&lt;delegate1&gt;'e'&lt;delegate2&gt;' non corrispondono</span><span class="sxs-lookup"><span data-stu-id="b2f31-102">Event &#39;&lt;eventname1&gt;&#39; cannot implement event &#39;&lt;eventname2&gt;&#39; on interface &#39;&lt;interface&gt;&#39; because their delegate types &#39;&lt;delegate1&gt;&#39; and &#39;&lt;delegate2&gt;&#39; do not match</span></span>
[!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)]<span data-ttu-id="b2f31-103">Impossibile implementare un evento perché il tipo di delegato dell'evento non corrisponde al tipo di delegato dell'evento nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b2f31-103"> cannot implement an event because the delegate type of the event does not match the delegate type of the event in the interface.</span></span> <span data-ttu-id="b2f31-104">Questo errore può insorgere quando si definiscono più eventi in un'interfaccia e si prova a implementarli assieme con lo stesso evento.</span><span class="sxs-lookup"><span data-stu-id="b2f31-104">This error can occur when you define multiple events in an interface and then attempt to implement them together with the same event.</span></span> <span data-ttu-id="b2f31-105">Un evento può implementare due o più eventi solo se tutti gli eventi implementati vengono dichiarati usando la sintassi `As` e se tutti specificano lo stesso tipo delegato.</span><span class="sxs-lookup"><span data-stu-id="b2f31-105">An event can implement two or more events only if all implemented events are declared using the `As` syntax and specify the same delegate type.</span></span>  
  
 <span data-ttu-id="b2f31-106">**ID errore:** BC31423</span><span class="sxs-lookup"><span data-stu-id="b2f31-106">**Error ID:** BC31423</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b2f31-107">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="b2f31-107">To correct this error</span></span>  
  
-   <span data-ttu-id="b2f31-108">Implementare gli eventi separatamente.</span><span class="sxs-lookup"><span data-stu-id="b2f31-108">Implement the events separately.</span></span>  
  
     <span data-ttu-id="b2f31-109">-oppure-</span><span class="sxs-lookup"><span data-stu-id="b2f31-109">—or—</span></span>  
  
-   <span data-ttu-id="b2f31-110">Definire gli eventi nell'interfaccia utilizzando il `As` sintassi e specificare lo stesso tipo di delegato.</span><span class="sxs-lookup"><span data-stu-id="b2f31-110">Define the events in the interface using the `As` syntax and specify the same delegate type.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2f31-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b2f31-111">See Also</span></span>  
 <span data-ttu-id="b2f31-112">[Istruzione Event](../../../visual-basic/language-reference/statements/event-statement.md) </span><span class="sxs-lookup"><span data-stu-id="b2f31-112">[Event Statement](../../../visual-basic/language-reference/statements/event-statement.md) </span></span>  
<span data-ttu-id="b2f31-113"> [Delegate (istruzione)](../../../visual-basic/language-reference/statements/delegate-statement.md) </span><span class="sxs-lookup"><span data-stu-id="b2f31-113"> [Delegate Statement](../../../visual-basic/language-reference/statements/delegate-statement.md) </span></span>  
<span data-ttu-id="b2f31-114"> [Eventi](../../../visual-basic/programming-guide/language-features/events/index.md)</span><span class="sxs-lookup"><span data-stu-id="b2f31-114"> [Events](../../../visual-basic/programming-guide/language-features/events/index.md)</span></span>
