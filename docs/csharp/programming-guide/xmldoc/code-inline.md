---
title: '&lt;c&gt; (Guida per programmatori C#)'
ms.date: 2015-07-20
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- c
- <c>
dev_langs:
- CSharp
helpviewer_keywords:
- text, marking as code [C#]
- code, marking text as [C#]
- c C# XML tag
- <c> C# XML tag
ms.assetid: aad5b16e-a29e-445e-bd0d-eea0b138d7b2
caps.latest.revision: 12
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
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 5a06e25061d4b98ee5e299089455224d39363a63
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="ltcgt-c-programming-guide"></a>&lt;c&gt; (Guida per programmatori C#)
## <a name="syntax"></a>Sintassi  
  
```xml  
<c>text</c>  
```  
  
#### <a name="parameters"></a>Parametri  
 `text`  
 Il testo che si desidera indicare come codice.  
  
## <a name="remarks"></a>Note  
 Il tag \<c> consente di indicare che il testo all'interno di una descrizione deve essere contrassegnato come codice. Usare [\<code>](../../../csharp/programming-guide/xmldoc/code.md) per indicare più righe come codice.  
  
 Compilare con [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) per elaborare i commenti relativi alla documentazione in un file.  
  
## <a name="example"></a>Esempio  
 [!code-cs[csProgGuideDocComments#2](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/code-inline_1.cs)]  
  
## <a name="see-also"></a>Vedere anche  
 [Guida per programmatori C#](../../../csharp/programming-guide/index.md)   
 [Tag consigliati per i commenti relativi alla documentazione](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)

