---
title: ref (Riferimenti per C#) | Microsoft Docs
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- ref_CSharpKeyword
- ref
dev_langs:
- CSharp
helpviewer_keywords:
- parameters [C#], ref
- ref keyword [C#]
ms.assetid: b8a5e59c-907d-4065-b41d-95bf4273c0bd
caps.latest.revision: 32
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
ms.translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 353abf8a0c852acbbb2949f9640c1465dec8593b
ms.contentlocale: it-it
ms.lasthandoff: 03/13/2017

---
# <a name="ref-c-reference"></a>ref (Riferimenti per C#)
La parola chiave `ref` fa sì che un argomento sia passati per riferimento, non per valore. L'effetto del passaggio per riferimento è che qualsiasi modifica al parametro nel metodo chiamato viene riflessa nel metodo di chiamata. Ad esempio, se il chiamante passa un'espressione variabile locale o un'espressione di accesso dell'elemento della matrice e il metodo chiamato sostituisce l'oggetto a cui fa riferimento il parametro ref, l'elemento della matrice o una variabile locale del chiamante fa ora riferimento al nuovo oggetto.  
  
> [!NOTE]
>  Non confondere il concetto di passaggio per riferimento con il concetto di tipi di riferimento. I due concetti non sono uguali. Un parametro di metodo può essere modificato da `ref` che si tratti di un tipo di valore o di un tipo di riferimento. Non viene eseguito il boxing di un tipo di valore quando viene passato per riferimento.  
  
 Per usare un parametro `ref`, la definizione del metodo e il metodo chiamante devono usare in modo esplicito la parola chiave `ref`, come illustrato nell'esempio seguente.  
  
[!code-cs[csrefKeywordsMethodParams#6](../../../../samples/snippets/csharp/language-reference/keywords/ref/ref-1.cs)]
  
 Un argomento passato a un parametro `ref` deve essere inizializzato prima di essere passato. Questo comportamento è diverso dai parametri `out`, i cui argomenti non è essere inizializzati in modo esplicito prima di essere passati. Per altre informazioni, vedere [out](../../../csharp/language-reference/keywords/out.md).  
  
 I membri di una classe non possono avere firme che differiscono solo per `ref` e `out`. Un errore del compilatore si verifica se l'unica differenza tra due membri di un tipo è che uno di essi ha un parametro `ref` e l'altro ha un parametro `out`. Il codice seguente, ad esempio, non viene compilato.  
  
 [!code-cs[csrefKeywordsMethodParams#2](../../../../samples/snippets/csharp/language-reference/keywords/ref/ref-2.cs)] 
  
 Tuttavia, l'overload può essere eseguito quando un metodo ha un parametro `ref` o `out` e l'altro ha un parametro di valore, come illustrato nell'esempio seguente.  
  
 [!code-cs[ref-and-overloads](../../../../samples/snippets/csharp/language-reference/keywords/ref/ref-3.cs)]
  
 In altre situazioni che richiedono la firma corrispondente, ad esempio nascondere o sottoporre a override, `ref` e `out` fanno parte della firma e non sono corrispondenti tra loro.  
  
 Le proprietà non sono variabili. Sono metodi e non possono essere passate ai parametri `ref`.  
  
 Per informazioni su come passare le matrici, vedere [Passaggio di matrici usando ref e out](../../../csharp/programming-guide/arrays/passing-arrays-using-ref-and-out.md).  
  
 Non è possibile usare le parole chiave `ref` e `out` per i seguenti tipi di metodi:  
  
-   Metodi Async, definiti usando il modificatore [async](../../../csharp/language-reference/keywords/async.md).  
  
-   Metodi Iterator, che comprendono un'istruzione [yield return](../../../csharp/language-reference/keywords/yield.md) o `yield break`.  
  
## <a name="example"></a>Esempio  
 Negli esempi precedenti viene illustrato cosa accade quando si passano i tipi di valore per riferimento. È anche possibile usare la parola chiave `ref` per passare i tipi di riferimento. Il passaggio di un tipo di riferimento per riferimento consente al metodo chiamato di sostituire l'oggetto nel metodo di chiamata a cui fa riferimento il parametro referenziato. Il percorso di archiviazione dell'oggetto viene passato al metodo come valore del parametro referenziato. Se si modifica il valore nella posizione di archiviazione del parametro (in modo che punti a un nuovo oggetto), è anche possibile modificare il percorso di archiviazione a cui fa riferimento il chiamante. Nell'esempio seguente viene passata un'istanza di un tipo di riferimento come parametro `ref`. Per altre informazioni su come passare i tipi di riferimento per valore e per riferimento, vedere [Passaggio di parametri di tipi di riferimento](../../../csharp/programming-guide/classes-and-structs/passing-reference-type-parameters.md).  
  
 [!code-cs[ReferencesByRef](../../../../samples/snippets/csharp/language-reference/keywords/ref/ref-4.cs)]  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Passaggio di parametri](../../../csharp/programming-guide/classes-and-structs/passing-parameters.md)   
 [Parametri di metodo](../../../csharp/language-reference/keywords/method-parameters.md)   

 [Parole chiave di C#](../../../csharp/language-reference/keywords/index.md)
 
