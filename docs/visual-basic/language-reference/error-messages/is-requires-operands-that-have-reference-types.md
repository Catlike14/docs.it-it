---
title: "&#39; è &#39; gli operandi devono che dispongono di tipi di riferimento, ma questo operando ha tipo di valore &#39; &lt;typename&gt;&#39;"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30020
- vbc30020
helpviewer_keywords: BC30020
ms.assetid: 228afebd-1203-4bd3-8d7a-c5c56f3cedc4
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 28d017a566fdc1e55cb53ce907641d6bccfb354c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="39is39-requires-operands-that-have-reference-types-but-this-operand-has-the-value-type-39lttypenamegt39"></a><span data-ttu-id="e9cee-102">&#39; è &#39; gli operandi devono che dispongono di tipi di riferimento, ma questo operando ha tipo di valore &#39; &lt;typename&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="e9cee-102">&#39;Is&#39; requires operands that have reference types, but this operand has the value type &#39;&lt;typename&gt;&#39;</span></span>
<span data-ttu-id="e9cee-103">Il `Is` operatore di confronto determina se due variabili oggetto fanno riferimento alla stessa istanza.</span><span class="sxs-lookup"><span data-stu-id="e9cee-103">The `Is` comparison operator determines whether two object variables refer to the same instance.</span></span> <span data-ttu-id="e9cee-104">Questo confronto non è definito per i tipi di valore.</span><span class="sxs-lookup"><span data-stu-id="e9cee-104">This comparison is not defined for value types.</span></span>  
  
 <span data-ttu-id="e9cee-105">**ID errore:** BC30020</span><span class="sxs-lookup"><span data-stu-id="e9cee-105">**Error ID:** BC30020</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="e9cee-106">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="e9cee-106">To correct this error</span></span>  
  
-   <span data-ttu-id="e9cee-107">Usare l'operatore di confronto aritmetico appropriato o `Like` l'operatore per confrontare due tipi di valore.</span><span class="sxs-lookup"><span data-stu-id="e9cee-107">Use the appropriate arithmetic comparison operator or the `Like` operator to compare two value types.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e9cee-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e9cee-108">See Also</span></span>  
 [<span data-ttu-id="e9cee-109">Operatore Is</span><span class="sxs-lookup"><span data-stu-id="e9cee-109">Is Operator</span></span>](../../../visual-basic/language-reference/operators/is-operator.md)  
 [<span data-ttu-id="e9cee-110">Operatore Like</span><span class="sxs-lookup"><span data-stu-id="e9cee-110">Like Operator</span></span>](../../../visual-basic/language-reference/operators/like-operator.md)  
 [<span data-ttu-id="e9cee-111">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="e9cee-111">Comparison Operators</span></span>](../../../visual-basic/language-reference/operators/comparison-operators.md)
