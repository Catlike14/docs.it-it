---
title: Funzioni definite dall'utente (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 3f9e6bbd-8e5a-43e1-809f-f8a61338e522
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: bf0592a3e88f4e8142f1fb0aeb1e7364d818d4ce
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="user-defined-functions-entity-sql"></a><span data-ttu-id="bf627-102">Funzioni definite dall'utente (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="bf627-102">User-Defined Functions (Entity SQL)</span></span>
<span data-ttu-id="bf627-103">Nelle query Entity SQL sono supportate le chiamate a funzioni definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="bf627-103">Entity SQL supports calling user-defined functions in a query.</span></span> <span data-ttu-id="bf627-104">È possibile definire queste funzioni inline con la query (vedere [procedura: chiamare una funzione definita dall'utente](http://msdn.microsoft.com/en-us/ad131b86-8b4e-4747-8605-d4fc64fb9d02)) o come parte del modello concettuale (vedere [procedura: definire funzioni personalizzate nel modello concettuale](http://msdn.microsoft.com/en-us/0dad7b8b-58f6-4271-b238-f34810d68e5f)).</span><span class="sxs-lookup"><span data-stu-id="bf627-104">You can define these functions inline with the query (see [How to: Call a User-Defined Function](http://msdn.microsoft.com/en-us/ad131b86-8b4e-4747-8605-d4fc64fb9d02)) or as part of the conceptual model (see [How to: Define Custom Functions in the Conceptual Model](http://msdn.microsoft.com/en-us/0dad7b8b-58f6-4271-b238-f34810d68e5f)).</span></span> <span data-ttu-id="bf627-105">Funzioni del modello concettuale sono definite come un comando Entity SQL nel [DefiningExpression](http://msdn.microsoft.com/en-us/d3da8d8b-a048-47ee-8d81-0c2ea3acdd3e) elemento di un [funzione](http://msdn.microsoft.com/en-us/dc3beca7-55cf-4977-8db0-5064cdbab134) elemento nel modello concettuale.</span><span class="sxs-lookup"><span data-stu-id="bf627-105">Conceptual model functions are defined as an Entity SQL command in the [DefiningExpression](http://msdn.microsoft.com/en-us/d3da8d8b-a048-47ee-8d81-0c2ea3acdd3e) element of a [Function](http://msdn.microsoft.com/en-us/dc3beca7-55cf-4977-8db0-5064cdbab134) element in the conceptual model.</span></span>  
  
 <span data-ttu-id="bf627-106">Entity SQL consente di definire delle funzioni nel comando di query stesso.</span><span class="sxs-lookup"><span data-stu-id="bf627-106">Entity SQL enables you to define functions in the query command itself.</span></span> <span data-ttu-id="bf627-107">Il [funzione](../../../../../../docs/framework/data/adonet/ef/language-reference/function-entity-sql.md) operatore consente di definire le funzioni inline.</span><span class="sxs-lookup"><span data-stu-id="bf627-107">The [FUNCTION](../../../../../../docs/framework/data/adonet/ef/language-reference/function-entity-sql.md) operator defines inline functions.</span></span> <span data-ttu-id="bf627-108">È possibile definire più funzioni in un singolo comando e queste funzioni possono avere lo stesso nome purché le rispettive firme siano univoche.</span><span class="sxs-lookup"><span data-stu-id="bf627-108">You can define multiple functions in a single command, and these functions can have the same function name, as long as the function signatures are unique.</span></span> <span data-ttu-id="bf627-109">Per altre informazioni, vedere [Function Overload Resolution](../../../../../../docs/framework/data/adonet/ef/language-reference/function-overload-resolution-entity-sql.md).</span><span class="sxs-lookup"><span data-stu-id="bf627-109">For more information, see [Function Overload Resolution](../../../../../../docs/framework/data/adonet/ef/language-reference/function-overload-resolution-entity-sql.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bf627-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="bf627-110">See Also</span></span>  
 [<span data-ttu-id="bf627-111">Funzioni</span><span class="sxs-lookup"><span data-stu-id="bf627-111">Functions</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/functions-entity-sql.md)
