---
title: virtual (Riferimenti per C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- virtual_CSharpKeyword
- virtual
helpviewer_keywords:
- virtual keyword [C#]
ms.assetid: 5da9abae-bc1e-434f-8bea-3601b8dcb3b2
caps.latest.revision: 
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: dce3333646bca6f558e3760849b6cffdb34a6c0b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="virtual-c-reference"></a>virtual (Riferimenti per C#)
La parola chiave `virtual` viene usata per modificare una dichiarazione di metodo, proprietà, indicizzatore o evento e consentire che sia sottoposta a override in una classe derivata. Ad esempio, questo metodo può essere sottoposto a override da qualsiasi classe che lo eredita:  
  
```  
public virtual double Area()   
{  
    return x * y;  
}  
```  
  
 L'implementazione di un membro virtuale può essere modificata da un [membro di sostituzione](../../../csharp/language-reference/keywords/override.md) di una classe derivata. Per altre informazioni sull'uso della parola chiave `virtual`, vedere [Controllo delle versioni con le parole chiave Override e New](../../../csharp/programming-guide/classes-and-structs/versioning-with-the-override-and-new-keywords.md) e [Sapere quando utilizzare le parole chiave Override e New](../../../csharp/programming-guide/classes-and-structs/knowing-when-to-use-override-and-new-keywords.md).  
  
## <a name="remarks"></a>Note  
 Quando viene richiamato un metodo virtuale, il tipo di runtime dell'oggetto viene controllato per verificare la presenza di un membro di sostituzione. Viene chiamato il membro di sostituzione nella classe più derivata e potrebbe trattarsi del membro originale, se nessuna classe derivata ha eseguito l'override del membro.  
  
 Per impostazione predefinita, i metodi sono non virtuali. Non è possibile eseguire l'override di un metodo non virtuale.  
  
 Non è possibile utilizzare il `virtual` modificatore con il `static`, `abstract`, `private`, o `override` modificatori. L'esempio seguente illustra una proprietà virtuale:  
  
 [!code-csharp[csrefKeywordsModifiers#26](../../../csharp/language-reference/keywords/codesnippet/CSharp/virtual_1.cs)]  
  
 Le proprietà virtuali si comportano come i metodi astratti, ad eccezione delle differenze nella sintassi di dichiarazione e di chiamata.  
  
-   Non è possibile usare il modificatore `virtual` su una proprietà static.  
  
-   Una proprietà virtuale ereditata può essere sottoposta a override in una classe derivata includendo una dichiarazione di proprietà che usa il modificatore `override`.  
  
## <a name="example"></a>Esempio  
 In questo esempio la classe `Shape` contiene le due coordinate `x`, `y`e il metodo virtuale `Area()`. Le classi di forma diversa, ad esempio `Circle`, `Cylinder` e `Sphere`, ereditano la classe `Shape` e la superficie viene calcolata per ogni figura. Ogni classe derivata ha la propria implementazione di override di `Area()`.  
  
 Si noti che le classi ereditate `Circle`, `Sphere` e `Cylinder` usano tutte costruttori che inizializzano la classe di base, come illustrato nella seguente dichiarazione.  
  
```  
public Cylinder(double r, double h): base(r, h) {}  
```  
  
 Il programma seguente calcola e visualizza l'area appropriata per ogni figura richiamando l'implementazione corretta del metodo `Area()` in base all'oggetto associato al metodo.  
  
 [!code-csharp[csrefKeywordsModifiers#23](../../../csharp/language-reference/keywords/codesnippet/CSharp/virtual_2.cs)]  
  
## <a name="c-language-specification"></a>Specifiche del linguaggio C#  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimenti per C#](../../../csharp/language-reference/index.md)  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
 [Modificatori](../../../csharp/language-reference/keywords/modifiers.md)  
 [Parole chiave di C#](../../../csharp/language-reference/keywords/index.md)  
 [Polimorfismo](../../../csharp/programming-guide/classes-and-structs/polymorphism.md)  
 [abstract](../../../csharp/language-reference/keywords/abstract.md)  
 [override](../../../csharp/language-reference/keywords/override.md)  
 [new](../../../csharp/language-reference/keywords/new.md)
