---
title: Creare un gruppo annidato (LINQ in C#)
description: Informazioni su come creare un gruppo annidato in un'espressione di query LINQ in C#.
ms.date: 12/1/2016
ms.assetid: e9f00708-362e-4d13-98c5-d77549347ba0
ms.openlocfilehash: 82b07c303215200fa974ce614a2d5a77882dcf4c
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43509968"
---
# <a name="create-a-nested-group"></a><span data-ttu-id="c908e-103">Creare un gruppo annidato</span><span class="sxs-lookup"><span data-stu-id="c908e-103">Create a nested group</span></span>

<span data-ttu-id="c908e-104">Nell'esempio seguente viene illustrato come creare gruppi annidati in un'espressione di query LINQ.</span><span class="sxs-lookup"><span data-stu-id="c908e-104">The following example shows how to create nested groups in a LINQ query expression.</span></span> <span data-ttu-id="c908e-105">Ogni gruppo creato in base all'anno o al livello degli studenti viene ulteriormente suddiviso in gruppi in base ai nomi delle persone.</span><span class="sxs-lookup"><span data-stu-id="c908e-105">Each group that is created according to student year or grade level is then further subdivided into groups based on the individuals' names.</span></span>

## <a name="example"></a><span data-ttu-id="c908e-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="c908e-106">Example</span></span>

> [!NOTE]
> <span data-ttu-id="c908e-107">Questo esempio contiene riferimenti a oggetti definiti nel codice di esempio in [Eseguire una query su una raccolta di oggetti](query-a-collection-of-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c908e-107">This example contains references to objects that are defined in the sample code in [Query a collection of objects](query-a-collection-of-objects.md).</span></span>

[!code-csharp[csProgGuideLINQ#24](~/samples/snippets/csharp/concepts/linq/how-to-create-a-nested-group_1.cs)]

<span data-ttu-id="c908e-108">Si noti che sono necessari tre cicli `foreach` annidati per eseguire l'iterazione degli elementi interni di un gruppo annidato.</span><span class="sxs-lookup"><span data-stu-id="c908e-108">Note that three nested `foreach` loops are required to iterate over the inner elements of a nested group.</span></span>

## <a name="see-also"></a><span data-ttu-id="c908e-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c908e-109">See also</span></span>

- [<span data-ttu-id="c908e-110">LINQ (Language-Integrated Query)</span><span class="sxs-lookup"><span data-stu-id="c908e-110">Language Integrated Query (LINQ)</span></span>](index.md)
