---
title: "Proprietà di esecuzione del flusso di lavoro"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: a50e088e-3a45-4267-bd51-1a3e6c2d246d
caps.latest.revision: "9"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: d119d721964df7ea1c007eadd17a8db54f4f8cd9
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="workflow-execution-properties"></a><span data-ttu-id="8f0b9-102">Proprietà di esecuzione del flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="8f0b9-102">Workflow Execution Properties</span></span>
<span data-ttu-id="8f0b9-103">Tramite l'archiviazione thread-local (TLS), CLR gestisce un contesto di esecuzione per ogni thread.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-103">Through thread local storage (TLS), the CLR maintains an execution context for each thread.</span></span> <span data-ttu-id="8f0b9-104">Questo contesto di esecuzione determina le proprietà note dei thread quali l'identità del thread, la transazione di ambiente e il set di autorizzazioni corrente oltre alle proprietà del thread definite dall'utente come gli slot denominati.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-104">This execution context governs well-known thread properties such as the thread identity, the ambient transaction, and the current permission set in addition to user-defined thread properties like named slots.</span></span>  
  
 <span data-ttu-id="8f0b9-105">A differenza dei programmi destinati direttamente a CLR, i programmi del flusso di lavoro sono alberi di attività con ambiti gerarchici che vengono eseguite in un ambiente indipendente dal thread.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-105">Unlike programs directly targeting the CLR, workflow programs are hierarchically scoped trees of activities that execute in a thread-agnostic environment.</span></span> <span data-ttu-id="8f0b9-106">Pertanto i meccanismi TLS standard non possono essere usati direttamente per determinare il contesto incluso nell'ambito per un elemento di lavoro specificato.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-106">This implies that the standard TLS mechanisms cannot directly be used to determine what context is in scope for a given work item.</span></span> <span data-ttu-id="8f0b9-107">Ad esempio, due rami paralleli di esecuzione potrebbero usare transazioni diverse, oppure il servizio di pianificazione potrebbe eseguire l'interfoliazione dell'esecuzione sullo stesso thread CLR.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-107">For example, two parallel branches of execution might use different transactions, yet the scheduler might interleave their execution on the same CLR thread.</span></span>  
  
 <span data-ttu-id="8f0b9-108">Le proprietà di esecuzione del flusso di lavoro forniscono un meccanismo per aggiungere proprietà specifiche del contesto all'ambiente di un'attività.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-108">Workflow execution properties provide a mechanism to add context specific properties to an activity’s environment.</span></span> <span data-ttu-id="8f0b9-109">In questo modo un'attività può dichiarare quali proprietà sono incluse nell'ambito per i relativi sottoalberi e inoltre fornire hook per impostare e chiudere TLS al fine di interoperare correttamente con gli oggetti CLR.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-109">This allows an activity to declare which properties are in scope for its sub-tree and also provides hooks for setting up and tearing down TLS to properly interoperate with CLR objects.</span></span>  
  
