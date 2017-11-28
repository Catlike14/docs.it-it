---
title: "L'inferenza di tipi nullable non è supportata in questo contesto"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords: BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: e7a5450d812260d3916296dff56abee27b3d586c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a>L'inferenza di tipi nullable non è supportata in questo contesto
Tipi di valore e le strutture possono essere dichiarate nullable.  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 Tuttavia, è possibile usare la dichiarazione che ammette valori null in combinazione con l'inferenza del tipo. Negli esempi seguenti generano questo errore.  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **ID errore:** BC36629  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Utilizzare un `As` clausola per dichiarare la variabile come nullable.  
  
## <a name="see-also"></a>Vedere anche  
 [Tipi di valori nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)  
 [Inferenza del tipo di variabile locale](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
