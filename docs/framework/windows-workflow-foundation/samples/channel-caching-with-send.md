---
title: "Memorizzazione nella cache dei canali con l'attività Send"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e69a2502-25cb-43bf-b8d2-95fbdecb41cb
caps.latest.revision: "5"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: 3f78b22d1481e260535e4aeb9764d8ee349a7a2c
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="channel-caching-with-send"></a><span data-ttu-id="9cfee-102">Memorizzazione nella cache dei canali con l'attività Send</span><span class="sxs-lookup"><span data-stu-id="9cfee-102">Channel Caching with Send</span></span>
<span data-ttu-id="9cfee-103">L'oggetto <xref:System.ServiceModel.Activities.SendMessageChannelCache> consente agli utenti di disporre di livelli diversi di memorizzazione nella cache di canali con le attività <xref:System.ServiceModel.Activities.Send> e <xref:System.ServiceModel.Activities.SendParametersContent>.</span><span class="sxs-lookup"><span data-stu-id="9cfee-103">The <xref:System.ServiceModel.Activities.SendMessageChannelCache> enables users to have different levels of channel caching with <xref:System.ServiceModel.Activities.Send> and <xref:System.ServiceModel.Activities.SendParametersContent> activities.</span></span> <span data-ttu-id="9cfee-104">La memorizzazione nella cache a livello di istanza è abilitata per impostazione predefinita e in questo esempio vengono illustrate le seguenti funzionalità:</span><span class="sxs-lookup"><span data-stu-id="9cfee-104">Instance-level caching is enabled by default and this sample demonstrates the following features:</span></span>  
  
1.  <span data-ttu-id="9cfee-105">Condividere un oggetto <xref:System.ServiceModel.Activities.SendMessageChannelCache> in un dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cfee-105">Share a <xref:System.ServiceModel.Activities.SendMessageChannelCache> across an application domain.</span></span>  
  
2.  <span data-ttu-id="9cfee-106">Disabilitare la memorizzazione nella cache di canali.</span><span class="sxs-lookup"><span data-stu-id="9cfee-106">Disable channel caching.</span></span>  
  
3.  <span data-ttu-id="9cfee-107">Condividere un oggetto <xref:System.ServiceModel.Activities.SendMessageChannelCache> tra istanze del flusso di lavoro in un oggetto <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span><span class="sxs-lookup"><span data-stu-id="9cfee-107">Share a <xref:System.ServiceModel.Activities.SendMessageChannelCache> among workflow instances in a <xref:System.ServiceModel.Activities.WorkflowServiceHost>.</span></span>  
  
## <a name="demonstrates"></a><span data-ttu-id="9cfee-108">Dimostrazione</span><span class="sxs-lookup"><span data-stu-id="9cfee-108">Demonstrates</span></span>  
 <span data-ttu-id="9cfee-109">Estensione <xref:System.ServiceModel.Activities.SendMessageChannelCache>, attività <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.ReceiveContent> e <xref:System.ServiceModel.Activities.SendReply>.</span><span class="sxs-lookup"><span data-stu-id="9cfee-109"><xref:System.ServiceModel.Activities.SendMessageChannelCache> extension, <xref:System.ServiceModel.Activities.Send>, <xref:System.ServiceModel.Activities.Receive>, <xref:System.ServiceModel.Activities.ReceiveContent> and <xref:System.ServiceModel.Activities.SendReply> activities.</span></span>  
  
#### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="9cfee-110">Per impostare, compilare ed eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="9cfee-110">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="9cfee-111">Caricare la soluzione del progetto in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] e compilare il progetto.</span><span class="sxs-lookup"><span data-stu-id="9cfee-111">Load the project solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)] and build the project.</span></span>  
  
2.  <span data-ttu-id="9cfee-112">Eseguire l'applicazione EchoWorkflowService generata in \EchoWorkflowService\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="9cfee-112">Run the EchoWorkflowService application generated in \EchoWorkflowService\bin\debug.</span></span>  
  
3.  <span data-ttu-id="9cfee-113">Eseguire l'applicazione EchoWorkflowClient generata in .\EchoWorkflowClient\bin\debug.</span><span class="sxs-lookup"><span data-stu-id="9cfee-113">Run the EchoWorkflowClient application generated in .\EchoWorkflowClient\bin\debug.</span></span>  
  
4.  <span data-ttu-id="9cfee-114">Il client chiama l'operazione Echo nel servizio e stampa i risultati.</span><span class="sxs-lookup"><span data-stu-id="9cfee-114">The client calls the Echo operation on the service and prints the results.</span></span> <span data-ttu-id="9cfee-115">Una volta stampati i risultati, premere INVIO per uscire dal client e dal servizio.</span><span class="sxs-lookup"><span data-stu-id="9cfee-115">When the results have been printed, press ENTER to exit the client and the service.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="9cfee-116">È possibile che gli esempi siano già installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="9cfee-116">The samples may already be installed on your machine.</span></span> <span data-ttu-id="9cfee-117">Verificare la directory seguente (impostazione predefinita) prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="9cfee-117">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="9cfee-118">Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="9cfee-118">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="9cfee-119">Questo esempio si trova nella directory seguente.</span><span class="sxs-lookup"><span data-stu-id="9cfee-119">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Services\ChannelCache`
