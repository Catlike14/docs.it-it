---
title: "Costruttori privati (Guida per programmatori C#) | Microsoft Docs"
ms.date: "2015-07-20"
ms.prod: ".net"
ms.technology: 
  - "devlang-csharp"
ms.topic: "article"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "linguaggio C#, costruttori privati"
  - "costruttori privati [C#]"
ms.assetid: 29eeaa7d-8d81-453c-94b9-0e2800172621
caps.latest.revision: 19
author: "BillWagner"
ms.author: "wiwagn"
caps.handback.revision: 19
---
# Costruttori privati (Guida per programmatori C#)
Un costruttore privato è un costruttore di istanza speciale  e viene generalmente utilizzato in classi contenenti solo membri static.  Se una classe dispone di uno o più costruttori privati ma non include alcun costruttore pubblico, alle altre classi, tranne quelle annidate, non sarà consentita la creazione delle istanze della classe.  Di seguito è riportato un esempio:  
  
 [!code-cs[csProgGuideObjects#11](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_1.cs)]  
  
 La dichiarazione del costruttore vuoto impedisce la generazione automatica di un costruttore predefinito.  Tenere presente che se non si utilizza un modificatore di accesso con il costruttore, questo rimarrà di tipo privato per impostazione predefinita.  Tuttavia, il modificatore [private](../../../csharp/language-reference/keywords/private.md) viene solitamente utilizzato in modo esplicito per specificare che non è possibile creare un'istanza della classe.  
  
 I costruttori privati vengono utilizzati per impedire la creazione di istanze di una classe in assenza di metodi e campi di istanza, ad esempio la classe <xref:System.Math>, oppure quando viene chiamato un metodo per ottenere un'istanza di una classe.  Se tutti i metodi della classe sono statici, è consigliabile rendere statica l'intera classe.  Per ulteriori informazioni, vedere [Classi statiche e membri di classi statiche](../../../csharp/programming-guide/classes-and-structs/static-classes-and-static-class-members.md).  
  
## Esempio  
 Di seguito è riportato l'esempio di una classe che utilizza un costruttore privato.  
  
 [!code-cs[csProgGuideObjects#12](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_2.cs)]  
  
 Se si rimuove il commento dall'istruzione dell'esempio riportata di seguito, verrà generato un errore poiché non è possibile accedere al costruttore a causa del livello di protezione.  
  
 [!code-cs[csProgGuideObjects#13](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/private-constructors_3.cs)]  
  
## Specifiche del linguaggio C\#  
 [!INCLUDE[CSharplangspec](../../../csharp/language-reference/keywords/includes/csharplangspec-md.md)]  
  
## Vedere anche  
 [Guida per programmatori C\#](../../../csharp/programming-guide/index.md)   
 [Classi e struct](../../../csharp/programming-guide/classes-and-structs/index.md)   
 [Costruttori](../../../csharp/programming-guide/classes-and-structs/constructors.md)   
 [Distruttori](../../../csharp/programming-guide/classes-and-structs/destructors.md)   
 [private](../../../csharp/language-reference/keywords/private.md)   
 [public](../../../csharp/language-reference/keywords/public.md)