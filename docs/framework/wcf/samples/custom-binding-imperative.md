---
title: Codice imperativo per associazioni personalizzate
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 6e13bf96-5de0-4476-b646-5f150774418d
caps.latest.revision: "18"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: ed463a22d011af0428cb5c18f7ac8c75a6fca44c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="custom-binding-imperative"></a><span data-ttu-id="5378a-102">Codice imperativo per associazioni personalizzate</span><span class="sxs-lookup"><span data-stu-id="5378a-102">Custom Binding Imperative</span></span>
<span data-ttu-id="5378a-103">L'esempio illustra come scrivere codice imperativo per definire e utilizzare associazioni personalizzate senza utilizzare file di configurazione o un [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] generato dal client.</span><span class="sxs-lookup"><span data-stu-id="5378a-103">The sample demonstrates how to write imperative code to define and use custom bindings without using a configuration file or a [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] generated client.</span></span> <span data-ttu-id="5378a-104">Questo esempio combina le funzionalità fornite dal trasporto HTTP e il canale di sessione attendibile per creare un'associazione basata su HTTP attendibile.</span><span class="sxs-lookup"><span data-stu-id="5378a-104">This sample combines the features provided by the HTTP transport and the reliable session channel to create a reliable HTTP-based binding.</span></span> <span data-ttu-id="5378a-105">Questo esempio è basato sul [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md) che implementa un servizio di calcolatrice.</span><span class="sxs-lookup"><span data-stu-id="5378a-105">This sample is based on the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) that implements a calculator service.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="5378a-106">La procedura di installazione e le istruzioni di compilazione per questo esempio si trovano alla fine di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="5378a-106">The setup procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
 <span data-ttu-id="5378a-107">Nel client e nel servizio, viene creata un'associazione personalizzata che contiene due elementi di associazione (Sessione attendibile e HTTP):</span><span class="sxs-lookup"><span data-stu-id="5378a-107">On both the client and the service, a custom binding is created that contains two binding elements (Reliable Session and HTTP):</span></span>  
  
```  
ReliableSessionBindingElement reliableSession = new ReliableSessionBindingElement();  
reliableSession.Ordered = true;  
  
HttpTransportBindingElement httpTransport = new HttpTransportBindingElement();  
httpTransport.AuthenticationScheme = System.Net.AuthenticationSchemes.Anonymous;  
httpTransport.HostNameComparisonMode = HostNameComparisonMode.StrongWildcard;  
  
CustomBinding binding = new CustomBinding(reliableSession, httpTransport);  
```  
  
 <span data-ttu-id="5378a-108">Nel servizio, l'associazione viene utilizzata aggiungendo un endpoint a ServiceHost:</span><span class="sxs-lookup"><span data-stu-id="5378a-108">On the service, the binding is used by adding an endpoint to the ServiceHost:</span></span>  
  
```  
serviceHost.AddServiceEndpoint(typeof(ICalculator), binding, "");  
```  
  
 <span data-ttu-id="5378a-109">Sul client, l'associazione viene utilizzata da una classe <xref:System.ServiceModel.ChannelFactory> per creare un canale al servizio:</span><span class="sxs-lookup"><span data-stu-id="5378a-109">On the client, the binding is used by a <xref:System.ServiceModel.ChannelFactory> to create a channel to the service:</span></span>  
  
```  
EndpointAddress address = new EndpointAddress("http://localhost:8000/servicemodelsamples/service");  
ChannelFactory<ICalculator> channelFactory = new ChannelFactory<ICalculator>(binding, address);  
ICalculator channel = channelFactory.CreateChannel();  
```  
  
 <span data-ttu-id="5378a-110">Questo canale viene quindi utilizzato per interagire con il servizio:</span><span class="sxs-lookup"><span data-stu-id="5378a-110">This channel is then used to interact with the service:</span></span>  
  
```  
// Call the Add service operation.  
double value1 = 100.00D;  
double value2 = 15.99D;  
double result = channel.Add(value1, value2);  
Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);  
```  
  
 <span data-ttu-id="5378a-111">Quando si esegue l'esempio, le richieste e le risposte dell'operazione vengono visualizzate nella finestra della console client.</span><span class="sxs-lookup"><span data-stu-id="5378a-111">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="5378a-112">Premere INVIO nella finestra del client per arrestare il client.</span><span class="sxs-lookup"><span data-stu-id="5378a-112">Press ENTER in the client window to shut down the client.</span></span>  
  
```  
Add(100,15.99) = 115.99  
Subtract(145,76.54) = 68.46  
Multiply(9,81.25) = 731.25  
Divide(22,7) = 3.14285714285714  
  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="5378a-113">Per impostare, compilare ed eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="5378a-113">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="5378a-114">Assicurarsi di avere eseguito la [procedura di installazione singola per gli esempi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5378a-114">Be sure you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
2.  <span data-ttu-id="5378a-115">Per compilare l'edizione in C# o Visual Basic .NET della soluzione, seguire le istruzioni in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5378a-115">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
3.  <span data-ttu-id="5378a-116">Per eseguire l'esempio in una configurazione singola o tra computer, seguire le istruzioni in [esegue gli esempi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5378a-116">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="5378a-117">È possibile che gli esempi siano già installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="5378a-117">The samples may already be installed on your machine.</span></span> <span data-ttu-id="5378a-118">Verificare la directory seguente (impostazione predefinita) prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="5378a-118">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="5378a-119">Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="5378a-119">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="5378a-120">Questo esempio si trova nella directory seguente.</span><span class="sxs-lookup"><span data-stu-id="5378a-120">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Binding\Custom\Imperative`  
  
## <a name="see-also"></a><span data-ttu-id="5378a-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5378a-121">See Also</span></span>  
 [<span data-ttu-id="5378a-122">Associazione personalizzata</span><span class="sxs-lookup"><span data-stu-id="5378a-122">Custom Binding</span></span>](http://msdn.microsoft.com/en-us/657e8143-beb0-472d-9cfe-ed1a19c2ab08)
