---
title: Operatore TypeOf (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- TypeOf
- vb.TypeOf
helpviewer_keywords:
- types [Visual Basic], compatible
- comparison operators [Visual Basic]
- TypeOf...Is expression
- data types [Visual Basic], compatible
- TypeOf operator [Visual Basic]
- compatible data types [Visual Basic]
ms.assetid: 33f65296-659a-4b9a-9a29-c2a91cff68b2
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 51bd2af7af28aa229fa62770c5b92d31e461333b
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="typeof-operator-visual-basic"></a>Operatore TypeOf (Visual Basic)
Confronta una variabile di riferimento a un oggetto con un tipo di dati.  
  
## <a name="syntax"></a>Sintassi  
  
```  
result = TypeOf objectexpression Is typename  
```  
  
```  
result = TypeOf objectexpression IsNot typename  
```  
  
## <a name="parts"></a>Parti  
 `result`  
 Restituita. Valore `Boolean`.  
  
 `objectexpression`  
 Obbligatorio. Qualsiasi espressione che restituisce un tipo riferimento.  
  
 `typename`  
 Obbligatorio. Qualsiasi nome di un tipo di dati.  
  
## <a name="remarks"></a>Note  
 L'operatore `TypeOf` determina se il tipo di `objectexpression` in fase di esecuzione è compatibile con `typename`. La compatibilità dipende dalla categoria del tipo di `typename`. La tabella seguente illustra come viene determinata la compatibilità.  
  
|Categoria del tipo di `typename`|Criterio di compatibilità|  
|---------------------------------|-----------------------------|  
|Classe|`objectexpression` è del tipo `typename` o eredita da `typename`|  
|Struttura|`objectexpression` è del tipo `typename`|  
|Interfaccia|`objectexpression` implementa `typename` o eredita da una classe che implementa `typename`|  
  
 Se il tipo di `objectexpression` in fase di esecuzione soddisfa il criterio di compatibilità, `result` sarà `True`. In caso contrario, `result` sarà `False`.  Se `objectexpression` è null, `TypeOf`...`Is` restituisce `False` e ...`IsNot` restituisce `True`.  
  
 `TypeOf` viene sempre usato con la parola chiave `Is` per costruire un'espressione `TypeOf`...`Is` oppure con la parola chiave `IsNot` per costruire un'espressione `TypeOf`...`IsNot`.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente le espressioni `TypeOf`...`Is` vengono usate per verificare la compatibilità dei tipi di due variabili di riferimento a un oggetto con diversi tipi di dati..  
  
 [!code-vb[VbVbalrOperators#39](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/typeof-operator_1.vb)]  
  
 La variabile `refInteger` presenta un tipo in fase di esecuzione `Integer`. È compatibile con `Integer`, ma non con `Double`. La variabile `refForm` presenta un tipo in fase di esecuzione <xref:System.Windows.Forms.Form>. È compatibile con <xref:System.Windows.Forms.Form> perché si tratta del relativo tipo, con <xref:System.Windows.Forms.Control> perché <xref:System.Windows.Forms.Form> eredita da <xref:System.Windows.Forms.Control> e con <xref:System.ComponentModel.IComponent> perché <xref:System.Windows.Forms.Form> eredita da <xref:System.ComponentModel.Component>, che implementa <xref:System.ComponentModel.IComponent>. `refForm` non è invece compatibile con <xref:System.Windows.Forms.Label>.  
  
## <a name="see-also"></a>Vedere anche  
 [Operatore Is](../../../visual-basic/language-reference/operators/is-operator.md)  
 [Operatore IsNot](../../../visual-basic/language-reference/operators/isnot-operator.md)  
 [Operatori di confronto in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)  
 [Precedenza tra gli operatori in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [Elenco degli operatori per funzionalità](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [Operatori ed espressioni](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
