---
title: 'Procedura: Creare un nuovo metodo per una enumerazione (Guida per programmatori C#) | Microsoft Docs'
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
helpviewer_keywords:
- enumerations [C#]
- extension methods [C#], for enums
- enum extensibility [C#]
ms.assetid: 100106f9-1e54-462c-8ebe-3892fe23b6eb
caps.latest.revision: 7
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
ms.sourcegitcommit: 31905a37f09db5f5192123f0118252fbe8b02eff
ms.openlocfilehash: f015ec08818de7f99c5f16d237114c489edae1b6
ms.contentlocale: it-it
ms.lasthandoff: 06/15/2017

---
# <a name="how-to-create-a-new-method-for-an-enumeration-c-programming-guide"></a>Procedura: creare un nuovo metodo per una enumerazione (Guida per programmatori C#)
È possibile usare metodi di estensione per aggiungere la funzionalità specifica di un particolare tipo enum.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente, l'enumerazione `Grades` rappresenta il voto che uno studente potrebbe ricevere in un corso. Il metodo di estensione denominato `Passing` viene aggiunto al tipo `Grades` in modo che ogni istanza di tale tipo ora "sa" se rappresenta un voto sufficiente oppure no.  
  
 [!code-cs[csProgGuideExtensionMethods#2](../../../csharp/programming-guide/classes-and-structs/codesnippet/CSharp/how-to-create-a-new-method-for-an-enumeration_1.cs)]  
  
 Si noti che la classe `Extensions` contiene anche una variabile statica aggiornata in modo dinamico e che il valore restituito dal metodo di estensione riflette il valore corrente di tale variabile. Ciò dimostra che dietro le quinte i metodi di estensione vengono chiamati direttamente per la classe statica nella quale sono definiti.  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 Per eseguire questo codice, copiarlo e incollarlo nel progetto di applicazione console di Visual C# creato in [!INCLUDE[vs_current_short](~/includes/vs-current-short-md.md)]. Per impostazione predefinita, questo progetto usa la versione 3.5 di [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)] e contiene un riferimento a System.Core.dll e una direttiva `using` per System.Linq. Se uno o più di questi requisiti non sono presenti nel progetto, è possibile aggiungerli manualmente.   
  
## <a name="see-also"></a>Vedere anche  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Metodi di estensione](../../../csharp/programming-guide/classes-and-structs/extension-methods.md)
