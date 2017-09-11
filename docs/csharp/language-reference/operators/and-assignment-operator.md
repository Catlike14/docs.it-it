---
title: Operatore &amp;= (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '&=_CSharpKeyword'
dev_langs:
- CSharp
helpviewer_keywords:
- AND assignment operator (&=) [C#]
- '&= operator [C#]'
ms.assetid: e8d58f3f-72dd-4b5a-b995-452fcce7e6bb
caps.latest.revision: 15
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
ms.openlocfilehash: 6dec8de5077c07150ea37b88979e7b59b231d610
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="ec218-102">Operatore &amp;= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="ec218-102">&amp;= Operator (C# Reference)</span></span>
<span data-ttu-id="ec218-103">Operatore di assegnazione AND.</span><span class="sxs-lookup"><span data-stu-id="ec218-103">The AND assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec218-104">Note</span><span class="sxs-lookup"><span data-stu-id="ec218-104">Remarks</span></span>  
 <span data-ttu-id="ec218-105">Un'espressione che usa l'operatore di assegnazione `&=`, ad esempio</span><span class="sxs-lookup"><span data-stu-id="ec218-105">An expression using the `&=` assignment operator, such as</span></span>  
  
```  
x &= y  
```  
  
 <span data-ttu-id="ec218-106">equivale a</span><span class="sxs-lookup"><span data-stu-id="ec218-106">is equivalent to</span></span>  
  
```  
x = x & y  
```  
  
 <span data-ttu-id="ec218-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="ec218-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="ec218-108">L'[operatore &](../../../csharp/language-reference/operators/and-operator.md) esegue un'operazione con AND logico bit per bit su operandi integrali e un'operazione con AND logico sugli operandi `bool`.</span><span class="sxs-lookup"><span data-stu-id="ec218-108">The [& operator](../../../csharp/language-reference/operators/and-operator.md) performs a bitwise logical AND operation on integral operands and logical AND on `bool` operands.</span></span>  
  
 <span data-ttu-id="ec218-109">L'operatore `&=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore &](../../../csharp/language-reference/operators/and-operator.md) binario (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="ec218-109">The `&=` operator cannot be overloaded directly, but user-defined types can overload the binary [& operator](../../../csharp/language-reference/operators/and-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec218-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec218-110">Example</span></span>  
 <span data-ttu-id="ec218-111">[!code-cs[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="ec218-111">[!code-cs[csRefOperators#34](../../../csharp/language-reference/operators/codesnippet/CSharp/and-assignment-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec218-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec218-112">See Also</span></span>  
 <span data-ttu-id="ec218-113">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="ec218-113">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="ec218-114">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="ec218-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="ec218-115">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="ec218-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

