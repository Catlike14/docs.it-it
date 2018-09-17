---
title: Tipi di riferimento (Riferimenti per C#)
ms.date: 07/20/2015
f1_keywords:
- cs.referencetypes
helpviewer_keywords:
- reference types [C#]
- C# language, reference types
- types [C#], reference types
ms.assetid: 801cf030-6e2d-4a0d-9daf-1431b0c31f47
ms.openlocfilehash: f99415fc9a2b728917cdf829ffb9e25823a824dd
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2018
ms.locfileid: "45609554"
---
# <a name="reference-types-c-reference"></a><span data-ttu-id="b3a57-102">Tipi di riferimento (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="b3a57-102">Reference types (C# Reference)</span></span>

<span data-ttu-id="b3a57-103">Esistono due generi di tipo in C#: tipi di riferimento e tipi di valore.</span><span class="sxs-lookup"><span data-stu-id="b3a57-103">There are two kinds of types in C#: reference types and value types.</span></span> <span data-ttu-id="b3a57-104">Le variabili dei tipi di riferimento archiviano i riferimenti ai relativi dati (oggetti), mentre le variabili dei tipi di valore contengono direttamente i dati.</span><span class="sxs-lookup"><span data-stu-id="b3a57-104">Variables of reference types store references to their data (objects), while variables of value types directly contain their data.</span></span> <span data-ttu-id="b3a57-105">Con i tipi di riferimento, due variabili possono fare riferimento allo stesso oggetto. Di conseguenza le operazioni su una variabile possono influire sull'oggetto a cui fa riferimento l'altra variabile.</span><span class="sxs-lookup"><span data-stu-id="b3a57-105">With reference types, two variables can reference the same object; therefore, operations on one variable can affect the object referenced by the other variable.</span></span> <span data-ttu-id="b3a57-106">Con i tipi valore, ogni variabile ha una propria copia dei dati e non è possibile che le operazioni su una variabile influiscano sull'altra (tranne nel caso delle variabili dei parametri in, ref e out, vedere Modificatore del parametro [in](in-parameter-modifier.md), [ref](ref.md) e [out](out-parameter-modifier.md)).</span><span class="sxs-lookup"><span data-stu-id="b3a57-106">With value types, each variable has its own copy of the data, and it is not possible for operations on one variable to affect the other (except in the case of in, ref and out parameter variables; see [in](in-parameter-modifier.md), [ref](ref.md) and [out](out-parameter-modifier.md) parameter modifier).</span></span>

 <span data-ttu-id="b3a57-107">Le seguenti parole chiave vengono utilizzate per dichiarare i tipi di riferimento:</span><span class="sxs-lookup"><span data-stu-id="b3a57-107">The following keywords are used to declare reference types:</span></span>

- [<span data-ttu-id="b3a57-108">class</span><span class="sxs-lookup"><span data-stu-id="b3a57-108">class</span></span>](class.md)

- [<span data-ttu-id="b3a57-109">interface</span><span class="sxs-lookup"><span data-stu-id="b3a57-109">interface</span></span>](interface.md)

- [<span data-ttu-id="b3a57-110">delegate</span><span class="sxs-lookup"><span data-stu-id="b3a57-110">delegate</span></span>](delegate.md)

 <span data-ttu-id="b3a57-111">In c# sono disponibili i seguenti tipi di riferimento predefiniti:</span><span class="sxs-lookup"><span data-stu-id="b3a57-111">C# also provides the following built-in reference types:</span></span>

- [<span data-ttu-id="b3a57-112">dynamic</span><span class="sxs-lookup"><span data-stu-id="b3a57-112">dynamic</span></span>](dynamic.md)

- [<span data-ttu-id="b3a57-113">object</span><span class="sxs-lookup"><span data-stu-id="b3a57-113">object</span></span>](object.md)

- [<span data-ttu-id="b3a57-114">string</span><span class="sxs-lookup"><span data-stu-id="b3a57-114">string</span></span>](string.md)

## <a name="see-also"></a><span data-ttu-id="b3a57-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b3a57-115">See also</span></span>

- [<span data-ttu-id="b3a57-116">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="b3a57-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="b3a57-117">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="b3a57-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="b3a57-118">Parole chiave di C#</span><span class="sxs-lookup"><span data-stu-id="b3a57-118">C# Keywords</span></span>](index.md)
- [<span data-ttu-id="b3a57-119">Tipi</span><span class="sxs-lookup"><span data-stu-id="b3a57-119">Types</span></span>](types.md)
- [<span data-ttu-id="b3a57-120">Tipi valore</span><span class="sxs-lookup"><span data-stu-id="b3a57-120">Value Types</span></span>](value-types.md)