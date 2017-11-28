---
title: "Il nome di variabile di intervallo può essere dedotto solo da un nome semplice o completo senza argomenti"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc36599
- bc36599
helpviewer_keywords: BC36599
ms.assetid: 17763dbe-f74f-4ccb-8086-cb7e45ec4d12
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 5c986fcf188482c526c53ddf3019cec5163d0b62
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="range-variable-name-can-be-inferred-only-from-a-simple-or-qualified-name-with-no-arguments"></a>Il nome di variabile di intervallo può essere dedotto solo da un nome semplice o completo senza argomenti
Un elemento di programmazione che accetta uno o più argomenti è incluso in una query LINQ. Il compilatore è in grado di dedurre una variabile di intervallo da tale elemento di programmazione.  
  
 **ID errore:** BC36599  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Specificare un nome di variabile esplicito per l'elemento di programmazione, come illustrato nel codice seguente:  
  
```  
Dim query = From var1 In collection1   
            Select VariableAlias= SampleFunction(var1), var1  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Introduzione a LINQ in Visual Basic](../../../visual-basic/programming-guide/language-features/linq/introduction-to-linq.md)  
 [Clausola Select](../../../visual-basic/language-reference/queries/select-clause.md)
