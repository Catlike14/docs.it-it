---
title: '#else (Riferimenti per C#)'
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- '#else'
helpviewer_keywords:
- '#else directive [C#]'
ms.assetid: 6a347322-cfa2-4a86-98f8-ddfa2cb7d4db
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: c3468d35a6e45c06f46fe8671708ce01a3cc7b65
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="else-c-reference"></a><span data-ttu-id="0b6d7-102">#else (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="0b6d7-102">#else (C# Reference)</span></span>
<span data-ttu-id="0b6d7-103">`#else` consente di creare una direttiva condizionale composita. In questo modo, se nessuna delle espressioni della direttiva [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) o [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) (facoltativa) precedenti ha restituito `true`, il compilatore valuterà tutto il codice tra `#else` e l'espressione `#endif` successiva.</span><span class="sxs-lookup"><span data-stu-id="0b6d7-103">`#else` lets you create a compound conditional directive, so that, if none of the expressions in the preceding [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) or (optional) [#elif](../../../csharp/language-reference/preprocessor-directives/preprocessor-elif.md) directives to `true`, the compiler will evaluate all code between `#else` and the subsequent `#endif`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0b6d7-104">Note</span><span class="sxs-lookup"><span data-stu-id="0b6d7-104">Remarks</span></span>  
 <span data-ttu-id="0b6d7-105">La direttiva per il preprocessore `#else` deve essere seguita da [#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md).</span><span class="sxs-lookup"><span data-stu-id="0b6d7-105">[#endif](../../../csharp/language-reference/preprocessor-directives/preprocessor-endif.md) must be the next preprocessor directive after `#else`.</span></span> <span data-ttu-id="0b6d7-106">Per un esempio di utilizzo di `#else`, vedere [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md).</span><span class="sxs-lookup"><span data-stu-id="0b6d7-106">See [#if](../../../csharp/language-reference/preprocessor-directives/preprocessor-if.md) for an example of how to use `#else`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0b6d7-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0b6d7-107">See Also</span></span>  
 [<span data-ttu-id="0b6d7-108">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="0b6d7-108">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="0b6d7-109">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="0b6d7-109">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0b6d7-110">Direttive per il preprocessore C#</span><span class="sxs-lookup"><span data-stu-id="0b6d7-110">C# Preprocessor Directives</span></span>](../../../csharp/language-reference/preprocessor-directives/index.md)
