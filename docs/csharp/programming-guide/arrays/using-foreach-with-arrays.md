---
title: Utilizzo di foreach con matrici (Guida per programmatori C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- arrays [C#], foreach
- foreach statement [C#], using with arrays
ms.assetid: 5f2da2a9-1f56-4de5-94cc-e07f4f7a0244
caps.latest.revision: 14
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
ms.openlocfilehash: a1d0b704233b110b5f499b8186a4a901f9b5408f
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="using-foreach-with-arrays-c-programming-guide"></a><span data-ttu-id="da018-102">Utilizzo di foreach con matrici (Guida per programmatori C#)</span><span class="sxs-lookup"><span data-stu-id="da018-102">Using foreach with Arrays (C# Programming Guide)</span></span>
<span data-ttu-id="da018-103">In C# è disponibile anche l'istruzione [foreach](../../../csharp/language-reference/keywords/foreach-in.md).</span><span class="sxs-lookup"><span data-stu-id="da018-103">C# also provides the [foreach](../../../csharp/language-reference/keywords/foreach-in.md) statement.</span></span> <span data-ttu-id="da018-104">Questa istruzione offre un metodo semplice e diretto per scorrere gli elementi di una matrice o qualsiasi raccolta enumerabile.</span><span class="sxs-lookup"><span data-stu-id="da018-104">This statement provides a simple, clean way to iterate through the elements of an array or any enumerable collection.</span></span> <span data-ttu-id="da018-105">L'istruzione `foreach` elabora gli elementi nell'ordine restituito dalla matrice o dall'enumeratore del tipo di raccolta, in genere dall'elemento zero all'ultimo.</span><span class="sxs-lookup"><span data-stu-id="da018-105">The `foreach` statement processes elements in the order returned by the array or collection type’s enumerator, which is usually from the 0th element to the last.</span></span> <span data-ttu-id="da018-106">Il codice che segue, ad esempio, consente la creazione di una matrice denominata `numbers` e di scorrere tale matrice con l'istruzione `foreach`:</span><span class="sxs-lookup"><span data-stu-id="da018-106">For example, the following code creates an array called `numbers` and iterates through it with the `foreach` statement:</span></span>  
  
 <span data-ttu-id="da018-107">[!code-cs[csProgGuideArrays#28](../../../csharp/programming-guide/arrays/codesnippet/CSharp/using-foreach-with-arrays_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="da018-107">[!code-cs[csProgGuideArrays#28](../../../csharp/programming-guide/arrays/codesnippet/CSharp/using-foreach-with-arrays_1.cs)]</span></span>  
  
 <span data-ttu-id="da018-108">Con le matrici multidimensionali è possibile utilizzare lo stesso metodo per scorrere gli elementi, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="da018-108">With multidimensional arrays, you can use the same method to iterate through the elements, for example:</span></span>  
  
 <span data-ttu-id="da018-109">[!code-cs[csProgGuideArrays#29](../../../csharp/programming-guide/arrays/codesnippet/CSharp/using-foreach-with-arrays_2.cs)]</span><span class="sxs-lookup"><span data-stu-id="da018-109">[!code-cs[csProgGuideArrays#29](../../../csharp/programming-guide/arrays/codesnippet/CSharp/using-foreach-with-arrays_2.cs)]</span></span>  
  
 <span data-ttu-id="da018-110">Con le matrici multidimensionali, tuttavia, l'uso di un ciclo [for](../../../csharp/language-reference/keywords/for.md) annidato fornisce maggiore controllo sugli elementi della matrice.</span><span class="sxs-lookup"><span data-stu-id="da018-110">However, with multidimensional arrays, using a nested [for](../../../csharp/language-reference/keywords/for.md) loop gives you more control over the array elements.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="da018-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="da018-111">See Also</span></span>  
 <span data-ttu-id="da018-112"><xref:System.Array></span><span class="sxs-lookup"><span data-stu-id="da018-112"><xref:System.Array></span></span>   
 <span data-ttu-id="da018-113">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="da018-113">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="da018-114">[Matrici](../../../csharp/programming-guide/arrays/index.md) </span><span class="sxs-lookup"><span data-stu-id="da018-114">[Arrays](../../../csharp/programming-guide/arrays/index.md) </span></span>  
 <span data-ttu-id="da018-115">[Matrici unidimensionali](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span><span class="sxs-lookup"><span data-stu-id="da018-115">[Single-Dimensional Arrays](../../../csharp/programming-guide/arrays/single-dimensional-arrays.md) </span></span>  
 <span data-ttu-id="da018-116">[Matrici multidimensionali](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) </span><span class="sxs-lookup"><span data-stu-id="da018-116">[Multidimensional Arrays](../../../csharp/programming-guide/arrays/multidimensional-arrays.md) </span></span>  
 [<span data-ttu-id="da018-117">Matrici irregolari</span><span class="sxs-lookup"><span data-stu-id="da018-117">Jagged Arrays</span></span>](../../../csharp/programming-guide/arrays/jagged-arrays.md)

