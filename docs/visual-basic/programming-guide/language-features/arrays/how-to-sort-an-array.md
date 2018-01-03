---
title: 'Procedura: ordinare una matrice in Visual Basic'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: Array.Sort
helpviewer_keywords:
- arrays [Visual Basic], sorting
- examples [Visual Basic], arrays
ms.assetid: 9289aeaa-9626-4698-94a7-1d1fd3702b87
caps.latest.revision: "19"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: f24c0625058dbd960411d5981b4e98e0e9422b99
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-sort-an-array-in-visual-basic"></a><span data-ttu-id="682c2-102">Procedura: ordinare una matrice in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="682c2-102">How to: Sort An Array in Visual Basic</span></span>
<span data-ttu-id="682c2-103">In questo esempio dichiara una matrice di `String` gli oggetti denominati `zooAnimals`, viene compilata e quindi la Ordina alfabeticamente.</span><span class="sxs-lookup"><span data-stu-id="682c2-103">This example declares an array of `String` objects named `zooAnimals`, populates it, and then sorts it alphabetically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="682c2-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="682c2-104">Example</span></span>  
  
```  
Private Sub sortAnimals()  
    Dim zooAnimals(2) As String  
    zooAnimals(0) = "lion"  
    zooAnimals(1) = "turtle"  
    zooAnimals(2) = "ostrich"  
    Array.Sort(zooAnimals)  
End Sub  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="682c2-105">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="682c2-105">Compiling the Code</span></span>  
 <span data-ttu-id="682c2-106">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="682c2-106">This example requires:</span></span>  
  
-   <span data-ttu-id="682c2-107">Accesso a mscorlib. dll e <xref:System> dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="682c2-107">Access to Mscorlib.dll and the <xref:System> namespace.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="682c2-108">Programmazione efficiente</span><span class="sxs-lookup"><span data-stu-id="682c2-108">Robust Programming</span></span>  
 <span data-ttu-id="682c2-109">Le seguenti condizioni possono generare un'eccezione:</span><span class="sxs-lookup"><span data-stu-id="682c2-109">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="682c2-110">Matrice è vuota (<xref:System.ArgumentNullException> classe)</span><span class="sxs-lookup"><span data-stu-id="682c2-110">Array is empty (<xref:System.ArgumentNullException> class)</span></span>  
  
-   <span data-ttu-id="682c2-111">La matrice è multidimensionale (<xref:System.RankException> classe)</span><span class="sxs-lookup"><span data-stu-id="682c2-111">Array is multidimensional (<xref:System.RankException> class)</span></span>  
  
-   <span data-ttu-id="682c2-112">Uno o più elementi della matrice non implementano il <xref:System.IComparable> interfaccia (<xref:System.InvalidOperationException> classe)</span><span class="sxs-lookup"><span data-stu-id="682c2-112">One or more elements of the array do not implement the <xref:System.IComparable> interface (<xref:System.InvalidOperationException> class)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="682c2-113">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="682c2-113">See Also</span></span>  
 <xref:System.Array.Sort%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="682c2-114">Array</span><span class="sxs-lookup"><span data-stu-id="682c2-114">Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/index.md)  
 [<span data-ttu-id="682c2-115">Risoluzione dei problemi relativi alle matrici</span><span class="sxs-lookup"><span data-stu-id="682c2-115">Troubleshooting Arrays</span></span>](../../../../visual-basic/programming-guide/language-features/arrays/troubleshooting-arrays.md)  
 [<span data-ttu-id="682c2-116">Raccolte</span><span class="sxs-lookup"><span data-stu-id="682c2-116">Collections</span></span>](../../concepts/collections.md)  
 [<span data-ttu-id="682c2-117">Istruzione For Each...Next</span><span class="sxs-lookup"><span data-stu-id="682c2-117">For Each...Next Statement</span></span>](../../../../visual-basic/language-reference/statements/for-each-next-statement.md)
