---
title: 'Formattazione di linee guida di codice F #'
description: 'Altre linee guida per la formattazione del codice F #.'
ms.date: 05/14/2018
ms.openlocfilehash: 6c8e4059fd4bf1e7450118a6df02609217c4f4db
ms.sourcegitcommit: 2ad7d06f4f469b5d8a5280ac0e0289a81867fc8e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "35231508"
---
# <a name="f-code-formatting-guidelines"></a><span data-ttu-id="f2284-103">Formattazione di linee guida di codice F #</span><span class="sxs-lookup"><span data-stu-id="f2284-103">F# code formatting guidelines</span></span>

<span data-ttu-id="f2284-104">In questo articolo vengono fornite linee guida per la modalità di formattazione del codice in modo che il codice F # è:</span><span class="sxs-lookup"><span data-stu-id="f2284-104">This article offers guidelines for how to format your code so that your F# code is:</span></span>

* <span data-ttu-id="f2284-105">In genere visualizzati come più leggibile</span><span class="sxs-lookup"><span data-stu-id="f2284-105">Generally viewed as more legible</span></span>
* <span data-ttu-id="f2284-106">È in base alle convenzioni applicate formattando altri editor e strumenti in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2284-106">Is in accordance with conventions applied by formatting tools in Visual Studio and other editors</span></span>
* <span data-ttu-id="f2284-107">Simile ad altro codice in linea</span><span class="sxs-lookup"><span data-stu-id="f2284-107">Similar to other code online</span></span>

