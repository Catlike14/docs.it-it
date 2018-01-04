---
title: LINQ to SQL esempio
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5f39db9e-0e62-42c9-8c98-bb8b54cec98c
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 06273f3ac7dd159adac4c058a23c187f44417d94
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="linq-to-sql-sample"></a>LINQ to SQL esempio
In questo esempio viene illustrato come creare un'attività per l'uso di entità di query LINQ to SQL da tabelle nei database SQL Server.  
  
> [!IMPORTANT]
>  È possibile che gli esempi di [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\Samples\WCFWFCardspace`  
>   
>  Se questa directory non esiste, fare clic sul collegamento per il download di esempi nella parte superiore di questa pagina. Notare che questo collegamento scarica e installa tutti gli esempi di [!INCLUDE[wf1](../../../../includes/wf1-md.md)], [!INCLUDE[indigo2](../../../../includes/indigo2-md.md)] e [!INCLUDE[infocard](../../../../includes/infocard-md.md)]. Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\Samples\WCFWFCardSpace\WF\Scenario\ActivityLibrary\Linq\LinqToSql`  
  
## <a name="activity-details-for-findinsqltable"></a>Dettagli dell'attività per FindInSqlTable  
 Questa attività consente agli utenti di eseguire query su entità di tabelle in un database usando LINQ to SQL. Gli utenti dell'attività devono inoltre fornire un predicato LINQ nel formato di un'espressione lambda per filtrare i risultati. Se non è fornito alcun predicato, viene restituita l'intera tabella. Nella tabella seguente viene descritta la proprietà e i valori restituiti per l'attività.  
  
|Proprietà o valore restituito|Descrizione|  
|------------------------------|-----------------|  
|Proprietà `Collection`|Proprietà obbligatoria che specifica la raccolta di origine.|  
|Proprietà `Predicate`|Proprietà obbligatoria che specifica il filtro per la raccolta nel formato di un'espressione lambda.|  
|Valore restituito|La raccolta filtrata.|  
  
## <a name="code-sample-that-uses-the-custom-activity"></a>Esempio di codice che usa l'attività personalizzata  
 Nell'esempio di codice seguente viene usata l'attività personalizzata `FindInSqlTable` per trovare tutte le righe in una tabella di SQL Server denominata `Employee` dove la colonna `Role` è uguale a `SDE`.  
  
```csharp  
new FindInSqlTable<Employee>   
{  
    ConnectionString = @"Data Source=.\SQLExpress;Initial Catalog=LinqToSqlSample;Integrated Security=True",                          
    Predicate = new LambdaValue<Func<Employee, bool>>(c => new Func<Employee, bool>(emp => emp.Role.Equals("SDE"))),  
    Result = new OutArgument<IList<Employee>>(employees)  
},  
```  
  
#### <a name="to-use-this-sample"></a>Per usare questo esempio  
  
1.  Aprire un prompt dei comandi.  
  
2.  Passare alla cartella contenente questo esempio.  
  
3.  Eseguire il file di comando Setup.cmd.  
  
    > [!NOTE]
    >  Lo script Setup.cmd tenta di installare il database di esempio in SQL Server Express nel computer locale. Se si desidera installarlo nell'altra istanza del server SQL, modificare Setup.cmd.  
  
     Lo script Setup.cmd esegue le azioni seguenti:  
  
    -   Crea un database denominato LinqToSqlSample.  
  
    -   Crea una tabella Ruoli.  
  
    -   Crea una tabella Employees.  
  
    -   Inserisce 3 record nella tabella Ruoli.  
  
    -   Inserisce 12 record nella tabella Employees.  
  
4.  Usando [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)], aprire il file della soluzione LinqToSQL.sln.  
  
5.  Per compilare la soluzione, premere CTRL+MAIUSC+B.  
  
6.  Per eseguire la soluzione, premere F5.  
  
#### <a name="to-uninstall-the-linqtosql-sample-database"></a>Per disinstallare il database di esempio LinqToSql  
  
1.  Aprire un prompt dei comandi.  
  
2.  Passare alla cartella contenente questo esempio.  
  
3.  Eseguire il file di comando Cleanup.cmd.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] . Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Scenario\ActivityLibrary\Liiinq\LinqToSql`  
  
## <a name="see-also"></a>Vedere anche  
 [LINQ to SQL](http://go.microsoft.com/fwlink/?LinkId=150376)  
 [Introduzione (LINQ to SQL)](http://go.microsoft.com/fwlink/?LinkId=150377)
