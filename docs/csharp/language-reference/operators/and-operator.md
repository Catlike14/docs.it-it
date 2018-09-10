---
title: Operatore &amp; (Riferimenti per C#)
ms.date: 04/04/2018
f1_keywords:
- '&_CSharpKeyword'
helpviewer_keywords:
- bitwise AND operator [C#]
- ampersand operator (&) [C#]
- '& operator [C#]'
- AND operator (&) [C#]
ms.assetid: afa346d5-90ec-4b1f-a2c8-3881f018741d
ms.openlocfilehash: b257c7d41618464e26ab3b54bcfb1f1e2c2e420e
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2018
ms.locfileid: "43467374"
---
# <a name="amp-operator-c-reference"></a><span data-ttu-id="1c9ff-102">Operatore &amp; (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="1c9ff-102">&amp; Operator (C# Reference)</span></span>
<span data-ttu-id="1c9ff-103">L'operatore `&` ha la funzione di operatore unario o binario.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-103">The `&` operator can function as either a unary or a binary operator.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1c9ff-104">Note</span><span class="sxs-lookup"><span data-stu-id="1c9ff-104">Remarks</span></span>  
 <span data-ttu-id="1c9ff-105">L'operatore unario `&` restituisce l'indirizzo del relativo operando (richiede il contesto [unsafe](../../../csharp/language-reference/keywords/unsafe.md)).</span><span class="sxs-lookup"><span data-stu-id="1c9ff-105">The unary `&` operator returns the address of its operand (requires [unsafe](../../../csharp/language-reference/keywords/unsafe.md) context).</span></span>  
  
 <span data-ttu-id="1c9ff-106">Gli operatori `&` binari sono predefiniti per i tipi integrali e `bool`.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-106">Binary `&` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="1c9ff-107">Per i tipi integrali, & calcola l'operatore AND logico bit per bit dei relativi operandi.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-107">For integral types, & computes the logical bitwise AND of its operands.</span></span> <span data-ttu-id="1c9ff-108">Per gli operandi `bool`, & calcola l'operatore AND logico dei relativi operandi, ovvero, il risultato è `true` se e solo se entrambi gli operandi sono `true`.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-108">For `bool` operands, & computes the logical AND of its operands; that is, the result is `true` if and only if both its operands are `true`.</span></span>  
  
 <span data-ttu-id="1c9ff-109">L'operatore binario `&` valuta i due operatori indipendentemente dal valore del primo, diversamente dall'[operatore AND condizionale](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-109">The binary `&` operator evaluates both operands regardless of the first one's value, in contrast to the [conditional AND operator](../../../csharp/language-reference/operators/conditional-and-operator.md) `&&`.</span></span> <span data-ttu-id="1c9ff-110">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="1c9ff-110">For example:</span></span>  
  
 [!code-csharp[csRefOperators#37](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_1.cs)]  
  
 <span data-ttu-id="1c9ff-111">I tipi definiti dall'utente possono eseguire l'overload dell'operatore `&` (vedere [operator](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="1c9ff-111">User-defined types can overload the binary `&` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="1c9ff-112">Le operazioni sui tipi integrali sono generalmente consentite sull'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-112">Operations on integral types are generally allowed on enumeration.</span></span> <span data-ttu-id="1c9ff-113">Quando viene eseguito l'overload di un operatore binario, viene anche eseguito in modo implicito l'overload dell'operatore di assegnazione corrispondente, se presente.</span><span class="sxs-lookup"><span data-stu-id="1c9ff-113">When a binary operator is overloaded, the corresponding assignment operator, if any, is also implicitly overloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1c9ff-114">Esempio</span><span class="sxs-lookup"><span data-stu-id="1c9ff-114">Example</span></span>  
 [!code-csharp[csRefOperators#38](../../../csharp/language-reference/operators/codesnippet/CSharp/and-operator_2.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="1c9ff-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1c9ff-115">See Also</span></span>

- [<span data-ttu-id="1c9ff-116">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="1c9ff-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="1c9ff-117">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="1c9ff-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="1c9ff-118">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="1c9ff-118">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
