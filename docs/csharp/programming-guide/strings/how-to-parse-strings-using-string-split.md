---
title: 'Procedura: Analizzare le stringhe con String.Split (Guida per programmatori C#)'
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
helpviewer_keywords:
- splitting strings [C#]
- Split method [C#]
- strings [C#], splitting
- parse strings
ms.assetid: 729c2923-4169-41c6-9c90-ef176c1e2953
caps.latest.revision: "17"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 7b97d1d89a4c74a4c759d1ed41a0bc2476b3b07a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-parse-strings-using-stringsplit-c-programming-guide"></a>Procedura: Analizzare le stringhe con String.Split (Guida per programmatori C#)
L'esempio di codice seguente mostra come analizzare una stringa con il metodo <xref:System.String.Split%2A?displayProperty=nameWithType> . <xref:System.String.Split%2A> accetta come input una matrice di caratteri che indica quali caratteri separano le sottostringhe rilevanti della stringa di destinazione.  La funzione restituisce una matrice di sottostringhe.  
  
 Questo esempio usa spazi, virgole, punti, due punti e tabulazioni, tutti passati in una matrice che contiene questi caratteri di separazione per <xref:System.String.Split%2A>.  Ogni parola nella frase della stringa di destinazione viene visualizzata separatamente rispetto alla matrice di stringhe risultante.  
  
## <a name="example"></a>Esempio  
 [!code-csharp[csProgGuideStrings#16](../../../csharp/programming-guide/strings/codesnippet/CSharp/how-to-parse-strings-using-string-split_1.cs)]  
  
## <a name="example"></a>Esempio  
 Per impostazione predefinita, String.Split restituisce stringhe vuote quando vengono visualizzati due caratteri di separazione adiacenti nella stringa di destinazione.  È possibile passare un parametro facoltativo StringSplitOptions.RemoveEmptyEntries per escludere le stringhe vuote nell'output.  
  
 String.Split può accettare una matrice di stringhe (sequenze di caratteri, al posto di caratteri singoli, che fungono da separatori per l'analisi della stringa di destinazione).  
  
```csharp  
class TestStringSplit  
{  
    static void Main()  
    {  
        string[] separatingChars = { "<<", "..." };  
  
        string text = "one<<two......three<four";  
        System.Console.WriteLine("Original text: '{0}'", text);  
  
        string[] words = text.Split(separatingChars, System.StringSplitOptions.RemoveEmptyEntries );  
        System.Console.WriteLine("{0} substrings in text:", words.Length);  
  
        foreach (string s in words)  
        {  
            System.Console.WriteLine(s);  
        }  
  
        // Keep the console window open in debug mode.  
        System.Console.WriteLine("Press any key to exit.");  
        System.Console.ReadKey();  
    }  
}  
/* Output:  
    Original text: 'one<<two......three<four'  
    3 words in text:  
    one  
    two  
    three<four  
*/  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
 [Stringhe](../../../csharp/programming-guide/strings/index.md)  
 [Espressioni regolari di .NET Framework](https://msdn.microsoft.com/library/hs600312)
