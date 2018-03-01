---
title: 'Procedura: usare un client di Windows Communication Foundation'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- WCF clients [WCF], using
ms.assetid: 190349fc-0573-49c7-bb85-8e316df7f31f
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 0330c386730c6b0436196bb5b85162bc4621c214
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-use-a-windows-communication-foundation-client"></a><span data-ttu-id="ac248-102">Procedura: usare un client di Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="ac248-102">How to: Use a Windows Communication Foundation Client</span></span>
<span data-ttu-id="ac248-103">Questa è l'ultima delle sei attività necessarie per creare un'applicazione [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] di base.</span><span class="sxs-lookup"><span data-stu-id="ac248-103">This is the last of six tasks required to create a basic [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] application.</span></span> <span data-ttu-id="ac248-104">Per una panoramica di tutte e sei le attività, vedere il [esercitazione introduttiva](../../../docs/framework/wcf/getting-started-tutorial.md) argomento.</span><span class="sxs-lookup"><span data-stu-id="ac248-104">For an overview of all six of the tasks, see the [Getting Started Tutorial](../../../docs/framework/wcf/getting-started-tutorial.md) topic.</span></span>  
  
 <span data-ttu-id="ac248-105">Una volta creato e configurato un proxy [!INCLUDE[indigo1](../../../includes/indigo1-md.md)], è possibile creare un'istanza del client e l'applicazione client può essere compilata e utilizzata per comunicare con il servizio [!INCLUDE[indigo2](../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="ac248-105">Once a [!INCLUDE[indigo1](../../../includes/indigo1-md.md)] proxy has been created and configured, a client instance can be created and the client application can be compiled and used to communicate with the [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] service.</span></span> <span data-ttu-id="ac248-106">In questo argomento vengono illustrate le procedure per la creazione di un'istanza e l'utilizzo di un client [!INCLUDE[indigo2](../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="ac248-106">This topic describes procedures for instantiating and using a [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] client.</span></span> <span data-ttu-id="ac248-107">La procedura consente di eseguire tre operazioni:</span><span class="sxs-lookup"><span data-stu-id="ac248-107">This procedure does three things:</span></span>  
  
1.  <span data-ttu-id="ac248-108">Creazione di un'istanza di un client [!INCLUDE[indigo2](../../../includes/indigo2-md.md)].</span><span class="sxs-lookup"><span data-stu-id="ac248-108">Instantiates a [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] client.</span></span>  
  
2.  <span data-ttu-id="ac248-109">Chiamata delle operazioni del servizio dal proxy generato.</span><span class="sxs-lookup"><span data-stu-id="ac248-109">Calls the service operations from the generated proxy.</span></span>  
  
3.  <span data-ttu-id="ac248-110">Chiusura del client dopo il completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ac248-110">Closes the client once the operation call is completed.</span></span>  
  
### <a name="to-use-a-windows-communication-foundation-client"></a><span data-ttu-id="ac248-111">Per utilizzare un client di Windows Communication Foundation</span><span class="sxs-lookup"><span data-stu-id="ac248-111">To use a Windows Communication Foundation client</span></span>  
  
1.  <span data-ttu-id="ac248-112">Aprire il file Program.cs o Program.vb dal progetto GettingStartedClient e sostituire il codice esistente con quello seguente:</span><span class="sxs-lookup"><span data-stu-id="ac248-112">Open the Program.cs or Program.vb file from the GettingStartedClient project and replace the existing code with the following code:</span></span>  
  
    ```  
    using System;  
    using System.Collections.Generic;  
    using System.Linq;  
    using System.Text;  
    using GettingStartedClient.ServiceReference1;  
  
    namespace GettingStartedClient  
    {  
        class Program  
        {  
            static void Main(string[] args)  
            {  
                //Step 1: Create an instance of the WCF proxy.  
                CalculatorClient client = new CalculatorClient();  
  
                // Step 2: Call the service operations.  
                // Call the Add service operation.  
                double value1 = 100.00D;  
                double value2 = 15.99D;  
                double result = client.Add(value1, value2);  
                Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result);  
  
                // Call the Subtract service operation.  
                value1 = 145.00D;  
                value2 = 76.54D;  
                result = client.Subtract(value1, value2);  
                Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result);  
  
                // Call the Multiply service operation.  
                value1 = 9.00D;  
                value2 = 81.25D;  
                result = client.Multiply(value1, value2);  
                Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result);  
  
                // Call the Divide service operation.  
                value1 = 22.00D;  
                value2 = 7.00D;  
                result = client.Divide(value1, value2);  
                Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result);  
  
                //Step 3: Closing the client gracefully closes the connection and cleans up resources.  
                client.Close();  
            }  
        }  
    }  
    ```  
  
    ```  
    Imports System  
    Imports System.Collections.Generic  
    Imports System.Text  
    Imports System.ServiceModel  
    Imports GettingStartedClientVB2.ServiceReference1  
  
    Module Module1  
  
        Sub Main()  
            ' Step 1: Create an instance of the WCF proxy  
            Dim Client As New CalculatorClient()  
  
            'Step 2: Call the service operations.  
            'Call the Add service operation.  
            Dim value1 As Double = 100D  
            Dim value2 As Double = 15.99D  
            Dim result As Double = Client.Add(value1, value2)  
            Console.WriteLine("Add({0},{1}) = {2}", value1, value2, result)  
  
            'Call the Subtract service operation.  
            value1 = 145D  
            value2 = 76.54D  
            result = Client.Subtract(value1, value2)  
            Console.WriteLine("Subtract({0},{1}) = {2}", value1, value2, result)  
  
            'Call the Multiply service operation.  
            value1 = 9D  
            value2 = 81.25D  
            result = Client.Multiply(value1, value2)  
            Console.WriteLine("Multiply({0},{1}) = {2}", value1, value2, result)  
  
            'Call the Divide service operation.  
            value1 = 22D  
            value2 = 7D  
            result = Client.Divide(value1, value2)  
            Console.WriteLine("Divide({0},{1}) = {2}", value1, value2, result)  
  
            ' Step 3: Closing the client gracefully closes the connection and cleans up resources.  
            Client.Close()  
  
            Console.WriteLine()  
            Console.WriteLine("Press <ENTER> to terminate client.")  
            Console.ReadLine()  
  
        End Sub  
  
    End Module  
    ```  
  
     <span data-ttu-id="ac248-113">Si noti l'istruzione Using o Imports con cui viene importato l'oggetto GettingStartedClient.ServiceReference1.</span><span class="sxs-lookup"><span data-stu-id="ac248-113">Notice the using or imports statement that imports the GettingStartedClient.ServiceReference1.</span></span> <span data-ttu-id="ac248-114">In questo modo viene importato il codice generato da Aggiungi riferimento al servizio in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ac248-114">This imports the code generated by Add Service Reference in Visual Studio.</span></span> <span data-ttu-id="ac248-115">Il codice crea un'istanza del proxy WCF, chiama tutte le operazioni del servizio esposte dal servizio calcolatrice, chiude il proxy, quindi termina.</span><span class="sxs-lookup"><span data-stu-id="ac248-115">The code instantiates the WCF proxy and then calls each of the service operations exposed by the calculator service, closes the proxy and terminates.</span></span>  
  
 <span data-ttu-id="ac248-116">L'esercitazione è ora completata.</span><span class="sxs-lookup"><span data-stu-id="ac248-116">You have now completed the tutorial.</span></span> <span data-ttu-id="ac248-117">È stato definito e implementato un contratto di servizio, è stato generato un proxy WCF, è stata configurata un'applicazione client WCF, quindi è stato utilizzato il proxy per chiamare le operazioni del servizio.</span><span class="sxs-lookup"><span data-stu-id="ac248-117">You defined a service contract, implemented the service contract, generated a WCF proxy, configured a WCF client application, and then used the proxy to call service operations.</span></span> <span data-ttu-id="ac248-118">Per testare l'applicazione, eseguire innanzitutto GettingStartedHost per l'avvio del servizio, quindi eseguire GettingStartedClient.</span><span class="sxs-lookup"><span data-stu-id="ac248-118">To test out the application first run GettingStartedHost to start the service and then run GettingStartedClient.</span></span> <span data-ttu-id="ac248-119">L'aspetto dell'output da GettingStartedHost è simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="ac248-119">The output from GettingStartedHost should look like this:</span></span>  
  
```Output  
The service is ready.Press <ENTER> to terminate service.Received Add(100,15.99)Return: 115.99Received Subtract(145,76.54)Return: 68.46Received Multiply(9,81.25)Return: 731.25Received Divide(22,7)Return: 3.14285714285714  
```  
  
 <span data-ttu-id="ac248-120">L'aspetto dell'output da GettingStartedClient è simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="ac248-120">The output from GettingStartedClient should look like this:</span></span>  
  
```Output  
Add(100,15.99) = 115.99Subtract(145,76.54) = 68.46Multiply(9,81.25) = 731.25Divide(22,7) = 3.14285714285714Press <ENTER> to terminate client.  
```  
  
## <a name="see-also"></a><span data-ttu-id="ac248-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ac248-121">See Also</span></span>  
 [<span data-ttu-id="ac248-122">Creazione di client</span><span class="sxs-lookup"><span data-stu-id="ac248-122">Building Clients</span></span>](../../../docs/framework/wcf/building-clients.md)  
 [<span data-ttu-id="ac248-123">Procedura: Creare un client</span><span class="sxs-lookup"><span data-stu-id="ac248-123">How to: Create a Client</span></span>](../../../docs/framework/wcf/how-to-create-a-wcf-client.md)  
 [<span data-ttu-id="ac248-124">Esercitazione introduttiva</span><span class="sxs-lookup"><span data-stu-id="ac248-124">Getting Started Tutorial</span></span>](../../../docs/framework/wcf/getting-started-tutorial.md)  
 [<span data-ttu-id="ac248-125">Programmazione WCF di base</span><span class="sxs-lookup"><span data-stu-id="ac248-125">Basic WCF Programming</span></span>](../../../docs/framework/wcf/basic-wcf-programming.md)  
 [<span data-ttu-id="ac248-126">Procedura: Creare un contratto duplex</span><span class="sxs-lookup"><span data-stu-id="ac248-126">How to: Create a Duplex Contract</span></span>](../../../docs/framework/wcf/feature-details/how-to-create-a-duplex-contract.md)  
 [<span data-ttu-id="ac248-127">Procedura: Accedere ai servizi con un contratto duplex</span><span class="sxs-lookup"><span data-stu-id="ac248-127">How to: Access Services with a Duplex Contract</span></span>](../../../docs/framework/wcf/feature-details/how-to-access-services-with-a-duplex-contract.md)  
 [<span data-ttu-id="ac248-128">Introduzione</span><span class="sxs-lookup"><span data-stu-id="ac248-128">Getting Started</span></span>](../../../docs/framework/wcf/samples/getting-started-sample.md)  
 [<span data-ttu-id="ac248-129">Servizio indipendente</span><span class="sxs-lookup"><span data-stu-id="ac248-129">Self-Host</span></span>](../../../docs/framework/wcf/samples/self-host.md)
