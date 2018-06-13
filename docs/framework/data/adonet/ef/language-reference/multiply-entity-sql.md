---
title: '* (Moltiplicazione) (Entity SQL)'
ms.date: 03/30/2017
ms.assetid: 508ce246-4e86-47dd-a605-4af4bebb9891
ms.openlocfilehash: ecb0a55e403dddc5f7e69947035c8aa1fe7560ad
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/03/2018
ms.locfileid: "32762546"
---
# <a name="-multiply-entity-sql"></a><span data-ttu-id="07518-102">\* (moltiplicazione) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="07518-102">\* (Multiply) (Entity SQL)</span></span>
<span data-ttu-id="07518-103">Moltiplica due espressioni.</span><span class="sxs-lookup"><span data-stu-id="07518-103">Multiplies two expressions.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="07518-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07518-104">Syntax</span></span>  
  
```  
expression * expression  
```  
  
## <a name="arguments"></a><span data-ttu-id="07518-105">Argomenti</span><span class="sxs-lookup"><span data-stu-id="07518-105">Arguments</span></span>  
 `expression`  
 <span data-ttu-id="07518-106">Qualsiasi espressione valida con qualsiasi tipo di dati numerici.</span><span class="sxs-lookup"><span data-stu-id="07518-106">Any valid expression of any one of the numeric data types.</span></span>  
  
## <a name="result-types"></a><span data-ttu-id="07518-107">Tipi di risultati</span><span class="sxs-lookup"><span data-stu-id="07518-107">Result Types</span></span>  
 <span data-ttu-id="07518-108">Tipo di dati ottenuto della promozione implicita del tipo dei due argomenti.</span><span class="sxs-lookup"><span data-stu-id="07518-108">The data type that results from the implicit type promotion of the two arguments.</span></span> <span data-ttu-id="07518-109">Per ulteriori informazioni sulla promozione implicita del tipo, vedere [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="07518-109">For more information about implicit type promotion, see [Type System](../../../../../../docs/framework/data/adonet/ef/language-reference/type-system-entity-sql.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="07518-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="07518-110">Example</span></span>  
 <span data-ttu-id="07518-111">Nella query Entity SQL seguente viene usato l'operatore aritmetico \* per moltiplicare due numeri.</span><span class="sxs-lookup"><span data-stu-id="07518-111">The following Entity SQL query uses the \* arithmetic operator to multiply two numbers.</span></span> <span data-ttu-id="07518-112">La query è basata sul modello Sales di AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="07518-112">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="07518-113">Per compilare ed eseguire questa query, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="07518-113">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="07518-114">Seguire la procedura indicata in [Procedura: eseguire una query che restituisce risultati StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="07518-114">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="07518-115">Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="07518-115">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#MULTIPLY](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#multiply)]  
  
## <a name="see-also"></a><span data-ttu-id="07518-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="07518-116">See Also</span></span>  
 [<span data-ttu-id="07518-117">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="07518-117">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
