---
title: Operatore ^= (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ^=_CSharpKeyword
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
caps.latest.revision: 16
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 8d4de06dbfd269dc5e0f2cc5003e8981068220a1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="-operator-c-reference"></a><span data-ttu-id="e40ab-102">Operatore ^= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="e40ab-102">^= Operator (C# Reference)</span></span>
<span data-ttu-id="e40ab-103">Operatore di assegnazione OR esclusivo.</span><span class="sxs-lookup"><span data-stu-id="e40ab-103">The exclusive-OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="e40ab-104">Note</span><span class="sxs-lookup"><span data-stu-id="e40ab-104">Remarks</span></span>  
 <span data-ttu-id="e40ab-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="e40ab-105">An expression of the form</span></span>  
  
```  
x ^= y  
```  
  
 <span data-ttu-id="e40ab-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="e40ab-106">is evaluated as</span></span>  
  
```  
x = x ^ y  
```  
  
 <span data-ttu-id="e40ab-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="e40ab-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="e40ab-108">L'[operatore ^](../../../csharp/language-reference/operators/xor-operator.md) esegue un'operazione con OR esclusivo bit per bit sugli operandi integrali e un'operazione con OR esclusivo logico sugli operandi [bool](../../../csharp/language-reference/keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="e40ab-108">The [^ operator](../../../csharp/language-reference/operators/xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../../../csharp/language-reference/keywords/bool.md) operands.</span></span>  
  
 <span data-ttu-id="e40ab-109">L'operatore ^= non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore ^](../../../csharp/language-reference/operators/xor-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="e40ab-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](../../../csharp/language-reference/operators/xor-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="e40ab-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="e40ab-110">Example</span></span>  
 [!code-csharp[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="e40ab-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e40ab-111">See Also</span></span>  
 [<span data-ttu-id="e40ab-112">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="e40ab-112">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="e40ab-113">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="e40ab-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="e40ab-114">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="e40ab-114">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
