---
title: Sospensione e ripresa di un flusso di lavoro
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 11f38339-79c7-4295-b610-24a7223bbf6d
caps.latest.revision: "4"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0d7637a9d49100d3a46ceb3c49769cacae14b5e8
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="pausing-and-resuming-a-workflow"></a><span data-ttu-id="f7c34-102">Sospensione e ripresa di un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="f7c34-102">Pausing and Resuming a Workflow</span></span>
<span data-ttu-id="f7c34-103">I flussi di lavoro verranno sospesi e ripresi in risposta ad attività di segnalibro e di blocco, ad esempio <xref:System.Activities.Statements.Delay>, ma un flusso di lavoro può anche essere sospeso, scaricato e ripreso in modo esplicito tramite la persistenza.</span><span class="sxs-lookup"><span data-stu-id="f7c34-103">Workflows will pause and resume in response to bookmarks and blocking activities such as <xref:System.Activities.Statements.Delay>, but a workflow can also be explicitly paused, unloaded, and resumed by using persistence.</span></span>  
  
## <a name="pausing-a-workflow"></a><span data-ttu-id="f7c34-104">Sospensione di un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="f7c34-104">Pausing a Workflow</span></span>  
 <span data-ttu-id="f7c34-105">Per sospendere un flusso di lavoro, usare <xref:System.Activities.WorkflowApplication.Unload%2A>.</span><span class="sxs-lookup"><span data-stu-id="f7c34-105">To pause a workflow, use <xref:System.Activities.WorkflowApplication.Unload%2A>.</span></span>  <span data-ttu-id="f7c34-106">Questo metodo richiede che il flusso di lavoro sia persistente e venga scaricato e genererà un'eccezione <xref:System.TimeoutException> se il flusso di lavoro non viene scaricato in 30 secondi.</span><span class="sxs-lookup"><span data-stu-id="f7c34-106">This method requests that the workflow persist and unload, and will throw a <xref:System.TimeoutException> if the workflow does not unload in 30 seconds.</span></span>  
  
```csharp  
try  
{  
    // attempt to unload will fail if the workflow is idle within a NoPersistZone  
    application.Unload(TimeSpan.FromSeconds(5));  
}  
catch (TimeoutException e)  
{  
    Console.WriteLine(e.Message);  
}  
```  
  
## <a name="resuming-a-workflow"></a><span data-ttu-id="f7c34-107">Ripresa di un flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="f7c34-107">Resuming a Workflow</span></span>  
 <span data-ttu-id="f7c34-108">Per riprendere un flusso di lavoro precedentemente sospeso e scaricato, usare <xref:System.Activities.WorkflowApplication.Load%2A>.</span><span class="sxs-lookup"><span data-stu-id="f7c34-108">To resume a previously paused and unloaded workflow, use <xref:System.Activities.WorkflowApplication.Load%2A>.</span></span> <span data-ttu-id="f7c34-109">Questo metodo carica un flusso di lavoro da un archivio di persistenza in memoria.</span><span class="sxs-lookup"><span data-stu-id="f7c34-109">This method loads a workflow from a persistence store into memory.</span></span>  
  
```csharp  
WorkflowApplication application = new WorkflowApplication(activity);  
application.InstanceStore = instanceStore;  
application.Load(id);  
```  
  
## <a name="example"></a><span data-ttu-id="f7c34-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="f7c34-110">Example</span></span>  
 <span data-ttu-id="f7c34-111">Nell'esempio di codice seguente viene illustrato come sospendere e riprendere un flusso di lavoro tramite persistenza.</span><span class="sxs-lookup"><span data-stu-id="f7c34-111">The following code sample demonstrates how to pause and resume a workflow by using persistence.</span></span>  
  
```csharp  
static string bkName = "bkName";  
static void Main(string[] args)   
{  
    StartAndUnloadInstance();  
}  
  
static void StartAndUnloadInstance()   
{  
    AutoResetEvent waitHandler = new AutoResetEvent(false);  
    WorkflowApplication wfApp = new WorkflowApplication(GetDelayedWF());  
    SqlWorkflowInstanceStore instanceStore = SetupSqlpersistenceStore();  
    wfApp.InstanceStore = instanceStore;  
    wfApp.Extensions.Add(SetupMyFileTrackingParticipant);  
    wfApp.PersistableIdle = (e) => {          ///persists application state and remove it from memory   
    return PersistableIdleAction.Unload;  
    };  
    wfApp.Unloaded = (e) => {  
        waitHandler.Set();  
    };  
    Guid id = wfApp.Id;  
    wfApp.Run();  
    waitHandler.WaitOne();  
    LoadAndCompleteInstance(id);  
}  
  
static void LoadAndCompleteInstance(Guid id)   
{            
    Console.WriteLine("Press <enter> to load the persisted workflow");  
    Console.ReadLine();  
    AutoResetEvent waitHandler = new AutoResetEvent(false);  
    WorkflowApplication wfApp = new WorkflowApplication(new Workflow1());  
    wfApp.InstanceStore =  
        new SqlWorkflowInstanceStore(ConfigurationManager.AppSettings["SqlWF4PersistenceConnectionString"].ToString());  
    wfApp.Completed = (workflowApplicationCompletedEventArgs) => {  
        Console.WriteLine("\nWorkflowApplication has Completed in the {0} state.",  
            workflowApplicationCompletedEventArgs.CompletionState);  
    };  
    wfApp.Unloaded = (workflowApplicationEventArgs) => {  
        Console.WriteLine("WorkflowApplication has Unloaded\n");  
        waitHandler.Set();  
    };  
    wfApp.Load(id);  
    wfApp.Run();  
    waitHandler.WaitOne();  
}  
  
public static Activity GetDelayedWF()   
{  
    return new Sequence {  
        Activities ={  
            new WriteLine{Text="Workflow Started"},  
            new Delay{Duration=TimeSpan.FromSeconds(10)},  
            new WriteLine{Text="Workflow Ended"}  
        }  
    };  
}  
  
private static SqlWorkflowInstanceStore SetupSqlpersistenceStore()   
{   
     string connectionString = ConfigurationManager.AppSettings["SqlWF4PersistenceConnectionString"].ToString();  
    SqlWorkflowInstanceStore sqlWFInstanceStore = new SqlWorkflowInstanceStore(connectionString);  
    sqlWFInstanceStore.InstanceCompletionAction = InstanceCompletionAction.DeleteAll;  
    InstanceHandle handle = sqlWFInstanceStore.CreateInstanceHandle();  
    InstanceView view = sqlWFInstanceStore.Execute(handle, new CreateWorkflowOwnerCommand(), TimeSpan.FromSeconds(5));  
    handle.Free();  
    sqlWFInstanceStore.DefaultInstanceOwner = view.InstanceOwner;  
    return sqlWFInstanceStore;  
}  
```
