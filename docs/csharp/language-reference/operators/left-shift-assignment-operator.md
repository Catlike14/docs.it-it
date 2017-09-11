---
title: Operatore &lt;&lt;= (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- <<=_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- <<= operator (left-shift assignment) [C#]
- left shift assignment operator (<<=) [C#]
ms.assetid: 3bc99c78-1edb-4827-86fc-bce6c3048871
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
ms.openlocfilehash: fd562a538891a5592cc724e74cffb3d086248898
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="ltlt-operator-c-reference"></a><span data-ttu-id="ff2bc-102">Operatore &lt;&lt;= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="ff2bc-102">&lt;&lt;= Operator (C# Reference)</span></span>
<span data-ttu-id="ff2bc-103">Operatore di assegnazione di spostamento a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-103">The left-shift assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ff2bc-104">Note</span><span class="sxs-lookup"><span data-stu-id="ff2bc-104">Remarks</span></span>  
 <span data-ttu-id="ff2bc-105">Un'espressione nel formato</span><span class="sxs-lookup"><span data-stu-id="ff2bc-105">An expression of the form</span></span>  
  
```  
x <<= y  
```  
  
 <span data-ttu-id="ff2bc-106">viene valutata come</span><span class="sxs-lookup"><span data-stu-id="ff2bc-106">is evaluated as</span></span>  
  
```  
x = x << y  
```  
  
 <span data-ttu-id="ff2bc-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="ff2bc-108">L'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) sposta `x` verso sinistra del numero di bit specificato da `y`.</span><span class="sxs-lookup"><span data-stu-id="ff2bc-108">The [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) shifts `x` left by the number of bits specified by `y`.</span></span>  
  
 <span data-ttu-id="ff2bc-109">L'operatore `<<=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore <<](../../../csharp/language-reference/operators/left-shift-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="ff2bc-109">The `<<=` operator cannot be overloaded directly, but user-defined types can overload the [<< operator](../../../csharp/language-reference/operators/left-shift-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff2bc-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff2bc-110">Example</span></span>  
 <span data-ttu-id="ff2bc-111">[!code-cs[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="ff2bc-111">[!code-cs[csRefOperators#12](../../../csharp/language-reference/operators/codesnippet/CSharp/left-shift-assignment-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ff2bc-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff2bc-112">See Also</span></span>  
 <span data-ttu-id="ff2bc-113">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="ff2bc-113">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="ff2bc-114">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="ff2bc-114">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="ff2bc-115">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="ff2bc-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

