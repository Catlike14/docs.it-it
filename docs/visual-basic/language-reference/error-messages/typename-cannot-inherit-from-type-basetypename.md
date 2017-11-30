---
title: "&#39; &lt;typename&gt;&#39; non può ereditare da &lt;tipo&gt; &#39;&lt; nomeTipoBase&gt;&#39; perché espande l'accesso di base &lt;tipo&gt; all'esterno dell'assembly"
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc30910
- bc30910
helpviewer_keywords: BC30910
ms.assetid: 68fc05c5-5d55-4742-9a3b-ea04312594f4
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d01981d3136968ae2534539b8eccab4c5c535fbc
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="39lttypenamegt39-cannot-inherit-from-lttypegt-39ltbasetypenamegt39-because-it-expands-the-access-of-the-base-lttypegt-outside-the-assembly"></a><span data-ttu-id="db609-102">&#39; &lt;typename&gt;&#39; non può ereditare da &lt;tipo&gt; &#39;&lt; nomeTipoBase&gt;&#39; perché espande l'accesso di base &lt;tipo&gt; all'esterno dell'assembly</span><span class="sxs-lookup"><span data-stu-id="db609-102">&#39;&lt;typename&gt;&#39; cannot inherit from &lt;type&gt; &#39;&lt;basetypename&gt;&#39; because it expands the access of the base &lt;type&gt; outside the assembly</span></span>
<span data-ttu-id="db609-103">Una classe o interfaccia eredita da una classe di base o interfaccia ma con un livello di accesso meno restrittivo.</span><span class="sxs-lookup"><span data-stu-id="db609-103">A class or interface inherits from a base class or interface but has a less restrictive access level.</span></span>  
  
 <span data-ttu-id="db609-104">Ad esempio, un `Public` interfaccia eredita da un `Friend` , interfaccia o un `Protected` classe eredita da un `Private` classe.</span><span class="sxs-lookup"><span data-stu-id="db609-104">For example, a `Public` interface inherits from a `Friend` interface, or a `Protected` class inherits from a `Private` class.</span></span> <span data-ttu-id="db609-105">Espone la classe di base o l'interfaccia per accedere a oltre il livello desiderato.</span><span class="sxs-lookup"><span data-stu-id="db609-105">This exposes the base class or interface to access beyond the intended level.</span></span>  
  
 <span data-ttu-id="db609-106">**ID errore:** BC30910</span><span class="sxs-lookup"><span data-stu-id="db609-106">**Error ID:** BC30910</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="db609-107">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="db609-107">To correct this error</span></span>  
  
-   <span data-ttu-id="db609-108">Modificare il livello di accesso della classe derivata o dell'interfaccia sia restrittiva almeno quanto quella della classe base o interfaccia.</span><span class="sxs-lookup"><span data-stu-id="db609-108">Change the access level of the derived class or interface to be at least as restrictive as that of the base class or interface.</span></span>  
  
     <span data-ttu-id="db609-109">-oppure-</span><span class="sxs-lookup"><span data-stu-id="db609-109">-or-</span></span>  
  
-   <span data-ttu-id="db609-110">Se è necessario il livello di accesso meno restrittivo, rimuovere il `Inherits` istruzione.</span><span class="sxs-lookup"><span data-stu-id="db609-110">If you require the less restrictive access level, remove the `Inherits` statement.</span></span> <span data-ttu-id="db609-111">È possibile ereditare da una classe di base più limitata o un'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="db609-111">You cannot inherit from a more restricted base class or interface.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="db609-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="db609-112">See Also</span></span>  
 [<span data-ttu-id="db609-113">Istruzione Class</span><span class="sxs-lookup"><span data-stu-id="db609-113">Class Statement</span></span>](../../../visual-basic/language-reference/statements/class-statement.md)  
 [<span data-ttu-id="db609-114">Istruzione Interface</span><span class="sxs-lookup"><span data-stu-id="db609-114">Interface Statement</span></span>](../../../visual-basic/language-reference/statements/interface-statement.md)  
 [<span data-ttu-id="db609-115">Istruzione Inherits</span><span class="sxs-lookup"><span data-stu-id="db609-115">Inherits Statement</span></span>](../../../visual-basic/language-reference/statements/inherits-statement.md)  
 [<span data-ttu-id="db609-116">Livelli di accesso in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="db609-116">Access levels in Visual Basic</span></span>](../../../visual-basic/programming-guide/language-features/declared-elements/access-levels.md)