## <a name="creating-and-using-workflow-execution-properties"></a><span data-ttu-id="8f0b9-110">Creazione e utilizzo di proprietà di esecuzione del flusso di lavoro</span><span class="sxs-lookup"><span data-stu-id="8f0b9-110">Creating and Using Workflow Execution Properties</span></span>  
 <span data-ttu-id="8f0b9-111">Le proprietà di esecuzione del flusso di lavoro in genere implementano l'interfaccia di <xref:System.Activities.IExecutionProperty>, anche se le proprietà incentrate sulla messaggistica possono implementare invece <xref:System.ServiceModel.Activities.ISendMessageCallback> e <xref:System.ServiceModel.Activities.IReceiveMessageCallback>.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-111">Workflow execution properties usually implement the <xref:System.Activities.IExecutionProperty> interface, though properties focused on messaging may implement <xref:System.ServiceModel.Activities.ISendMessageCallback> and <xref:System.ServiceModel.Activities.IReceiveMessageCallback> instead.</span></span> <span data-ttu-id="8f0b9-112">Per creare una proprietà di esecuzione del flusso di lavoro, creare una classe che implementa l'interfaccia <xref:System.Activities.IExecutionProperty> e implementare i membri <xref:System.Activities.IExecutionProperty.SetupWorkflowThread%2A> e <xref:System.Activities.IExecutionProperty.CleanupWorkflowThread%2A>.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-112">To create a workflow execution property, create a class that implements the <xref:System.Activities.IExecutionProperty> interface and implement the members <xref:System.Activities.IExecutionProperty.SetupWorkflowThread%2A> and <xref:System.Activities.IExecutionProperty.CleanupWorkflowThread%2A>.</span></span> <span data-ttu-id="8f0b9-113">Questi membri forniscono la proprietà di esecuzione e consentono di impostare e chiudere correttamente l'archivio locale del thread durante ogni impulso di lavoro dell'attività che contiene la proprietà, incluse eventuali attività figlio.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-113">These members provide the execution property with an opportunity to properly set up and tear down the thread local storage during each pulse of work of the activity that contains the property, including any child activities.</span></span> <span data-ttu-id="8f0b9-114">In questo esempio viene creato un oggetto `ConsoleColorProperty` che imposta l'oggetto `Console.ForegroundColor`.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-114">In this example, a `ConsoleColorProperty` is created that sets the `Console.ForegroundColor`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="8f0b9-115">Esempio di codice seguente in questo argomento si basa sul [le proprietà di esecuzione](../../../docs/framework/windows-workflow-foundation/samples/execution-properties.md) esempio.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-115">The following example code in this topic is based on the [Execution Properties](../../../docs/framework/windows-workflow-foundation/samples/execution-properties.md) sample.</span></span>  
  
```csharp  
class ConsoleColorProperty : IExecutionProperty  
{  
    public const string Name = "ConsoleColorProperty";  
  
    ConsoleColor original;  
    ConsoleColor color;  
  
    public ConsoleColorProperty(ConsoleColor color)  
    {  
        this.color = color;  
    }  
  
    void IExecutionProperty.SetupWorkflowThread()  
    {  
        original = Console.ForegroundColor;  
        Console.ForegroundColor = color;  
    }  
  
    void IExecutionProperty.CleanupWorkflowThread()  
    {  
        Console.ForegroundColor = original;  
    }  
}  
```  
  
 <span data-ttu-id="8f0b9-116">Gli autori di attività possono usare questa proprietà registrandola nell'override di esecuzione dell'attività.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-116">Activity authors can use this property by registering it in the activity’s execute override.</span></span> <span data-ttu-id="8f0b9-117">In questo esempio viene definita un'attività `ConsoleColorScope` che registra l'oggetto `ConsoleColorProperty` aggiungendolo alla raccolta <xref:System.Activities.NativeActivityContext.Properties%2A> dell'oggetto <xref:System.Activities.NativeActivityContext> corrente.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-117">In this example, a `ConsoleColorScope` activity is defined that registers the `ConsoleColorProperty` by adding it to the <xref:System.Activities.NativeActivityContext.Properties%2A> collection of the current <xref:System.Activities.NativeActivityContext>.</span></span>  
  
```csharp  
public sealed class ConsoleColorScope : NativeActivity  
{  
    public ConsoleColorScope()  
        : base()  
    {  
    }  
  
    public ConsoleColor Color { get; set; }  
    public Activity Body { get; set; }  
  
    protected override void Execute(NativeActivityContext context)  
    {  
        context.Properties.Add(ConsoleColorProperty.Name, new ConsoleColorProperty(this.Color));  
  
        if (this.Body != null)  
        {  
            context.ScheduleActivity(this.Body);  
        }  
    }  
}  
```  
  
 <span data-ttu-id="8f0b9-118">Quando il corpo dell'attività inizia un impulso di lavoro, viene chiamato il metodo <xref:System.Activities.IExecutionProperty.SetupWorkflowThread%2A> della proprietà e quando l'impulso di lavoro viene completato, viene chiamato il metodo <xref:System.Activities.IExecutionProperty.CleanupWorkflowThread%2A>.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-118">When the activity’s body starts a pulse of work, the <xref:System.Activities.IExecutionProperty.SetupWorkflowThread%2A> method of the property is called, and when the pulse of work is complete, the <xref:System.Activities.IExecutionProperty.CleanupWorkflowThread%2A> is called.</span></span> <span data-ttu-id="8f0b9-119">In questo esempio viene creato un flusso di lavoro che usa un'attività <xref:System.Activities.Statements.Parallel> con tre rami.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-119">In this example, a workflow is created that uses a <xref:System.Activities.Statements.Parallel> activity with three branches.</span></span> <span data-ttu-id="8f0b9-120">I primi due rami, a differenza del terzo, usano l'attività `ConsoleColorScope`.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-120">The first two branches use the `ConsoleColorScope` activity and the third branch does not.</span></span> <span data-ttu-id="8f0b9-121">Tutti i tre rami contengono due attività <xref:System.Activities.Statements.WriteLine> e un'attività <xref:System.Activities.Statements.Delay>.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-121">All three branches contain two <xref:System.Activities.Statements.WriteLine> activities and a <xref:System.Activities.Statements.Delay> activity.</span></span> <span data-ttu-id="8f0b9-122">Quando l'attività <xref:System.Activities.Statements.Parallel> viene eseguita, le attività contenute nei rami vengono eseguite in un modo caratterizzato da interfoliazione, ma quando ogni attività figlio viene eseguita, l'oggetto `ConsoleColorProperty` applica il corretto colore della console.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-122">When the <xref:System.Activities.Statements.Parallel> activity executes, the activities that are contained in the branches execute in an interleaved manner, but as each child activity executes the correct console color is applied by the `ConsoleColorProperty`.</span></span>  
  
