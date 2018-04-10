---
title: Operatore &gt; (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '>_CSharpKeyword'
helpviewer_keywords:
- '> operator [C#]'
- greater than operator (>) [C#]
ms.assetid: 26d3cb69-9c0b-4cc5-858b-5be1abd6659d
caps.latest.revision: 16
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: fc7c173ecc97bd3ca3b76a92ccbabc0f40062ac7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="gt-operator-c-reference"></a><span data-ttu-id="2208f-102">Operatore &gt; (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="2208f-102">&gt; Operator (C# Reference)</span></span>
<span data-ttu-id="2208f-103">Tutti i tipi numerici e di enumerazione definiscono un operatore relazionale "maggiore di", `>`, che restituisce `true` se il primo operando è maggiore del secondo, in caso contrario `false`.</span><span class="sxs-lookup"><span data-stu-id="2208f-103">All numeric and enumeration types define a "greater than" relational operator (`>`) that returns `true` if the first operand is greater than the second, `false` otherwise.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2208f-104">Note</span><span class="sxs-lookup"><span data-stu-id="2208f-104">Remarks</span></span>  
 <span data-ttu-id="2208f-105">I tipi definiti dall'utente possono eseguire l'overload dell'operatore `>` (vedere [operatore](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="2208f-105">User-defined types can overload the `>` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="2208f-106">Se `>` è sottoposto a overload, deve esserlo anche [<](../../../csharp/language-reference/operators/less-than-operator.md).</span><span class="sxs-lookup"><span data-stu-id="2208f-106">If `>` is overloaded, [<](../../../csharp/language-reference/operators/less-than-operator.md) must also be overloaded.</span></span> <span data-ttu-id="2208f-107">Quando viene eseguito l'overload di un operatore binario, viene anche eseguito in modo implicito l'overload dell'operatore di assegnazione corrispondente, se presente.</span><span class="sxs-lookup"><span data-stu-id="2208f-107">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2208f-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="2208f-108">Example</span></span>  
 [!code-csharp[csRefOperators#29](../../../csharp/language-reference/operators/codesnippet/CSharp/greater-than-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="2208f-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2208f-109">See Also</span></span>  
 [<span data-ttu-id="2208f-110">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="2208f-110">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="2208f-111">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="2208f-111">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="2208f-112">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="2208f-112">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)  
 [<span data-ttu-id="2208f-113">explicit</span><span class="sxs-lookup"><span data-stu-id="2208f-113">explicit</span></span>](../../../csharp/language-reference/keywords/explicit.md)
