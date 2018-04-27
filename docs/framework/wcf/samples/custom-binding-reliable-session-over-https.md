---
title: Sessione affidabile di associazione personalizzata su HTTPS
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 16aaa80d-3ffe-47c4-8b16-ec65c4d25f8d
caps.latest.revision: 13
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 716970f87d52a7535b9d42abd333d22685fdafc4
ms.sourcegitcommit: 2042de78fcdceebb6b8ac4b7a292b93e8782cbf5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/27/2018
---
# <a name="custom-binding-reliable-session-over-https"></a><span data-ttu-id="0888d-102">Sessione affidabile di associazione personalizzata su HTTPS</span><span class="sxs-lookup"><span data-stu-id="0888d-102">Custom Binding Reliable Session over HTTPS</span></span>
<span data-ttu-id="0888d-103">In questo esempio viene illustrato l'utilizzo della sicurezza del trasporto SSL con le sessioni affidabili.</span><span class="sxs-lookup"><span data-stu-id="0888d-103">This sample demonstrates the use of SSL transport security with Reliable Sessions.</span></span> <span data-ttu-id="0888d-104">Le sessioni affidabili implementano il protocollo WS-RM (WS-Reliable Messaging).</span><span class="sxs-lookup"><span data-stu-id="0888d-104">Reliable Sessions implements the WS-Reliable Messaging protocol.</span></span> <span data-ttu-id="0888d-105">È possibile ottenere una sessione affidabile protetta componendo WS-Security su sessioni affidabili.</span><span class="sxs-lookup"><span data-stu-id="0888d-105">You can have a secure reliable session by composing WS-Security over Reliable Sessions.</span></span> <span data-ttu-id="0888d-106">Tuttavia, è anche possibile scegliere di utilizzare la sicurezza del trasporto HTTP con SSL.</span><span class="sxs-lookup"><span data-stu-id="0888d-106">But sometimes, you may choose to instead use HTTP transport security with SSL.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="0888d-107">È possibile che gli esempi siano già installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="0888d-107">The samples may already be installed on your machine.</span></span> <span data-ttu-id="0888d-108">Verificare la directory seguente (impostazione predefinita) prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="0888d-108">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="0888d-109">Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="0888d-109">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="0888d-110">Questo esempio si trova nella directory seguente.</span><span class="sxs-lookup"><span data-stu-id="0888d-110">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\Custom\ReliableSessionOverHttps`  
  
## <a name="sample-details"></a><span data-ttu-id="0888d-111">Dettagli dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0888d-111">Sample Details</span></span>  
 <span data-ttu-id="0888d-112">SSL assicura che i pacchetti stessi siano protetti.</span><span class="sxs-lookup"><span data-stu-id="0888d-112">SSL ensures that the packets themselves are secured.</span></span> <span data-ttu-id="0888d-113">È importante notare che questo meccanismo è diverso dalla protezione della sessione affidabile mediante WS-Secure Conversation.</span><span class="sxs-lookup"><span data-stu-id="0888d-113">It is important to note that this is different from securing the reliable session using WS-Secure Conversation.</span></span>  
  
 <span data-ttu-id="0888d-114">Per utilizzare sessioni affidabili su HTTPS, è necessario creare un'associazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0888d-114">To use reliable session over HTTPS, you must create a custom binding.</span></span> <span data-ttu-id="0888d-115">Questo esempio è basato sul [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md) che implementa un servizio di calcolatrice.</span><span class="sxs-lookup"><span data-stu-id="0888d-115">This sample is based on the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) that implements a calculator service.</span></span> <span data-ttu-id="0888d-116">Un'associazione personalizzata viene creata utilizzando l'elemento di associazione di sessione affidabile e [ \<httpsTransport >](../../../../docs/framework/configure-apps/file-schema/wcf/httpstransport.md).</span><span class="sxs-lookup"><span data-stu-id="0888d-116">A custom binding is created using the reliable session binding element and the [\<httpsTransport>](../../../../docs/framework/configure-apps/file-schema/wcf/httpstransport.md).</span></span> <span data-ttu-id="0888d-117">La configurazione seguente riguarda l'associazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="0888d-117">The following configuration is of the custom binding.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
  <system.serviceModel>  
    <services>  
      <service   
          name="Microsoft.ServiceModel.Samples.CalculatorService"  
          behaviorConfiguration="CalculatorServiceBehavior">  
        <!-- use base address provided by host -->  
        <endpoint address=""  
                  binding="customBinding"  
                  bindingConfiguration="reliableSessionOverHttps"   
                  contract="Microsoft.ServiceModel.Samples.ICalculator" />  
        <!-- the mex endpoint is exposed as http://localhost/servicemodelsamples/service.svc/mex-->  
        <endpoint address="mex"  
                  binding="mexHttpBinding"  
                  contract="IMetadataExchange"/>  
      </service>  
    </services>  
  
    <bindings>  
      <customBinding>  
        <binding name="reliableSessionOverHttps">  
          <reliableSession />  
          <httpsTransport />  
        </binding>  
      </customBinding>  
    </bindings>  
  
    <!--For debugging purposes set the includeExceptionDetailInFaults attribute to true-->  
    <behaviors>  
      <serviceBehaviors>  
        <behavior name="CalculatorServiceBehavior">  
          <serviceMetadata httpGetEnabled="true" />  
          <serviceDebug includeExceptionDetailInFaults="False" />  
        </behavior>  
      </serviceBehaviors>  
    </behaviors>  
  
  </system.serviceModel>  
  
