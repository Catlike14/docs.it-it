---
title: Partizionamento dei dati (C#)
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.topic: article
dev_langs:
- CSharp
ms.assetid: 2a5c507b-fe22-443c-a768-dec7f9ec568d
caps.latest.revision: 3
author: BillWagner
ms.author: wiwagn
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 2f1690dac93d5e74f1305bd457f8bc749bec5449
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="partitioning-data-c"></a><span data-ttu-id="5fd89-102">Partizionamento dei dati (C#)</span><span class="sxs-lookup"><span data-stu-id="5fd89-102">Partitioning Data (C#)</span></span>
<span data-ttu-id="5fd89-103">Il partizionamento in LINQ è l'operazione di divisione di una sequenza di input in due sezioni senza ridisposizione degli elementi e la successiva restituzione di una delle sezioni.</span><span class="sxs-lookup"><span data-stu-id="5fd89-103">Partitioning in LINQ refers to the operation of dividing an input sequence into two sections, without rearranging the elements, and then returning one of the sections.</span></span>  
  
 <span data-ttu-id="5fd89-104">La figura seguente illustra i risultati di tre diverse operazioni di partizionamento in una sequenza di caratteri.</span><span class="sxs-lookup"><span data-stu-id="5fd89-104">The following illustration shows the results of three different partitioning operations on a sequence of characters.</span></span> <span data-ttu-id="5fd89-105">La prima operazione restituisce i primi tre elementi nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="5fd89-105">The first operation returns the first three elements in the sequence.</span></span> <span data-ttu-id="5fd89-106">La seconda operazione ignora i primi tre elementi e restituisce gli elementi rimanenti.</span><span class="sxs-lookup"><span data-stu-id="5fd89-106">The second operation skips the first three elements and returns the remaining elements.</span></span> <span data-ttu-id="5fd89-107">La terza operazione ignora i primi due elementi nella sequenza e restituisce i tre elementi successivi.</span><span class="sxs-lookup"><span data-stu-id="5fd89-107">The third operation skips the first two elements in the sequence and returns the next three elements.</span></span>  
  
 <span data-ttu-id="5fd89-108">![Operazioni di partizionamento LINQ](../../../../csharp/programming-guide/concepts/linq/media/linq_partition.png "LINQ_Partition")</span><span class="sxs-lookup"><span data-stu-id="5fd89-108">![LINQ Partitioning Operations](../../../../csharp/programming-guide/concepts/linq/media/linq_partition.png "LINQ_Partition")</span></span>  
  
 <span data-ttu-id="5fd89-109">Nella sezione seguente sono elencati i metodi degli operatori di query standard che eseguono la partizione delle sequenze.</span><span class="sxs-lookup"><span data-stu-id="5fd89-109">The standard query operator methods that partition sequences are listed in the following section.</span></span>  
  
## <a name="operators"></a><span data-ttu-id="5fd89-110">Operatori</span><span class="sxs-lookup"><span data-stu-id="5fd89-110">Operators</span></span>  
  
|<span data-ttu-id="5fd89-111">Nome dell'operatore</span><span class="sxs-lookup"><span data-stu-id="5fd89-111">Operator Name</span></span>|<span data-ttu-id="5fd89-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fd89-112">Description</span></span>|<span data-ttu-id="5fd89-113">Sintassi di espressione della query C#</span><span class="sxs-lookup"><span data-stu-id="5fd89-113">C# Query Expression Syntax</span></span>|<span data-ttu-id="5fd89-114">Altre informazioni</span><span class="sxs-lookup"><span data-stu-id="5fd89-114">More Information</span></span>|  
|-------------------|-----------------|---------------------------------|----------------------|  
|<span data-ttu-id="5fd89-115">Skip</span><span class="sxs-lookup"><span data-stu-id="5fd89-115">Skip</span></span>|<span data-ttu-id="5fd89-116">Ignora gli elementi fino a una posizione specificata in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="5fd89-116">Skips elements up to a specified position in a sequence.</span></span>|<span data-ttu-id="5fd89-117">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="5fd89-117">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Skip%2A?displayProperty=fullName><br /><br /> <xref:System.Linq.Queryable.Skip%2A?displayProperty=fullName>|  
|<span data-ttu-id="5fd89-118">SkipWhile</span><span class="sxs-lookup"><span data-stu-id="5fd89-118">SkipWhile</span></span>|<span data-ttu-id="5fd89-119">Ignora gli elementi in base a una funzione di predicato fino a quando un elemento non soddisfa la condizione.</span><span class="sxs-lookup"><span data-stu-id="5fd89-119">Skips elements based on a predicate function until an element does not satisfy the condition.</span></span>|<span data-ttu-id="5fd89-120">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="5fd89-120">Not applicable.</span></span>|<xref:System.Linq.Enumerable.SkipWhile%2A?displayProperty=fullName><br /><br /> <xref:System.Linq.Queryable.SkipWhile%2A?displayProperty=fullName>|  
|<span data-ttu-id="5fd89-121">Take</span><span class="sxs-lookup"><span data-stu-id="5fd89-121">Take</span></span>|<span data-ttu-id="5fd89-122">Accetta gli elementi fino a una posizione specificata in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="5fd89-122">Takes elements up to a specified position in a sequence.</span></span>|<span data-ttu-id="5fd89-123">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="5fd89-123">Not applicable.</span></span>|<xref:System.Linq.Enumerable.Take%2A?displayProperty=fullName><br /><br /> <xref:System.Linq.Queryable.Take%2A?displayProperty=fullName>|  
|<span data-ttu-id="5fd89-124">TakeWhile</span><span class="sxs-lookup"><span data-stu-id="5fd89-124">TakeWhile</span></span>|<span data-ttu-id="5fd89-125">Accetta gli elementi in base a una funzione di predicato fino a quando un elemento non soddisfa la condizione.</span><span class="sxs-lookup"><span data-stu-id="5fd89-125">Takes elements based on a predicate function until an element does not satisfy the condition.</span></span>|<span data-ttu-id="5fd89-126">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="5fd89-126">Not applicable.</span></span>|<xref:System.Linq.Enumerable.TakeWhile%2A?displayProperty=fullName><br /><br /> <xref:System.Linq.Queryable.TakeWhile%2A?displayProperty=fullName>|  
  
## <a name="see-also"></a><span data-ttu-id="5fd89-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5fd89-127">See Also</span></span>  
 <span data-ttu-id="5fd89-128"><xref:System.Linq></span><span class="sxs-lookup"><span data-stu-id="5fd89-128"><xref:System.Linq></span></span>   
 [<span data-ttu-id="5fd89-129">Cenni preliminari sugli operatori di query standard (C#)</span><span class="sxs-lookup"><span data-stu-id="5fd89-129">Standard Query Operators Overview (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/standard-query-operators-overview.md)

