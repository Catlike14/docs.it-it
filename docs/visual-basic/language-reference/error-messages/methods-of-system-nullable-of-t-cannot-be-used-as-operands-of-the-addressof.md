---
title: Metodi di &#39;System. Nullable (Of T)&#39; non possono essere usati come operandi del &#39;AddressOf&#39; (operatore)
ms.date: 07/20/2015
f1_keywords:
- vbc32126
- bc32126
helpviewer_keywords:
- BC32126
ms.assetid: 2325668b-e2ad-40ee-a1ec-30450236c20d
ms.openlocfilehash: 3a3e4fc033f47fb6a72076dff79f1eece8d01a30
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33594120"
---
# <a name="methods-of-39systemnullableof-t39-cannot-be-used-as-operands-of-the-39addressof39-operator"></a>Metodi di &#39;System. Nullable (Of T)&#39; non possono essere usati come operandi del &#39;AddressOf&#39; (operatore)
Un'istruzione utilizza il `AddressOf` operatore con un operando che rappresenta una procedura del <xref:System.Nullable%601> struttura.  
  
 **ID errore:** BC32126  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Sostituire il nome della routine nel `AddressOf` clausola con un operando che non è un membro di <xref:System.Nullable%601>.  
  
-   Scrivere una classe che include il metodo di <xref:System.Nullable%601> che si desidera utilizzare. Nell'esempio seguente, il `NullableWrapper` classe definisce un nuovo metodo denominato `GetValueOrDefault`. Poiché questo nuovo metodo non è un membro di <xref:System.Nullable%601>, può essere applicato a `nullInstance`, un'istanza di un tipo nullable, in modo da formare un argomento per `AddressOf`.  
  
```vb  
Module Module1  
  
    Delegate Function Deleg() As Integer  
  
    Sub Main()  
        Dim nullInstance As New Nullable(Of Integer)(1)  
  
        Dim del As Deleg  
  
        ' GetValueOrDefault is a method of the Nullable generic  
        ' type. It cannot be used as an operand of AddressOf.  
        ' del = AddressOf nullInstance.GetValueOrDefault  
  
        ' The following line uses the GetValueOrDefault method  
        ' defined in the NullableWrapper class.  
        del = AddressOf (New NullableWrapper(  
            Of Integer)(nullInstance)).GetValueOrDefault  
  
        Console.WriteLine(del.Invoke())  
    End Sub  
  
    Class NullableWrapper(Of T As Structure)  
        Private m_Value As Nullable(Of T)  
  
        Sub New(ByVal Value As Nullable(Of T))  
            m_Value = Value  
        End Sub  
  
        Public Function GetValueOrDefault() As T  
            Return m_Value.Value  
        End Function  
    End Class  
End Module  
```  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Nullable%601>  
 [Operatore AddressOf](../../../visual-basic/language-reference/operators/addressof-operator.md)  
 [Tipi di valori nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
 [Tipi generici in Visual Basic](../../../visual-basic/programming-guide/language-features/data-types/generic-types.md)
