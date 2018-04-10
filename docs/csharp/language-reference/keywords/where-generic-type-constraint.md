---
title: where (vincolo di tipo generico) (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- whereconstraint
- whereconstraint_CSharpKeyword
helpviewer_keywords:
- where (generic type constraint) [C#]
ms.assetid: d7aa871b-0714-416a-bab2-96f87ada4310
caps.latest.revision: 10
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: f2b7b159689aa771d3f9d59e3b1dd340c85b1d79
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="where-generic-type-constraint-c-reference"></a>where (vincolo di tipo generico) (Riferimenti per C#)
In una definizione di tipo generico, la clausola `where` viene usata per specificare i vincoli per i tipi che possono essere usati come argomenti per un parametro di tipo definito in una dichiarazione generica. Ad esempio, una classe generica, `MyGenericClass`, può essere dichiarata in modo che tramite il parametro di tipo `T` venga implementata l'interfaccia <xref:System.IComparable%601>:  
  
```csharp  
public class MyGenericClass<T> where T:IComparable { }  
```  
  
> [!NOTE]
>  Per altre informazioni sulla clausola where in un'espressione di query, vedere [Clausola where](../../../csharp/language-reference/keywords/where-clause.md).  
  
 Oltre ai vincoli di interfaccia, una clausola `where` può includere un vincolo di classe di base, che stabilisce che un tipo deve usare la classe specificata come classe di base (o essere la classe stessa) per poter essere usato come argomento di tipo per tale tipo generico. Se viene usato tale vincolo, deve apparire prima di tutti gli altri vincoli per quel parametro di tipo.  
  
 [!code-csharp[csrefKeywordsContextual#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/where-generic-type-constraint_1.cs)]  
  
 La clausola `where` può anche includere un vincolo di costruttore. È possibile creare un'istanza di un parametro di tipo usando l'operatore new. Tuttavia, per poter eseguire questa operazione, è necessario che il parametro di tipo sia vincolato dal vincolo di costruttore, `new()`. Il [vincolo new()](../../../csharp/language-reference/keywords/new-constraint.md) consente al compilatore di sapere che ogni argomento di tipo specificato deve usare un costruttore accessibile senza parametri o predefinito. Ad esempio:  
  
 [!code-csharp[csrefKeywordsContextual#7](../../../csharp/language-reference/keywords/codesnippet/CSharp/where-generic-type-constraint_2.cs)]  
  
 Il vincolo `new()` viene visualizzato per ultimo nella clausola `where`.  
  
 Con più parametri di tipo, usare una clausola `where` per ogni parametro di tipo, ad esempio:  
  
 [!code-csharp[csrefKeywordsContextual#8](../../../csharp/language-reference/keywords/codesnippet/CSharp/where-generic-type-constraint_3.cs)]  
  
 È anche possibile associare vincoli ai parametri di tipo di metodi generici, come indicato di seguito:  
  
```csharp  
public bool MyMethod<T>(T t) where T : IMyInterface { }  
```  
  
 Si noti che la sintassi usata per descrivere i vincoli dei parametri di tipo per i delegati è uguale a quella dei metodi:  
  
```csharp  
delegate T MyDelegate<T>() where T : new()  
```  
  
 Per informazioni sui delegati generici, vedere [Delegati generici](../../../csharp/programming-guide/generics/generic-delegates.md).  
  
 Per informazioni dettagliate sulla sintassi e sull'uso dei vincoli, vedere [Vincoli sui parametri di tipo](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md).  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
 [Introduzione ai generics](../../../csharp/programming-guide/generics/introduction-to-generics.md)  
 [Vincolo new](../../../csharp/language-reference/keywords/new-constraint.md)  
 [Vincoli sui parametri di tipo](../../../csharp/programming-guide/generics/constraints-on-type-parameters.md)
