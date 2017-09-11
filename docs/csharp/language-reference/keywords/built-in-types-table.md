---
title: Tabella dei tipi incorporati (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- types [C#], built-in
- built-in C# types
ms.assetid: 54f901f2-bf2f-472c-ae8d-73e8ecfc57fe
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
ms.openlocfilehash: df13a45544491dee9e592a4ab0b90b5235f12abc
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="built-in-types-table-c-reference"></a><span data-ttu-id="19238-102">Tabella dei tipi incorporati (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="19238-102">Built-In Types Table (C# Reference)</span></span>
<span data-ttu-id="19238-103">La tabella seguente include le parole chiave per i tipi predefiniti di C#, che rappresentano gli alias dei tipi predefiniti nello spazio dei nomi <xref:System>.</span><span class="sxs-lookup"><span data-stu-id="19238-103">The following table shows the keywords for built-in C# types, which are aliases of predefined types in the <xref:System> namespace.</span></span>  
  
|<span data-ttu-id="19238-104">Tipo C#</span><span class="sxs-lookup"><span data-stu-id="19238-104">C# Type</span></span>|<span data-ttu-id="19238-105">Tipo .NET Framework</span><span class="sxs-lookup"><span data-stu-id="19238-105">.NET Framework Type</span></span>|  
|--------------|-------------------------|  
|[<span data-ttu-id="19238-106">bool</span><span class="sxs-lookup"><span data-stu-id="19238-106">bool</span></span>](../../../csharp/language-reference/keywords/bool.md)|`System.Boolean`|  
|[<span data-ttu-id="19238-107">byte</span><span class="sxs-lookup"><span data-stu-id="19238-107">byte</span></span>](../../../csharp/language-reference/keywords/byte.md)|`System.Byte`|  
|[<span data-ttu-id="19238-108">sbyte</span><span class="sxs-lookup"><span data-stu-id="19238-108">sbyte</span></span>](../../../csharp/language-reference/keywords/sbyte.md)|`System.SByte`|  
|[<span data-ttu-id="19238-109">char</span><span class="sxs-lookup"><span data-stu-id="19238-109">char</span></span>](../../../csharp/language-reference/keywords/char.md)|`System.Char`|  
|[<span data-ttu-id="19238-110">decimal</span><span class="sxs-lookup"><span data-stu-id="19238-110">decimal</span></span>](../../../csharp/language-reference/keywords/decimal.md)|`System.Decimal`|  
|[<span data-ttu-id="19238-111">double</span><span class="sxs-lookup"><span data-stu-id="19238-111">double</span></span>](../../../csharp/language-reference/keywords/double.md)|`System.Double`|  
|[<span data-ttu-id="19238-112">float</span><span class="sxs-lookup"><span data-stu-id="19238-112">float</span></span>](../../../csharp/language-reference/keywords/float.md)|`System.Single`|  
|[<span data-ttu-id="19238-113">int</span><span class="sxs-lookup"><span data-stu-id="19238-113">int</span></span>](../../../csharp/language-reference/keywords/int.md)|`System.Int32`|  
|[<span data-ttu-id="19238-114">uint</span><span class="sxs-lookup"><span data-stu-id="19238-114">uint</span></span>](../../../csharp/language-reference/keywords/uint.md)|`System.UInt32`|  
|[<span data-ttu-id="19238-115">long</span><span class="sxs-lookup"><span data-stu-id="19238-115">long</span></span>](../../../csharp/language-reference/keywords/long.md)|`System.Int64`|  
|[<span data-ttu-id="19238-116">ulong</span><span class="sxs-lookup"><span data-stu-id="19238-116">ulong</span></span>](../../../csharp/language-reference/keywords/ulong.md)|`System.UInt64`|  
|[<span data-ttu-id="19238-117">object</span><span class="sxs-lookup"><span data-stu-id="19238-117">object</span></span>](../../../csharp/language-reference/keywords/object.md)|`System.Object`|  
|[<span data-ttu-id="19238-118">short</span><span class="sxs-lookup"><span data-stu-id="19238-118">short</span></span>](../../../csharp/language-reference/keywords/short.md)|`System.Int16`|  
|[<span data-ttu-id="19238-119">ushort</span><span class="sxs-lookup"><span data-stu-id="19238-119">ushort</span></span>](../../../csharp/language-reference/keywords/ushort.md)|`System.UInt16`|  
|[<span data-ttu-id="19238-120">string</span><span class="sxs-lookup"><span data-stu-id="19238-120">string</span></span>](../../../csharp/language-reference/keywords/string.md)|`System.String`|  
  
## <a name="remarks"></a><span data-ttu-id="19238-121">Note</span><span class="sxs-lookup"><span data-stu-id="19238-121">Remarks</span></span>  
 <span data-ttu-id="19238-122">Tutti i tipi nella tabella, ad eccezione di `object` e `string`, sono detti tipi semplici.</span><span class="sxs-lookup"><span data-stu-id="19238-122">All of the types in the table, except `object` and `string`, are referred to as simple types.</span></span>  
  
 <span data-ttu-id="19238-123">Le parole chiave per i tipi C# e i relativi alias sono intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="19238-123">The C# type keywords and their aliases are interchangeable.</span></span> <span data-ttu-id="19238-124">Ad esempio, è possibile dichiarare una variabile integer, usando le seguenti dichiarazioni:</span><span class="sxs-lookup"><span data-stu-id="19238-124">For example, you can declare an integer variable by using either of the following declarations:</span></span>  
  
```  
int x = 123;  
System.Int32 x = 123;  
```  
  
 <span data-ttu-id="19238-125">Per visualizzare il tipo effettivo di qualsiasi tipo in C#, usare il metodo di sistema `GetType()`.</span><span class="sxs-lookup"><span data-stu-id="19238-125">To display the actual type for any C# type, use the system method `GetType()`.</span></span> <span data-ttu-id="19238-126">Ad esempio, l'istruzione seguente consente di visualizzare l'alias di sistema che rappresenta il tipo di `myVariable`:</span><span class="sxs-lookup"><span data-stu-id="19238-126">For example, the following statement displays the system alias that represents the type of `myVariable`:</span></span>  
  
```  
Console.WriteLine(myVariable.GetType());  
```  
  
 <span data-ttu-id="19238-127">È anche possibile usare l'operatore [typeof](../../../csharp/language-reference/keywords/typeof.md).</span><span class="sxs-lookup"><span data-stu-id="19238-127">You can also use the [typeof](../../../csharp/language-reference/keywords/typeof.md) operator.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19238-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="19238-128">See Also</span></span>  
 <span data-ttu-id="19238-129">[Riferimenti per C#](../../../csharp/language-reference/index.md) </span><span class="sxs-lookup"><span data-stu-id="19238-129">[C# Reference](../../../csharp/language-reference/index.md) </span></span>  
 <span data-ttu-id="19238-130">[Guida per programmatori C#](../../../csharp/programming-guide/index.md) </span><span class="sxs-lookup"><span data-stu-id="19238-130">[C# Programming Guide](../../../csharp/programming-guide/index.md) </span></span>  
 <span data-ttu-id="19238-131">[Parole chiave di C#](../../../csharp/language-reference/keywords/index.md) </span><span class="sxs-lookup"><span data-stu-id="19238-131">[C# Keywords](../../../csharp/language-reference/keywords/index.md) </span></span>  
 <span data-ttu-id="19238-132">[Tipi di valore](../../../csharp/language-reference/keywords/value-types.md) </span><span class="sxs-lookup"><span data-stu-id="19238-132">[Value Types](../../../csharp/language-reference/keywords/value-types.md) </span></span>  
 <span data-ttu-id="19238-133">[Tabella dei valori predefiniti](../../../csharp/language-reference/keywords/default-values-table.md) </span><span class="sxs-lookup"><span data-stu-id="19238-133">[Default Values Table](../../../csharp/language-reference/keywords/default-values-table.md) </span></span>  
 <span data-ttu-id="19238-134">[Tabella di formattazione dei risultati numerici](../../../csharp/language-reference/keywords/formatting-numeric-results-table.md) </span><span class="sxs-lookup"><span data-stu-id="19238-134">[Formatting Numeric Results Table](../../../csharp/language-reference/keywords/formatting-numeric-results-table.md) </span></span>  
 <span data-ttu-id="19238-135">[dynamic](../../../csharp/language-reference/keywords/dynamic.md) </span><span class="sxs-lookup"><span data-stu-id="19238-135">[dynamic](../../../csharp/language-reference/keywords/dynamic.md) </span></span>  
 [<span data-ttu-id="19238-136">Tabelle di riferimento per i tipi</span><span class="sxs-lookup"><span data-stu-id="19238-136">Reference Tables for Types</span></span>](../../../csharp/language-reference/keywords/reference-tables-for-types.md)

