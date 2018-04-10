---
title: Operatore ^ (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ^_CSharpKeyword
helpviewer_keywords:
- ^ operator [C#]
- bitwise exclusive OR operator [C#]
ms.assetid: b09bc815-570f-4db6-a637-5b4ed99d014a
caps.latest.revision: 19
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 4ccd32ea8abd8ca3252380083eafecad2b572ed7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="-operator-c-reference"></a><span data-ttu-id="55e3a-102">Operatore ^ (Riferimenti per C#)</span><span class="sxs-lookup"><span data-stu-id="55e3a-102">^ Operator (C# Reference)</span></span>
<span data-ttu-id="55e3a-103">Gli operatori `^` binari sono predefiniti per i tipi integrali e `bool`.</span><span class="sxs-lookup"><span data-stu-id="55e3a-103">Binary `^` operators are predefined for the integral types and `bool`.</span></span> <span data-ttu-id="55e3a-104">Per i tipi integrali, `^` calcola l'operazione di OR esclusivo bit per bit dei relativi operandi.</span><span class="sxs-lookup"><span data-stu-id="55e3a-104">For integral types, `^` computes the bitwise exclusive-OR of its operands.</span></span> <span data-ttu-id="55e3a-105">Per gli operandi `bool`, `^` calcola l'operazione di OR esclusivo logico dei relativi operandi, ovvero, il risultato è `true` se e solo se esattamente uno degli operandi è `true`.</span><span class="sxs-lookup"><span data-stu-id="55e3a-105">For `bool` operands, `^` computes the logical exclusive-or of its operands; that is, the result is `true` if and only if exactly one of its operands is `true`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="55e3a-106">Note</span><span class="sxs-lookup"><span data-stu-id="55e3a-106">Remarks</span></span>  
 <span data-ttu-id="55e3a-107">I tipi definiti dall'utente possono eseguire l'overload dell'operatore `^` (vedere [operatore](../../../csharp/language-reference/keywords/operator.md)).</span><span class="sxs-lookup"><span data-stu-id="55e3a-107">User-defined types can overload the `^` operator (see [operator](../../../csharp/language-reference/keywords/operator.md)).</span></span> <span data-ttu-id="55e3a-108">Le operazioni sui tipi integrali sono generalmente consentite sull'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="55e3a-108">Operations on integral types are generally allowed on enumeration.</span></span>  
  
## <a name="example"></a><span data-ttu-id="55e3a-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="55e3a-109">Example</span></span>  
 [!code-csharp[csRefOperators#30](../../../csharp/language-reference/operators/codesnippet/CSharp/xor-operator_1.cs)]  
  
 <span data-ttu-id="55e3a-110">Il calcolo di `0xf8 ^ 0x3f` nell'esempio precedente esegue un'operazione di OR esclusivo bit per bit dei due valori binari seguenti, che corrispondono ai valori esadecimali F8 e 3F:</span><span class="sxs-lookup"><span data-stu-id="55e3a-110">The computation of `0xf8 ^ 0x3f` in the previous example performs a bitwise exclusive-OR of the following two binary values, which correspond to the hexadecimal values F8 and 3F:</span></span>  
  
 `1111 1000`  
  
 `0011 1111`  
  
 <span data-ttu-id="55e3a-111">Il risultato dell'operazione di OR esclusivo è `1100 0111`, ovvero C7 in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="55e3a-111">The result of the exclusive-OR is `1100 0111`, which is C7 in hexadecimal.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="55e3a-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="55e3a-112">See Also</span></span>  
 [<span data-ttu-id="55e3a-113">Riferimenti per C#</span><span class="sxs-lookup"><span data-stu-id="55e3a-113">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
 [<span data-ttu-id="55e3a-114">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="55e3a-114">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="55e3a-115">Operatori C#</span><span class="sxs-lookup"><span data-stu-id="55e3a-115">C# Operators</span></span>](../../../csharp/language-reference/operators/index.md)
