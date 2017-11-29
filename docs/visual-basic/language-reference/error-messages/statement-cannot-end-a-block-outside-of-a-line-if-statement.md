---
title: "L'istruzione non può terminare un blocco all'esterno di una riga &#39; se &#39; istruzione"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc32005
- bc32005
helpviewer_keywords: BC32005
ms.assetid: 4039f51b-e0ee-4789-a89b-45d06de06b5d
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 73fe3eb44e904366db7d505bbe8c5fef461eb78b
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="statement-cannot-end-a-block-outside-of-a-line-39if39-statement"></a><span data-ttu-id="94573-102">L'istruzione non può terminare un blocco all'esterno di una riga &#39; se &#39; istruzione</span><span class="sxs-lookup"><span data-stu-id="94573-102">Statement cannot end a block outside of a line &#39;If&#39; statement</span></span>
<span data-ttu-id="94573-103">Una riga singola `If` istruzione contiene più istruzioni separate da punti (:), di cui uno è un `End` istruzione per un blocco di controllo esterno a riga singola `If`.</span><span class="sxs-lookup"><span data-stu-id="94573-103">A single-line `If` statement contains several statements separated by colons (:), one of which is an `End` statement for a control block outside the single-line `If`.</span></span> <span data-ttu-id="94573-104">Riga singola `If` istruzioni non utilizzano il `End If` istruzione.</span><span class="sxs-lookup"><span data-stu-id="94573-104">Single-line `If` statements do not use the `End If` statement.</span></span>  
  
 <span data-ttu-id="94573-105">**ID errore:** BC32005</span><span class="sxs-lookup"><span data-stu-id="94573-105">**Error ID:** BC32005</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="94573-106">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="94573-106">To correct this error</span></span>  
  
-   <span data-ttu-id="94573-107">Spostare il controllo a riga singola `If` istruzione all'esterno del blocco di controllo che contiene il `End If` istruzione.</span><span class="sxs-lookup"><span data-stu-id="94573-107">Move the single-line `If` statement outside the control block that contains the `End If` statement.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="94573-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="94573-108">See Also</span></span>  
 [<span data-ttu-id="94573-109">Istruzione If...Then...Else</span><span class="sxs-lookup"><span data-stu-id="94573-109">If...Then...Else Statement</span></span>](../../../visual-basic/language-reference/statements/if-then-else-statement.md)
