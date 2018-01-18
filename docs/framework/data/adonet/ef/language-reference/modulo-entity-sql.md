---
title: (Modulo) (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 243ddc4f-3c4e-41e1-a3ef-4ed39e36248b
caps.latest.revision: "3"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: e204612904aa55b4a0ae9aa65f2bbfd644bbc396
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="modulo-entity-sql"></a><span data-ttu-id="a84d5-102">(Modulo) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="a84d5-102">(Modulo) (Entity SQL)</span></span>
<span data-ttu-id="a84d5-103">Restituisce il resto di un'espressione divisa per un'altra.</span><span class="sxs-lookup"><span data-stu-id="a84d5-103">Returns the remainder of one expression divided by another.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="a84d5-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a84d5-104">Syntax</span></span>  
  
```  
dividend % divisor  
```  
  
## <a name="arguments"></a><span data-ttu-id="a84d5-105">Argomenti</span><span class="sxs-lookup"><span data-stu-id="a84d5-105">Arguments</span></span>  
 `dividend`  
 <span data-ttu-id="a84d5-106">Espressione numerica da dividere.</span><span class="sxs-lookup"><span data-stu-id="a84d5-106">The numeric expression to divide.</span></span> <span data-ttu-id="a84d5-107">`dividend` è qualsiasi espressione valida con qualsiasi tipo di dati numerici.</span><span class="sxs-lookup"><span data-stu-id="a84d5-107">`dividend` is any valid expression of any one of the numeric data types.</span></span>  
  
 `divisor`  
 <span data-ttu-id="a84d5-108">Espressione numerica per la quale dividere il dividendo.</span><span class="sxs-lookup"><span data-stu-id="a84d5-108">The numeric expression to divide the dividend by.</span></span> <span data-ttu-id="a84d5-109">`divisor` è qualsiasi espressione valida con qualsiasi tipo di dati numerici.</span><span class="sxs-lookup"><span data-stu-id="a84d5-109">`divisor` is any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="a84d5-110">Tipi di risultati</span><span class="sxs-lookup"><span data-stu-id="a84d5-110">Result Types</span></span>  
 <span data-ttu-id="a84d5-111">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="a84d5-111">Edm.Int32</span></span>  
  
## <a name="example"></a><span data-ttu-id="a84d5-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a84d5-112">Example</span></span>  
 <span data-ttu-id="a84d5-113">Nella query Entity SQL seguente viene usato l'operatore aritmetico % per restituire il resto della divisione di un'espressione per un'altra.</span><span class="sxs-lookup"><span data-stu-id="a84d5-113">The following Entity SQL query uses the % arithmetic operator to return the remainder of one expression divided by another.</span></span> <span data-ttu-id="a84d5-114">La query è basata sul modello Sales di AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="a84d5-114">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="a84d5-115">Per compilare ed eseguire questa query, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a84d5-115">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="a84d5-116">Seguire la procedura indicata in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="a84d5-116">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="a84d5-117">Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="a84d5-117">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MODULO](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#modulo)]  
  
## <a name="see-also"></a><span data-ttu-id="a84d5-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a84d5-118">See Also</span></span>  
 [<span data-ttu-id="a84d5-119">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="a84d5-119">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
