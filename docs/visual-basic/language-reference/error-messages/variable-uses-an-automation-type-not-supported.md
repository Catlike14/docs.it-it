---
title: La variabile utilizza un tipo di automazione non supportato in Visual Basic | Documenti di Microsoft
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbrID458
dev_langs:
- VB
ms.assetid: bde4f4da-493b-452c-b6e4-1d370edba4cd
caps.latest.revision: 12
author: dotnet-bot
ms.author: dotnetcontent
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 74c4472230a3a8c54859771c0b2f7fc954ac0966
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="variable-uses-an-automation-type-not-supported-in-visual-basic"></a><span data-ttu-id="32e67-102">La variabile utilizza un tipo di automazione non supportato in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="32e67-102">Variable uses an Automation type not supported in Visual Basic</span></span>
<span data-ttu-id="32e67-103">Si è tentato di utilizzare una variabile definita in una libreria dei tipi o oggetti con un tipo di dati non supportato da [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].</span><span class="sxs-lookup"><span data-stu-id="32e67-103">You tried to use a variable defined in a type library or object library that has a data type not supported by [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="32e67-104">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="32e67-104">To correct this error</span></span>  
  
-   <span data-ttu-id="32e67-105">Utilizzare una variabile di tipo riconosciuto da [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].</span><span class="sxs-lookup"><span data-stu-id="32e67-105">Use a variable of a type recognized by [!INCLUDE[vbprvb](../../../csharp/programming-guide/concepts/linq/includes/vbprvb_md.md)].</span></span>  
  
     <span data-ttu-id="32e67-106">-oppure-</span><span class="sxs-lookup"><span data-stu-id="32e67-106">-or-</span></span>  
  
-   <span data-ttu-id="32e67-107">Se questo errore si verifica durante l'utilizzo di `FileGet` o `FileGetOBject`, assicurarsi che il file si sta tentando di utilizzare è stato scritto con `FilePut` o `FilePutObject`.</span><span class="sxs-lookup"><span data-stu-id="32e67-107">If you encounter this error while using `FileGet` or `FileGetOBject`, make sure the file you are trying to use was written to with `FilePut` or `FilePutObject`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="32e67-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="32e67-108">See Also</span></span>  
 [<span data-ttu-id="32e67-109">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="32e67-109">Data Types</span></span>](../../../visual-basic/language-reference/data-types/data-type-summary.md)
