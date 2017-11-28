---
title: Conversione implicita da &#39; &lt;NomeTipo1&gt;&#39; a &#39;&lt; NomeTipo2&gt;&#39; copiare il valore di &#39; ByRef &#39; parametro &#39; &lt;parametername&gt;&#39; back nell'argomento corrispondente.
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords:
- vbc41999
- bc41999
helpviewer_keywords: BC41999
ms.assetid: ae48c738-dff8-4c0f-8931-bbb70b2c8b03
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 9e858b475a816a35d18822643de5a273abe28562
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="implicit-conversion-from-39lttypename1gt39-to-39lttypename2gt39-in-copying-the-value-of-39byref39-parameter-39ltparameternamegt39-back-to-the-matching-argument"></a><span data-ttu-id="3247a-102">Conversione implicita da &#39; &lt;NomeTipo1&gt;&#39; a &#39;&lt; NomeTipo2&gt;&#39; copiare il valore di &#39; ByRef &#39; parametro &#39; &lt;parametername&gt;&#39; back nell'argomento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3247a-102">Implicit conversion from &#39;&lt;typename1&gt;&#39; to &#39;&lt;typename2&gt;&#39; in copying the value of &#39;ByRef&#39; parameter &#39;&lt;parametername&gt;&#39; back to the matching argument.</span></span>
<span data-ttu-id="3247a-103">Una routine viene chiamata con un [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) argomento di tipo diverso rispetto a quello del parametro corrispondente.</span><span class="sxs-lookup"><span data-stu-id="3247a-103">A procedure is called with a [ByRef](../../../visual-basic/language-reference/modifiers/byref.md) argument of a different type than that of its corresponding parameter.</span></span>  
  
 <span data-ttu-id="3247a-104">Se si passa un argomento `ByRef`, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] copia a volte il valore dell'argomento in una variabile locale nella routine invece di passare un riferimento.</span><span class="sxs-lookup"><span data-stu-id="3247a-104">If you pass an argument `ByRef`, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] sometimes copies the argument value into a local variable in the procedure instead of passing a reference.</span></span> <span data-ttu-id="3247a-105">In un caso simile, alla restituzione della routine [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] deve quindi ricopiare il valore della variabile locale nell'argomento nel codice chiamante.</span><span class="sxs-lookup"><span data-stu-id="3247a-105">In such a case, when the procedure returns, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] must then copy the local variable value back into the argument in the calling code.</span></span>  
  
 <span data-ttu-id="3247a-106">Se un valore dell'argomento `ByRef` viene copiato nella routine e l'argomento e il parametro sono dello stesso tipo, non è necessaria alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="3247a-106">If a `ByRef` argument value is copied into the procedure and the argument and parameter are of the same type, no conversion is necessary.</span></span> <span data-ttu-id="3247a-107">Se invece i tipi sono diversi, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] deve eseguire la conversione in entrambe le direzioni.</span><span class="sxs-lookup"><span data-stu-id="3247a-107">But if the types are different, [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] must convert in both directions.</span></span> <span data-ttu-id="3247a-108">Poiché non è possibile utilizzare `CType` o una delle altre parole chiave di conversione su un argomento di routine o parametro, tale conversione è sempre implicita.</span><span class="sxs-lookup"><span data-stu-id="3247a-108">Because you cannot use `CType` or any of the other conversion keywords on a procedure argument or parameter, such a conversion is always implicit.</span></span>  
  
 <span data-ttu-id="3247a-109">Per impostazione predefinita, si tratta di un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="3247a-109">By default, this message is a warning.</span></span> <span data-ttu-id="3247a-110">Per informazioni su come nascondere gli avvisi o considerarli come errori, vedere [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span><span class="sxs-lookup"><span data-stu-id="3247a-110">For information on hiding warnings or treating warnings as errors, see [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).</span></span>  
  
 <span data-ttu-id="3247a-111">**ID errore:** BC41999</span><span class="sxs-lookup"><span data-stu-id="3247a-111">**Error ID:** BC41999</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="3247a-112">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="3247a-112">To correct this error</span></span>  
  
-   <span data-ttu-id="3247a-113">Se possibile, usare un argomento chiamante dello stesso tipo del parametro della routine, in modo che [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] non debba eseguire alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="3247a-113">If possible, use a calling argument of the same type as the procedure parameter, so [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] does not need to do any conversion.</span></span>  
  
-   <span data-ttu-id="3247a-114">Se è necessario chiamare la routine con un argomento di tipo diverso dal tipo di parametro ma non è necessario restituire un valore nell'argomento chiamante, definire il parametro come [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) anziché `ByRef`.</span><span class="sxs-lookup"><span data-stu-id="3247a-114">If you need to call the procedure with an argument type different from the parameter type but do not need to return a value into the calling argument, define the parameter to be [ByVal](../../../visual-basic/language-reference/modifiers/byval.md) instead of `ByRef`.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3247a-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3247a-115">See Also</span></span>  
 [<span data-ttu-id="3247a-116">Routine</span><span class="sxs-lookup"><span data-stu-id="3247a-116">Procedures</span></span>](../../../visual-basic/programming-guide/language-features/procedures/index.md)  
 [<span data-ttu-id="3247a-117">Parametri e argomenti delle routine</span><span class="sxs-lookup"><span data-stu-id="3247a-117">Procedure Parameters and Arguments</span></span>](../../../visual-basic/programming-guide/language-features/procedures/procedure-parameters-and-arguments.md)  
 [<span data-ttu-id="3247a-118">Passaggio di argomenti per valore e per riferimento</span><span class="sxs-lookup"><span data-stu-id="3247a-118">Passing Arguments by Value and by Reference</span></span>](../../../visual-basic/programming-guide/language-features/procedures/passing-arguments-by-value-and-by-reference.md)  
 [<span data-ttu-id="3247a-119">Conversioni implicite ed esplicite</span><span class="sxs-lookup"><span data-stu-id="3247a-119">Implicit and Explicit Conversions</span></span>](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