</configuration>  
```  
  
 <span data-ttu-id="0888d-118">Nell'esempio di codice programma è identico a quello del [Introduzione](../../../../docs/framework/wcf/samples/getting-started-sample.md) servizio.</span><span class="sxs-lookup"><span data-stu-id="0888d-118">The program code in the sample is identical to that of the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) service.</span></span> <span data-ttu-id="0888d-119">È necessario creare un certificato e assegnarlo utilizzando la Gestione guidata certificati server Web prima di compilare ed eseguire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="0888d-119">You must create a certificate and assign it by using the Web Server Certificate Wizard before building and running the sample.</span></span> <span data-ttu-id="0888d-120">Le definizioni dell'endpoint e dell'associazione nelle impostazioni del file di configurazione abilitano l'uso dell'associazione personalizzata, come illustrato nella configurazione di esempio seguente per il client.</span><span class="sxs-lookup"><span data-stu-id="0888d-120">The endpoint definition and binding definition in the configuration file settings enable the use of custom binding as shown in the following sample configuration for the client.</span></span>  
  
```xml  
<?xml version="1.0" encoding="utf-8" ?>  
<configuration>  
  <system.serviceModel>  
  
    <client>  
      <!-- this endpoint has an https: address -->  
      <endpoint name=""  
                address="https://localhost/servicemodelsamples/service.svc"   
                binding="customBinding"   
                bindingConfiguration="reliableSessionOverHttps"   
                contract="Microsoft.ServiceModel.Samples.ICalculator" />  
    </client>  
  
      <bindings>  
        <customBinding>  
          <binding name="reliableSessionOverHttps">  
            <reliableSession />  
            <httpsTransport />  
          </binding>  
        </customBinding>        
    </bindings>  
  
  </system.serviceModel>  
  
</configuration>  
```  
  
 <span data-ttu-id="0888d-121">L'indirizzo specificato utilizza lo schema https://.</span><span class="sxs-lookup"><span data-stu-id="0888d-121">The address specified uses the https:// scheme.</span></span>  
  
 <span data-ttu-id="0888d-122">Poiché il certificato utilizzato in questo esempio è un certificato di prova creato con Makecert.exe, viene visualizzato un avviso di sicurezza quando si tenta di accedere a https: indirizzi, ad esempio https://localhost/servicemodelsamples/service.svc, dal browser.</span><span class="sxs-lookup"><span data-stu-id="0888d-122">Because the certificate used in this sample is a test certificate created with Makecert.exe, a security alert appears when you try to access an https: address, such as https://localhost/servicemodelsamples/service.svc, from your browser.</span></span> <span data-ttu-id="0888d-123">Per consentire al client [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] di lavorare con un certificato di prova, è stato aggiunto altro codice al client per sopprimere l'avviso di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="0888d-123">To allow the [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] client to work with a test certificate in place, some additional code has been added to the client to suppress the security alert.</span></span> <span data-ttu-id="0888d-124">Il codice e la classe associata non sono richiesti quando si utilizzano i certificati di produzione.</span><span class="sxs-lookup"><span data-stu-id="0888d-124">This code, and the accompanying class, is not required when using production certificates.</span></span>  

```csharp
// This code is required only for test certificates like those created by Makecert.exe.  
PermissiveCertificatePolicy.Enact("CN=ServiceModelSamples-HTTPS-Server");  
```

 <span data-ttu-id="0888d-125">Quando si esegue l'esempio, le richieste e le risposte dell'operazione vengono visualizzate nella finestra della console client.</span><span class="sxs-lookup"><span data-stu-id="0888d-125">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="0888d-126">Premere INVIO nella finestra del client per arrestare il client.</span><span class="sxs-lookup"><span data-stu-id="0888d-126">Press ENTER in the client window to shut down the client.</span></span>  
  
```  
Add(100,15.99) = 115.99  
Subtract(145,76.54) = 68.46  
Multiply(9,81.25) = 731.25  
Divide(22,7) = 3.14285714285714  
  
Press <ENTER> to terminate client.  
```  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="0888d-127">Per impostare, compilare ed eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="0888d-127">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="0888d-128">Installare [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 4.0 usando il comando seguente.</span><span class="sxs-lookup"><span data-stu-id="0888d-128">Install  [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 4.0 using the following command.</span></span>  
  
    ```  
    %windir%\Microsoft.NET\Framework\v4.0.XXXXX\aspnet_regiis.exe /i /enable  
    ```  
  
2.  <span data-ttu-id="0888d-129">Assicurarsi di avere eseguito la [procedura di installazione singola per gli esempi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0888d-129">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
3.  <span data-ttu-id="0888d-130">Assicurarsi di avere eseguito la [istruzioni di installazione certificato Server Internet Information Services (IIS)](../../../../docs/framework/wcf/samples/iis-server-certificate-installation-instructions.md).</span><span class="sxs-lookup"><span data-stu-id="0888d-130">Ensure that you have performed the [Internet Information Services (IIS) Server Certificate Installation Instructions](../../../../docs/framework/wcf/samples/iis-server-certificate-installation-instructions.md).</span></span>  
  
4.  <span data-ttu-id="0888d-131">Per compilare l'edizione in C# o Visual Basic .NET della soluzione, seguire le istruzioni in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0888d-131">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
5.  <span data-ttu-id="0888d-132">Per eseguire l'esempio in una configurazione singola o tra computer, seguire le istruzioni in [esegue gli esempi di Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0888d-132">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0888d-133">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="0888d-133">See Also</span></span>
