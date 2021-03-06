---
title: 'Procedura: chiamare un metodo di estensione (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- calling extension methods [Visual Basic]
- extension methods [Visual Basic]
ms.assetid: df07750f-40f4-4c07-a79e-1113a27cfbea
ms.openlocfilehash: 32691183bcd1632a82b1e9a2668790abbf8f80fd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-call-an-extension-method-visual-basic"></a>Procedura: chiamare un metodo di estensione (Visual Basic)
Metodi di estensione consentono di aggiungere metodi alla classe esistente. Dopo che un metodo di estensione è dichiarato e inserito nell'ambito, è possibile chiamare questo metodo di istanza del tipo che estende. Per ulteriori informazioni su come scrivere un metodo di estensione, vedere [procedura: scrivere un metodo di estensione](./how-to-write-an-extension-method.md).  
  
 Le istruzioni seguenti fanno riferimento al metodo di estensione `PrintAndPunctuate`, che visualizza l'istanza di stringa che richiama, seguita dal valore inviato per il secondo parametro, `punc`.  
  
```vb  
Imports System.Runtime.CompilerServices  
  
Module StringExtensions  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
  
End Module  
```  
  
 Il metodo deve essere nell'ambito quando viene chiamato.  
  
### <a name="to-call-an-extension-method"></a>Per chiamare un metodo di estensione  
  
1.  Dichiarare una variabile con il tipo di dati del primo parametro del metodo di estensione. Per `PrintAndPunctuate`, è necessario un <xref:System.String> variabile:  
  
    ```  
    Dim example = "Ready"  
    ```  
  
2.  Variabile richiama il metodo di estensione che il valore è associato il primo parametro, `aString`. Verrà visualizzata la seguente istruzione di chiamata `Ready?`.  
  
    ```  
    example.PrintAndPunctuate("?")  
    ```  
  
     Si noti che la chiamata a questo metodo di estensione è analoga a una chiamata a uno qualsiasi del <xref:System.String> metodi che richiedono un parametro di istanza:  
  
    ```  
    example.EndsWith("dy")  
    example.IndexOf("R")  
    ```  
  
3.  Dichiarare un'altra variabile di stringa e chiamare nuovamente il metodo per verificare che funziona con qualsiasi stringa.  
  
    ```  
    Dim example2 = " or not"  
    example2.PrintAndPunctuate("!!!")  
    ```  
  
     In questo caso il risultato è: `or not!!!`.  
  
## <a name="example"></a>Esempio  
 Il codice seguente è un esempio completo di creazione e utilizzo di un metodo di estensione semplice.  
  
```vb  
Imports System.Runtime.CompilerServices  
Imports ConsoleApplication1.StringExtensions  
  
Module Module1  
  
    Sub Main()  
  
        Dim example = "Hello"  
        example.PrintAndPunctuate(".")  
        example.PrintAndPunctuate("!!!!")  
  
        Dim example2 = "Goodbye"  
        example2.PrintAndPunctuate("?")  
    End Sub  
  
    <Extension()>   
    Public Sub PrintAndPunctuate(ByVal aString As String,   
                                 ByVal punc As String)  
        Console.WriteLine(aString & punc)  
    End Sub  
End Module  
  
' Output:  
' Hello.  
' Hello!!!!  
' Goodbye?  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Procedura: Scrivere un metodo di estensione](./how-to-write-an-extension-method.md)  
 [Metodi di estensione](./extension-methods.md)  
 [Ambito in Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
