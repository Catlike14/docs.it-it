---
title: = (uguale a) (Entity SQL)
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-ado
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 948eb588-7080-4046-bb48-633b007393bf
caps.latest.revision: ''
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload:
- dotnet
ms.openlocfilehash: 27faf6c59afd4de2481f474053812b12182e3f58
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="-equals-entity-sql"></a>= (uguale a) (Entity SQL)
Consente di confrontare due espressioni per verificare se sono uguali.  
  
## <a name="syntax"></a>Sintassi  
  
```  
expression = expression  
or   
expression == expression  
```  
  
## <a name="arguments"></a>Argomenti  
 `expression`  
 Qualsiasi espressione valida. Entrambe le espressioni devono contenere tipi di dati convertibili in modo implicito.  
  
## <a name="result-types"></a>Tipi di risultati  
 `true` se l'espressione a sinistra è uguale a quella a destra; in caso contrario, `false`.  
  
## <a name="remarks"></a>Note  
 L'operatore == è equivalente a =.  
  
## <a name="example"></a>Esempio  
 Nella query Entity SQL seguente viene usato l'operatore di confronto = per confrontare due espressioni e verificare se sono uguali. La query è basata sul modello Sales di AdventureWorks. Per compilare ed eseguire questa query, effettuare le operazioni seguenti:  
  
1.  Seguire la procedura indicata in [Procedura: eseguire una query che restituisce risultati StructuralType](../../../../../../docs/framework/data/adonet/ef/how-to-execute-a-query-that-returns-structuraltype-results.md).  
  
2.  Passare la query seguente come argomento al metodo `ExecuteStructuralTypeQuery` :  
  
 [!code-csharp[DP EntityServices Concepts 2#EQUALS](../../../../../../samples/snippets/csharp/VS_Snippets_Data/dp entityservices concepts 2/cs/entitysql.cs#equals)]  
  
## <a name="see-also"></a>Vedere anche  
 [Riferimento a Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
