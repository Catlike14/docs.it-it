---
title: Transazioni distribuite Oracle
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c340ca81-ef79-402f-b204-c5156b890fe5
caps.latest.revision: "3"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: c901ccf9132dc766d78efb24428b6469458a70fa
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="oracle-distributed-transactions"></a><span data-ttu-id="49ec4-102">Transazioni distribuite Oracle</span><span class="sxs-lookup"><span data-stu-id="49ec4-102">Oracle Distributed Transactions</span></span>
<span data-ttu-id="49ec4-103">Se rileva una transazione attiva, l'oggetto <xref:System.Data.OracleClient.OracleConnection> esegue l'inserimento automatico in una transazione distribuita esistente.</span><span class="sxs-lookup"><span data-stu-id="49ec4-103">The <xref:System.Data.OracleClient.OracleConnection> object automatically enlists in an existing distributed transaction if it determines that a transaction is active.</span></span> <span data-ttu-id="49ec4-104">L'inserimento automatico in una transazione viene eseguito anche quando la connessione viene aperta o recuperata dal pool di connessioni.</span><span class="sxs-lookup"><span data-stu-id="49ec4-104">Automatic transaction enlistment occurs when the connection is opened or retrieved from the connection pool.</span></span> <span data-ttu-id="49ec4-105">È possibile disabilitare l'inserimento automatico in transazioni esistenti specificando</span><span class="sxs-lookup"><span data-stu-id="49ec4-105">You can disable auto-enlistment in existing transactions by specifying</span></span>  
  
```  
Enlist=false  
```  
  
 <span data-ttu-id="49ec4-106">come parametro della stringa di connessione per un tipo <xref:System.Data.OracleClient.OracleConnection>.</span><span class="sxs-lookup"><span data-stu-id="49ec4-106">as a connection string parameter for an <xref:System.Data.OracleClient.OracleConnection>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="49ec4-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="49ec4-107">See Also</span></span>  
 [<span data-ttu-id="49ec4-108">Oracle e ADO.NET</span><span class="sxs-lookup"><span data-stu-id="49ec4-108">Oracle and ADO.NET</span></span>](../../../../docs/framework/data/adonet/oracle-and-adonet.md)  
 [<span data-ttu-id="49ec4-109">Provider gestiti ADO.NET e Centro per sviluppatori di set di dati</span><span class="sxs-lookup"><span data-stu-id="49ec4-109">ADO.NET Managed Providers and DataSet Developer Center</span></span>](http://go.microsoft.com/fwlink/?LinkId=217917)
