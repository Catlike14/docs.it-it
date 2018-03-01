---
title: sbyte (Riferimenti per C#)
ms.date: 03/14/2017
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- sbyte_CSharpKeyword
- sbyte
helpviewer_keywords:
- sbyte keyword [C#]
ms.assetid: 1a9c7b48-73d1-4d33-b485-c4faf0a816bc
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 010ac98f523eca5929100f7c51b8b6ef5d11de30
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="sbyte-c-reference"></a><span data-ttu-id="98b9c-102">sbyte (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="98b9c-102">sbyte (C# Reference)</span></span>

<span data-ttu-id="98b9c-103">`sbyte` denota un tipo integrale che archivia valori in base alla dimensione e all'intervallo visualizzato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="98b9c-103">`sbyte` denotes an integral type that stores values according to the size and range shown in the following table.</span></span>  
  
|<span data-ttu-id="98b9c-104">Tipo</span><span class="sxs-lookup"><span data-stu-id="98b9c-104">Type</span></span>|<span data-ttu-id="98b9c-105">Intervallo</span><span class="sxs-lookup"><span data-stu-id="98b9c-105">Range</span></span>|<span data-ttu-id="98b9c-106">Dimensioni</span><span class="sxs-lookup"><span data-stu-id="98b9c-106">Size</span></span>|<span data-ttu-id="98b9c-107">Tipo .NET Framework</span><span class="sxs-lookup"><span data-stu-id="98b9c-107">.NET Framework type</span></span>|  
|----------|-----------|----------|-------------------------|  
|`sbyte`|<span data-ttu-id="98b9c-108">Da -128 a 127</span><span class="sxs-lookup"><span data-stu-id="98b9c-108">-128 to 127</span></span>|<span data-ttu-id="98b9c-109">Valore intero con segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="98b9c-109">Signed 8-bit integer</span></span>|<xref:System.SByte?displayProperty=nameWithType>|  
  
## <a name="literals"></a><span data-ttu-id="98b9c-110">Valori letterali</span><span class="sxs-lookup"><span data-stu-id="98b9c-110">Literals</span></span>  

<span data-ttu-id="98b9c-111">È possibile dichiarare e inizializzare una variabile `sbyte` assegnandole un valore letterale decimale, un valore letterale esadecimale o (a partire da C# 7) un valore letterale binario.</span><span class="sxs-lookup"><span data-stu-id="98b9c-111">You can declare and initialize an `sbyte` variable by assigning a decimal literal, a hexadecimal literal, or (starting with C# 7) a binary literal to it.</span></span> 

<span data-ttu-id="98b9c-112">Nell'esempio seguente, i valori interi uguali a 102 rappresentati come valori letterali decimali, esadecimali o binari vengono convertiti da valori [int](../../../csharp/language-reference/keywords/int.md) a valori `sbyte`.</span><span class="sxs-lookup"><span data-stu-id="98b9c-112">In the following example, integers equal to -102 that are represented as decimal, hexadecimal, and binary literals are converted from [int](../../../csharp/language-reference/keywords/int.md) to `sbyte` values.</span></span>    
  
[!code-csharp[SByte](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#SByte)]  

> [!NOTE] 
> <span data-ttu-id="98b9c-113">Viene usato il prefisso `0x` o `0X` per identificare un valore letterale esadecimale e il prefisso `0b` o `0B` per identificare un valore letterale binario.</span><span class="sxs-lookup"><span data-stu-id="98b9c-113">You use the prefix `0x` or `0X` to denote a hexadecimal literal and the prefix `0b` or `0B` to denote a binary literal.</span></span> <span data-ttu-id="98b9c-114">I valori letterali decimali non hanno prefissi.</span><span class="sxs-lookup"><span data-stu-id="98b9c-114">Decimal literals have no prefix.</span></span>

<span data-ttu-id="98b9c-115">A partire da c# 7, alcune funzionalità sono state aggiunte migliorare la leggibilità.</span><span class="sxs-lookup"><span data-stu-id="98b9c-115">Starting with C# 7, a couple of features have been added to enhance readability.</span></span> 
 - <span data-ttu-id="98b9c-116">C# 7.0 consente l'utilizzo dei caratteri di sottolineatura, `_`, come un separatore di cifre.</span><span class="sxs-lookup"><span data-stu-id="98b9c-116">C# 7.0 allows the usage of the underscore character, `_`, as a digit separator.</span></span>
 - <span data-ttu-id="98b9c-117">Consente di c# 7.2 `_` da utilizzare come separatore di cifre per un valore letterale binario o esadecimale, dopo il prefisso.</span><span class="sxs-lookup"><span data-stu-id="98b9c-117">C# 7.2 allows `_` to be used as a digit separator for a binary or hexadecimal literal, after the prefix.</span></span> <span data-ttu-id="98b9c-118">Un valore letterale decimale non è consentito utilizzare un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="98b9c-118">A decimal literal isn't permitted to have a leading underscore.</span></span>

 <span data-ttu-id="98b9c-119">Di seguito sono illustrati alcuni esempi.</span><span class="sxs-lookup"><span data-stu-id="98b9c-119">Some examples are shown below.</span></span>

[!code-csharp[SByteSeparator](../../../../samples/snippets/csharp/language-reference/keywords/numeric-literals.cs#SByteS)]  

<span data-ttu-id="98b9c-120">Se il valore letterale integer è esterno all'intervallo di `sbyte`, vale a dire se è minore di <xref:System.SByte.MinValue?displayProperty=nameWithType> o maggiore di <xref:System.SByte.MaxValue?displayProperty=nameWithType>, si verifica un errore di compilazione.</span><span class="sxs-lookup"><span data-stu-id="98b9c-120">If the integer literal is outside the range of `sbyte` (that is, if it is less than <xref:System.SByte.MinValue?displayProperty=nameWithType> or greater than <xref:System.SByte.MaxValue?displayProperty=nameWithType>, a compilation error occurs.</span></span> <span data-ttu-id="98b9c-121">Quando un valore letterale integer non ha alcun suffisso, il tipo è il primo di questi tipi in cui può essere rappresentato il relativo valore: [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-121">When an integer literal has no suffix, its type is the first of these types in which its value can be represented: [int](int.md), [uint](uint.md), [long](long.md), [ulong](ulong.md).</span></span> <span data-ttu-id="98b9c-122">Ciò significa che, in questo esempio, i valori letterali numerici `0x9A` e `0b10011010` vengono interpretati come interi con segno a 32 bit con un valore corrispondente a 156, che supera <xref:System.SByte.MaxValue?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="98b9c-122">This means that, in this example, the numeric literals `0x9A` and `0b10011010` are interpreted as 32-bit signed integers with a value of 156, which exceeds <xref:System.SByte.MaxValue?displayProperty=nameWithType>.</span></span> <span data-ttu-id="98b9c-123">Per questo motivo, è necessario l'operatore di cast e l'assegnazione deve trovarsi in un contesto [unchecked](unchecked.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-123">Because of this, the casting operator is needed, and the assignment must occur in an [unchecked](unchecked.md) context.</span></span> 

## <a name="compiler-overload-resolution"></a><span data-ttu-id="98b9c-124">Risoluzione dell'overload del compilatore</span><span class="sxs-lookup"><span data-stu-id="98b9c-124">Compiler overload resolution</span></span>

 <span data-ttu-id="98b9c-125">È necessario usare un cast quando si chiamano metodi di overload.</span><span class="sxs-lookup"><span data-stu-id="98b9c-125">A cast must be used when calling overloaded methods.</span></span> <span data-ttu-id="98b9c-126">Considerare, ad esempio, i metodi seguenti di overload che usano i parametri `sbyte` e [int](../../../csharp/language-reference/keywords/int.md):</span><span class="sxs-lookup"><span data-stu-id="98b9c-126">Consider, for example, the following overloaded methods that use `sbyte` and [int](../../../csharp/language-reference/keywords/int.md) parameters:</span></span>  
  
```csharp  
public static void SampleMethod(int i) {}  
public static void SampleMethod(sbyte b) {}  
```  
  
 <span data-ttu-id="98b9c-127">L'uso del cast `sbyte` garantisce che venga chiamato il tipo corretto, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="98b9c-127">Using the `sbyte` cast guarantees that the correct type is called, for example:</span></span>  
  
```csharp 
// Calling the method with the int parameter:  
SampleMethod(5);  
// Calling the method with the sbyte parameter:  
SampleMethod((sbyte)5);  
```  
  
## <a name="conversions"></a><span data-ttu-id="98b9c-128">Conversioni</span><span class="sxs-lookup"><span data-stu-id="98b9c-128">Conversions</span></span>  
 <span data-ttu-id="98b9c-129">Si verifica una conversione implicita predefinita da `sbyte` a [short](../../../csharp/language-reference/keywords/short.md), [int](../../../csharp/language-reference/keywords/int.md), [long](../../../csharp/language-reference/keywords/long.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md) o [decimal](../../../csharp/language-reference/keywords/decimal.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-129">There is a predefined implicit conversion from `sbyte` to [short](../../../csharp/language-reference/keywords/short.md), [int](../../../csharp/language-reference/keywords/int.md), [long](../../../csharp/language-reference/keywords/long.md), [float](../../../csharp/language-reference/keywords/float.md), [double](../../../csharp/language-reference/keywords/double.md), or [decimal](../../../csharp/language-reference/keywords/decimal.md).</span></span>  
  
 <span data-ttu-id="98b9c-130">Non è possibile convertire in modo implicito tipi numerici non letterali che necessitano di maggiore spazio in memoria in `sbyte`. Per informazioni sullo spazio necessario per l'archiviazione dei tipi integrali, vedere [Tabella dei tipi integrali](../../../csharp/language-reference/keywords/integral-types-table.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-130">You cannot implicitly convert nonliteral numeric types of larger storage size to `sbyte` (see [Integral Types Table](../../../csharp/language-reference/keywords/integral-types-table.md) for the storage sizes of integral types).</span></span> <span data-ttu-id="98b9c-131">Considerare, ad esempio, le due variabili `sbyte` seguenti, `x` e `y`:</span><span class="sxs-lookup"><span data-stu-id="98b9c-131">Consider, for example, the following two `sbyte` variables `x` and `y`:</span></span>  
  
```csharp  
sbyte x = 10, y = 20;  
```  
  
 <span data-ttu-id="98b9c-132">L'istruzione di assegnazione che segue provocherà un errore di compilazione poiché, per impostazione predefinita, l'espressione aritmetica a destra dell'operatore di assegnazione restituisce [int](../../../csharp/language-reference/keywords/int.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-132">The following assignment statement will produce a compilation error, because the arithmetic expression on the right side of the assignment operator evaluates to [int](../../../csharp/language-reference/keywords/int.md) by default.</span></span>  
  
```csharp  
sbyte z = x + y;   // Error: conversion from int to sbyte  
```  
  
 <span data-ttu-id="98b9c-133">Per risolvere il problema, eseguire il cast dell'espressione come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="98b9c-133">To fix this problem, cast the expression as in the following example:</span></span>  
  
```csharp  
sbyte z = (sbyte)(x + y);   // OK: explicit conversion  
```  
  
 <span data-ttu-id="98b9c-134">È possibile tuttavia usare le istruzioni seguenti dove la variabile di destinazione ha la stessa dimensione di archiviazione o una dimensione maggiore:</span><span class="sxs-lookup"><span data-stu-id="98b9c-134">It is possible though to use the following statements, where the destination variable has the same storage size or a larger storage size:</span></span>  
  
```csharp
sbyte x = 10, y = 20;  
int m = x + y;  
long n = x + y;  
```  
  
 <span data-ttu-id="98b9c-135">Si noti inoltre che non avviene alcuna conversione implicita dai tipi a virgola mobile in `sbyte`.</span><span class="sxs-lookup"><span data-stu-id="98b9c-135">Notice also that there is no implicit conversion from floating-point types to `sbyte`.</span></span> <span data-ttu-id="98b9c-136">Ad esempio, l'istruzione seguente genera un errore del compilatore, a meno che non venga usato un cast esplicito:</span><span class="sxs-lookup"><span data-stu-id="98b9c-136">For example, the following statement generates a compiler error unless an explicit cast is used:</span></span>  
  
```csharp  
sbyte x = 3.0;         // Error: no implicit conversion from double  
sbyte y = (sbyte)3.0;  // OK: explicit conversion  
```  
  
 <span data-ttu-id="98b9c-137">Per informazioni sulle espressioni aritmetiche con tipi a virgola mobile e tipi integrali, vedere [float](../../../csharp/language-reference/keywords/float.md) e [double](../../../csharp/language-reference/keywords/double.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-137">For information about arithmetic expressions with mixed floating-point types and integral types, see [float](../../../csharp/language-reference/keywords/float.md) and [double](../../../csharp/language-reference/keywords/double.md).</span></span>  
  
 <span data-ttu-id="98b9c-138">Per altre informazioni sulle regole di conversione numeriche implicite, vedere [Tabella delle conversioni numeriche implicite](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md).</span><span class="sxs-lookup"><span data-stu-id="98b9c-138">For more information about implicit numeric conversion rules, see the [Implicit Numeric Conversions Table](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md).</span></span>  
  
## <a name="c-language-specification"></a><span data-ttu-id="98b9c-139">Specifiche del linguaggio C#</span><span class="sxs-lookup"><span data-stu-id="98b9c-139">C# Language Specification</span></span>  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="98b9c-140">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="98b9c-140">See Also</span></span>  
 <xref:System.SByte>  
 [<span data-ttu-id="98b9c-141">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="98b9c-141">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="98b9c-142">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="98b9c-142">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="98b9c-143">Parole chiave di C#</span><span class="sxs-lookup"><span data-stu-id="98b9c-143">C# Keywords</span></span>](../../../csharp/language-reference/keywords/index.md)  
 [<span data-ttu-id="98b9c-144">Tabella dei tipi integrali</span><span class="sxs-lookup"><span data-stu-id="98b9c-144">Integral Types Table</span></span>](../../../csharp/language-reference/keywords/integral-types-table.md)  
 [<span data-ttu-id="98b9c-145">Tabella dei tipi incorporati</span><span class="sxs-lookup"><span data-stu-id="98b9c-145">Built-In Types Table</span></span>](../../../csharp/language-reference/keywords/built-in-types-table.md)  
 [<span data-ttu-id="98b9c-146">Tabella delle conversioni numeriche implicite</span><span class="sxs-lookup"><span data-stu-id="98b9c-146">Implicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/implicit-numeric-conversions-table.md)  
 [<span data-ttu-id="98b9c-147">Tabella delle conversioni numeriche esplicite</span><span class="sxs-lookup"><span data-stu-id="98b9c-147">Explicit Numeric Conversions Table</span></span>](../../../csharp/language-reference/keywords/explicit-numeric-conversions-table.md)
