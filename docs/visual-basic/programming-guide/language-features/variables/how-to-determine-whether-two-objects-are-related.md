---
title: 'Procedura: determinare se due oggetti sono correlati (Visual Basic)'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- inheritance [Visual Basic], Visual Basic objects
- objects [Visual Basic], inheritance
- object variables [Visual Basic], determining relation
ms.assetid: da002e3f-6616-4bad-a229-f842d06652bb
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 7824742459fca355c0043ad8ed20a26330402c05
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-determine-whether-two-objects-are-related-visual-basic"></a><span data-ttu-id="ea0f9-102">Procedura: determinare se due oggetti sono correlati (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ea0f9-102">How to: Determine Whether Two Objects Are Related (Visual Basic)</span></span>
<span data-ttu-id="ea0f9-103">È possibile confrontare due oggetti per determinare la relazione, se presente, tra le classi da cui vengono creati.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-103">You can compare two objects to determine the relationship, if any, between the classes from which they are created.</span></span> <span data-ttu-id="ea0f9-104">Il <xref:System.Type.IsInstanceOfType%2A> metodo il <xref:System.Type?displayProperty=nameWithType> classe restituisce `True` se la classe specificata eredita dalla classe corrente o se il tipo corrente è un'interfaccia supportata dalla classe specificata.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-104">The <xref:System.Type.IsInstanceOfType%2A> method of the <xref:System.Type?displayProperty=nameWithType> class returns `True` if the specified class inherits from the current class, or if the current type is an interface supported by the specified class.</span></span>  
  
### <a name="to-determine-if-one-object-inherits-from-another-objects-class-or-interface"></a><span data-ttu-id="ea0f9-105">Per determinare se un oggetto eredita dalla classe o interfaccia di un altro oggetto</span><span class="sxs-lookup"><span data-stu-id="ea0f9-105">To determine if one object inherits from another object's class or interface</span></span>  
  
1.  <span data-ttu-id="ea0f9-106">Per l'oggetto si ritiene che potrebbero essere del tipo di base, richiamare il <xref:System.Object.GetType%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-106">On the object you think might be of the base type, invoke the <xref:System.Object.GetType%2A> method.</span></span>  
  
2.  <span data-ttu-id="ea0f9-107">Nel <xref:System.Type?displayProperty=nameWithType> oggetto restituito da <xref:System.Object.GetType%2A>, richiamare il <xref:System.Type.IsInstanceOfType%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-107">On the <xref:System.Type?displayProperty=nameWithType> object returned by <xref:System.Object.GetType%2A>, invoke the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>  
  
3.  <span data-ttu-id="ea0f9-108">Nell'elenco di argomenti per <xref:System.Type.IsInstanceOfType%2A>, specificare l'oggetto si ritiene che potrà essere del tipo derivato.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-108">In the argument list for <xref:System.Type.IsInstanceOfType%2A>, specify the object you think might be of the derived type.</span></span>  
  
     <span data-ttu-id="ea0f9-109"><xref:System.Type.IsInstanceOfType%2A>Restituisce `True` se il tipo di argomento eredita il <xref:System.Type?displayProperty=nameWithType> tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-109"><xref:System.Type.IsInstanceOfType%2A> returns `True` if its argument type inherits from the <xref:System.Type?displayProperty=nameWithType> object type.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ea0f9-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="ea0f9-110">Example</span></span>  
 <span data-ttu-id="ea0f9-111">Nell'esempio seguente determina se un oggetto rappresenta una classe derivata dalla classe dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-111">The following example determines whether one object represents a class derived from another object's class.</span></span>  
  
```  
Public Class baseClass  
End Class  
Public Class derivedClass : Inherits baseClass  
End Class  
Public Class testTheseClasses  
    Public Sub seeIfRelated()  
        Dim baseObj As Object = New baseClass()  
        Dim derivedObj As Object = New derivedClass()  
        Dim related As Boolean  
        related = baseObj.GetType().IsInstanceOfType(derivedObj)  
        MsgBox(CStr(related))  
    End Sub  
End Class  
```  
  
 <span data-ttu-id="ea0f9-112">Si noti la posizione imprevista delle due variabili oggetto nella chiamata a <xref:System.Type.IsInstanceOfType%2A>.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-112">Note the unexpected placement of the two object variables in the call to <xref:System.Type.IsInstanceOfType%2A>.</span></span> <span data-ttu-id="ea0f9-113">Il tipo base previsto viene utilizzato per generare il <xref:System.Type?displayProperty=nameWithType> classe e il tipo derivato previsto viene passata come argomento per il <xref:System.Type.IsInstanceOfType%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="ea0f9-113">The supposed base type is used to generate the <xref:System.Type?displayProperty=nameWithType> class, and the supposed derived type is passed as an argument to the <xref:System.Type.IsInstanceOfType%2A> method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea0f9-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ea0f9-114">See Also</span></span>  
 <xref:System.Object.GetType%2A>  
 <xref:System.Type?displayProperty=nameWithType>  
 <xref:System.Type.IsInstanceOfType%2A>  
 [<span data-ttu-id="ea0f9-115">Tipo di dati Object</span><span class="sxs-lookup"><span data-stu-id="ea0f9-115">Object Data Type</span></span>](../../../../visual-basic/language-reference/data-types/object-data-type.md)  
 [<span data-ttu-id="ea0f9-116">Variabili oggetto</span><span class="sxs-lookup"><span data-stu-id="ea0f9-116">Object Variables</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variables.md)  
 [<span data-ttu-id="ea0f9-117">Valori di variabili oggetto</span><span class="sxs-lookup"><span data-stu-id="ea0f9-117">Object Variable Values</span></span>](../../../../visual-basic/programming-guide/language-features/variables/object-variable-values.md)  
 [<span data-ttu-id="ea0f9-118">Procedura: determinare se due oggetti sono identici</span><span class="sxs-lookup"><span data-stu-id="ea0f9-118">How to: Determine Whether Two Objects Are Identical</span></span>](../../../../visual-basic/programming-guide/language-features/variables/how-to-determine-whether-two-objects-are-identical.md)
