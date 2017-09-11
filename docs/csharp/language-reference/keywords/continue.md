---
title: continue (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- continue_CSharpKeyword
- continue
dev_langs:
- CSharp
helpviewer_keywords:
- continue keyword [C#]
ms.assetid: 8a5ac96f-f98a-4519-b32d-345847ed7be0
caps.latest.revision: 20
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 4a0dcedb32b153c31ec5ed799f66062463307db9
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="continue-c-reference"></a><span data-ttu-id="e1306-102">continue (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="e1306-102">continue (C# Reference)</span></span>
<span data-ttu-id="e1306-103">L'istruzione `continue` passa il controllo all'iterazione successiva dell'istruzione [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md) o [foreach](../../../csharp/language-reference/keywords/foreach-in.md) di inclusione in cui è presente.</span><span class="sxs-lookup"><span data-stu-id="e1306-103">The `continue` statement passes control to the next iteration of the enclosing [while](../../../csharp/language-reference/keywords/while.md), [do](../../../csharp/language-reference/keywords/do.md), [for](../../../csharp/language-reference/keywords/for.md), or [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement in which it appears.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e1306-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="e1306-104">Example</span></span>  
 <span data-ttu-id="e1306-105">In questo esempio viene inizializzato un contatore per il conteggio da 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="e1306-105">In this example, a counter is initialized to count from 1 to 10.</span></span> <span data-ttu-id="e1306-106">Usando l'istruzione `continue` in combinazione con l'espressione `(i < 9)`, le istruzioni comprese tra `continue` e la fine del corpo di `for` vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="e1306-106">By using the `continue` statement in conjunction with the expression `(i < 9)`, the statements between `continue` and the end of the `for` body are skipped.</span></span>  
  
 <span data-ttu-id="e1306-107">[!code-cs[csrefKeywordsJump#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/continue_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="e1306-107">[!code-cs[csrefKeywordsJump#3](../../../csharp/language-reference/keywords/codesnippet/CSharp/continue_1.cs)]</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="e1306-108">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="e1306-108">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="e1306-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e1306-109">See Also</span></span>  
 <span data-ttu-id="e1306-110">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="e1306-110">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="e1306-111">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="e1306-111">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="e1306-112">[Parole chiave di C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="e1306-112">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="e1306-113">[Istruzione break](/cpp/cpp/break-statement-cpp) </span><span class="sxs-lookup"><span data-stu-id="e1306-113">[break Statement](/cpp/cpp/break-statement-cpp) </span></span>  
 [<span data-ttu-id="e1306-114">Istruzioni di spostamento</span><span class="sxs-lookup"><span data-stu-id="e1306-114">Jump Statements</span></span>](../../../csharp/language-reference/keywords/jump-statements.md)

