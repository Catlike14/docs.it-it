---
title: Funzioni canoniche bit per bit
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 993868ca-16e3-47b6-9915-c29cd63b0a21
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: a4311b610859b36f1587e5e3f85e2a5f06503e1d
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="bitwise-canonical-functions"></a><span data-ttu-id="700dc-102">Funzioni canoniche bit per bit</span><span class="sxs-lookup"><span data-stu-id="700dc-102">Bitwise Canonical Functions</span></span>
[!INCLUDE[esql](../../../../../../includes/esql-md.md)]<span data-ttu-id="700dc-103"> include funzioni canoniche bit per bit.</span><span class="sxs-lookup"><span data-stu-id="700dc-103"> includes bitwise canonical functions.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="700dc-104">Note</span><span class="sxs-lookup"><span data-stu-id="700dc-104">Remarks</span></span>  
 <span data-ttu-id="700dc-105">Nella tabella seguente sono illustrate le funzioni canoniche bit per bit [!INCLUDE[esql](../../../../../../includes/esql-md.md)].</span><span class="sxs-lookup"><span data-stu-id="700dc-105">The following table shows the bitwise [!INCLUDE[esql](../../../../../../includes/esql-md.md)] canonical functions.</span></span> <span data-ttu-id="700dc-106">Queste funzioni restituiscono `Null` se `Null` viene specificato l'input.</span><span class="sxs-lookup"><span data-stu-id="700dc-106">These functions will return `Null` if `Null` input is provided.</span></span> <span data-ttu-id="700dc-107">Il tipo restituito delle funzioni sarà uguale ai tipi di argomenti.</span><span class="sxs-lookup"><span data-stu-id="700dc-107">The return type of the functions is the same as the argument type(s).</span></span> <span data-ttu-id="700dc-108">Gli argomenti devono essere dello stesso tipo, se la funzione ne accetta più di uno.</span><span class="sxs-lookup"><span data-stu-id="700dc-108">Arguments must be of the same type, if the function takes more than one argument.</span></span> <span data-ttu-id="700dc-109">Per eseguire operazioni bit per bit tra tipi diversi, è necessario eseguire il cast in modo esplicito lo stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="700dc-109">To perform bitwise operations across different types, you need to cast to the same type explicitly.</span></span>  
  
|<span data-ttu-id="700dc-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="700dc-110">Function</span></span>|<span data-ttu-id="700dc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="700dc-111">Description</span></span>|  
|--------------|-----------------|  
|<span data-ttu-id="700dc-112">`BitWiseAnd (` `value1` `,`  `value2` `)`</span><span class="sxs-lookup"><span data-stu-id="700dc-112">`BitWiseAnd (` `value1` `,`  `value2` `)`</span></span>|<span data-ttu-id="700dc-113">Restituisce la congiunzione bit per bit di `value1` e `value2` come tipo di `value1` e `value2`.</span><span class="sxs-lookup"><span data-stu-id="700dc-113">Returns the bitwise conjunction of `value1` and `value2` as the type of `value1` and `value2`.</span></span><br /><br /> <span data-ttu-id="700dc-114">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="700dc-114">**Arguments**</span></span><br /><br /> <span data-ttu-id="700dc-115">Oggetto `Byte`, `Int16`, `Int32`, e `Int64`.</span><span class="sxs-lookup"><span data-stu-id="700dc-115">A `Byte`, `Int16`, `Int32`, and `Int64`.</span></span><br /><br /> <span data-ttu-id="700dc-116">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="700dc-116">**Example**</span></span><br /><br /> `-- The following example returns 1.`<br /><br /> `BitWiseAnd(1,3)`|  
|<span data-ttu-id="700dc-117">`BitWiseNot (` `value` `)`</span><span class="sxs-lookup"><span data-stu-id="700dc-117">`BitWiseNot (` `value` `)`</span></span>|<span data-ttu-id="700dc-118">Restituisce la negazione bit per bit di `value`.</span><span class="sxs-lookup"><span data-stu-id="700dc-118">Returns the bitwise negation of `value`.</span></span><br /><br /> <span data-ttu-id="700dc-119">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="700dc-119">**Arguments**</span></span><br /><br /> <span data-ttu-id="700dc-120">Oggetto `Byte`, `Int16`, `Int32`, e `Int64`.</span><span class="sxs-lookup"><span data-stu-id="700dc-120">A `Byte`, `Int16`, `Int32`, and `Int64`.</span></span><br /><br /> <span data-ttu-id="700dc-121">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="700dc-121">**Example**</span></span><br /><br /> `-- The following example returns -4.`<br /><br /> `BitWiseNot(3)`|  
|<span data-ttu-id="700dc-122">`BitWiseOr (` `value1` `,`  `value2` `)`</span><span class="sxs-lookup"><span data-stu-id="700dc-122">`BitWiseOr (` `value1` `,`  `value2` `)`</span></span>|<span data-ttu-id="700dc-123">Restituisce la disgiunzione bit per bit di `value1` e `value2` come tipo di `value1` e `value2`.</span><span class="sxs-lookup"><span data-stu-id="700dc-123">Returns the bitwise disjunction of `value1` and `value2` as the type of `value1` and `value2`.</span></span><br /><br /> <span data-ttu-id="700dc-124">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="700dc-124">**Arguments**</span></span><br /><br /> <span data-ttu-id="700dc-125">Oggetto `Byte`, `Int16`, `Int32` e `Int64`.</span><span class="sxs-lookup"><span data-stu-id="700dc-125">A `Byte`, `Int16`, `Int32` and `Int64`.</span></span><br /><br /> <span data-ttu-id="700dc-126">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="700dc-126">**Example**</span></span><br /><br /> `-- The following example returns 3.`<br /><br /> `BitWiseOr(1,3)`|  
|<span data-ttu-id="700dc-127">`BitWiseXor (` `value1` `,`  `value2` `)`</span><span class="sxs-lookup"><span data-stu-id="700dc-127">`BitWiseXor (` `value1` `,`  `value2` `)`</span></span>|<span data-ttu-id="700dc-128">Restituisce la disgiunzione esclusiva bit per bit di `value1` e `value2` come tipo di `value1` e `value2`.</span><span class="sxs-lookup"><span data-stu-id="700dc-128">Returns the bitwise exclusive disjunction of `value1` and `value2` as the type of `value1` and `value2`.</span></span><br /><br /> <span data-ttu-id="700dc-129">**Argomenti**</span><span class="sxs-lookup"><span data-stu-id="700dc-129">**Arguments**</span></span><br /><br /> <span data-ttu-id="700dc-130">Oggetto `Byte`, `Int16`, `Int32` e `Int64`.</span><span class="sxs-lookup"><span data-stu-id="700dc-130">A `Byte`, `Int16`, `Int32` and `Int64`.</span></span><br /><br /> <span data-ttu-id="700dc-131">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="700dc-131">**Example**</span></span><br /><br /> `-- The following example returns 2.`<br /><br /> `BitWiseXor (1,3)`|  
  
## <a name="see-also"></a><span data-ttu-id="700dc-132">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="700dc-132">See Also</span></span>  
 [<span data-ttu-id="700dc-133">Funzioni canoniche</span><span class="sxs-lookup"><span data-stu-id="700dc-133">Canonical Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
