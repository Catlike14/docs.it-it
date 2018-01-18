---
title: Esecuzione di query tra relazioni
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
ms.assetid: 297878d0-685b-4c01-b2e0-9d731b7322bc
caps.latest.revision: "5"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: f06297f79807a1548a6b5ac77aed45f52c8d03af
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/17/2018
---
# <a name="querying-across-relationships"></a>Esecuzione di query tra relazioni
I riferimenti ad altri oggetti o raccolte di altri oggetti nelle definizioni della classe corrispondono direttamente alle relazioni di chiavi esterne nel database. È possibile usare queste relazioni quando si esegue una query usando la notazione del punto per accedere alle proprietà della relazione e spostarsi tra gli oggetti. Queste operazioni di accesso vengono convertite in join più complessi o sottoquery correlate nell'equivalente SQL.  
  
 Ad esempio, usando la query seguente è possibile spostarsi da ordini a clienti per limitare i risultati solo agli ordini per i clienti residenti nell'area londinese.  
  
 [!code-csharp[DLinqQueryConcepts#3](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#3)]
 [!code-vb[DLinqQueryConcepts#3](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#3)]  
  
 Se le proprietà della relazione non esistessero sarebbe necessario scriverle manualmente come *join*, esattamente come si farebbe in una query SQL, come illustrato nel codice seguente:  
  
 [!code-csharp[DLinqQueryConcepts#4](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#4)]
 [!code-vb[DLinqQueryConcepts#4](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#4)]  
  
 È possibile utilizzare il *relazione* proprietà per definire questa particolare relazione una volta. quindi usare la più pratica sintassi del punto. Le proprietà della relazione esistono tuttavia soprattutto perché i modelli a oggetti specifici del dominio sono in genere definiti come gerarchie o grafici. Gli oggetti usati nella programmazione dispongono di riferimenti ad altri oggetti. È solo una coincidenza che le relazioni da oggetto a oggetto corrispondano alle relazioni di tipo chiave esterna nei database. L'accesso alle proprietà offre quindi un modo pratico per scrivere join.  
  
 A questo riguardo, le proprietà della relazione sono più importanti sul lato dei risultati di una query anziché nella query stessa. Dopo il recupero dei dati su un cliente particolare tramite la query, la definizione della classe indica che sono presenti ordini. In altre parole, si prevede che la proprietà `Orders` di un particolare cliente sia una raccolta popolata con tutti gli ordini di tale cliente. Si tratta in effetti del contratto dichiarato definendo le classi in questo modo. Si prevede che nei risultati siano inclusi gli ordini, anche se non sono stati espressamente richiesti nella query. Si prevede che il modello a oggetti appaia come un'estensione in memoria del database con gli oggetti correlati immediatamente disponibili.  
  
 Dopo avere creato le relazioni, è possibile scrivere query facendo riferimento alle proprietà delle relazioni definite nelle classi. Questi riferimenti alle relazioni corrispondono alle relazioni di chiave esterna nel database. Le operazioni che usano queste relazioni vengono convertite in join più complessi nell'equivalente SQL. A condizione che sia stata definita una relazione usando l'attributo <xref:System.Data.Linq.Mapping.AssociationAttribute>, non sarà necessario codificare un join esplicito in [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].  
  
 Per mantenere questa apparenza, [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] implementa una tecnica denominata *il caricamento posticipato*. Per ulteriori informazioni, vedere [posticipata e il caricamento immediato](../../../../../../docs/framework/data/adonet/sql/linq/deferred-versus-immediate-loading.md).  
  
 Si consideri la query SQL seguente al progetto un elenco di `CustomerID` - `OrderID` coppie:  
  
```  
SELECT t0.CustomerID, t1.OrderID  
FROM   Customers AS t0 INNER JOIN  
          Orders AS t1 ON t0.CustomerID = t1.CustomerID  
WHERE  (t0.City = @p0)  
```  
  
 Per ottenere gli stessi risultati tramite [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)], usare il riferimento alla proprietà `Orders` esistente nella classe `Customer`. Il `Orders` riferimento fornisce le informazioni necessarie per eseguire la query e il progetto di `CustomerID` - `OrderID` coppie, come illustrato nel codice seguente:  
  
 [!code-csharp[DLinqQueryConcepts#5](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#5)]
 [!code-vb[DLinqQueryConcepts#5](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#5)]  
  
 È inoltre possibile procedere in senso inverso, ovvero eseguire una query su `Orders` e usare il relativo riferimento alla relazione di `Customer` per accedere alle informazioni sull'oggetto `Customer` associato. Il codice seguente vengono proiettate le stesse `CustomerID` - `OrderID` coppie come in precedenza, ma questa volta eseguendo una query `Orders` anziché `Customers`.  
  
 [!code-csharp[DLinqQueryConcepts#6](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqQueryConcepts/cs/Program.cs#6)]
 [!code-vb[DLinqQueryConcepts#6](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqQueryConcepts/vb/Module1.vb#6)]  
  
## <a name="see-also"></a>Vedere anche  
 [Concetti relativi alle query](../../../../../../docs/framework/data/adonet/sql/linq/query-concepts.md)
