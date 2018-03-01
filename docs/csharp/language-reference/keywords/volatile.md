---
title: volatile (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- volatile_CSharpKeyword
- volatile
helpviewer_keywords:
- volatile keyword [C#]
ms.assetid: 78089bc7-7b38-4cfd-9e49-87ac036af009
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 1cefa39313c3c551e8d05fbc31e528b86c6888d9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="volatile-c-reference"></a>volatile (Riferimenti per C#)
La parola chiave `volatile` indica che un campo potrebbe essere modificato da più thread eseguiti contemporaneamente. Un campo dichiarato `volatile` non è soggetto a ottimizzazioni del compilatore che presuppongono l'accesso da parte di un singolo thread. Ciò garantisce che il valore più aggiornato sia sempre presente nel campo.  
  
 Il modificatore `volatile` si usa in genere per un campo a cui accedono più thread senza usare l'istruzione [lock](../../../csharp/language-reference/keywords/lock-statement.md) per serializzare l'accesso.  
  
 La parola chiave `volatile` può essere applicata ai campi di questi tipi:  
  
-   Tipi di riferimento.  
  
-   Tipi di puntatore (in un contesto non sicuro). Si noti che sebbene il puntatore in sé possa essere volatile, non può esserlo l'oggetto a cui punta. In altre parole, non è possibile dichiarare un "puntatore a volatile".  
  
-   Tipi come sbyte, byte, short, ushort, int, uint, char, float e bool.  
  
-   Un tipo enum con uno dei seguenti tipi di base: byte, sbyte, short, ushort, int o uint.  
  
-   Parametri di tipo generico noti come tipi di riferimento.  
  
-   <xref:System.IntPtr> e <xref:System.UIntPtr>.  
  
 La parola chiave volatile può essere applicata solo a campi di una classe o struct. Le variabili locali non possono essere dichiarate `volatile`.  
  
## <a name="example"></a>Esempio  
 Nell'esempio riportato di seguito viene illustrato come dichiarare `volatile` una variabile di campo pubblico.  
  
 [!code-csharp[csrefKeywordsModifiers#24](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_1.cs)]  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene illustrato come un thread di lavoro o ausiliario può essere creato e usato per eseguire l'elaborazione in parallelo con quella del thread principale. Per informazioni di base sul multithreading, vedere [Threading](../../../standard/threading/index.md) and [Threading](../../programming-guide/concepts/threading/index.md).  
  
 [!code-csharp[csProgGuideThreading#1](../../../csharp/language-reference/keywords/codesnippet/CSharp/volatile_2.cs)]  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
 [Parole chiave di C#](../../../csharp/language-reference/keywords/index.md)  
 [Modificatori](../../../csharp/language-reference/keywords/modifiers.md)
