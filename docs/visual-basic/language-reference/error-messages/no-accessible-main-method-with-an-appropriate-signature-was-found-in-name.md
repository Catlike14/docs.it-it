---
title: "Non è accessibile &#39; Main &#39; metodo con una firma appropriata è stato trovato &#39; &lt;nome&gt;&#39;"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- bc30737
- vbc30737
helpviewer_keywords: BC30737
ms.assetid: 3f40bacd-3fac-4741-b204-852f693d4340
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 3f45dc17304c3c9d62b65760f2c1b5d461812a66
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="no-accessible-39main39-method-with-an-appropriate-signature-was-found-in-39ltnamegt39"></a><span data-ttu-id="b547b-102">Non è accessibile &#39; Main &#39; metodo con una firma appropriata è stato trovato &#39; &lt;nome&gt;&#39;</span><span class="sxs-lookup"><span data-stu-id="b547b-102">No accessible &#39;Main&#39; method with an appropriate signature was found in &#39;&lt;name&gt;&#39;</span></span>
<span data-ttu-id="b547b-103">Applicazioni della riga di comando devono avere un `Sub Main` definito.</span><span class="sxs-lookup"><span data-stu-id="b547b-103">Command-line applications must have a `Sub Main` defined.</span></span> <span data-ttu-id="b547b-104">`Main`deve essere dichiarato come `Public Shared` se è definito in una classe o come `Public` se definita in un modulo.</span><span class="sxs-lookup"><span data-stu-id="b547b-104">`Main` must be declared as `Public Shared` if it is defined in a class, or as `Public` if defined in a module.</span></span>  
  
 <span data-ttu-id="b547b-105">Per ulteriori informazioni su `Main`, vedere [NIB: Visual Basic versione di Hello, World](http://msdn.microsoft.com/en-us/9d030b60-e148-4366-a462-69532f02294c).</span><span class="sxs-lookup"><span data-stu-id="b547b-105">For more information on `Main`, see [NIB: Visual Basic Version of Hello, World](http://msdn.microsoft.com/en-us/9d030b60-e148-4366-a462-69532f02294c).</span></span>  
  
 <span data-ttu-id="b547b-106">**ID errore:** BC30737</span><span class="sxs-lookup"><span data-stu-id="b547b-106">**Error ID:** BC30737</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="b547b-107">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="b547b-107">To correct this error</span></span>  
  
-   <span data-ttu-id="b547b-108">Definire un `Public Sub Main` procedure per il progetto.</span><span class="sxs-lookup"><span data-stu-id="b547b-108">Define a `Public Sub Main` procedure for your project.</span></span> <span data-ttu-id="b547b-109">Dichiara la classe come `Shared` se e solo se viene definita in una classe.</span><span class="sxs-lookup"><span data-stu-id="b547b-109">Declare it as `Shared` if and only if you define it inside a class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b547b-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b547b-110">See Also</span></span>  
 [<span data-ttu-id="b547b-111">NIB: versione di Visual Basic di Hello, World</span><span class="sxs-lookup"><span data-stu-id="b547b-111">NIB: Visual Basic Version of Hello, World</span></span>](http://msdn.microsoft.com/en-us/9d030b60-e148-4366-a462-69532f02294c)  
 [<span data-ttu-id="b547b-112">Struttura di un programma Visual Basic</span><span class="sxs-lookup"><span data-stu-id="b547b-112">Structure of a Visual Basic Program</span></span>](../../../visual-basic/programming-guide/program-structure/structure-of-a-visual-basic-program.md)  
 [<span data-ttu-id="b547b-113">Routine</span><span class="sxs-lookup"><span data-stu-id="b547b-113">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)
