---
title: Utilizzo di struct (Guida per programmatori C#)
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- structs [C#], using
ms.assetid: cea4a459-9eb9-442b-8d08-490e0797ba38
caps.latest.revision: 28
author: BillWagner
ms.author: wiwagn
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 67fa4f764e6e40041e4b8e37eccbd1adb2b509d3
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="using-structs-c-programming-guide"></a>Utilizzo di struct (Guida per programmatori C#)
Il tipo `struct` è adatto a rappresentare oggetti leggeri come `Point`, `Rectangle`e `Color`. Sebbene sia altrettanto conveniente rappresentare un punto con una [classe](../../../csharp/language-reference/keywords/class.md) con [proprietà implementate automaticamente](../../../csharp/programming-guide/classes-and-structs/auto-implemented-properties.md), lo [struct](../../../csharp/language-reference/keywords/struct.md) potrebbe essere più efficiente in alcuni scenari. Ad esempio, se si dichiara una matrice di 1000 oggetti `Point` , verrà allocata memoria aggiuntiva per fare riferimento a ogni oggetto. In questo caso, lo struct risulterebbe meno costoso. Dal momento che [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] contiene un oggetto denominato <xref:System.Drawing.Point>, lo struct in questo esempio è invece denominato "CoOrds".  
  
 [!code-cs[csProgGuideObjects#1](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-structs_1.cs)]  
  
 È un errore definire un costruttore predefinito (senza parametri) per uno struct. È anche errato inizializzare un campo di istanza nel corpo di uno struct. È possibile inizializzare i membri dello struct solo usando un costruttore con parametri o accedendo ai membri singolarmente dopo la dichiarazione dello struct. I membri privati o altrimenti inaccessibili possono essere inizializzati solo in un costruttore.  
  
 Quando si crea un oggetto struct mediante l'operatore [new](../../../csharp/language-reference/keywords/new.md) , questo viene creato e viene chiamato il costruttore appropriato. A differenza delle classi, è possibile creare istanze di struct senza usare l'operatore `new` . In tal caso, non vi è alcuna chiamata al costruttore, il che rende più efficiente l'allocazione. Tuttavia, i campi restano non assegnati e l'oggetto non può essere usato fino all'inizializzazione di tutti i campi.  
  
 Quando uno struct contiene un tipo di riferimento come membro, il costruttore predefinito del membro deve essere richiamato in modo esplicito, altrimenti il membro rimane non assegnato e lo struct non può essere usato. (Ciò dà origine all'errore del compilatore CS0171).  
  
 Per gli struct non è prevista la stessa ereditarietà delle classi. Uno struct non può ereditare da un altro struct o da una classe e non può essere la base di una classe. Gli struct, tuttavia, ereditano dalla classe base <xref:System.Object>. Uno struct può implementare interfacce esattamente come le classi.  
  
 Non è possibile dichiarare una classe usando la parola chiave `struct`. In C# le classi e gli struct sono semanticamente diversi. Uno struct è un tipo di valore, mentre una classe è un tipo di riferimento. Per altre informazioni, vedere [Tipi di valore](../../../csharp/language-reference/keywords/value-types.md).  
  
 A meno che non sia richiesta una semantica tipo-riferimento, una classe piccola può essere gestita in modo più efficiente dal sistema se dichiarata come uno struct.  
  
## <a name="example-1"></a>Esempio 1  
  
### <a name="description"></a>Descrizione  
 Questo esempio mostra l'inizializzazione `struct` tramite costruttori con parametri e valore predefinito.  
  
### <a name="code"></a>Codice  
 [!code-cs[csProgGuideObjects#1](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-structs_1.cs)]  
  
 [!code-cs[csProgGuideObjects#2](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-structs_2.cs)]  
  
## <a name="example-2"></a>Esempio 2  
  
### <a name="description"></a>Descrizione  
 Questo esempio illustra una funzionalità univoca per struct. Crea un oggetto CoOrds senza usare l'operatore `new` . Se si sostituisce la parola `struct` con la parola `class`, il programma non verrà compilato.  
  
### <a name="code"></a>Codice  
 [!code-cs[csProgGuideObjects#1](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-structs_1.cs)]  
  
 [!code-cs[csProgGuideObjects#3](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/using-structs_3.cs)]  
  
## <a name="see-also"></a>Vedere anche  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Struct](../../../csharp/programming-guide/classes-and-structs/structs.md)

