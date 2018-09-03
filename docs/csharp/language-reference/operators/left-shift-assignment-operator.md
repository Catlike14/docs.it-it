---
title: Operatore &lt;&lt;= (Riferimenti per C#)
ms.date: 07/20/2015
f1_keywords:
- <<=_CSharpKeyword
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
ms.openlocfilehash: c689aeccdf3ad6cc6c672cc101a4f0aa92f19791
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2018
ms.locfileid: "43406974"
---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="182b6-102">Operatore &lt;&lt;= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="182b6-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="182b6-103">Operatore di assegnazione di spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="182b6-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="182b6-104">Note</span><span class="sxs-lookup"><span data-stu-id="182b6-104">Remarks</span></span>  
 <span data-ttu-id="182b6-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="182b6-105">An expression of the form</span></span>  
  
```csharp  
x <<= y  
```  
  
 <span data-ttu-id="182b6-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="182b6-106">is evaluated as</span></span>  
  
```csharp  
x = x << y  
```  
  
 <span data-ttu-id="182b6-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="182b6-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="182b6-108">L'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) sposta `x` verso sinistra del numero di bit specificato da `y`.</span><span class="sxs-lookup"><span data-stu-id="182b6-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="182b6-109">L'operatore `<<=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="182b6-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="182b6-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="182b6-110">Example</span></span>  
 [!code-csharp[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="182b6-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="182b6-111">See Also</span></span>

- [<span data-ttu-id="182b6-112">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="182b6-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="182b6-113">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="182b6-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="182b6-114">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="182b6-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
