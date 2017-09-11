---
title: Posticipata esecuzione e valutazione differita in LINQ to XML (Visual Basic) | Documenti di Microsoft
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
ms.assetid: 31998eed-b95e-47fb-a865-9de1f337d1fb
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 9ecb4d18cf7c61442e17de1c0f08824b360362e1
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017


---
# <a name="deferred-execution-and-lazy-evaluation-in-linq-to-xml-visual-basic"></a><span data-ttu-id="69d00-102">Esecuzione posticipata e valutazione differita in LINQ to XML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="69d00-102">Deferred Execution and Lazy Evaluation in LINQ to XML (Visual Basic)</span></span>
<span data-ttu-id="69d00-103">Operazioni di query e su asse vengono spesso implementate in modo da usare l'esecuzione posticipata.</span><span class="sxs-lookup"><span data-stu-id="69d00-103">Query and axis operations are often implemented to use deferred execution.</span></span> <span data-ttu-id="69d00-104">In questo argomento vengono illustrati requisiti e vantaggi dell'esecuzione posticipata e vengono fornite alcune considerazioni sull'implementazione.</span><span class="sxs-lookup"><span data-stu-id="69d00-104">This topic explains the requirements and advantages of deferred execution, and some implementation considerations.</span></span>  
  
## <a name="deferred-execution"></a><span data-ttu-id="69d00-105">Esecuzione posticipata</span><span class="sxs-lookup"><span data-stu-id="69d00-105">Deferred Execution</span></span>  
 <span data-ttu-id="69d00-106">Esecuzione posticipata si intende che la valutazione di un'espressione viene ritardata finché il relativo *realizzato* valore risulta effettivamente necessario.</span><span class="sxs-lookup"><span data-stu-id="69d00-106">Deferred execution means that the evaluation of an expression is delayed until its *realized* value is actually required.</span></span> <span data-ttu-id="69d00-107">L'esecuzione posticipata può contribuire a migliorare notevolmente le prestazioni quando è necessario modificare grandi raccolte di dati, in particolare in programmi che contengono una serie di modifiche o query concatenate.</span><span class="sxs-lookup"><span data-stu-id="69d00-107">Deferred execution can greatly improve performance when you have to manipulate large data collections, especially in programs that contain a series of chained queries or manipulations.</span></span> <span data-ttu-id="69d00-108">Nel migliore dei casi l'esecuzione posticipata consente di eseguire un'unica iterazione nella raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="69d00-108">In the best case, deferred execution enables only a single iteration through the source collection.</span></span>  
  
 <span data-ttu-id="69d00-109">Le tecnologie LINQ usano ampiamente l'esecuzione posticipata sia nei membri di base <xref:System.Linq?displayProperty=fullName>classi e nei metodi di estensione negli spazi dei nomi diversi di LINQ, ad esempio <xref:System.Xml.Linq.Extensions?displayProperty=fullName>.</xref:System.Xml.Linq.Extensions?displayProperty=fullName> </xref:System.Linq?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="69d00-109">The LINQ technologies make extensive use of deferred execution in both the members of core <xref:System.Linq?displayProperty=fullName> classes and in the extension methods in the various LINQ namespaces, such as <xref:System.Xml.Linq.Extensions?displayProperty=fullName>.</span></span>  
  
## <a name="eager-vs-lazy-evaluation"></a><span data-ttu-id="69d00-110">Valutazione eager e valutazione lazy</span><span class="sxs-lookup"><span data-stu-id="69d00-110">Eager vs. Lazy Evaluation</span></span>  
 <span data-ttu-id="69d00-111">Quando si scrive un metodo che implementa l'esecuzione posticipata, è inoltre necessario decidere se implementare il metodo tramite la valutazione lazy o la valutazione eager.</span><span class="sxs-lookup"><span data-stu-id="69d00-111">When you write a method that implements deferred execution, you also have to decide whether to implement the method using lazy evaluation or eager evaluation.</span></span>  
  
-   <span data-ttu-id="69d00-112">In *valutazione lazy*, durante ogni chiamata all'iteratore viene elaborato un singolo elemento della raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="69d00-112">In *lazy evaluation*, a single element of the source collection is processed during each call to the iterator.</span></span> <span data-ttu-id="69d00-113">Si tratta della modalità di implementazione tipica degli iteratori.</span><span class="sxs-lookup"><span data-stu-id="69d00-113">This is the typical way in which iterators are implemented.</span></span>  
  
-   <span data-ttu-id="69d00-114">In *valutazione eager*, la prima chiamata all'iteratore comporterà l'intera raccolta in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="69d00-114">In *eager evaluation*, the first call to the iterator will result in the entire collection being processed.</span></span> <span data-ttu-id="69d00-115">Potrebbe inoltre essere necessaria una copia temporanea della raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="69d00-115">A temporary copy of the source collection might also be required.</span></span> <span data-ttu-id="69d00-116">Ad esempio, il <xref:System.Linq.Enumerable.OrderBy%2A>metodo deve ordinare l'intera raccolta prima di restituire il primo elemento.</xref:System.Linq.Enumerable.OrderBy%2A></span><span class="sxs-lookup"><span data-stu-id="69d00-116">For example, the <xref:System.Linq.Enumerable.OrderBy%2A> method has to sort the entire collection before it returns the first element.</span></span>  
  
 <span data-ttu-id="69d00-117">La valutazione lazy offre in genere prestazioni migliori perché implica una distribuzione uniforme dell'overhead di elaborazione in tutte le fasi della valutazione della raccolta e riduce al minimo l'uso di dati temporanei.</span><span class="sxs-lookup"><span data-stu-id="69d00-117">Lazy evaluation usually yields better performance because it distributes overhead processing evenly throughout the evaluation of the collection and minimizes the use of temporary data.</span></span> <span data-ttu-id="69d00-118">Per alcune operazioni è naturalmente inevitabile dover materializzare i risultati intermedi.</span><span class="sxs-lookup"><span data-stu-id="69d00-118">Of course, for some operations, there is no other option than to materialize intermediate results.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="69d00-119">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="69d00-119">Next Steps</span></span>  
 <span data-ttu-id="69d00-120">Nel successivo argomento dell'esercitazione verrà illustrata l'esecuzione posticipata:</span><span class="sxs-lookup"><span data-stu-id="69d00-120">The next topic in this tutorial illustrates deferred execution:</span></span>  
  
-   [<span data-ttu-id="69d00-121">Esempio di esecuzione posticipata (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="69d00-121">Deferred Execution Example (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/deferred-execution-example.md)  
  
## <a name="see-also"></a><span data-ttu-id="69d00-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="69d00-122">See Also</span></span>  
 <span data-ttu-id="69d00-123">[Esercitazione: Posticipata esecuzione (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/tutorial-deferred-execution.md) </span><span class="sxs-lookup"><span data-stu-id="69d00-123">[Tutorial: Deferred Execution (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/tutorial-deferred-execution.md) </span></span>  
<span data-ttu-id="69d00-124"> [Concetti e terminologia (trasformazione funzionale) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/concepts-and-terminology-functional-transformation.md) </span><span class="sxs-lookup"><span data-stu-id="69d00-124"> [Concepts and Terminology (Functional Transformation) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/concepts-and-terminology-functional-transformation.md) </span></span>  
<span data-ttu-id="69d00-125"> [Operazioni di aggregazione (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/aggregation-operations.md)</span><span class="sxs-lookup"><span data-stu-id="69d00-125"> [Aggregation Operations (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/aggregation-operations.md)</span></span>
