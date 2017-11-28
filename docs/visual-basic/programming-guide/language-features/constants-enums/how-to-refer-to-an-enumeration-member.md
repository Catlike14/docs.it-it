---
title: 'Procedura: fare riferimento a un membro di enumerazione (Visual Basic)'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- enumerations [Visual Basic], referring to
- values [Visual Basic], associating constant values with names
- enumeration members
- constants [Visual Basic], enumerated
ms.assetid: bbb5c3cc-7cdb-4814-8d6a-a6d91546ed1e
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: ae4e6eb9c011095c6cf0abe1ee3ac7a68f156f01
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-refer-to-an-enumeration-member-visual-basic"></a><span data-ttu-id="869a9-102">Procedura: fare riferimento a un membro di enumerazione (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="869a9-102">How to: Refer to an Enumeration Member (Visual Basic)</span></span>
<span data-ttu-id="869a9-103">Le enumerazioni forniscono un modo pratico per utilizzare i set di costanti correlate e per associare ai nomi di valori costanti.</span><span class="sxs-lookup"><span data-stu-id="869a9-103">Enumerations provide a convenient way to work with sets of related constants and to associate constant values with names.</span></span> <span data-ttu-id="869a9-104">Ad esempio, si può dichiarare un'enumerazione per un set di costanti integer associate ai giorni della settimana e quindi usare i nomi dei giorni anziché i relativi valori integer nel codice.</span><span class="sxs-lookup"><span data-stu-id="869a9-104">For example, you can declare an enumeration for a set of integer constants associated with the days of the week, and then use the names of the days rather than their integer values in your code.</span></span>  
  
 <span data-ttu-id="869a9-105">È possibile evitare l'utilizzo dei nomi completi con il `Imports` istruzione.</span><span class="sxs-lookup"><span data-stu-id="869a9-105">You can avoid using fully qualified names with the `Imports` statement.</span></span> <span data-ttu-id="869a9-106">Per ulteriori informazioni, vedere [qualifica di nomi ed enumerazioni](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span><span class="sxs-lookup"><span data-stu-id="869a9-106">For more information, see [Enumerations and Name Qualification](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md).</span></span>  
  
### <a name="to-refer-to-an-enumeration-member"></a><span data-ttu-id="869a9-107">Per fare riferimento a un membro di enumerazione</span><span class="sxs-lookup"><span data-stu-id="869a9-107">To refer to an enumeration member</span></span>  
  
-   <span data-ttu-id="869a9-108">Qualificare il nome del membro con l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="869a9-108">Qualify the member name with the enumeration.</span></span> <span data-ttu-id="869a9-109">Ad esempio, nell'esempio seguente assegna la `Saturday` appartenente il `FirstDayOfWeek` enumerazione alla variabile `DayValue`.</span><span class="sxs-lookup"><span data-stu-id="869a9-109">For example, the following example assigns the `Saturday` member of the `FirstDayOfWeek` enumeration to the variable `DayValue`.</span></span>  
  
     [!code-vb[VbEnumsTask#19](../../../../visual-basic/language-reference/statements/codesnippet/VisualBasic/how-to-refer-to-an-enumeration-member_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="869a9-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="869a9-110">See Also</span></span>  
 [<span data-ttu-id="869a9-111">Procedura: dichiarare un'enumerazione</span><span class="sxs-lookup"><span data-stu-id="869a9-111">How to: Declare an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-declare-enumerations.md)  
 [<span data-ttu-id="869a9-112">Qualifica di nomi ed enumerazioni</span><span class="sxs-lookup"><span data-stu-id="869a9-112">Enumerations and Name Qualification</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/enumerations-and-name-qualification.md)  
 [<span data-ttu-id="869a9-113">Procedura: scorrere un'enumerazione in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="869a9-113">How to: Iterate Through An Enumeration in Visual Basic</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-iterate-through-an-enumeration.md)  
 [<span data-ttu-id="869a9-114">Procedura: Determinare la stringa associata a un valore di enumerazione</span><span class="sxs-lookup"><span data-stu-id="869a9-114">How to: Determine the String Associated with an Enumeration Value</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/how-to-determine-the-string-associated-with-an-enumeration-value.md)  
 [<span data-ttu-id="869a9-115">Quando usare un'enumerazione</span><span class="sxs-lookup"><span data-stu-id="869a9-115">When to Use an Enumeration</span></span>](../../../../visual-basic/programming-guide/language-features/constants-enums/when-to-use-an-enumeration.md)
