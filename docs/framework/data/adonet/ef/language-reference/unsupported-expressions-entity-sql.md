---
title: Espressioni non supportate (Entity SQL)
ms.date: 03/30/2017
ms.prod: .net-framework
ms.technology:
- dotnet-ado
ms.topic: article
ms.assetid: 5e79da7e-e78a-413c-8fb0-f3f9cd84f579
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
dev_langs:
- sql
ms.openlocfilehash: 075daf0e4f0477dda50231760fbb3d990a9f8468
ms.sourcegitcommit: c3957fdb990060559d73cca44ab3e2c7b4d049c0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2018
---
# <a name="unsupported-expressions"></a><span data-ttu-id="d9193-102">Espressioni non supportate</span><span class="sxs-lookup"><span data-stu-id="d9193-102">Unsupported expressions</span></span>

<span data-ttu-id="d9193-103">In questo argomento vengono descritte le espressioni [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] non supportate in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9193-103">This topic describes [!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] expressions that are not supported in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span></span> <span data-ttu-id="d9193-104">Per ulteriori informazioni, vedere [Entity SQL differenze di Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md).</span><span class="sxs-lookup"><span data-stu-id="d9193-104">For more information, see [How Entity SQL Differs from Transact-SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md).</span></span>

## <a name="quantified-predicates"></a><span data-ttu-id="d9193-105">Predicati quantificati</span><span class="sxs-lookup"><span data-stu-id="d9193-105">Quantified predicates</span></span>

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] <span data-ttu-id="d9193-106">Consente i costrutti con il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="d9193-106">allows constructs of the following form:</span></span>

```sql
sal > all (select salary from employees)
sal > any (select salary from employees)
```

[!INCLUDE[esql](../../../../../../includes/esql-md.md)]<span data-ttu-id="d9193-107">, tuttavia, non supporta tali costrutti.</span><span class="sxs-lookup"><span data-stu-id="d9193-107">, however, does not support such constructs.</span></span> <span data-ttu-id="d9193-108">È possibile scrivere espressioni equivalenti in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="d9193-108">Equivalent expressions can be written in [!INCLUDE[esql](../../../../../../includes/esql-md.md)] as follows:</span></span>

```sql
not exists(select 0 from employees as e where sal > e.salary)
exists(select 0 from employees as e where sal > e.salary)
```

## <a name="-operator"></a><span data-ttu-id="d9193-109">\* (operatore)</span><span class="sxs-lookup"><span data-stu-id="d9193-109">\* operator</span></span>

[!INCLUDE[tsql](../../../../../../includes/tsql-md.md)] <span data-ttu-id="d9193-110">supporta l'utilizzo di \* (operatore) nella clausola SELECT per indicare che tutte le colonne devono essere proiettate. Questa opzione non è supportata in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9193-110">supports the use of the \* operator in the SELECT clause to indicate that all columns should be projected out. This is not supported in [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="d9193-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d9193-111">See also</span></span>

[<span data-ttu-id="d9193-112">Panoramica di Entity SQL</span><span class="sxs-lookup"><span data-stu-id="d9193-112">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
[<span data-ttu-id="d9193-113">Differenze tra Entity SQL e Transact-SQL</span><span class="sxs-lookup"><span data-stu-id="d9193-113">How Entity SQL Differs from Transact-SQL</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/how-entity-sql-differs-from-transact-sql.md)  
