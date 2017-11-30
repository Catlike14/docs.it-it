---
title: "Attributo &#39; &lt;attributename&gt;&#39; non può essere applicato più volte"
ms.date: 07/20/2015
ms.prod: .net
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30663
- vbc30663
helpviewer_keywords: BC30663
ms.assetid: 3760e7ff-7238-40a1-8676-77d858a64fc0
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 216cf54fd164ca95b6378517a679b5b54183559f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="attribute-39ltattributenamegt39-cannot-be-applied-multiple-times"></a>Attributo &#39; &lt;attributename&gt;&#39; non può essere applicato più volte
L'attributo può essere applicato solo una volta. Il `AttributeUsage` attributo determina se un attributo può essere applicato più volte.  
  
 **ID errore:** BC30663  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Verificare che l'attributo viene applicato solo una volta.  
  
2.  Se si utilizza attributi personalizzati, è possibile modificare i relativi `AttributeUsage` attributo per consentire più utilizzo dell'attributo, come con l'esempio seguente.  
  
```vb  
<AttributeUsage(AllowMultiple := True)>  
```  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.AttributeUsageAttribute>  
 [Creazione di attributi personalizzati](../../../visual-basic/programming-guide/concepts/attributes/creating-custom-attributes.md)  
 [AttributeUsage](../../../visual-basic/programming-guide/concepts/attributes/attributeusage.md)
