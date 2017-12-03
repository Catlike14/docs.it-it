---
title: Servizi e transazioni
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: service contracts [WCF], designing services and transactions
ms.assetid: 864813ff-2709-4376-912d-f5c8d318c460
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 680a86d453dd8ca7c78d0ca6ba60cbaa691e44f3
ms.sourcegitcommit: ce279f2d7fe2220e6ea0a25a8a7a5370ddf8d9f0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2017
---
# <a name="services-and-transactions"></a><span data-ttu-id="29c93-102">Servizi e transazioni</span><span class="sxs-lookup"><span data-stu-id="29c93-102">Services and Transactions</span></span>
<span data-ttu-id="29c93-103">Le applicazioni di [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] possono avviare una transazione dall'interno di un client e coordinarla all'interno dell'operazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="29c93-103">[!INCLUDE[indigo1](../../../includes/indigo1-md.md)] applications can initiate a transaction from within a client and coordinate the transaction within the service operation.</span></span> <span data-ttu-id="29c93-104">I client possono avviare una transazione e richiamare varie operazioni di servizio nonché fare in modo che per queste ultime venga eseguito il commit o il rollback come unità singola.</span><span class="sxs-lookup"><span data-stu-id="29c93-104">Clients can initiate a transaction and invoke several service operations and ensure that the service operations are either committed or rolled back as a single unit.</span></span>  
  
 <span data-ttu-id="29c93-105">È possibile attivare il comportamento della transazione nel contratto di servizio specificando un elemento <xref:System.ServiceModel.ServiceBehaviorAttribute> e impostando le proprietà <xref:System.ServiceModel.ServiceBehaviorAttribute.TransactionIsolationLevel%2A> e <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionScopeRequired%2A> per operazioni di servizio che richiedono transazioni client.</span><span class="sxs-lookup"><span data-stu-id="29c93-105">You can enable the transaction behavior in the service contract by specifying a <xref:System.ServiceModel.ServiceBehaviorAttribute> and setting its <xref:System.ServiceModel.ServiceBehaviorAttribute.TransactionIsolationLevel%2A> and <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionScopeRequired%2A> properties for service operations that require client transactions.</span></span> <span data-ttu-id="29c93-106">Il parametro <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionAutoComplete%2A> specifica se la transazione in cui viene eseguito il metodo viene completata automaticamente nel caso in cui non venga generata alcuna eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="29c93-106">The <xref:System.ServiceModel.OperationBehaviorAttribute.TransactionAutoComplete%2A> parameter specifies whether the transaction in which the method executes is automatically completed if no unhandled exceptions are thrown.</span></span> [!INCLUDE[crabout](../../../includes/crabout-md.md)]<span data-ttu-id="29c93-107">Questi attributi, vedere [gli attributi della transazione di ServiceModel](../../../docs/framework/wcf/feature-details/servicemodel-transaction-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="29c93-107"> these attributes, see [ServiceModel Transaction Attributes](../../../docs/framework/wcf/feature-details/servicemodel-transaction-attributes.md).</span></span>  
  
 <span data-ttu-id="29c93-108">Il lavoro eseguito nelle operazioni di servizio e curato da un gestore di risorse, ad esempio la registrazione di aggiornamenti del database, fa parte della transazione del client.</span><span class="sxs-lookup"><span data-stu-id="29c93-108">The work that is performed in the service operations and managed by a resource manager, such as logging database updates, is part of the client’s transaction.</span></span>  
  
 <span data-ttu-id="29c93-109">Nell'esempio seguente viene dimostrato l'utilizzo degli attributi <xref:System.ServiceModel.ServiceBehaviorAttribute> e <xref:System.ServiceModel.OperationBehaviorAttribute> per controllare il comportamento della transazione dal lato del servizio.</span><span class="sxs-lookup"><span data-stu-id="29c93-109">The following sample demonstrates usage of the <xref:System.ServiceModel.ServiceBehaviorAttribute> and <xref:System.ServiceModel.OperationBehaviorAttribute> attributes to control service-side transaction behavior.</span></span>  
  
```  
[ServiceBehavior(TransactionIsolationLevel = System.Transactions.IsolationLevel.Serializable)]  
public class CalculatorService: ICalculatorLog  
{  
    [OperationBehavior(TransactionScopeRequired = true,  
                           TransactionAutoComplete = true)]  
    public double Add(double n1, double n2)  
    {  
        recordToLog(String.Format("Added {0} to {1}", n1, n2));  
        return n1 + n2;  
    }  
  
    [OperationBehavior(TransactionScopeRequired = true,   
                               TransactionAutoComplete = true)]  
    public double Subtract(double n1, double n2)  
    {  
        recordToLog(String.Format("Subtracted {0} from {1}", n1, n2));  
        return n1 - n2;  
    }  
  
    [OperationBehavior(TransactionScopeRequired = true,   
                                       TransactionAutoComplete = true)]  
    public double Multiply(double n1, double n2)  
    {  
        recordToLog(String.Format("Multiplied {0} by {1}", n1, n2));  
        return n1 * n2;  
    }  
  
    [OperationBehavior(TransactionScopeRequired = true,   
                                       TransactionAutoComplete = true)]  
    public double Divide(double n1, double n2)  
    {  
        recordToLog(String.Format("Divided {0} by {1}", n1, n2));  
        return n1 / n2;  
    }  
  
}  
```  
  
 <span data-ttu-id="29c93-110">È possibile abilitare le transazioni e delle transazioni flusso mediante la configurazione del client e servizio di associazioni per utilizzare il protocollo WS-AtomicTransaction e impostazione di [ \<transactionFlow >](../../../docs/framework/configure-apps/file-schema/wcf/transactionflow.md) elemento `true`, come mostrato Nell'esempio di configurazione seguente.</span><span class="sxs-lookup"><span data-stu-id="29c93-110">You can enable transactions and transaction flow by configuring the client and service bindings to use the WS-AtomicTransaction protocol, and setting the [\<transactionFlow>](../../../docs/framework/configure-apps/file-schema/wcf/transactionflow.md) element to `true`, as shown in the following sample configuration.</span></span>  
  
```xml  
<client>  
    <endpoint address="net.tcp://localhost/ServiceModelSamples/service"   
          binding="netTcpBinding"   
          bindingConfiguration="netTcpBindingWSAT"   
          contract="Microsoft.ServiceModel.Samples.ICalculatorLog" />  
</client>  
  
<bindings>  
    <netTcpBinding>  
        <binding name="netTcpBindingWSAT"  
                transactionFlow="true"  
                transactionProtocol="WSAtomicTransactionOctober2004" />  
     </netTcpBinding>  
</bindings>  
```  
  
 <span data-ttu-id="29c93-111">I client possono iniziare una transazione creando un elemento <xref:System.Transactions.TransactionScope> e richiamando operazioni di servizio nell'ambito della transazione.</span><span class="sxs-lookup"><span data-stu-id="29c93-111">Clients can begin a transaction by creating a <xref:System.Transactions.TransactionScope> and invoking service operations within the scope of the transaction.</span></span>  
  
```  
using (TransactionScope ts = new TransactionScope(TransactionScopeOption.RequiresNew))  
{  
    //Do work here  
    ts.Complete();  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="29c93-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="29c93-112">See Also</span></span>  
 [<span data-ttu-id="29c93-113">Supporto transazionale in System. ServiceModel</span><span class="sxs-lookup"><span data-stu-id="29c93-113">Transactional Support in System.ServiceModel</span></span>](../../../docs/framework/wcf/feature-details/transactional-support-in-system-servicemodel.md)  
 [<span data-ttu-id="29c93-114">Modelli di transazione</span><span class="sxs-lookup"><span data-stu-id="29c93-114">Transaction Models</span></span>](../../../docs/framework/wcf/feature-details/transaction-models.md)  
 [<span data-ttu-id="29c93-115">Flusso delle transazioni WS</span><span class="sxs-lookup"><span data-stu-id="29c93-115">WS Transaction Flow</span></span>](../../../docs/framework/wcf/samples/ws-transaction-flow.md)
