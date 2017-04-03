---
title: Istruzione using (Riferimenti per C#) | Microsoft Docs
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- using statement [C#]
ms.assetid: afc355e6-f0b9-4240-94dd-0d93f17d9fc3
caps.latest.revision: 31
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
translationtype: Human Translation
ms.sourcegitcommit: a06bd2a17f1d6c7308fa6337c866c1ca2e7281c0
ms.openlocfilehash: 587e50d5c81c19d75e9d8bf4779064947a373b71
ms.lasthandoff: 03/13/2017

---
# <a name="using-statement-c-reference"></a>Istruzione using (Riferimenti per C#)
Offre una comoda sintassi che garantisce l'uso corretto degli oggetti <xref:System.IDisposable>.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente illustra come usare l'istruzione using.  
  
 [!code-cs[csrefKeywordsNamespace#4](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-statement_1.cs)]  
  
## <a name="remarks"></a>Note  
 <xref:System.IO.File> e <xref:System.Drawing.Font> sono esempi di tipi gestiti che accedono a risorse non gestite (in questo caso handle di file e contesti di dispositivo). Esistono molti altri tipi di risorse non gestite e tipi della libreria di classi che le incapsulano. Tutti questi tipi devono implementare l'interfaccia <xref:System.IDisposable>.  
  
 Di norma, quando si usa un oggetto `IDisposable` è necessario dichiararlo e creare la relativa istanza in un'istruzione `using`. L'istruzione `using` chiama il metodo <xref:System.IDisposable.Dispose%2A> per l'oggetto in modo corretto e, quando si usa come illustrato in precedenza, fa in modo che l'oggetto stesso esca dall'ambito, non appena si chiama <xref:System.IDisposable.Dispose%2A>. All'interno del blocco `using` l'oggetto è di sola lettura e non può essere modificato o riassegnato.  
  
 L'istruzione `using` garantisce che il metodo <xref:System.IDisposable.Dispose%2A> venga chiamato anche se si verifica un'eccezione mentre si chiamano i metodi per l'oggetto. È possibile ottenere lo stesso risultato inserendo l'oggetto all'interno di un blocco try e chiamando <xref:System.IDisposable.Dispose%2A> in un blocco finally. Di fatto questo è il modo in cui l'istruzione `using` viene convertita dal compilatore. L'esempio di codice precedente si espande al codice seguente in fase di compilazione (si notino le parentesi graffe aggiuntive per creare l'ambito limitato per l'oggetto):  
  
 [!code-cs[csrefKeywordsNamespace#5](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-statement_2.cs)]  
  
 È possibile dichiarare più istanze di un tipo in un'istruzione `using`, come illustrato nell'esempio seguente.  
  
 [!code-cs[csrefKeywordsNamespace#6](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-statement_3.cs)]  
  
 È possibile creare un'istanza dell'oggetto risorsa e quindi passare la variabile all'istruzione `using`, ma questa procedura non è consigliata. In questo caso l'oggetto rimane nell'ambito quando il controllo lascia il blocco `using`, anche se probabilmente non avrà più accesso alle relative risorse non gestite. In altre parole, non verrà più completamente inizializzato. Se si tenta di usare l'oggetto di fuori del blocco `using`, si rischia di causare la generazione di un'eccezione. Per questo motivo, in genere è preferibile creare un'istanza dell'oggetto nell'istruzione `using` e limitare l'ambito al blocco `using`.  
  
 [!code-cs[csrefKeywordsNamespace#7](../../../csharp/language-reference/keywords/codesnippet/CSharp/using-statement_4.cs)]  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec_md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)   
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Parole chiave di C#](../../../csharp/language-reference/keywords/index.md)   
 [Direttiva using](../../../csharp/language-reference/keywords/using-directive.md)   
 [Garbage Collection](../../../standard/garbagecollection/index.md)   
 [Implementazione di un metodo Dispose](http://msdn.microsoft.com/library/eb4e1af0-3b48-4fbc-ad4e-fc2f64138bf9)
