---
title: Struttura generale di un programma C# (Guida per programmatori C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- C# language, program structure
ms.assetid: 5ae964a5-0ef0-40fe-88fb-6d1793371d0d
caps.latest.revision: 21
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
ms.openlocfilehash: d55ac6a6d35e5f47ab26da681afe9fb5555331ec
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="general-structure-of-a-c-program-c-programming-guide"></a><span data-ttu-id="0c1a3-102">Struttura generale di un programma C# (Guida per programmatori C#)</span><span class="sxs-lookup"><span data-stu-id="0c1a3-102">General Structure of a C# Program (C# Programming Guide)</span></span>
<span data-ttu-id="0c1a3-103">I programmi C# possono essere costituiti da uno o più file.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-103">C# programs can consist of one or more files.</span></span> <span data-ttu-id="0c1a3-104">Ciascun file può contenere zero o più spazi dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-104">Each file can contain zero or more namespaces.</span></span> <span data-ttu-id="0c1a3-105">Uno spazio dei nomi può contenere tipi, quali classi, struct, interfacce, enumerazioni e delegati.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-105">A namespace can contain types such as classes, structs, interfaces, enumerations, and delegates, in addition to other namespaces.</span></span> <span data-ttu-id="0c1a3-106">Di seguito viene illustrata la struttura di base di un programma C# che contiene tutti questi elementi.</span><span class="sxs-lookup"><span data-stu-id="0c1a3-106">The following is the skeleton of a C# program that contains all of these elements.</span></span>  
  
 <span data-ttu-id="0c1a3-107">[!code-cs[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]</span><span class="sxs-lookup"><span data-stu-id="0c1a3-107">[!code-cs[csProgGuide#34](../../../csharp/programming-guide/inside-a-program/codesnippet/CSharp/general-structure-of-a-csharp-program_1.cs)]</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="0c1a3-108">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="0c1a3-108">Related Sections</span></span>  
 <span data-ttu-id="0c1a3-109">Per ulteriori informazioni:</span><span class="sxs-lookup"><span data-stu-id="0c1a3-109">For more information:</span></span>  
  
-   [<span data-ttu-id="0c1a3-110">Classi</span><span class="sxs-lookup"><span data-stu-id="0c1a3-110">Classes</span></span>](../../../csharp/programming-guide/classes-and-structs/classes.md)  
  
-   [<span data-ttu-id="0c1a3-111">Struct</span><span class="sxs-lookup"><span data-stu-id="0c1a3-111">Structs</span></span>](../../../csharp/programming-guide/classes-and-structs/structs.md)  
  
-   [<span data-ttu-id="0c1a3-112">Spazi dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c1a3-112">Namespaces</span></span>](../../../csharp/programming-guide/namespaces/index.md)  
  
-   [<span data-ttu-id="0c1a3-113">Interfacce</span><span class="sxs-lookup"><span data-stu-id="0c1a3-113">Interfaces</span></span>](../../../csharp/programming-guide/interfaces/index.md)  
  
-   [<span data-ttu-id="0c1a3-114">Delegati</span><span class="sxs-lookup"><span data-stu-id="0c1a3-114">Delegates</span></span>](../../../csharp/programming-guide/delegates/index.md)  
  
## <a name="c-language-specification"></a><span data-ttu-id="0c1a3-115">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="0c1a3-115">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="0c1a3-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0c1a3-116">See Also</span></span>  
 <span data-ttu-id="0c1a3-117">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="0c1a3-117">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="0c1a3-118">[Contenuto di un programma C#](../../../csharp/programming-guide/inside-a-program/index.md) </span><span class="sxs-lookup"><span data-stu-id="0c1a3-118">[Inside a C# Program](../../../csharp/programming-guide/inside-a-program/index.md) </span></span>  
 <span data-ttu-id="0c1a3-119">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="0c1a3-119">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 [<span data-ttu-id="0c1a3-120">\<Applicazioni di esempio di C#</span><span class="sxs-lookup"><span data-stu-id="0c1a3-120">\<paveover>C# Sample Applications</span></span>](http://msdn.microsoft.com/en-us/9a9d7aaa-51d3-4224-b564-95409b0f3e15)

