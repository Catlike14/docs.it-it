---
title: Operatore &gt;&gt;= (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '>>=_CSharpKeyword'
helpviewer_keywords:
- right shift assignment operator (>>=) [C#]
- '>>= operator (right-shift assignment) [C#]'
ms.assetid: b593778c-b9b4-440d-8b29-c1ac22cb81c0
caps.latest.revision: 14
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 6bd0a61860c35a485d61585a90ba297f75d8cf1a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="gtgt-operator-c-reference"></a><span data-ttu-id="15d41-102">Operatore &gt;&gt;= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="15d41-102">&gt;&gt;= Operator (C# Reference)</span></span>
<span data-ttu-id="15d41-103">Operatore di assegnazione di spostamento a destra.</span><span class="sxs-lookup"><span data-stu-id="15d41-103">The right-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="15d41-104">Note</span><span class="sxs-lookup"><span data-stu-id="15d41-104">Remarks</span></span>  
 <span data-ttu-id="15d41-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="15d41-105">An expression of the form</span></span>  
  
```  
x >>= y  
```  
  
 <span data-ttu-id="15d41-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="15d41-106">is evaluated as</span></span>  
  
```  
x = x >> y  
```  
  
 <span data-ttu-id="15d41-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="15d41-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="15d41-108">L'[operatore >>](../../../csharp/language-reference/operators/right-shift-operator.md) sposta `x` verso destra di una quantità specificata da `y`.</span><span class="sxs-lookup"><span data-stu-id="15d41-108">The [>> operator](../../../csharp/language-reference/operators/right-shift-operator.md) shifts `x` right by an amount specified by `y`.</span></span>  
  
 <span data-ttu-id="15d41-109">L'operatore >>= non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore >>](../../../csharp/language-reference/operators/right-shift-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="15d41-109">The >>= operator cannot be overloaded directly, but user-defined types can overload the [>> operator](../../../csharp/language-reference/operators/right-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="15d41-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="15d41-110">Example</span></span>  
 [!code-csharp[csRefOperators#11](../../../csharp/language-reference/operators/codesnippet/CSharp/right-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="15d41-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="15d41-111">See Also</span></span>  
 [<span data-ttu-id="15d41-112">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="15d41-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="15d41-113">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="15d41-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="15d41-114">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="15d41-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
