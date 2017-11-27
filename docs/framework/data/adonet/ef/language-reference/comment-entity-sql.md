---
title: -- (commento) (Entity SQL)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5d9de735-2099-47f1-b7e7-60856f494924
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 1961542e615bbbd99bbc517bdd7d649be3f3ef07
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="---comment-entity-sql"></a><span data-ttu-id="c9dde-102">-- (commento) (Entity SQL)</span><span class="sxs-lookup"><span data-stu-id="c9dde-102">-- (Comment) (Entity SQL)</span></span>
<span data-ttu-id="c9dde-103">Le query[!INCLUDE[esql](../../../../../../includes/esql-md.md)] possono contenere commenti.</span><span class="sxs-lookup"><span data-stu-id="c9dde-103">[!INCLUDE[esql](../../../../../../includes/esql-md.md)] queries can contain comments.</span></span> <span data-ttu-id="c9dde-104">Due trattini (`--`) indicano l'inizio di una riga di commento.</span><span class="sxs-lookup"><span data-stu-id="c9dde-104">Two dashes (`--`) start a comment line.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c9dde-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9dde-105">Syntax</span></span>  
  
```  
-- text_of_comment  
```  
  
## <a name="arguments"></a><span data-ttu-id="c9dde-106">Argomenti</span><span class="sxs-lookup"><span data-stu-id="c9dde-106">Arguments</span></span>  
 `text_of_comment`  
 <span data-ttu-id="c9dde-107">Stringa di caratteri contenente il testo del commento.</span><span class="sxs-lookup"><span data-stu-id="c9dde-107">Is the character string that contains the text of the comment.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9dde-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="c9dde-108">Example</span></span>  
 <span data-ttu-id="c9dde-109">Nella query Entity SQL seguente viene illustrato come usare i commenti.</span><span class="sxs-lookup"><span data-stu-id="c9dde-109">The following Entity SQL query demonstrates how to use comments.</span></span> <span data-ttu-id="c9dde-110">La query è basata sul modello Sales di AdventureWorks.</span><span class="sxs-lookup"><span data-stu-id="c9dde-110">The query is based on the AdventureWorks Sales Model.</span></span> <span data-ttu-id="c9dde-111">Per compilare ed eseguire questa query, effettuare le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="c9dde-111">To compile and run this query, follow these steps:</span></span>  
  
1.  <span data-ttu-id="c9dde-112">Seguire la procedura indicata in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span><span class="sxs-lookup"><span data-stu-id="c9dde-112">Follow the procedure in [How to: Execute a Query that Returns StructuralType Results](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).</span></span>  
  
2.  <span data-ttu-id="c9dde-113">Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :</span><span class="sxs-lookup"><span data-stu-id="c9dde-113">Pass the following query as an argument to the `ExecuteStructuralTypeQuery` method:</span></span>  
  
 [!code-csharp[DP EntityServices Concepts 2#COMMENT](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#comment)]  
  
## <a name="see-also"></a><span data-ttu-id="c9dde-114">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c9dde-114">See Also</span></span>  
 [<span data-ttu-id="c9dde-115">Panoramica di Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c9dde-115">Entity SQL Overview</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-overview.md)  
 [<span data-ttu-id="c9dde-116">Riferimento a Entity SQL</span><span class="sxs-lookup"><span data-stu-id="c9dde-116">Entity SQL Reference</span></span>](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
