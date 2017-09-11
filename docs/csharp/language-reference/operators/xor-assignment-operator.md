---
title: Operatore ^= (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ^=_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- ^= operator [C#]
ms.assetid: 3658ff9a-61cd-467e-ad6b-8fbf1cfbaae4
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
ms.openlocfilehash: 33b0dccf5031809bb4fcb73d0f7d6a344accdea3
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="-operator-c-reference"></a><span data-ttu-id="c82ec-102">Operatore ^= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="c82ec-102">^= Operator (C# Reference)</span></span>
<span data-ttu-id="c82ec-103">Operatore di assegnazione OR esclusivo.</span><span class="sxs-lookup"><span data-stu-id="c82ec-103">The exclusive-OR assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c82ec-104">Note</span><span class="sxs-lookup"><span data-stu-id="c82ec-104">Remarks</span></span>  
 <span data-ttu-id="c82ec-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="c82ec-105">An expression of the form</span></span>  
  
```  
x ^= y  
```  
  
 <span data-ttu-id="c82ec-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="c82ec-106">is evaluated as</span></span>  
  
```  
x = x ^ y  
```  
  
 <span data-ttu-id="c82ec-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="c82ec-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="c82ec-108">L'[operatore ^](../../../csharp/language-reference/operators/xor-operator.md) esegue un'operazione con OR esclusivo bit per bit sugli operandi integrali e un'operazione con OR esclusivo logico sugli operandi [bool](../../../csharp/language-reference/keywords/bool.md).</span><span class="sxs-lookup"><span data-stu-id="c82ec-108">The [^ operator](../../../csharp/language-reference/operators/xor-operator.md) performs a bitwise exclusive-OR operation on integral operands and logical exclusive-OR on [bool](../../../csharp/language-reference/keywords/bool.md) operands.</span></span>  
  
 <span data-ttu-id="c82ec-109">L'operatore ^= non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore ^](../../../csharp/language-reference/operators/xor-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="c82ec-109">The ^= operator cannot be overloaded directly, but user-defined types can overload the [^ operator](../../../csharp/language-reference/operators/xor-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="c82ec-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="c82ec-110">Example</span></span>  
 <span data-ttu-id="c82ec-111">[!code-cs[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="c82ec-111">[!code-cs[csRefOperators#23](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-assignment-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c82ec-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c82ec-112">See Also</span></span>  
 <span data-ttu-id="c82ec-113">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="c82ec-113">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="c82ec-114">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="c82ec-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="c82ec-115">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="c82ec-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

