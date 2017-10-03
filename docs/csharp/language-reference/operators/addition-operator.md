---
title: + Operatore (Riferimenti per C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- +_CSharpKeyword
dev_langs:
- CSharp
helpviewer_keywords:
- + operator [C#]
- concatenation operator [C#]
- addition operator [C#]
ms.assetid: 93e56486-bb42-43c1-bd43-60af11e64e67
caps.latest.revision: 19
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
ms.openlocfilehash: 5455375148f1924c7fe1cdb10e7924abb83a1565
ms.contentlocale: it-it
ms.lasthandoff: 09/25/2017

---
# <a name="-operator-c-reference"></a>Operatore + (Riferimenti per C#)
L'operatore `+` ha la funzione di operatore unario o binario.  
  
## <a name="remarks"></a>Note  
 Gli operatori `+` unari sono predefiniti per tutti i tipi numerici. Il risultato di un'operazione `+` unaria su un tipo numerico corrisponde al valore dell'operando.  
  
 Gli operatori `+` binari sono predefiniti per i tipi numerici e stringa. Per i tipi numerici, + calcola la somma dei due operandi. Quando uno o entrambi gli operandi sono di tipo stringa, + concatena le rappresentazioni di stringa degli operandi.  
  
 I tipi delegati offrono anche un operatore `+` binario, che esegue la concatenazione dei delegati.  
  
 I tipi definiti dall'utente possono eseguire l'overload degli operatori `+` unari e `+` binari. Le operazioni sui tipi integrali sono generalmente consentite sull'enumerazione. Per altre informazioni, vedere [operatore (Riferimenti per C#)](../../../csharp/language-reference/keywords/operator.md).  
  
## <a name="example"></a>Esempio  
 [!code-cs[csRefOperators#28](../../../csharp/language-reference/operators/codesnippet/CSharp/addition-operator_1.cs)]  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Operatori di C#](../../../csharp/language-reference/operators/index.md)   
 [operatore (Riferimenti per C#)](../../../csharp/language-reference/keywords/operator.md)

