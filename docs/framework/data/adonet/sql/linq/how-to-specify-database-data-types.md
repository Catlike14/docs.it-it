---
title: 'Procedura: specificare i tipi di dati del database'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2228fdad-7e6a-4b1b-b4d1-79d0198b7c28
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: d46c63f5944895311e73524a0ba31a126d768522
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-specify-database-data-types"></a><span data-ttu-id="03535-102">Procedura: specificare i tipi di dati del database</span><span class="sxs-lookup"><span data-stu-id="03535-102">How to: Specify Database Data Types</span></span>
<span data-ttu-id="03535-103">Utilizzare il [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> proprietà in un <xref:System.Data.Linq.Mapping.ColumnAttribute> attributo per specificare il testo esatto che definisce la colonna in una dichiarazione di tabella T-SQL.</span><span class="sxs-lookup"><span data-stu-id="03535-103">Use the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property on a <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute to specify the exact text that defines the column in a T-SQL table declaration.</span></span>  
  
 <span data-ttu-id="03535-104">È necessario specificare la proprietà <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> solo se si prevede di usare <xref:System.Data.Linq.DataContext.CreateDatabase%2A> per creare un'istanza del database.</span><span class="sxs-lookup"><span data-stu-id="03535-104">You must specify the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property only if you plan to use <xref:System.Data.Linq.DataContext.CreateDatabase%2A> to create an instance of the database.</span></span>  
  
 <span data-ttu-id="03535-105">Per esempi di codice, vedere <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span><span class="sxs-lookup"><span data-stu-id="03535-105">For code examples, see <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A>.</span></span>  
  
### <a name="to-specify-text-to-define-a-data-type-in-a-t-sql-table"></a><span data-ttu-id="03535-106">Per specificare il testo per definire un tipo di dati in una tabella T-SQL</span><span class="sxs-lookup"><span data-stu-id="03535-106">To specify text to define a data type in a T-SQL table</span></span>  
  
1.  <span data-ttu-id="03535-107">Aggiungere la proprietà <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> all'attributo <xref:System.Data.Linq.Mapping.ColumnAttribute>.</span><span class="sxs-lookup"><span data-stu-id="03535-107">Add the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property to the <xref:System.Data.Linq.Mapping.ColumnAttribute> attribute.</span></span>  
  
2.  <span data-ttu-id="03535-108">Impostare il valore della proprietà <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> specificando il testo esatto usato da T-SQL.</span><span class="sxs-lookup"><span data-stu-id="03535-108">Set the value of the <xref:System.Data.Linq.Mapping.ColumnAttribute.DbType%2A> property to the exact text that is used by T-SQL.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="03535-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="03535-109">See Also</span></span>  
 [<span data-ttu-id="03535-110">LINQ to SQL modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="03535-110">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 [<span data-ttu-id="03535-111">Procedura: personalizzare classi di entità utilizzando l'Editor di codice</span><span class="sxs-lookup"><span data-stu-id="03535-111">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