<span data-ttu-id="f2284-108">Queste linee guida si basano [una guida completa alla convenzioni di formattazione di F #](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) da [Phan Anh letame](https://github.com/dungpa).</span><span class="sxs-lookup"><span data-stu-id="f2284-108">These guidelines are based on [A comprehensive guide to F# Formatting Conventions](https://github.com/dungpa/fantomas/blob/master/docs/FormattingConventions.md) by [Anh-Dung Phan](https://github.com/dungpa).</span></span>

## <a name="general-rules-for-indentation"></a><span data-ttu-id="f2284-109">Regole generali per il rientro</span><span class="sxs-lookup"><span data-stu-id="f2284-109">General rules for indentation</span></span>

<span data-ttu-id="f2284-110">F # utilizza degli spazi vuoti significativi per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="f2284-110">F# uses significant whitespace by default.</span></span> <span data-ttu-id="f2284-111">Le linee guida seguenti sono destinate a fornire istruzioni su come alcune problematiche ciò può imporre l'esigenza.</span><span class="sxs-lookup"><span data-stu-id="f2284-111">The following guidelines are intended to provide guidance as to how to juggle some challenges this can impose.</span></span>

### <a name="using-spaces"></a><span data-ttu-id="f2284-112">Uso di spazi</span><span class="sxs-lookup"><span data-stu-id="f2284-112">Using spaces</span></span>

<span data-ttu-id="f2284-113">Quando è necessario il rientro, è necessario utilizzare spazi e non tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="f2284-113">When indentation is required, you must use spaces, not tabs.</span></span> <span data-ttu-id="f2284-114">È necessario almeno uno spazio.</span><span class="sxs-lookup"><span data-stu-id="f2284-114">At least one space is required.</span></span> <span data-ttu-id="f2284-115">L'organizzazione può creare standard di codifica per specificare il numero di spazi da utilizzare per il rientro. in genere viene due, tre o quattro spazi di rientro a ogni livello in cui si verifica il rientro.</span><span class="sxs-lookup"><span data-stu-id="f2284-115">Your organization can create coding standards to specify the number of spaces to use for indentation; two, three or four spaces of indentation at each level where indentation occurs is typical.</span></span>

<span data-ttu-id="f2284-116">**Si consiglia di 4 spazi per il rientro.**</span><span class="sxs-lookup"><span data-stu-id="f2284-116">**We recommend 4 spaces per indentation.**</span></span>

<span data-ttu-id="f2284-117">Ciò premesso, rientro dei programmi è una questione soggettiva.</span><span class="sxs-lookup"><span data-stu-id="f2284-117">That said, indentation of programs is a subjective matter.</span></span> <span data-ttu-id="f2284-118">Le variazioni sono OK, ma è la prima regola è necessario seguire *coerenza di rientro*.</span><span class="sxs-lookup"><span data-stu-id="f2284-118">Variations are OK, but the first rule you should follow is *consistency of indentation*.</span></span> <span data-ttu-id="f2284-119">Scegliere uno stile di rientro generalmente accettato e usarlo sistematicamente in tutta la codebase.</span><span class="sxs-lookup"><span data-stu-id="f2284-119">Choose a generally accepted style of indentation and use it systematically throughout your codebase.</span></span>

## <a name="formatting-blank-lines"></a><span data-ttu-id="f2284-120">Formattazione di righe vuote</span><span class="sxs-lookup"><span data-stu-id="f2284-120">Formatting blank lines</span></span>

* <span data-ttu-id="f2284-121">Separato (funzione) e la classe definizioni di primo livello con due righe vuote.</span><span class="sxs-lookup"><span data-stu-id="f2284-121">Separate top-level function and class definitions with two blank lines.</span></span>
* <span data-ttu-id="f2284-122">Le definizioni di metodo all'interno di una classe sono separate da una singola riga vuota.</span><span class="sxs-lookup"><span data-stu-id="f2284-122">Method definitions inside a class are separated by a single blank line.</span></span>
* <span data-ttu-id="f2284-123">Righe vuote aggiuntive possono essere utilizzate (solo se necessario) per separare i gruppi di funzioni correlate.</span><span class="sxs-lookup"><span data-stu-id="f2284-123">Extra blank lines may be used (sparingly) to separate groups of related functions.</span></span> <span data-ttu-id="f2284-124">Le righe vuote possono essere omesse tra una serie di comandi correlati di una riga (ad esempio, un set di implementazioni fittizie).</span><span class="sxs-lookup"><span data-stu-id="f2284-124">Blank lines may be omitted between a bunch of related one-liners (for example, a set of dummy implementations).</span></span>
* <span data-ttu-id="f2284-125">Utilizzare le righe vuote nelle funzioni, solo se necessario, per indicare sezioni logiche.</span><span class="sxs-lookup"><span data-stu-id="f2284-125">Use blank lines in functions, sparingly, to indicate logical sections.</span></span>

## <a name="formatting-comments"></a><span data-ttu-id="f2284-126">Formattazione di commenti</span><span class="sxs-lookup"><span data-stu-id="f2284-126">Formatting comments</span></span>

<span data-ttu-id="f2284-127">In genere preferire più commenti doppia barra commenti del blocco di stile di ML.</span><span class="sxs-lookup"><span data-stu-id="f2284-127">Generally prefer multiple double-slash comments over ML-style block comments.</span></span>

```fsharp
// Prefer this style of comments when you want
// to express written ideas on multiple lines.

(*
    ML-style comments are fine, but not a .NET-ism.
    They are useful when needing to modify multi-line comments, though.
*)
```

<span data-ttu-id="f2284-128">Commenti devono converte in maiuscolo la prima lettera.</span><span class="sxs-lookup"><span data-stu-id="f2284-128">Inline comments should capitalize the first letter.</span></span>

```fsharp
let f x = x + 1 // Increment by one.
```

## <a name="naming-conventions"></a><span data-ttu-id="f2284-129">Convenzioni di denominazione</span><span class="sxs-lookup"><span data-stu-id="f2284-129">Naming conventions</span></span>

### <a name="use-camelcase-for-class-bound-expression-bound-and-pattern-bound-values-and-functions"></a><span data-ttu-id="f2284-130">Utilizzare camelCase per le funzioni e i valori associati a classe, espressione di associazione e con associazione a modello</span><span class="sxs-lookup"><span data-stu-id="f2284-130">Use camelCase for class-bound, expression-bound and pattern-bound values and functions</span></span>

<span data-ttu-id="f2284-131">È normale e F # è stato accettato stile da usare camelCase per tutti i nomi associati come variabili locali o in Criteri di ricerca e le definizioni di funzione.</span><span class="sxs-lookup"><span data-stu-id="f2284-131">It is common and accepted F# style to use camelCase for all names bound as local variables or in pattern matches and function definitions.</span></span>

```fsharp
// OK
let addIAndJ i j = i + j

// Bad
let addIAndJ I J = I+J

// Bad
let AddIAndJ i j = i + j
```

<span data-ttu-id="f2284-132">In locale con associazione a funzioni nelle classi devono inoltre utilizzare camelCase.</span><span class="sxs-lookup"><span data-stu-id="f2284-132">Locally-bound functions in classes should also use camelCase.</span></span>

```fsharp
type MyClass() =

    let doSomething () =

    let firstResult = ...

    let secondResult = ...

    member x.Result = doSomething()
```

### <a name="use-camelcase-for-module-bound-public-functions"></a><span data-ttu-id="f2284-133">Utilizzare camelCase per le funzioni pubbliche associate a modulo</span><span class="sxs-lookup"><span data-stu-id="f2284-133">Use camelCase for module-bound public functions</span></span>

<span data-ttu-id="f2284-134">Quando una funzione associata a modulo fa parte di un'API pubblica, è necessario utilizzare camelCase:</span><span class="sxs-lookup"><span data-stu-id="f2284-134">When a module-bound function is part of a public API, it should use camelCase:</span></span>

```fsharp
module MyAPI =
    let publicFunctionOne param1 param2 param2 = ...

    let publicFunctionTwo param1 param2 param3 = ...
```

### <a name="use-camelcase-for-internal-and-private-module-bound-values-and-functions"></a><span data-ttu-id="f2284-135">Utilizzare camelCase per le funzioni e i valori associati a modulo interni e privati</span><span class="sxs-lookup"><span data-stu-id="f2284-135">Use camelCase for internal and private module-bound values and functions</span></span>

<span data-ttu-id="f2284-136">Utilizzare camelCase per i valori associati a modulo privati, inclusi i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f2284-136">Use camelCase for private module-bound values, including the following:</span></span>

* <span data-ttu-id="f2284-137">Funzioni ad hoc negli script</span><span class="sxs-lookup"><span data-stu-id="f2284-137">Ad hoc functions in scripts</span></span>

* <span data-ttu-id="f2284-138">Valori che costituiscono l'implementazione interna del tipo o modulo</span><span class="sxs-lookup"><span data-stu-id="f2284-138">Values making up the internal implementation of a module or type</span></span>

```fsharp
let emailMyBossTheLatestResults =
    ...
```

### <a name="use-camelcase-for-parameters"></a><span data-ttu-id="f2284-139">Utilizzare camelCase per i parametri</span><span class="sxs-lookup"><span data-stu-id="f2284-139">Use camelCase for parameters</span></span>

<span data-ttu-id="f2284-140">Tutti i parametri devono utilizzare camelCase in base alle convenzioni di denominazione .NET.</span><span class="sxs-lookup"><span data-stu-id="f2284-140">All parameters should use camelCase in accordance with .NET naming conventions.</span></span>

```fsharp
module MyModule =
    let myFunction paramOne paramTwo = ...

type MyClass() =
    member this.MyMethod(paramOne, paramTwo) = ...
```

### <a name="use-pascalcase-for-modules"></a><span data-ttu-id="f2284-141">Usa PascalCase per i moduli</span><span class="sxs-lookup"><span data-stu-id="f2284-141">Use PascalCase for modules</span></span>

<span data-ttu-id="f2284-142">Tutti i moduli (primo livello, interni, privati, annidati) devono utilizzare PascalCase.</span><span class="sxs-lookup"><span data-stu-id="f2284-142">All modules (top-level, internal, private, nested) should use PascalCase.</span></span>

```fsharp
module MyTopLevelModule

module Helpers =
    module private SuperHelpers =
        ...

    ...
```

### <a name="use-pascalcase-for-type-declarations-members-and-labels"></a><span data-ttu-id="f2284-143">Utilizzare PascalCase per le dichiarazioni di tipi, membri e le etichette</span><span class="sxs-lookup"><span data-stu-id="f2284-143">Use PascalCase for type declarations, members, and labels</span></span>

<span data-ttu-id="f2284-144">Le classi, interfacce, strutture, enumerazioni, delegati, i record e unioni discriminate devono essere denominate con PascalCase.</span><span class="sxs-lookup"><span data-stu-id="f2284-144">Classes, interfaces, structs, enumerations, delegates, records, and discriminated unions should all be named with PascalCase.</span></span> <span data-ttu-id="f2284-145">I membri all'interno di tipi e le etichette per i record e le unioni discriminate devono utilizzare anche PascalCase.</span><span class="sxs-lookup"><span data-stu-id="f2284-145">Members within types and labels for records and discriminated unions should also use PascalCase.</span></span>

```fsharp
type IMyInterface =
    abstract Something: int

type MyClass() =
    member this.MyMethod(x, y) = x + y

type MyRecord = { IntVal: int; StringVal: string }

type SchoolPerson =
    | Professor
    | Student
    | Advisor
    | Administrator
```

### <a name="use-pascalcase-for-constructs-intrinsic-to-net"></a><span data-ttu-id="f2284-146">Utilizzare PascalCase per i costrutti intrinseci per .NET</span><span class="sxs-lookup"><span data-stu-id="f2284-146">Use PascalCase for constructs intrinsic to .NET</span></span>

<span data-ttu-id="f2284-147">Spazi dei nomi, le eccezioni, eventi e progetto /`.dll` nomi devono inoltre utilizzare PascalCase.</span><span class="sxs-lookup"><span data-stu-id="f2284-147">Namespaces, exceptions, events, and project/`.dll` names should also use PascalCase.</span></span> <span data-ttu-id="f2284-148">Non solo si apporta consumo da parte di altri linguaggi .NET sentirsi più naturale per i consumer, è anche coerenza con le convenzioni di denominazione di .NET, è possibile che si verifichi.</span><span class="sxs-lookup"><span data-stu-id="f2284-148">Not only does this make consumption from other .NET languages feel more natural to consumers, it's also consistent with .NET naming conventions that you are likely to encounter.</span></span>

### <a name="avoid-underscores-in-names"></a><span data-ttu-id="f2284-149">Evitare di caratteri di sottolineatura nei nomi</span><span class="sxs-lookup"><span data-stu-id="f2284-149">Avoid underscores in names</span></span>

<span data-ttu-id="f2284-150">In passato, alcune librerie F # Usa caratteri di sottolineatura nei nomi.</span><span class="sxs-lookup"><span data-stu-id="f2284-150">Historically, some F# libraries have used underscores in names.</span></span> <span data-ttu-id="f2284-151">Tuttavia, ciò è non è più diffuso, in parte perché è in conflitto con le convenzioni di denominazione .NET.</span><span class="sxs-lookup"><span data-stu-id="f2284-151">However, this is no longer widely accepted, partly because it clashes with .NET naming conventions.</span></span> <span data-ttu-id="f2284-152">Ciò premesso, alcuni programmatori F # usare caratteri di sottolineatura molto frequentemente, in parte per motivi cronologici e tolleranza e riguardo è importante.</span><span class="sxs-lookup"><span data-stu-id="f2284-152">That said, some F# programmers use underscores heavily, partly for historical reasons, and tolerance and respect is important.</span></span> <span data-ttu-id="f2284-153">Tuttavia, tenere presente che lo stile è spesso disliked da altri utenti che dispongono di una scelta sulla possibilità di utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="f2284-153">However, be aware that the style is often disliked by others who have a choice about whether to use it.</span></span>

<span data-ttu-id="f2284-154">Alcune eccezioni includono l'interazione con componenti nativi, in cui i caratteri di sottolineatura sono molto comuni.</span><span class="sxs-lookup"><span data-stu-id="f2284-154">Some exceptions includes interoperating with native components, where underscores are very common.</span></span>

### <a name="use-standard-f-operators"></a><span data-ttu-id="f2284-155">Utilizzare gli operatori standard F #</span><span class="sxs-lookup"><span data-stu-id="f2284-155">Use standard F# operators</span></span>

<span data-ttu-id="f2284-156">Gli operatori seguenti vengono definiti nella libreria standard di F # e devono essere usati in sostituzione definizione equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f2284-156">The following operators are defined in the F# standard library and should be used instead of defining equivalents.</span></span> <span data-ttu-id="f2284-157">Come tende a rendere il codice più leggibile e idiomatica, è consigliabile usare questi operatori.</span><span class="sxs-lookup"><span data-stu-id="f2284-157">Using these operators is recommended as it tends to make code more readable and idiomatic.</span></span> <span data-ttu-id="f2284-158">Gli sviluppatori con uno sfondo in OCaml o altri linguaggi di programmazione funzionale potrebbero essere familiarità con linguaggi diversi.</span><span class="sxs-lookup"><span data-stu-id="f2284-158">Developers with a background in OCaml or other functional programming language may be accustomed to different idioms.</span></span> <span data-ttu-id="f2284-159">Nell'elenco seguente sono riepilogati gli operatori F # consigliati.</span><span class="sxs-lookup"><span data-stu-id="f2284-159">The following list summarizes the recommended F# operators.</span></span>

```fsharp
x |> f // Forward pipeline
f >> g // Forward composition
x |> ignore // Discard away a value
x + y // Overloaded addition (including string concatenation)
x - y // Overloaded subtraction
x * y // Overloaded multiplication
x / y // Overloaded division
x % y // Overloaded modulus
x && y // Lazy/short-cut "and"
x || y // Lazy/short-cut "or"
x <<< y // Bitwise left shift
x >>> y // Bitwise right shift
x ||| y // Bitwise or, also for working with “flags” enumeration
x &&& y // Bitwise and, also for working with “flags” enumeration
x ^^^ y // Bitwise xor, also for working with “flags” enumeration
```

### <a name="use-prefix-syntax-for-generics-foot-in-preference-to-postfix-syntax-t-foo"></a><span data-ttu-id="f2284-160">Utilizzare la sintassi di prefisso per i generics (`Foo<T>`) anziché la sintassi di forma suffissa (`T Foo`)</span><span class="sxs-lookup"><span data-stu-id="f2284-160">Use prefix syntax for generics (`Foo<T>`) in preference to postfix syntax (`T Foo`)</span></span>

<span data-ttu-id="f2284-161">F # eredita sia lo stile di ML suffisso di denominazione dei tipi generici (ad esempio `int list`), nonché il prefisso stile .NET (ad esempio, `list<int>`).</span><span class="sxs-lookup"><span data-stu-id="f2284-161">F# inherits both the postfix ML style of naming generic types (for example, `int list`) as well as the prefix .NET style (for example, `list<int>`).</span></span> <span data-ttu-id="f2284-162">Preferisce lo stile di .NET, ad eccezione di quattro tipi specifici:</span><span class="sxs-lookup"><span data-stu-id="f2284-162">Prefer the .NET style, except for four specific types:</span></span>

1. <span data-ttu-id="f2284-163">Per F # sono elencate, utilizzare il form della forma suffissa: `int list` anziché `list<int>`.</span><span class="sxs-lookup"><span data-stu-id="f2284-163">For F# Lists, use the postfix form: `int list` rather than `list<int>`.</span></span>
2. <span data-ttu-id="f2284-164">Per le opzioni di F #, utilizzare il form della forma suffissa: `int option` anziché `option<int>`.</span><span class="sxs-lookup"><span data-stu-id="f2284-164">For F# Options, use the postfix form: `int option` rather than `option<int>`.</span></span>
3. <span data-ttu-id="f2284-165">Per le matrici di F #, utilizzare il nome sintattico `int[]` anziché `int array` o `array<int>`.</span><span class="sxs-lookup"><span data-stu-id="f2284-165">For F# arrays, use the syntactic name `int[]` rather than `int array` or `array<int>`.</span></span>
4. <span data-ttu-id="f2284-166">Per le celle di riferimento, utilizzare `int ref` anziché `ref<int>` o `Ref<int>`.</span><span class="sxs-lookup"><span data-stu-id="f2284-166">For Reference Cells, use `int ref` rather than `ref<int>` or `Ref<int>`.</span></span>

<span data-ttu-id="f2284-167">Per tutti gli altri tipi, utilizzare la forma prefissa.</span><span class="sxs-lookup"><span data-stu-id="f2284-167">For all other types, use the prefix form.</span></span>

## <a name="formatting-discriminated-union-declarations"></a><span data-ttu-id="f2284-168">Formattazione di dichiarazioni di unione discriminata</span><span class="sxs-lookup"><span data-stu-id="f2284-168">Formatting discriminated union declarations</span></span>

<span data-ttu-id="f2284-169">Impostare un rientro `|` nella definizione del tipo da 4 spazi:</span><span class="sxs-lookup"><span data-stu-id="f2284-169">Indent `|` in type definition by 4 spaces:</span></span>

```fsharp
// OK
type Volume =
    | Liter of float
    | FluidOunce of float
    | ImperialPint of float

// Not OK
type Volume =
| Liter of float
| USPint of float
| ImperialPint of float
```

<span data-ttu-id="f2284-170">Le unioni discriminate istanziato divisi su più righe prestare dati in essi contenuti un nuovo ambito con rientro:</span><span class="sxs-lookup"><span data-stu-id="f2284-170">Instantiated Discriminated Unions that split across multiple lines should give contained data a new scope with indentation:</span></span>

```fsharp
let tree1 =
    BinaryNode
        (BinaryNode(BinaryValue 1, BinaryValue 2),
         BinaryNode(BinaryValue 3, BinaryValue 4))
```

<span data-ttu-id="f2284-171">La parentesi di chiusura può inoltre trovarsi in una nuova riga:</span><span class="sxs-lookup"><span data-stu-id="f2284-171">The closing parenthesis can also be on a new line:</span></span>

```fsharp
let tree1 =
    BinaryNode(
        BinaryNode(BinaryValue 1, BinaryValue 2),
        BinaryNode(BinaryValue 3, BinaryValue 4)
    )
```

## <a name="formatting-tuples"></a><span data-ttu-id="f2284-172">Formattazione Tuple</span><span class="sxs-lookup"><span data-stu-id="f2284-172">Formatting tuples</span></span>

<span data-ttu-id="f2284-173">Creazione di un'istanza di tupla deve essere racchiuso tra parentesi e delimitati da virgole all'interno devono essere seguite da uno spazio singolo, ad esempio: `(1, 2)`, `(x, y, z)`.</span><span class="sxs-lookup"><span data-stu-id="f2284-173">A tuple instantiation should be parenthesized, and the delimiting commas within should be followed by a single space, for example: `(1, 2)`, `(x, y, z)`.</span></span>

<span data-ttu-id="f2284-174">È un'eccezione comunemente accettata per omettere le parentesi nei criteri di ricerca di tuple:</span><span class="sxs-lookup"><span data-stu-id="f2284-174">A commonly accepted exception is to omit parentheses in pattern matching of tuples:</span></span>

```fsharp
let (x, y) = z // Destructuring

match x, y with
| 1, _ -> 0
| x, 1 -> 0
| x, y -> 1
```

## <a name="formatting-records"></a><span data-ttu-id="f2284-175">Formattazione di record</span><span class="sxs-lookup"><span data-stu-id="f2284-175">Formatting records</span></span>

<span data-ttu-id="f2284-176">Breve record possono essere scritti in una riga:</span><span class="sxs-lookup"><span data-stu-id="f2284-176">Short records can be written in one line:</span></span>

```fsharp
let point = { X = 1.0; Y = 0.0 }
```

<span data-ttu-id="f2284-177">I record che sono più devono utilizzare le nuove righe per le etichette:</span><span class="sxs-lookup"><span data-stu-id="f2284-177">Records that are longer should use new lines for labels:</span></span>

```fsharp
let rainbow =
    { Boss = "Jeffrey"
      Lackeys = ["Zippy"; "George"; "Bungle"] }
```

<span data-ttu-id="f2284-178">Inserire il token di apertura nella stessa riga e il token di chiusura in una nuova riga è inoltre:</span><span class="sxs-lookup"><span data-stu-id="f2284-178">Placing the opening token on the same line and the closing token on a new line is also fine:</span></span>

```fsharp
let rainbow = {
    Boss1 = "Jeffrey"
    Boss2 = "Jeffrey"
    Boss3 = "Jeffrey"
    Boss4 = "Jeffrey"
    Boss5 = "Jeffrey"
    Boss6 = "Jeffrey"
    Boss7 = "Jeffrey"
    Boss8 = "Jeffrey"
    Lackeys = ["Zippy"; "George"; "Bungle"]
}
```

<span data-ttu-id="f2284-179">Le stesse regole valide per gli elementi di elenco e matrice.</span><span class="sxs-lookup"><span data-stu-id="f2284-179">The same rules apply for list and array elements.</span></span>

## <a name="formatting-lists-and-arrays"></a><span data-ttu-id="f2284-180">Formattazione di elenchi e matrici</span><span class="sxs-lookup"><span data-stu-id="f2284-180">Formatting lists and arrays</span></span>

<span data-ttu-id="f2284-181">Scrivere `x :: l` con spazi prima e dopo il `::` operatore (`::` è un operatore infisso, pertanto delimitato da spazi) e `[1; 2; 3]` (`;` è un delimitatore, pertanto seguito da uno spazio).</span><span class="sxs-lookup"><span data-stu-id="f2284-181">Write `x :: l` with spaces around the `::` operator (`::` is an infix operator, hence surrounded by spaces) and `[1; 2; 3]` (`;` is a delimiter, hence followed by a space).</span></span>

<span data-ttu-id="f2284-182">Utilizzare sempre almeno uno spazio tra due operatori simile a parentesi graffa distinti.</span><span class="sxs-lookup"><span data-stu-id="f2284-182">Always use at least one space between two distinct brace-like operators.</span></span> <span data-ttu-id="f2284-183">Ad esempio, lasciare uno spazio tra un `[` e un `{`.</span><span class="sxs-lookup"><span data-stu-id="f2284-183">For example, leave a space between a `[` and a `{`.</span></span>

```fsharp
// OK
[ { IngredientName = "Green beans"; Quantity = 250 }
  { IngredientName = "Pine nuts"; Quantity = 250 }
  { IngredientName = "Feta cheese"; Quantity = 250 }
  { IngredientName = "Olive oil"; Quantity = 10 }
  { IngredientName = "Lemon"; Quantity = 1 } ]

// Not OK
[{ IngredientName = "Green beans"; Quantity = 250 }
 { IngredientName = "Pine nuts"; Quantity = 250 }
 { IngredientName = "Feta cheese"; Quantity = 250 }
 { IngredientName = "Olive oil"; Quantity = 10 }
 { IngredientName = "Lemon"; Quantity = 1 }]
```

<span data-ttu-id="f2284-184">Gli elenchi e matrici divisi su più righe seguono una regola simile dei record:</span><span class="sxs-lookup"><span data-stu-id="f2284-184">Lists and arrays that split across multiple lines follow a similar rule as records do:</span></span>

```fsharp
let pascalsTriangle = [|
    [|1|]
    [|1; 1|]
    [|1; 2; 1|]
    [|1; 3; 3; 1|]
    [|1; 4; 6; 4; 1|]
    [|1; 5; 10; 10; 5; 1|]
    [|1; 6; 15; 20; 15; 6; 1|]
    [|1; 7; 21; 35; 35; 21; 7; 1|]
    [|1; 8; 28; 56; 70; 56; 28; 8; 1|]
|]
```

## <a name="formatting-if-expressions"></a><span data-ttu-id="f2284-185">Formattazione se le espressioni</span><span class="sxs-lookup"><span data-stu-id="f2284-185">Formatting if expressions</span></span>

<span data-ttu-id="f2284-186">Il rientro di istruzioni condizionali dipende le dimensioni delle espressioni che li compongono.</span><span class="sxs-lookup"><span data-stu-id="f2284-186">Indentation of conditionals depends on the sizes of the expressions that make them up.</span></span> <span data-ttu-id="f2284-187">Se `cond`, `e1` e `e2` piccole, semplicemente scriverli su un'unica riga:</span><span class="sxs-lookup"><span data-stu-id="f2284-187">If `cond`, `e1` and `e2` are small, simply write them on one line:</span></span>

```fsharp
if cond then e1 else e2
```

<span data-ttu-id="f2284-188">Se `e1` e `cond` sono di dimensioni ridotte, ma `e2` è di grandi dimensioni:</span><span class="sxs-lookup"><span data-stu-id="f2284-188">If `e1` and `cond` are small, but `e2` is large:</span></span>

```fsharp
if cond then e1
else
    e2
```

<span data-ttu-id="f2284-189">Se `e1` e `cond` sono di grandi dimensioni e `e2` è piccolo:</span><span class="sxs-lookup"><span data-stu-id="f2284-189">If `e1` and `cond` are large and `e2` is small:</span></span>

```fsharp
if cond then
    e1
else e2
```

<span data-ttu-id="f2284-190">Se tutte le espressioni sono di grandi dimensioni:</span><span class="sxs-lookup"><span data-stu-id="f2284-190">If all the expressions are large:</span></span>

```fsharp
if cond then
    e1
else
    e2
```

<span data-ttu-id="f2284-191">Più istruzioni condizionali, con `elif` e `else` vengono rientrate nello stesso ambito come il `if`:</span><span class="sxs-lookup"><span data-stu-id="f2284-191">Multiple conditionals with `elif` and `else` are indented at the same scope as the `if`:</span></span>

```fsharp
if cond1 then e1
elif cond2 then e2
elif cond3 then e3
else e4
```

### <a name="pattern-matching-constructs"></a><span data-ttu-id="f2284-192">Costrutti di criterio corrispondenti</span><span class="sxs-lookup"><span data-stu-id="f2284-192">Pattern matching constructs</span></span>

<span data-ttu-id="f2284-193">Utilizzare un `|` per ogni clausola di una corrispondenza con alcun rientro.</span><span class="sxs-lookup"><span data-stu-id="f2284-193">Use a `|` for each clause of a match with no indentation.</span></span> <span data-ttu-id="f2284-194">Se l'espressione è breve, è possibile utilizzare una singola riga se ogni sottoespressione anche è semplice.</span><span class="sxs-lookup"><span data-stu-id="f2284-194">If the expression is short, you can consider using a single line if each subexpression is also simple.</span></span>

```fsharp
// OK
match l with
| { him = x; her = "Posh" } :: tail -> _
| _ :: tail -> findDavid tail
| [] -> failwith "Couldn't find David"

// Not OK
match l with
    | { him = x; her = "Posh" } :: tail -> _
    | _ :: tail -> findDavid tail
    | [] -> failwith "Couldn't find David"
```

<span data-ttu-id="f2284-195">Se l'espressione a destra del criteri di ricerca freccia è troppo grande, spostarla nella seguente riga, rientrato un unico passaggio dal `match` / `|`.</span><span class="sxs-lookup"><span data-stu-id="f2284-195">If the expression on the right of the pattern matching arrow is too large, move it to the following line, indented one step from the `match`/`|`.</span></span>

```fsharp
match lam with
| Var v -> 1
| Abs(x, body) ->
    1 + sizeLambda body
| App(lam1, lam2) ->
    sizeLambda lam1 + sizeLambda lam2

```

<span data-ttu-id="f2284-196">Criteri di corrispondenza di funzioni anonime, a partire da `function`, devono in genere non impostare un rientro troppo lontano.</span><span class="sxs-lookup"><span data-stu-id="f2284-196">Pattern matching of anonymous functions, starting by `function`, should generally not indent too far.</span></span> <span data-ttu-id="f2284-197">Ad esempio, è correttamente i rientri di un ambito come segue:</span><span class="sxs-lookup"><span data-stu-id="f2284-197">For example, indenting one scope as follows is fine:</span></span>

```fsharp
lambdaList
|> List.map (function
    | Abs(x, body) -> 1 + sizeLambda 0 body
    | App(lam1, lam2) -> sizeLambda (sizeLambda 0 lam1) lam2
    | Var v -> 1)
```

<span data-ttu-id="f2284-198">Criteri di ricerca nelle funzioni definite dal `let` oppure `let rec` deve essere rientrati 4 spazi dopo l'avvio di `let`, anche se `function` parola chiave viene utilizzata:</span><span class="sxs-lookup"><span data-stu-id="f2284-198">Pattern matching in functions defined by `let` or `let rec` should be indented 4 spaces after starting of `let`, even if `function` keyword is used:</span></span>

```fsharp
let rec sizeLambda acc = function
    | Abs(x, body) -> sizeLambda (succ acc) body
    | App(lam1, lam2) -> sizeLambda (sizeLambda acc lam1) lam2
    | Var v -> succ acc
```

<span data-ttu-id="f2284-199">Non è consigliabile allineamento frecce.</span><span class="sxs-lookup"><span data-stu-id="f2284-199">We do not recommend aligning arrows.</span></span>

## <a name="formatting-trywith-expressions"></a><span data-ttu-id="f2284-200">Formattazione try / with espressioni</span><span class="sxs-lookup"><span data-stu-id="f2284-200">Formatting try/with expressions</span></span>

<span data-ttu-id="f2284-201">Criteri di ricerca nel tipo di eccezione devono essere rientrato allo stesso livello `with`.</span><span class="sxs-lookup"><span data-stu-id="f2284-201">Pattern matching on the exception type should be indented at the same level as `with`.</span></span>

```fsharp
try
    if System.DateTime.Now.Second % 3 = 0 then
        raise (new System.Exception())
    else
        raise (new System.ApplicationException())
with
| :? System.ApplicationException ->
    printfn "A second that was not a multiple of 3"
| _ ->
    printfn "A second that was a multiple of 3"
```

## <a name="formatting-function-parameter-application"></a><span data-ttu-id="f2284-202">Formattazione dell'applicazione di parametri di funzione</span><span class="sxs-lookup"><span data-stu-id="f2284-202">Formatting function parameter application</span></span>

<span data-ttu-id="f2284-203">In generale, la maggior parte delle applicazione di parametri di funzione viene eseguita nella stessa riga.</span><span class="sxs-lookup"><span data-stu-id="f2284-203">In general, most function parameter application is done on the same line.</span></span>

<span data-ttu-id="f2284-204">Se si desidera applicare parametri a una funzione in una nuova riga, impostare un rientro per un ambito.</span><span class="sxs-lookup"><span data-stu-id="f2284-204">If you wish to apply parameters to a function on a new line, indent them by one scope.</span></span>

```fsharp
// OK
sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
sprintf
     "\t%s - %i\n\r"
     x.IngredientName x.Quantity

// OK
let printVolumes x =
    printf "Volume in liters = %f, in us pints = %f, in imperial = %f"
        (convertVolumeToLiter x)
        (convertVolumeUSPint x)
        (convertVolumeImperialPint x)
```

<span data-ttu-id="f2284-205">Applicano le stesse linee guida per le espressioni lambda come argomenti della funzione.</span><span class="sxs-lookup"><span data-stu-id="f2284-205">The same guidelines apply for lambda expressions as function arguments.</span></span> <span data-ttu-id="f2284-206">Se il corpo di un'espressione lambda, il corpo può essere un'altra riga, rientrata in base a un ambito</span><span class="sxs-lookup"><span data-stu-id="f2284-206">If the body of a lambda expression, the body can have another line, indented by one scope</span></span>

```fsharp
let printListWithOffset a list1 =
    List.iter
        (fun elem -> printfn "%d" (a + elem))
        list1

// OK if lambda body is long enough
let printListWithOffset a list1 =
    List.iter
        (fun elem ->
            printfn "%d" (a + elem))
        list1
```

<span data-ttu-id="f2284-207">Tuttavia, se il corpo di un'espressione lambda su più righe, provare a impostarlo come eseguire il factoring in funzioni separate anziché avere un costrutto multilinea applicato a una funzione come argomento singolo.</span><span class="sxs-lookup"><span data-stu-id="f2284-207">However, if the body of a lambda expression is more than one line, consider factoring it out into a separate function rather than have a multi-line construct applied as a single argument to a function.</span></span>

### <a name="formatting-infix-operators"></a><span data-ttu-id="f2284-208">Gli operatori infissi di formattazione</span><span class="sxs-lookup"><span data-stu-id="f2284-208">Formatting infix operators</span></span>

<span data-ttu-id="f2284-209">Operatori separati da spazi.</span><span class="sxs-lookup"><span data-stu-id="f2284-209">Separate operators by spaces.</span></span> <span data-ttu-id="f2284-210">Ovvie eccezioni a questa regola sono il `!` e `.` operatori.</span><span class="sxs-lookup"><span data-stu-id="f2284-210">Obvious exceptions to this rule are the `!` and `.` operators.</span></span>

<span data-ttu-id="f2284-211">Le espressioni di infissi sono OK per l'elemento lineup nella stessa colonna:</span><span class="sxs-lookup"><span data-stu-id="f2284-211">Infix expressions are OK to lineup on same column:</span></span>

```fsharp
acc +
(sprintf "\t%s - %i\n\r"
     x.IngredientName x.Quantity)

let function1 arg1 arg2 arg3 arg4 =
    arg1 + arg2 +
    arg3 + arg4
```

### <a name="formatting-pipeline-operators"></a><span data-ttu-id="f2284-212">Formattazione operatori pipeline</span><span class="sxs-lookup"><span data-stu-id="f2284-212">Formatting pipeline operators</span></span>

<span data-ttu-id="f2284-213">Pipeline `|>` operatori va sotto le espressioni cui operare.</span><span class="sxs-lookup"><span data-stu-id="f2284-213">Pipeline `|>` operators should go underneath the expressions they operate on.</span></span>

```fsharp
// Preferred approach
let methods2 =
    System.AppDomain.CurrentDomain.GetAssemblies()
    |> List.ofArray
    |> List.map (fun assm -> assm.GetTypes())
    |> Array.concat
    |> List.ofArray
    |> List.map (fun t -> t.GetMethods())
    |> Array.concat

// Not OK
let methods2 = System.AppDomain.CurrentDomain.GetAssemblies()
            |> List.ofArray
            |> List.map (fun assm -> assm.GetTypes())
            |> Array.concat
            |> List.ofArray
            |> List.map (fun t -> t.GetMethods())
            |> Array.concat
```

### <a name="formatting-modules"></a><span data-ttu-id="f2284-214">Formattazione di moduli</span><span class="sxs-lookup"><span data-stu-id="f2284-214">Formatting modules</span></span>

<span data-ttu-id="f2284-215">Il codice in un modulo locale deve essere rientrato rispetto al modulo, ma il codice in un modulo di livello superiore non deve essere rientrato.</span><span class="sxs-lookup"><span data-stu-id="f2284-215">Code in a local module must be indented relative to the module, but code in a top-level module should not be indented.</span></span> <span data-ttu-id="f2284-216">Elementi Namespace non è necessario impostare un rientro.</span><span class="sxs-lookup"><span data-stu-id="f2284-216">Namespace elements do not have to be indented.</span></span>

```fsharp
// A is a top-level module.
module A

let function1 a b = a - b * b
```

```fsharp
// A1 and A2 are local modules.
module A1 =
    let function1 a b = a*a + b*b

module A2 =
    let function2 a b = a*a - b*b
```

### <a name="formatting-object-expressions-and-interfaces"></a><span data-ttu-id="f2284-217">Formattazione di espressioni di oggetto e le interfacce</span><span class="sxs-lookup"><span data-stu-id="f2284-217">Formatting object expressions and interfaces</span></span>

<span data-ttu-id="f2284-218">Espressioni di oggetto e le interfacce devono essere allineate in modo analogo alle `member` viene aumentato il rientro dopo 4 spazi.</span><span class="sxs-lookup"><span data-stu-id="f2284-218">Object expressions and interfaces should be aligned in the same way with `member` being indented after 4 spaces.</span></span>

```fsharp
let comparer =
    { new IComparer<string> with
          member x.Compare(s1, s2) =
              let rev (s : String) =
                  new String (Array.rev (s.ToCharArray()))
              let reversed = rev s1
              reversed.CompareTo (rev s2) }
```

### <a name="formatting-whitespace-in-expressions"></a><span data-ttu-id="f2284-219">Gli spazi vuoti nelle espressioni di formattazione</span><span class="sxs-lookup"><span data-stu-id="f2284-219">Formatting whitespace in expressions</span></span>

<span data-ttu-id="f2284-220">Evitare gli spazi vuoti estranei nelle espressioni F #.</span><span class="sxs-lookup"><span data-stu-id="f2284-220">Avoid extraneous whitespace in F# expressions.</span></span>

```fsharp
// OK
spam (ham.[1])

// Not OK
spam ( ham.[ 1 ] )
```

<span data-ttu-id="f2284-221">Argomenti denominati anche senza spazio che circonda il `=`:</span><span class="sxs-lookup"><span data-stu-id="f2284-221">Named arguments should also not have space surrounding the `=`:</span></span>

```fsharp
// OK
let makeStreamReader x = new System.IO.StreamReader(path=x)

// Not OK
let makeStreamReader x = new System.IO.StreamReader(path = x)
```
