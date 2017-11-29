---
title: Parametri (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 8d618edd-0988-4ff2-8263-ce59448af7a5
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 2a3700b5f9bdc996b147609d86bcaed0ec0bb116
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="parameters-entity-sql"></a><span data-ttu-id="4f299-102">Parametri (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="4f299-102">Parameters (Entity SQL)</span></span>
<span data-ttu-id="4f299-103">I parametri sono variabili definite esternamente a [!INCLUDE[esql](../../../../../../includes/esql-md.md)], generalmente tramite un'API di associazione usata da un linguaggio host.</span><span class="sxs-lookup"><span data-stu-id="4f299-103">Parameters are variables that are defined outside [!INCLUDE[esql](../../../../../../includes/esql-md.md)], usually through a binding API that is used by a host language.</span></span> <span data-ttu-id="4f299-104">Ogni parametro è associato a un nome e un tipo.</span><span class="sxs-lookup"><span data-stu-id="4f299-104">Each parameter has a name and a type.</span></span> <span data-ttu-id="4f299-105">I nomi dei parametri sono definiti nelle espressioni di query con il simbolo chiocciola (@) come prefisso.</span><span class="sxs-lookup"><span data-stu-id="4f299-105">Parameter names are defined in query expressions with the at (@) symbol as a prefix.</span></span> <span data-ttu-id="4f299-106">Questo consente di distinguerli dai nomi di proprietà o dagli altri nomi definiti nella query.</span><span class="sxs-lookup"><span data-stu-id="4f299-106">This disambiguates them from the names of properties or other names that are defined in the query.</span></span>  
  
 <span data-ttu-id="4f299-107">L'API di associazione del linguaggio host fornisce le API per l'associazione dei parametri.</span><span class="sxs-lookup"><span data-stu-id="4f299-107">The host-language binding API provides APIs for binding parameters.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f299-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="4f299-108">Example</span></span>  
  
```  
select c   
      from LOB.Customers as c   
      where c.Name = @name  
```  
  
## <a name="see-also"></a><span data-ttu-id="4f299-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4f299-109">See Also</span></span>  
 [<span data-ttu-id="4f299-110">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="4f299-110">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)  
 [<span data-ttu-id="4f299-111">Panoramica di Entity SQL</span><span class="sxs-lookup"><span data-stu-id="4f299-111">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)