```csharp  
Activity wf = new Parallel  
{  
    Branches =   
    {  
        new ConsoleColorScope  
        {  
            Color = ConsoleColor.Blue,  
            Body = new Sequence  
            {  
                Activities =   
                {  
                    new WriteLine  
                    {  
                        Text = "Start blue text."  
                    },  
                    new Delay  
                    {  
                        Duration = TimeSpan.FromSeconds(1)  
                    },  
                    new WriteLine  
                    {  
                        Text = "End blue text."  
                    }  
                }  
            }  
        },  
        new ConsoleColorScope  
        {  
            Color = ConsoleColor.Red,  
            Body = new Sequence  
            {  
                Activities =   
                {  
                    new WriteLine  
                    {  
                        Text = "Start red text."  
                    },  
                    new Delay  
                    {  
                        Duration = TimeSpan.FromSeconds(1)  
                    },  
                    new WriteLine  
                    {  
                        Text = "End red text."  
                    }  
                }  
            }  
        },  
        new Sequence  
        {  
            Activities =   
            {  
                new WriteLine  
                {  
                    Text = "Start default text."  
                },  
                new Delay  
                {  
                    Duration = TimeSpan.FromSeconds(1)  
                },  
                new WriteLine  
                {  
                    Text = "End default text."  
                }  
            }  
        }  
    }  
};  
  
WorkflowInvoker.Invoke(wf);  
```  
  
 <span data-ttu-id="8f0b9-123">Quando il flusso di lavoro viene richiamato, l'output seguente viene scritto nella finestra della console.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-123">When the workflow is invoked, the following output is written to the console window.</span></span>  
  
```  
Start blue text.  
Start red text.  
Start default text.  
End blue text.  
End red text.  
End default text.  
```  
  
> [!NOTE]
>  <span data-ttu-id="8f0b9-124">Sebbene non venga mostrata nell'output precedente, ogni riga di testo nella finestra della console viene visualizzata con il colore indicato.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-124">Although it is not shown in the previous output, each line of text in the console window is displayed in the indicated color.</span></span>  
  
 <span data-ttu-id="8f0b9-125">Le proprietà di esecuzione del flusso di lavoro possono essere usate dagli autori di attività personalizzate e consentono di gestire l'handle per attività quali <xref:System.ServiceModel.Activities.CorrelationScope> e <xref:System.Activities.Statements.TransactionScope>.</span><span class="sxs-lookup"><span data-stu-id="8f0b9-125">Workflow execution properties can be used by custom activity authors, and they also provide the mechanism for handle management for activities such as the <xref:System.ServiceModel.Activities.CorrelationScope> and <xref:System.Activities.Statements.TransactionScope> activities.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8f0b9-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f0b9-126">See Also</span></span>  
 <xref:System.Activities.IExecutionProperty>  
 <xref:System.Activities.IPropertyRegistrationCallback>  
 <xref:System.Activities.RegistrationContext>
