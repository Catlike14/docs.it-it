---
title: Operatore /= (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- /=_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- division assignment operator (/=) [C#]
- /= (division assignment operator) [C#]
ms.assetid: 50fc02b0-ee9c-4c3e-b58d-d591282caf1c
caps.latest.revision: 17
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
ms.openlocfilehash: 5e105bf11f5413d77d62be4177ed22ba420312c3
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="-operator-c-reference"></a><span data-ttu-id="03e36-102">Operatore /= (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="03e36-102">/= Operator (C# Reference)</span></span>
<span data-ttu-id="03e36-103">Operatore di assegnazione di divisione.</span><span class="sxs-lookup"><span data-stu-id="03e36-103">The division assignment operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="03e36-104">Note</span><span class="sxs-lookup"><span data-stu-id="03e36-104">Remarks</span></span>  
 <span data-ttu-id="03e36-105">Un'espressione che usa l'operatore di assegnazione `/=`, ad esempio</span><span class="sxs-lookup"><span data-stu-id="03e36-105">An expression using the `/=` assignment operator, such as</span></span>  
  
```  
x /= y  
```  
  
 <span data-ttu-id="03e36-106">equivale a</span><span class="sxs-lookup"><span data-stu-id="03e36-106">is equivalent to</span></span>  
  
```  
x = x / y  
```  
  
 <span data-ttu-id="03e36-107">con la differenza che `x` viene valutato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="03e36-107">except that `x` is only evaluated once.</span></span> <span data-ttu-id="03e36-108">L'[operatore /](../../../csharp/language-reference/operators/division-operator.md) è già definito per i tipi numerici per l'esecuzione di divisioni.</span><span class="sxs-lookup"><span data-stu-id="03e36-108">The [/ operator](../../../csharp/language-reference/operators/division-operator.md) is predefined for numeric types to perform division.</span></span>  
  
 <span data-ttu-id="03e36-109">L'operatore `/=` non può essere sottoposto direttamente a overload. I tipi definiti dall'utente, tuttavia, possono eseguire l'overload dell'[operatore /](../../../csharp/language-reference/operators/division-operator.md) (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="03e36-109">The `/=` operator cannot be overloaded directly, but user-defined types can overload the [/ operator](../../../csharp/language-reference/operators/division-operator.md) (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="03e36-110">Su tutti gli operatori di assegnazione composti, l'overload dell'operatore binario esegue in modo implicito l'overload dell'assegnazione composta equivalente.</span><span class="sxs-lookup"><span data-stu-id="03e36-110">On all compound assignment operators, overloading the binary operator implicitly overloads the equivalent compound assignment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="03e36-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="03e36-111">Example</span></span>  
 <span data-ttu-id="03e36-112">[!code-cs[csRefOperators#5](codesnippet/CSharp/division-assignment-operator_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="03e36-112">[!code-cs[csRefOperators#5](codesnippet/CSharp/division-assignment-operator_1.cs)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03e36-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03e36-113">See Also</span></span>  
 <span data-ttu-id="03e36-114">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="03e36-114">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="03e36-115">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="03e36-115">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 [<span data-ttu-id="03e36-116">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="03e36-116">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)

