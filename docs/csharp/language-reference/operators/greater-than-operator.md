---
title: Operatore &gt; (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '>_CSharpKeyword'
dev_langs:
- CSharp
helpviewer_keywords:
- '> operator [C#]'
- greater than operator (>) [C#]
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
caps.latest.revision: 16
author: BillWagner
ms.author: wiwagn
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
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 5b4eb1f6fcca311fc772e4dbe0ce0391201af3de
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="47709-102">Operatore &gt; (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="47709-102">&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="47709-103">Tutti i tipi numerici e di enumerazione definiscono un operatore relazionale "maggiore di", `>`, che restituisce `true` se il primo operando è maggiore del secondo, in caso contrario `false`.</span><span class="sxs-lookup"><span data-stu-id="47709-103">All numeric and enumeration types define a "greater than" relational operator (`>`) that returns `true` if the first operand is greater than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="47709-104">Note</span><span class="sxs-lookup"><span data-stu-id="47709-104">Remarks</span></span>  
 <span data-ttu-id="47709-105">I tipi definiti dall'utente possono eseguire l'overload dell'operatore `>` (vedere [operatore](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="47709-105">User-defined types can overload the `>` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="47709-106">Se `>` è sottoposto a overload, deve esserlo anche [<](../../../csharp/language-reference/operators/less-than-operator.md).</span><span class="sxs-lookup"><span data-stu-id="47709-106">If `>` is overloaded, [<](../../../csharp/language-reference/operators/less-than-operator.md) must also be overloaded.</span></span> <span data-ttu-id="47709-107">Quando viene eseguito l'overload di un operatore binario, viene anche eseguito in modo implicito l'overload dell'operatore di assegnazione corrispondente, se presente.</span><span class="sxs-lookup"><span data-stu-id="47709-107">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="47709-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="47709-108">Example</span></span>  
 <span data-ttu-id="47709-109">[!code-cs[csRefOperators#29](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="47709-109">[!code-cs[csRefOperators#29](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47709-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="47709-110">See Also</span></span>  
 <span data-ttu-id="47709-111">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="47709-111">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="47709-112">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="47709-112">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="47709-113">[Operatori C#](../../../csharp/language-reference/operators/index.md) </span><span class="sxs-lookup"><span data-stu-id="47709-113">[C# Operators](../../../csharp/language-reference/operators/index.md) </span></span>  
 [<span data-ttu-id="47709-114">explicit</span><span class="sxs-lookup"><span data-stu-id="47709-114">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)

