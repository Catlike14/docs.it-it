---
title: NotOverridable (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.NotOverridable
- NotOverridable
helpviewer_keywords:
- sealed methods [Visual Basic]
- NotOverridable keyword [Visual Basic]
- properties [Visual Basic], redefining
- elements [Visual Basic], sealed
- sealed [elements VB]
- procedures [Visual Basic], overriding
- procedures [Visual Basic], redefining
- overriding
- methods [Visual Basic], sealed
- properties [Visual Basic], overriding
ms.assetid: 66ec6984-f5f5-4857-b362-6a3907aaf9e0
ms.openlocfilehash: 3fae1a4b587c379dbc459cbc973982851e713785
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33600753"
---
# <a name="notoverridable-visual-basic"></a>NotOverridable (Visual Basic)
Specifica che una proprietà o routine non può essere sottoposto a override in una classe derivata.  
  
## <a name="remarks"></a>Note  
 Il `NotOverridable` modificatore impedisce una proprietà o metodo di override in una classe derivata.  Il [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md) modificatore consente a una proprietà o metodo in una classe per eseguire l'override in una classe derivata. Per altre informazioni, vedere [Nozioni fondamentali sull'ereditarietà](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md).  
  
 Se il `Overridable` o `NotOverridable` modificatore non è specificato, l'impostazione predefinita varia a seconda se la proprietà o il metodo esegue l'override di metodo o una proprietà di classe di base. Se la proprietà o il metodo esegue l'override di una proprietà della classe base o un metodo, l'impostazione predefinita è `Overridable`; in caso contrario, è `NotOverridable`.  
  
 Un elemento che non può essere sottoposto a override viene talvolta definito un *sealed* elemento.  
  
 È possibile usare `NotOverridable` solo in un'istruzione per la dichiarazione di proprietà o routine. È possibile specificare `NotOverridable` solo su una proprietà o routine che esegue l'override di un'altra proprietà o routine, ovvero solo in combinazione con `Overrides`.  
  
## <a name="combined-modifiers"></a>Modificatori combinati  
 Non è possibile specificare `Overridable` o `NotOverridable` per un `Private` metodo.  
  
 Non è possibile specificare `NotOverridable` con `MustOverride`, `Overridable`, o `Shared` nella stessa dichiarazione.  
  
## <a name="usage"></a>Utilizzo  
 Il modificatore `NotOverridable` può essere usato nei contesti seguenti:  
  
 [Istruzione Function](../../../visual-basic/language-reference/statements/function-statement.md)  
  
 [Istruzione Property](../../../visual-basic/language-reference/statements/property-statement.md)  
  
 [Istruzione Sub](../../../visual-basic/language-reference/statements/sub-statement.md)  
  
## <a name="see-also"></a>Vedere anche  
 [Modificatori](../../../visual-basic/language-reference/modifiers/index.md)  
 [Nozioni fondamentali sull'ereditarietà](../../../visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics.md)  
 [MustOverride](../../../visual-basic/language-reference/modifiers/mustoverride.md)  
 [Overridable](../../../visual-basic/language-reference/modifiers/overridable.md)  
 [Overrides](../../../visual-basic/language-reference/modifiers/overrides.md)  
 [Parole chiave](../../../visual-basic/language-reference/keywords/index.md)  
 [Shadowing in Visual Basic](../../../visual-basic/programming-guide/language-features/declared-elements/shadowing.md)
