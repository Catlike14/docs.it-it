---
title: = (uguale a) (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 948eb588-7080-4046-bb48-633b007393bf
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: c6b258bd06fd3e7e348e190b0897d66036006873
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="-equals-entity-sql"></a><span data-ttu-id="c8380-102">= (uguale a) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c8380-102">= (Equals) (Entity SQL)</span></span>
<span data-ttu-id="c8380-103">Consente di confrontare due espressioni per verificare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="c8380-103">Compares the equality of two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c8380-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8380-104">Syntax</span></span>  
  
```  
expression = expression  
or   
expression == expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="c8380-105">Argomenti</span><span class="sxs-lookup"><span data-stu-id="c8380-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="c8380-106">Qualsiasi espressione valida.</span><span class="sxs-lookup"><span data-stu-id="c8380-106">Any valid expression.</span></span> <span data-ttu-id="c8380-107">Entrambe le espressioni devono contenere tipi di dati convertibili in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="c8380-107">Both expressions must have implicitly convertible data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="c8380-108">Tipi di risultati</span><span class="sxs-lookup"><span data-stu-id="c8380-108">Result Types</span></span>  
 <span data-ttu-id="c8380-109">`true` se l'espressione a sinistra è uguale a quella a destra; in caso contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="c8380-109">`true` if the left expression is equal to the right expression; otherwise, `false`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c8380-110">Note</span><span class="sxs-lookup"><span data-stu-id="c8380-110">Remarks</span></span>  
 <span data-ttu-id="c8380-111">L'operatore == è equivalente a =.</span><span class="sxs-lookup"><span data-stu-id="c8380-111">The == operator is equivalent to =.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c8380-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="c8380-112">Example</span></span>  
 <span data-ttu-id="c8380-113">Nella query Entity SQL seguente viene usato l'operatore di confronto = per confrontare due espressioni e verificare se sono uguali.</span><span class="sxs-lookup"><span data-stu-id="c8380-113">The following Entity SQL query uses = comparison operator to compare the equality of two expressions.</span></span> <span data-ttu-id="c8380-114">La query è basata sul modello Sales di AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="c8380-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c8380-115">Per compilare ed eseguire questa query, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8380-115">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="c8380-116">Seguire la procedura indicata in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="c8380-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="c8380-117">Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="c8380-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#equals)]  
  
## <a name="see-also"></a><span data-ttu-id="c8380-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c8380-118">See Also</span></span>  
 [<span data-ttu-id="c8380-119">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c8380-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
