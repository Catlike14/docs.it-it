---
title: Operatore &lt;&lt;= (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
caps.latest.revision: 16
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: b5c2a177182561075442afc3f1b76603c6646bd6
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="dc24c-102">Operatore &lt;&lt;= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="dc24c-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="dc24c-103">Operatore di assegnazione di spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="dc24c-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc24c-104">Note</span><span class="sxs-lookup"><span data-stu-id="dc24c-104">Remarks</span></span>  
 <span data-ttu-id="dc24c-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="dc24c-105">An expression of the form</span></span>  
  
```  
x <<= y  
```  
  
 <span data-ttu-id="dc24c-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="dc24c-106">is evaluated as</span></span>  
  
```  
x = x << y  
```  
  
 <span data-ttu-id="dc24c-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="dc24c-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="dc24c-108">L'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) sposta `x` verso sinistra del numero di bit specificato da `y`.</span><span class="sxs-lookup"><span data-stu-id="dc24c-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="dc24c-109">L'operatore `<<=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="dc24c-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc24c-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc24c-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="dc24c-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc24c-111">See Also</span></span>  
 [<span data-ttu-id="dc24c-112">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="dc24c-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="dc24c-113">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="dc24c-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="dc24c-114">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="dc24c-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
