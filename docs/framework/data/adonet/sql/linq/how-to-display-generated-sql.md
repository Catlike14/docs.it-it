---
title: 'Procedura: visualizzare il codice SQL generato'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 626492c0-5ee3-4675-88e8-8c40379510b6
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 5c75ac8734a92fc76613643c3831d0b767e92feb
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="how-to-display-generated-sql"></a><span data-ttu-id="5c622-102">Procedura: visualizzare il codice SQL generato</span><span class="sxs-lookup"><span data-stu-id="5c622-102">How to: Display Generated SQL</span></span>
<span data-ttu-id="5c622-103">È possibile visualizzare il codice SQL generato per le query e modificare l'elaborazione usando la proprietà <xref:System.Data.Linq.DataContext.Log%2A>.</span><span class="sxs-lookup"><span data-stu-id="5c622-103">You can view the SQL code generated for queries and change processing by using the <xref:System.Data.Linq.DataContext.Log%2A> property.</span></span> <span data-ttu-id="5c622-104">Questo approccio può essere utile per comprendere la funzionalità di [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] e per eseguire il debug di problemi specifici.</span><span class="sxs-lookup"><span data-stu-id="5c622-104">This approach can be useful for understanding [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] functionality and for debugging specific problems.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5c622-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c622-105">Example</span></span>  
 <span data-ttu-id="5c622-106">Nell'esempio riportato di seguito viene usata la proprietà <xref:System.Data.Linq.DataContext.Log%2A> per visualizzare il codice SQL nella finestra della console prima di eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="5c622-106">The following example uses the <xref:System.Data.Linq.DataContext.Log%2A> property to display SQL code in the console window before the code is executed.</span></span>  <span data-ttu-id="5c622-107">È possibile usare questa proprietà con comandi di query, inserimento, aggiornamento ed eliminazione.</span><span class="sxs-lookup"><span data-stu-id="5c622-107">You can use this property with query, insert, update, and delete commands.</span></span>  
  
 <span data-ttu-id="5c622-108">Le righe nella finestra della console sono le stesse che vengono visualizzate quando si esegue il codice [!INCLUDE[vbprvb](../../../../../../includes/vbprvb-md.md)] o C# seguente.</span><span class="sxs-lookup"><span data-stu-id="5c622-108">The lines from the console window are what you see when you execute the [!INCLUDE[vbprvb](../../../../../../includes/vbprvb-md.md)] or C# code that follows.</span></span>  
  
```  
SELECT [t0].[CustomerID], [t0].[CompanyName], [t0].[ContactName], [t0].[ContactT  
itle], [t0].[Address], [t0].[City], [t0].[Region], [t0].[PostalCode], [t0].[Coun  
try], [t0].[Phone], [t0].[Fax]  
FROM [dbo].[Customers] AS [t0]  
WHERE [t0].[City] = @p0  
-- @p0: Input String (Size = 6; Prec = 0; Scale = 0) [London]  
-- Context: SqlProvider(Sql2005) Model: AttributedMetaModel Build: 3.5.20810.0  
```  
  
```  
AROUT  
BSBEV  
CONSH  
EASTC  
NORTS  
SEVES  
```  
  
 [!code-csharp[DLinqDebuggingSupport#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqDebuggingSupport/cs/Program.cs#1)]
 [!code-vb[DLinqDebuggingSupport#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqDebuggingSupport/vb/Module1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="5c622-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5c622-109">See Also</span></span>  
 [<span data-ttu-id="5c622-110">Supporto per il debug</span><span class="sxs-lookup"><span data-stu-id="5c622-110">Debugging Support</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/debugging-support.md)
