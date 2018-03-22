---
title: '- (Sottrazione) (Entity SQL)'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: bc4327f9-09c0-438f-a008-927c5c478040
caps.latest.revision: ''
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: 5ca2bc8cb34d99421962289930c26de84eaa68e2
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="--subtract-entity-sql"></a><span data-ttu-id="41117-102">- (sottrazione) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="41117-102">- (Subtract) (Entity SQL)</span></span>
<span data-ttu-id="41117-103">Esegue la sottrazione di due numeri.</span><span class="sxs-lookup"><span data-stu-id="41117-103">Subtracts two numbers.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="41117-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41117-104">Syntax</span></span>  
  
```  
expression - expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="41117-105">Argomenti</span><span class="sxs-lookup"><span data-stu-id="41117-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="41117-106">Qualsiasi espressione valida con qualsiasi tipo di dati numerici.</span><span class="sxs-lookup"><span data-stu-id="41117-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="41117-107">Tipi di risultati</span><span class="sxs-lookup"><span data-stu-id="41117-107">Result Types</span></span>  
 <span data-ttu-id="41117-108">Tipo di dati ottenuto della promozione implicita del tipo dei due argomenti.</span><span class="sxs-lookup"><span data-stu-id="41117-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="41117-109">Per ulteriori informazioni sulla promozione implicita del tipo, vedere [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="41117-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="41117-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="41117-110">Example</span></span>  
 <span data-ttu-id="41117-111">Nella query Entity SQL seguente viene usato l'operatore aritmetico - per sottrarre due numeri.</span><span class="sxs-lookup"><span data-stu-id="41117-111">The following Entity SQL query uses the - arithmetic operator to subtract two numbers.</span></span> <span data-ttu-id="41117-112">La query è basata sul modello Sales di AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="41117-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="41117-113">Per compilare ed eseguire questa query, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="41117-113">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="41117-114">Seguire la procedura indicata in [Procedura: eseguire una query che restituisce risultati StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="41117-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="41117-115">Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="41117-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#SUBTRACT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#subtract)]  
  
## <a name="see-also"></a><span data-ttu-id="41117-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="41117-116">See Also</span></span>  
 [<span data-ttu-id="41117-117">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="41117-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
