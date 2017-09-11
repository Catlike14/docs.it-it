---
title: Operazioni di proiezione (Visual Basic) | Documenti di Microsoft
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
ms.assetid: b8d38e6d-21cf-4619-8dbb-94476f4badc7
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: aac5cf69e6c3f4041a4302e8d606ca8dfddbc8a2
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="projection-operations-visual-basic"></a><span data-ttu-id="9beb8-102">Operazioni di proiezione (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="9beb8-102">Projection Operations (Visual Basic)</span></span>
<span data-ttu-id="9beb8-103">Proiezione si riferisce all'operazione di trasformazione di un oggetto in un nuovo form che spesso costituita solo le proprietà che verranno utilizzate successivamente.</span><span class="sxs-lookup"><span data-stu-id="9beb8-103">Projection refers to the operation of transforming an object into a new form that often consists only of those properties that will be subsequently used.</span></span> <span data-ttu-id="9beb8-104">Utilizzando la proiezione, è possibile costruire un nuovo tipo compilato in base a ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="9beb8-104">By using projection, you can construct a new type that is built from each object.</span></span> <span data-ttu-id="9beb8-105">È possibile proiettare una proprietà ed eseguire una funzione matematica su di esso.</span><span class="sxs-lookup"><span data-stu-id="9beb8-105">You can project a property and perform a mathematical function on it.</span></span> <span data-ttu-id="9beb8-106">È inoltre possibile proiettare l'oggetto originale senza modificarlo.</span><span class="sxs-lookup"><span data-stu-id="9beb8-106">You can also project the original object without changing it.</span></span>  
  
 <span data-ttu-id="9beb8-107">Nella sezione seguente sono elencati i metodi dell'operatore query standard che eseguono la proiezione.</span><span class="sxs-lookup"><span data-stu-id="9beb8-107">The standard query operator methods that perform projection are listed in the following section.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="9beb8-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="9beb8-108">Methods</span></span>  
  
|<span data-ttu-id="9beb8-109">Nome metodo</span><span class="sxs-lookup"><span data-stu-id="9beb8-109">Method Name</span></span>|<span data-ttu-id="9beb8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9beb8-110">Description</span></span>|<span data-ttu-id="9beb8-111">Sintassi delle espressioni di Query Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9beb8-111">Visual Basic Query Expression Syntax</span></span>|<span data-ttu-id="9beb8-112">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="9beb8-112">More Information</span></span>|  
|-----------------|-----------------|------------------------------------------|----------------------|  
|<span data-ttu-id="9beb8-113">Seleziona</span><span class="sxs-lookup"><span data-stu-id="9beb8-113">Select</span></span>|<span data-ttu-id="9beb8-114">Valori di progetti basati su una funzione di trasformazione.</span><span class="sxs-lookup"><span data-stu-id="9beb8-114">Projects values that are based on a transform function.</span></span>|`Select`|<span data-ttu-id="9beb8-115"><xref:System.Linq.Enumerable.Select%2A?displayProperty=fullName></xref:System.Linq.Enumerable.Select%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="9beb8-115"><xref:System.Linq.Enumerable.Select%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="9beb8-116"><xref:System.Linq.Queryable.Select%2A?displayProperty=fullName></xref:System.Linq.Queryable.Select%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="9beb8-116"><xref:System.Linq.Queryable.Select%2A?displayProperty=fullName></span></span>|  
|<span data-ttu-id="9beb8-117">SelectMany</span><span class="sxs-lookup"><span data-stu-id="9beb8-117">SelectMany</span></span>|<span data-ttu-id="9beb8-118">Proietta le sequenze di valori che si basano su una funzione di trasformazione e quindi li converte in un'unica sequenza.</span><span class="sxs-lookup"><span data-stu-id="9beb8-118">Projects sequences of values that are based on a transform function and then flattens them into one sequence.</span></span>|<span data-ttu-id="9beb8-119">Utilizzare più `From` clausole</span><span class="sxs-lookup"><span data-stu-id="9beb8-119">Use multiple `From` clauses</span></span>|<span data-ttu-id="9beb8-120"><xref:System.Linq.Enumerable.SelectMany%2A?displayProperty=fullName></xref:System.Linq.Enumerable.SelectMany%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="9beb8-120"><xref:System.Linq.Enumerable.SelectMany%2A?displayProperty=fullName></span></span><br /><br /> <span data-ttu-id="9beb8-121"><xref:System.Linq.Queryable.SelectMany%2A?displayProperty=fullName></xref:System.Linq.Queryable.SelectMany%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="9beb8-121"><xref:System.Linq.Queryable.SelectMany%2A?displayProperty=fullName></span></span>|  
  
## <a name="query-expression-syntax-examples"></a><span data-ttu-id="9beb8-122">Esempi di sintassi delle espressioni di query</span><span class="sxs-lookup"><span data-stu-id="9beb8-122">Query Expression Syntax Examples</span></span>  
  
### <a name="select"></a><span data-ttu-id="9beb8-123">Seleziona</span><span class="sxs-lookup"><span data-stu-id="9beb8-123">Select</span></span>  
 <span data-ttu-id="9beb8-124">Nell'esempio seguente viene utilizzata la `Select` clausola per la prima lettera di ogni stringa in un elenco di stringhe del progetto.</span><span class="sxs-lookup"><span data-stu-id="9beb8-124">The following example uses the `Select` clause to project the first letter from each string in a list of strings.</span></span>  
  
```vb  
Dim words = New List(Of String) From {"an", "apple", "a", "day"}  
  
Dim query = From word In words   
            Select word.Substring(0, 1)  
  
Dim sb As New System.Text.StringBuilder()  
For Each letter As String In query  
    sb.AppendLine(letter)  
Next  
  
' Display the output.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' a  
' a  
' a  
' d  
```  
  
### <a name="selectmany"></a><span data-ttu-id="9beb8-125">SelectMany</span><span class="sxs-lookup"><span data-stu-id="9beb8-125">SelectMany</span></span>  
 <span data-ttu-id="9beb8-126">Nell'esempio seguente usa più `From` clausole per ogni parola di ogni stringa in un elenco di stringhe del progetto.</span><span class="sxs-lookup"><span data-stu-id="9beb8-126">The following example uses multiple `From` clauses to project each word from each string in a list of strings.</span></span>  
  
```vb  
Dim phrases = New List(Of String) From {"an apple a day", "the quick brown fox"}  
  
Dim query = From phrase In phrases   
            From word In phrase.Split(" "c)   
            Select word  
  
Dim sb As New System.Text.StringBuilder()  
For Each str As String In query  
    sb.AppendLine(str)  
Next  
  
' Display the output.  
MsgBox(sb.ToString())  
  
' This code produces the following output:  
  
' an  
' apple  
' a  
' day  
' the  
' quick  
' brown  
' fox  
```  
  
## <a name="select-versus-selectmany"></a><span data-ttu-id="9beb8-127">Selezionare e SelectMany</span><span class="sxs-lookup"><span data-stu-id="9beb8-127">Select versus SelectMany</span></span>  
 <span data-ttu-id="9beb8-128">La funzione di `Select()` e `SelectMany()` consiste nel produrre un valore di risultato (o valori) dai valori di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-128">The work of both `Select()` and `SelectMany()` is to produce a result value (or values) from source values.</span></span> <span data-ttu-id="9beb8-129">`Select()`produce un valore per ogni valore di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-129">`Select()` produces one result value for every source value.</span></span> <span data-ttu-id="9beb8-130">Il risultato complessivo è pertanto una raccolta con lo stesso numero di elementi della raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-130">The overall result is therefore a collection that has the same number of elements as the source collection.</span></span> <span data-ttu-id="9beb8-131">Al contrario, `SelectMany()` produce un unico risultato complessivo che contiene sottoraccolte concatenate di ogni valore di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-131">In contrast, `SelectMany()` produces a single overall result that contains concatenated sub-collections from each source value.</span></span> <span data-ttu-id="9beb8-132">La funzione di trasformazione che viene passata come argomento `SelectMany()` deve restituire una sequenza enumerabile di valori per ogni valore di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-132">The transform function that is passed as an argument to `SelectMany()` must return an enumerable sequence of values for each source value.</span></span> <span data-ttu-id="9beb8-133">Queste sequenze enumerabili vengono quindi concatenate da `SelectMany()` per creare una sequenza di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="9beb8-133">These enumerable sequences are then concatenated by `SelectMany()` to create one large sequence.</span></span>  
  
 <span data-ttu-id="9beb8-134">Nelle due figure seguenti mostrano la differenza tra le azioni di questi due metodi.</span><span class="sxs-lookup"><span data-stu-id="9beb8-134">The following two illustrations show the conceptual difference between the actions of these two methods.</span></span> <span data-ttu-id="9beb8-135">In ogni caso, si supponga che la funzione del selettore (transform) consente di selezionare la matrice di fiori da ogni valore di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-135">In each case, assume that the selector (transform) function selects the array of flowers from each source value.</span></span>  
  
 <span data-ttu-id="9beb8-136">Questa figura viene illustrato come `Select()` restituisce una raccolta con lo stesso numero di elementi della raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-136">This illustration depicts how `Select()` returns a collection that has the same number of elements as the source collection.</span></span>  
  
 <span data-ttu-id="9beb8-137">![Illustrazione concettuale dell'azione di Select ()](../../../../csharp/programming-guide/concepts/linq/media/selectaction.png "SelectAction")</span><span class="sxs-lookup"><span data-stu-id="9beb8-137">![Conceptual illustration of the action of Select&#40;&#41;](../../../../csharp/programming-guide/concepts/linq/media/selectaction.png "SelectAction")</span></span>  
  
 <span data-ttu-id="9beb8-138">Questa figura viene illustrato come `SelectMany()` concatena la sequenza intermedia di matrici in un unico valore finale che contiene ogni valore di ogni matrice intermedia.</span><span class="sxs-lookup"><span data-stu-id="9beb8-138">This illustration depicts how `SelectMany()` concatenates the intermediate sequence of arrays into one final result value that contains each value from each intermediate array.</span></span>  
  
 <span data-ttu-id="9beb8-139">![Rappresentazione grafica dell'azione di SelectMany (). ] (../../../../csharp/programming-guide/concepts/linq/media/selectmany.png "SelectMany")</span><span class="sxs-lookup"><span data-stu-id="9beb8-139">![Graphic showing the action of SelectMany&#40;&#41;.](../../../../csharp/programming-guide/concepts/linq/media/selectmany.png "SelectMany")</span></span>  
  
### <a name="code-example"></a><span data-ttu-id="9beb8-140">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="9beb8-140">Code Example</span></span>  
 <span data-ttu-id="9beb8-141">Nell'esempio seguente viene confrontato il comportamento di `Select()` e `SelectMany()`.</span><span class="sxs-lookup"><span data-stu-id="9beb8-141">The following example compares the behavior of `Select()` and `SelectMany()`.</span></span> <span data-ttu-id="9beb8-142">Il codice crea un "bouquet" di fiori prendendo i primi due elementi di ogni elenco di nomi di fiori nella raccolta di origine.</span><span class="sxs-lookup"><span data-stu-id="9beb8-142">The code creates a "bouquet" of flowers by taking the first two items from each list of flower names in the source collection.</span></span> <span data-ttu-id="9beb8-143">In questo esempio, "singolo valore" che la funzione di trasformazione <xref:System.Linq.Enumerable.Select%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29>è essa stessa una raccolta di valori.</xref:System.Linq.Enumerable.Select%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29></span><span class="sxs-lookup"><span data-stu-id="9beb8-143">In this example, the "single value" that the transform function <xref:System.Linq.Enumerable.Select%60%602%28System.Collections.Generic.IEnumerable%7B%60%600%7D%2CSystem.Func%7B%60%600%2C%60%601%7D%29> uses is itself a collection of values.</span></span> <span data-ttu-id="9beb8-144">Questa operazione richiede aggiuntivo `For Each` ciclo per enumerare tutte le stringhe ogni sottosequenza.</span><span class="sxs-lookup"><span data-stu-id="9beb8-144">This requires the extra `For Each` loop in order to enumerate each string in each sub-sequence.</span></span>  
  
```vb  
Class Bouquet  
    Public Flowers As List(Of String)  
End Class  
  
Sub SelectVsSelectMany()  
    Dim bouquets = New List(Of Bouquet) From {   
        New Bouquet With {.Flowers = New List(Of String)(New String() {"sunflower", "daisy", "daffodil", "larkspur"})},   
        New Bouquet With {.Flowers = New List(Of String)(New String() {"tulip", "rose", "orchid"})},   
        New Bouquet With {.Flowers = New List(Of String)(New String() {"gladiolis", "lily", "snapdragon", "aster", "protea"})},   
        New Bouquet With {.Flowers = New List(Of String)(New String() {"larkspur", "lilac", "iris", "dahlia"})}}  
  
    Dim output As New System.Text.StringBuilder  
  
    ' Select()  
    Dim query1 = bouquets.Select(Function(b) b.Flowers)  
  
    output.AppendLine("Using Select():")  
    For Each flowerList In query1  
        For Each str As String In flowerList  
            output.AppendLine(str)  
        Next  
    Next  
  
    ' SelectMany()  
    Dim query2 = bouquets.SelectMany(Function(b) b.Flowers)  
  
    output.AppendLine(vbCrLf & "Using SelectMany():")  
    For Each str As String In query2  
        output.AppendLine(str)  
    Next  
  
    ' Display the output  
    MsgBox(output.ToString())  
  
    ' This code produces the following output:  
    '  
    ' Using Select():  
    ' sunflower  
    ' daisy  
    ' daffodil  
    ' larkspur  
    ' tulip  
    ' rose  
    ' orchid  
    ' gladiolis  
    ' lily  
    ' snapdragon  
    ' aster  
    ' protea  
    ' larkspur  
    ' lilac  
    ' iris  
    ' dahlia  
  
    ' Using SelectMany()  
    ' sunflower  
    ' daisy  
    ' daffodil  
    ' larkspur  
    ' tulip  
    ' rose  
    ' orchid  
    ' gladiolis  
    ' lily  
    ' snapdragon  
    ' aster  
    ' protea  
    ' larkspur  
    ' lilac  
    ' iris  
    ' dahlia  
  
End Sub  
```  
  
## <a name="see-also"></a><span data-ttu-id="9beb8-145">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="9beb8-145">See Also</span></span>  
 <span data-ttu-id="9beb8-146"><xref:System.Linq></xref:System.Linq></span><span class="sxs-lookup"><span data-stu-id="9beb8-146"><xref:System.Linq></span></span>   
<span data-ttu-id="9beb8-147"> [Cenni preliminari sugli operatori di Query standard (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md) </span><span class="sxs-lookup"><span data-stu-id="9beb8-147"> [Standard Query Operators Overview (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/standard-query-operators-overview.md) </span></span>  
<span data-ttu-id="9beb8-148"> [Clausola SELECT](../../../../visual-basic/language-reference/queries/select-clause.md) </span><span class="sxs-lookup"><span data-stu-id="9beb8-148"> [Select Clause](../../../../visual-basic/language-reference/queries/select-clause.md) </span></span>  
<span data-ttu-id="9beb8-149"> [Procedura: combinare dati utilizzando join](../../../../visual-basic/programming-guide/language-features/linq/how-to-combine-data-with-linq-by-using-joins.md) </span><span class="sxs-lookup"><span data-stu-id="9beb8-149"> [How to: Combine Data with Joins](../../../../visual-basic/programming-guide/language-features/linq/how-to-combine-data-with-linq-by-using-joins.md) </span></span>  
<span data-ttu-id="9beb8-150"> [Procedura: popolare raccolte di oggetti da più origini (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-populate-object-collections-from-multiple-sources-linq.md) </span><span class="sxs-lookup"><span data-stu-id="9beb8-150"> [How to: Populate Object Collections from Multiple Sources (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-populate-object-collections-from-multiple-sources-linq.md) </span></span>  
<span data-ttu-id="9beb8-151"> [Procedura: restituire un risultato di Query LINQ come tipo specifico](../../../../visual-basic/programming-guide/language-features/linq/how-to-return-a-linq-query-result-as-a-specific-type.md) </span><span class="sxs-lookup"><span data-stu-id="9beb8-151"> [How to: Return a LINQ Query Result as a Specific Type](../../../../visual-basic/programming-guide/language-features/linq/how-to-return-a-linq-query-result-as-a-specific-type.md) </span></span>  
<span data-ttu-id="9beb8-152"> [Procedura: suddividere un File in molti file utilizzando i gruppi (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-split-a-file-into-many-files-by-using-groups-linq.md)</span><span class="sxs-lookup"><span data-stu-id="9beb8-152"> [How to: Split a File Into Many Files by Using Groups (LINQ) (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/how-to-split-a-file-into-many-files-by-using-groups-linq.md)</span></span>
