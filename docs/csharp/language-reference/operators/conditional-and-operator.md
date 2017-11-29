---
title: '&amp;&amp; Operatore (Riferimenti per C#)'
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords: '&&_CSharpKeyword'
helpviewer_keywords:
- '&& operator [C#]'
- logical AND operator [C#]
ms.assetid: 2e4f0a1c-92a3-40f8-8e3b-17b607f20c31
caps.latest.revision: "18"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 16bc2fa650031d2b1f6cfaf7d128ba487963f707
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ampamp-operator-c-reference"></a><span data-ttu-id="9eded-102">&amp;&amp; Operatore (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="9eded-102">&amp;&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="9eded-103">L'operatore AND condizionale (`&&`) esegue un AND logico sugli operandi `bool`, ma valuta il secondo operando solo se necessario.</span><span class="sxs-lookup"><span data-stu-id="9eded-103">The conditional-AND operator (`&&`) performs a logical-AND of its `bool` operands, but only evaluates its second operand if necessary.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9eded-104">Note</span><span class="sxs-lookup"><span data-stu-id="9eded-104">Remarks</span></span>  
 <span data-ttu-id="9eded-105">L'operazione</span><span class="sxs-lookup"><span data-stu-id="9eded-105">The operation</span></span>  
  
```  
x && y  
```  
  
 <span data-ttu-id="9eded-106">corrisponde all'operazione</span><span class="sxs-lookup"><span data-stu-id="9eded-106">corresponds to the operation</span></span>  
  
```  
x & y  
```  
  
 <span data-ttu-id="9eded-107">tuttavia se `x` è `false`, `y` non viene valutato, poiché il risultato dell'operazione AND sarà `false` indipendentemente dal valore di `y`.</span><span class="sxs-lookup"><span data-stu-id="9eded-107">except that if `x` is `false`, `y` is not evaluated, because the result of the AND operation is `false` no matter what the value of `y`  is.</span></span> <span data-ttu-id="9eded-108">Questa condizione è denominata "valutazione short circuit".</span><span class="sxs-lookup"><span data-stu-id="9eded-108">This is known as "short-circuit" evaluation.</span></span>  
  
 <span data-ttu-id="9eded-109">L'operatore AND condizionale non può essere soggetto a overload, ma anche gli overload degli operatori logici comuni e degli operatori [true](../../../csharp/language-reference/keywords/true.md) e [false](../../../csharp/language-reference/keywords/false.md) (con certe limitazioni) sono considerati overload degli operatori logici condizionali.</span><span class="sxs-lookup"><span data-stu-id="9eded-109">The conditional-AND operator cannot be overloaded, but overloads of the regular logical operators and operators [true](../../../csharp/language-reference/keywords/true.md) and [false](../../../csharp/language-reference/keywords/false.md) are, with certain restrictions, also considered overloads of the conditional logical operators.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9eded-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="9eded-110">Example</span></span>  
 <span data-ttu-id="9eded-111">Nell'esempio seguente l'espressione condizionale nella seconda istruzione `if` valuta solo il primo operando, perché l'operando restituisce `false`.</span><span class="sxs-lookup"><span data-stu-id="9eded-111">In the following example, the conditional expression in the second `if` statement evaluates only the first operand because the operand returns `false`.</span></span>  
  
 [!code-csharp[csRefOperators#48](../../../csharp/language-reference/operators/codesnippet/CSharp/conditional-and-operator_1.cs)]  
  
## <a name="c-language-specification"></a><span data-ttu-id="9eded-112">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="9eded-112">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="9eded-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9eded-113">See Also</span></span>  
 [<span data-ttu-id="9eded-114">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="9eded-114">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="9eded-115">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="9eded-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="9eded-116">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="9eded-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
