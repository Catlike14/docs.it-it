---
title: Operatore |= (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '|=_CSharpKeyword'
dev_langs:
- CSharp
helpviewer_keywords:
- OR assignment operator (|=) [C#]
- '|= operator (OR assignment) [C#]'
ms.assetid: 8315b8cf-dd15-402f-92f0-c7db931696ca
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
ms.openlocfilehash: f1c0a92414739efc2ab091871e80852737fdf931
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="-operator-c-reference"></a><span data-ttu-id="eab57-102">Operatore |= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="eab57-102">|= Operator (C# Reference)</span></span>
<span data-ttu-id="eab57-103">Operatore di assegnazione OR.</span><span class="sxs-lookup"><span data-stu-id="eab57-103">The OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eab57-104">Note</span><span class="sxs-lookup"><span data-stu-id="eab57-104">Remarks</span></span>  
 <span data-ttu-id="eab57-105">Un'espressione che usa l'operatore di assegnazione `|=`, ad esempio</span><span class="sxs-lookup"><span data-stu-id="eab57-105">An expression using the `|=` assignment operator, such as</span></span>  
  
```  
x |= y  
```  
  
 <span data-ttu-id="eab57-106">equivale a</span><span class="sxs-lookup"><span data-stu-id="eab57-106">is equivalent to</span></span>  
  
```  
x = x | y  
```  
  
 <span data-ttu-id="eab57-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="eab57-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="eab57-108">L'[operatore &#124;](../../../csharp/language-reference/operators/or-operator.md) esegue un'operazione con OR logico bit per bit su operandi integrali e un'operazione con OR logico sugli operandi bool.</span><span class="sxs-lookup"><span data-stu-id="eab57-108">The [&#124; operator](../../../csharp/language-reference/operators/or-operator.md) performs a bitwise logical OR operation on integral operands and logical OR on bool operands.</span></span>  
  
 <span data-ttu-id="eab57-109">L'operatore `|=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore &#124;](../../../csharp/language-reference/operators/or-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="eab57-109">The `|=` operator cannot be overloaded directly, but user-defined types can overload the [&#124; operator](../../../csharp/language-reference/operators/or-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="eab57-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="eab57-110">Example</span></span>  
 <span data-ttu-id="eab57-111">[!code-cs[csRefOperators#10](../../../csharp/language-reference/operators/codesnippet/CSharp/or-assignment-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="eab57-111">[!code-cs[csRefOperators#10](../../../csharp/language-reference/operators/codesnippet/CSharp/or-assignment-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eab57-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="eab57-112">See Also</span></span>  
 <span data-ttu-id="eab57-113">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="eab57-113">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="eab57-114">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="eab57-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="eab57-115">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="eab57-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

