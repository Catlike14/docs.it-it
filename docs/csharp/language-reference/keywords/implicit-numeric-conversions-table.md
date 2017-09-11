---
title: Tabella delle conversioni numeriche implicite (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- conversions [C#], implicit numeric
- implicit numeric conversions [C#]
- numeric conversions [C#], implicit
- types [C#], implicit numeric conversions
ms.assetid: 72eb5a94-0491-48bf-8032-d7ebfdfeb8d8
caps.latest.revision: 12
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
ms.openlocfilehash: 4c7aa29f9bdeb5f30918e6d7b990c5197e7fe1a1
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="implicit-numeric-conversions-table-c-reference"></a><span data-ttu-id="83c09-102">Tabella delle conversioni numeriche implicite (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="83c09-102">Implicit Numeric Conversions Table (C# Reference)</span></span>
<span data-ttu-id="83c09-103">Nella tabella che segue sono illustrate le conversioni numeriche implicite predefinite.</span><span class="sxs-lookup"><span data-stu-id="83c09-103">The following table shows the predefined implicit numeric conversions.</span></span> <span data-ttu-id="83c09-104">Le conversioni implicite possono avere luogo in numerose situazioni, ad esempio le chiamate di metodi e le istruzioni di assegnazione.</span><span class="sxs-lookup"><span data-stu-id="83c09-104">Implicit conversions might occur in many situations, including method invoking and assignment statements.</span></span>  
  
|<span data-ttu-id="83c09-105">Da</span><span class="sxs-lookup"><span data-stu-id="83c09-105">From</span></span>|<span data-ttu-id="83c09-106">A</span><span class="sxs-lookup"><span data-stu-id="83c09-106">To</span></span>|  
|----------|--------|  
|[<span data-ttu-id="83c09-107">sbyte</span><span class="sxs-lookup"><span data-stu-id="83c09-107">sbyte</span></span>](../../../csharp/language-reference/keywords/sbyte.md)|<span data-ttu-id="83c09-108">`short`, `int`, `long`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-108">`short`, `int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-109">byte</span><span class="sxs-lookup"><span data-stu-id="83c09-109">byte</span></span>](../../../csharp/language-reference/keywords/byte.md)|<span data-ttu-id="83c09-110">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-110">`short`, `ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-111">short</span><span class="sxs-lookup"><span data-stu-id="83c09-111">short</span></span>](../../../csharp/language-reference/keywords/short.md)|<span data-ttu-id="83c09-112">`int`, `long`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-112">`int`, `long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-113">ushort</span><span class="sxs-lookup"><span data-stu-id="83c09-113">ushort</span></span>](../../../csharp/language-reference/keywords/ushort.md)|<span data-ttu-id="83c09-114">`int`, `uint`, `long`, `ulong`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-114">`int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-115">int</span><span class="sxs-lookup"><span data-stu-id="83c09-115">int</span></span>](../../../csharp/language-reference/keywords/int.md)|<span data-ttu-id="83c09-116">`long`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-116">`long`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-117">uint</span><span class="sxs-lookup"><span data-stu-id="83c09-117">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)|<span data-ttu-id="83c09-118">`long`, `ulong`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-118">`long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-119">long</span><span class="sxs-lookup"><span data-stu-id="83c09-119">long</span></span>](../../../csharp/language-reference/keywords/long.md)|<span data-ttu-id="83c09-120">`float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-120">`float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-121">char</span><span class="sxs-lookup"><span data-stu-id="83c09-121">char</span></span>](../../../csharp/language-reference/keywords/char.md)|<span data-ttu-id="83c09-122">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-122">`ushort`, `int`, `uint`, `long`, `ulong`, `float`, `double`, or `decimal`</span></span>|  
|[<span data-ttu-id="83c09-123">float</span><span class="sxs-lookup"><span data-stu-id="83c09-123">float</span></span>](../../../csharp/language-reference/keywords/float.md)|`double`|  
|[<span data-ttu-id="83c09-124">ulong</span><span class="sxs-lookup"><span data-stu-id="83c09-124">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md)|<span data-ttu-id="83c09-125">`float`, `double` o `decimal`</span><span class="sxs-lookup"><span data-stu-id="83c09-125">`float`, `double`, or `decimal`</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="83c09-126">Note</span><span class="sxs-lookup"><span data-stu-id="83c09-126">Remarks</span></span>  
  
-   <span data-ttu-id="83c09-127">Nella conversione da `int`, `uint`, `long` o `ulong` a `float` e da `long` o `ulong` a `double` può andare persa la precisione ma non la grandezza.</span><span class="sxs-lookup"><span data-stu-id="83c09-127">Precision but not magnitude might be lost in the conversions from `int`, `uint`,  `long`, or `ulong` to `float` and from `long` or `ulong` to `double`.</span></span>  
  
-   <span data-ttu-id="83c09-128">Non esiste alcuna conversione implicita verso il tipo `char`.</span><span class="sxs-lookup"><span data-stu-id="83c09-128">There are no implicit conversions to the `char` type.</span></span>  
  
-   <span data-ttu-id="83c09-129">Non esiste alcuna conversione implicita tra tipi a virgola mobile e il tipo `decimal`.</span><span class="sxs-lookup"><span data-stu-id="83c09-129">There are no implicit conversions between floating-point types and the `decimal` type.</span></span>  
  
-   <span data-ttu-id="83c09-130">Un'espressione costante di tipo `int` può essere convertita in `sbyte`, `byte`, `short`, `ushort`, `uint` o `ulong`, a condizione che il valore di tale espressione sia compreso nell'intervallo del tipo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83c09-130">A constant expression of type `int` can be converted to `sbyte`, `byte`, `short`, `ushort`, `uint`, or `ulong`, provided the value of the constant expression is within the range of the destination type.</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="83c09-131">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="83c09-131">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="83c09-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="83c09-132">See Also</span></span>  
 <span data-ttu-id="83c09-133">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="83c09-133">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="83c09-134">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="83c09-134">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="83c09-135">[Tabella dei tipi integrali](../../../csharp/language-reference/keywords/integral-types-table.md) </span><span class="sxs-lookup"><span data-stu-id="83c09-135">[Integral Types Table](../../../csharp/language-reference/keywords/integral-types-table.md) </span></span>  
 <span data-ttu-id="83c09-136">[Tabella dei tipi predefiniti](../../../csharp/language-reference/keywords/built-in-types-table.md) </span><span class="sxs-lookup"><span data-stu-id="83c09-136">[Built-In Types Table](../../../csharp/language-reference/keywords/built-in-types-table.md) </span></span>  
 <span data-ttu-id="83c09-137">[Tabella delle conversioni numeriche esplicite](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md) </span><span class="sxs-lookup"><span data-stu-id="83c09-137">[Explicit Numeric Conversions Table](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md) </span></span>  
 [<span data-ttu-id="83c09-138">Cast e conversioni di tipi</span><span class="sxs-lookup"><span data-stu-id="83c09-138">Casting and Type Conversions</span></span>](../../../csharp/programming-guide/types/casting-and-type-conversions.md)

