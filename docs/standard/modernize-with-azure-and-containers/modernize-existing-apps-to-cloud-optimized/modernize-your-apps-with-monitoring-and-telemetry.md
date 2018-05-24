---
title: Modernizzare le app con monitoraggio e telemetria
description: Modernizzare le applicazioni .NET esistenti con i contenitori di Windows e Cloud di Azure | Modernizzare le app con monitoraggio e telemetria
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/30/2018
ms.openlocfilehash: 8f5f9bfebf46db7b98bedc4b5b8204d23357c72e
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2018
---
# <a name="modernize-your-apps-with-monitoring-and-telemetry"></a><span data-ttu-id="7c5ed-103">Modernizzare le app con monitoraggio e telemetria</span><span class="sxs-lookup"><span data-stu-id="7c5ed-103">Modernize your apps with monitoring and telemetry</span></span>

<span data-ttu-id="7c5ed-104">Quando si esegue un'applicazione nell'ambiente di produzione, è fondamentale disporre di informazioni dettagliate delle prestazioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-104">When you run an application in production, it's critical that you have insights about how your application is performing.</span></span> <span data-ttu-id="7c5ed-105">Sta eseguendo un livello elevato?</span><span class="sxs-lookup"><span data-stu-id="7c5ed-105">Is it performing at a high level?</span></span> <span data-ttu-id="7c5ed-106">Gli utenti ricevono errori o l'applicazione stabile e affidabile?</span><span class="sxs-lookup"><span data-stu-id="7c5ed-106">Are users getting errors, or is the application stable and reliable?</span></span> <span data-ttu-id="7c5ed-107">È necessario il monitoraggio delle prestazioni avanzate, potente avvisi e i dashboard per garantire che l'applicazione sia disponibile e verrà eseguito come previsto.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-107">You need rich performance monitoring, powerful alerting, and dashboards to help ensure that your application is available and performing as expected.</span></span> <span data-ttu-id="7c5ed-108">È inoltre necessario essere in grado di verificare rapidamente se esiste un problema, determinare il numero di clienti interessato ed esegue un'analisi causa radice per individuare e correggere il problema.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-108">You also need to be able to see quickly if there's a problem, determine how many customers are affected, and perform a root-cause analysis to find and fix the issue.</span></span>

## <a name="monitor-your-application-with-application-insights"></a><span data-ttu-id="7c5ed-109">Monitorare l'applicazione con Application Insights</span><span class="sxs-lookup"><span data-stu-id="7c5ed-109">Monitor your application with Application Insights</span></span>

<span data-ttu-id="7c5ed-110">Application Insights è un servizio di gestione delle prestazioni dell'applicazione (APM) estendibile per gli sviluppatori web che lavorano su più piattaforme.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-110">Application Insights is an extensible Application Performance Management (APM) service for web developers who work on multiple platforms.</span></span> <span data-ttu-id="7c5ed-111">Utilizzarlo per monitorare l'applicazione web in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-111">Use it to monitor your live web application.</span></span> <span data-ttu-id="7c5ed-112">Application Insights rileva automaticamente le anomalie delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-112">Application Insights automatically detects performance anomalies.</span></span> <span data-ttu-id="7c5ed-113">Include inoltre strumenti potenti analitica per facilitare la diagnosi di problemi e per comprendere cosa gli utenti effettivamente eseguire con l'app.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-113">It includes powerful analytics tools to help you diagnose issues, and to help you understand what users actually do with your app.</span></span> <span data-ttu-id="7c5ed-114">Application Insights è progettato per migliorare continuamente le prestazioni e usabilità.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-114">Application Insights is designed to help you continuously improve performance and usability.</span></span> <span data-ttu-id="7c5ed-115">Funziona per le app su una vasta gamma di piattaforme, tra cui .NET, Node.js e J2EE, se ospitato in locale o nel cloud.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-115">It works for apps on a wide variety of platforms, including .NET, Node.js, and J2EE, whether hosted on-premises or in the cloud.</span></span> <span data-ttu-id="7c5ed-116">Application Insights si integra con i processi di DevOps e dispone di punti di connessione a un'ampia gamma di strumenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-116">Application Insights integrates with your DevOps processes, and has connection points to a variety of development tools.</span></span>

<span data-ttu-id="7c5ed-117">Figura 4-10 è illustrato un esempio di come Application Insights consente di monitorare l'applicazione e come espone tali informazioni a un dashboard.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-117">Figure 4-10 shows an example of how Application Insights monitors your application and how it surfaces those insights to a dashboard.</span></span>

![Dashboard di monitoraggio di Application Insights](./media/image10.png)

> <span data-ttu-id="7c5ed-119">**Figura 4-10.**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-119">**Figure 4-10.**</span></span> <span data-ttu-id="7c5ed-120">Dashboard di monitoraggio di Application Insights</span><span class="sxs-lookup"><span data-stu-id="7c5ed-120">Application Insights monitoring dashboard</span></span>

## <a name="monitor-your-docker-infrastructure-with-log-analytics-and-its-container-monitoring-solution"></a><span data-ttu-id="7c5ed-121">Monitorare l'infrastruttura di Docker con Log Analitica e la soluzione di monitoraggio contenitore</span><span class="sxs-lookup"><span data-stu-id="7c5ed-121">Monitor your Docker infrastructure with Log Analytics and its Container Monitoring solution</span></span>

<span data-ttu-id="7c5ed-122">[Azure Log Analitica](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview) fa parte di [complessive nella soluzione di monitoraggio di Microsoft Azure](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview).</span><span class="sxs-lookup"><span data-stu-id="7c5ed-122">[Azure Log Analytics](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview) is part of the [Microsoft Azure overall monitoring solution](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview).</span></span> <span data-ttu-id="7c5ed-123">È anche un servizio [Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview).</span><span class="sxs-lookup"><span data-stu-id="7c5ed-123">It's also a service in [Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview).</span></span> <span data-ttu-id="7c5ed-124">Log Analitica monitora cloud e in ambienti locali (OMS per on-premise) per preservare la disponibilità e prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-124">Log Analytics monitors cloud and on-premises environments (OMS for on-premises) to help maintain availability and performance.</span></span> <span data-ttu-id="7c5ed-125">Vengono raccolti i dati generati dalle risorse negli ambienti di cloud e locali e di altri strumenti di monitoraggio per fornire analisi in più origini.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-125">It collects data generated by resources in your cloud and on-premises environments and from other monitoring tools to provide analysis across multiple sources.</span></span>

<span data-ttu-id="7c5ed-126">In relazione i log dell'infrastruttura di Azure, Log Analitica, come un servizio di Azure, inserisce dati di metrica e di log da altri servizi di Azure (tramite [Monitor Azure](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)), macchine virtuali di Azure, contenitori di Docker e altre infrastrutture di cloud o locali.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-126">In relation to Azure infrastructure logs, Log Analytics, as an Azure service, ingests log and metric data from other Azure services (via [Azure Monitor](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)), Azure VMs, Docker containers, and on-premises or other cloud infrastructures.</span></span> <span data-ttu-id="7c5ed-127">Log Analitica offre ricerca nei log flessibile e analitica out-predefinito all'inizio di questo tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-127">Log Analytics offers flexible log search and out-of-the box analytics on top of this data.</span></span> <span data-ttu-id="7c5ed-128">Fornisce strumenti avanzati che è possibile utilizzare per analizzare i dati tra origini e consente query complesse in tutti i log, mentre è possibile verificare in modo proattivo in base alle condizioni specificate.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-128">It provides rich tools that you can use to analyze data across sources, it allows complex queries across all logs, and it can proactively alert based on specified conditions.</span></span> <span data-ttu-id="7c5ed-129">È anche possibile raccogliere dati personalizzati nel repository Log Analitica centrale, in cui è possibile eseguire una query e visualizzarla.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-129">You can even collect custom data in the central Log Analytics repository, where you can query and visualize it.</span></span> <span data-ttu-id="7c5ed-130">È anche possibile sfruttare le soluzioni predefinite Analitica di Log per ottenere immediatamente informazioni dettagliate della sicurezza in e le funzionalità dell'infrastruttura.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-130">You also can take advantage of the Log Analytics built-in solutions to immediately gain insights into the security and functionality of your infrastructure.</span></span>

<span data-ttu-id="7c5ed-131">È possibile accedere a Analitica Log tramite il portale di OMS o il portale di Azure, che vengono eseguite in qualsiasi browser, e fornire all'utente l'accesso alle impostazioni di configurazione e con più strumenti per analizzare e agire sui dati raccolti.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-131">You can access Log Analytics through the OMS portal or the Azure portal, which run in any browser, and provide you with access to configuration settings and multiple tools to analyze and act on collected data.</span></span>

<span data-ttu-id="7c5ed-132">Il [soluzione di monitoraggio contenitore](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers) in Analitica Log consente visualizzare e gestire gli host Docker e contenitore di Windows in un'unica posizione.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-132">The [Container Monitoring solution](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers) in Log Analytics helps you view and manage your Docker and Windows Container hosts in a single location.</span></span> <span data-ttu-id="7c5ed-133">La soluzione Mostra i contenitori sono in esecuzione, quali immagini contenitore vengono eseguiti e in cui vengono eseguiti i contenitori.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-133">The solution shows which containers are running, what container image they're running, and where containers are running.</span></span> <span data-ttu-id="7c5ed-134">È possibile visualizzare informazioni dettagliate di controllo, inclusi i comandi che vengono utilizzati con i contenitori.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-134">You can view detailed audit information, including commands that are being used with containers.</span></span> <span data-ttu-id="7c5ed-135">È anche possibile risolvere contenitori mediante la visualizzazione e la ricerca di log centralizzato, senza la necessità di visualizzare in remoto host Docker o di Windows.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-135">You also can troubleshoot containers by viewing and searching centralized logs, without needing to remotely view Docker or Windows hosts.</span></span> <span data-ttu-id="7c5ed-136">È possibile trovare i contenitori che potrebbero essere rumore e dispendiosa in termini di quantità eccessiva di risorse in un host.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-136">You can find containers that might be noisy and consuming excess resources on a host.</span></span> <span data-ttu-id="7c5ed-137">Inoltre, è possibile visualizzare centralizzata della CPU, memoria, archiviazione e utilizzo della rete e informazioni sulle prestazioni, per i contenitori.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-137">Additionally, you can view centralized CPU, memory, storage, and network usage, and performance information, for containers.</span></span> <span data-ttu-id="7c5ed-138">Nei computer che eseguono Windows, è possibile centralizzare e confrontare i registri di Windows Server, Hyper-V e i contenitori di Docker.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-138">On computers running Windows, you can centralize and compare logs from Windows Server, Hyper-V, and Docker containers.</span></span> <span data-ttu-id="7c5ed-139">La soluzione supporta orchestrators il contenitore seguente:</span><span class="sxs-lookup"><span data-stu-id="7c5ed-139">The solution supports the following container orchestrators:</span></span>

-   <span data-ttu-id="7c5ed-140">Docker Swarm</span><span class="sxs-lookup"><span data-stu-id="7c5ed-140">Docker Swarm</span></span>

-   <span data-ttu-id="7c5ed-141">DC/OS</span><span class="sxs-lookup"><span data-stu-id="7c5ed-141">DC/OS</span></span>

-   <span data-ttu-id="7c5ed-142">Kubernetes</span><span class="sxs-lookup"><span data-stu-id="7c5ed-142">Kubernetes</span></span>

-   <span data-ttu-id="7c5ed-143">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="7c5ed-143">Service Fabric</span></span>

-   <span data-ttu-id="7c5ed-144">Red Hat OpenShift</span><span class="sxs-lookup"><span data-stu-id="7c5ed-144">Red Hat OpenShift</span></span>

<span data-ttu-id="7c5ed-145">Figura 4-11 Mostra le relazioni tra vari host contenitore e gli agenti e OMS.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-145">Figure 4-11 shows the relationships between various container hosts and agents and OMS.</span></span>

![Soluzione di monitoraggio di contenitore Analitica di log](./media/image11.png)

> <span data-ttu-id="7c5ed-147">**Figura 4-11.**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-147">**Figure 4-11.**</span></span> <span data-ttu-id="7c5ed-148">Soluzione di monitoraggio di contenitore Analitica di log</span><span class="sxs-lookup"><span data-stu-id="7c5ed-148">Log Analytics Container Monitoring solution</span></span>

<span data-ttu-id="7c5ed-149">È possibile utilizzare la soluzione di monitoraggio del Log Analitica contenitore per:</span><span class="sxs-lookup"><span data-stu-id="7c5ed-149">You can use the Log Analytics Container Monitoring solution to:</span></span>

-   <span data-ttu-id="7c5ed-150">Visualizzare informazioni su tutti gli host contenitore in un'unica posizione.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-150">See information about all container hosts in a single location.</span></span>

-   <span data-ttu-id="7c5ed-151">I contenitori sono in esecuzione, quali immagini che siano in esecuzione e in cui vengono eseguiti.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-151">Know which containers are running, what image they're running, and where they're running.</span></span>

-   <span data-ttu-id="7c5ed-152">Vedere un audit trail per le azioni sui contenitori.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-152">See an audit trail for actions on containers.</span></span>

-   <span data-ttu-id="7c5ed-153">Risoluzione dei problemi con la visualizzazione e la ricerca di log centralizzato senza account di accesso remoto agli host Docker.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-153">Troubleshoot by viewing and searching centralized logs without remote login to the Docker hosts.</span></span>

-   <span data-ttu-id="7c5ed-154">Trovare i contenitori che potrebbero essere "rumore router adiacenti" e stia utilizzando una quantità eccessiva di risorse in un host.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-154">Find containers that might be "noisy neighbors," and be consuming excess resources on a host.</span></span>

-   <span data-ttu-id="7c5ed-155">Consente di visualizzare centralizzata della CPU, memoria, archiviazione e utilizzo della rete e informazioni sulle prestazioni, per i contenitori.</span><span class="sxs-lookup"><span data-stu-id="7c5ed-155">View centralized CPU, memory, storage, and network usage, and performance information, for containers.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="7c5ed-156">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="7c5ed-156">Additional resources</span></span>

-   <span data-ttu-id="7c5ed-157">**Panoramica di monitoraggio in Microsoft Azure**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-157">**Overview of monitoring in Microsoft Azure**</span></span>

[https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview)

-   <span data-ttu-id="7c5ed-158">**Che cos'è Application Insights?**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-158">**What is Application Insights?**</span></span>

[https://docs.microsoft.com/azure/application-insights/app-insights-overview](https://docs.microsoft.com/azure/application-insights/app-insights-overview)

-   <span data-ttu-id="7c5ed-159">**Che cos'è Analitica Log?**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-159">**What is Log Analytics?**</span></span>

[https://docs.microsoft.com/azure/log-analytics/log-analytics-overview](https://docs.microsoft.com/azure/log-analytics/log-analytics-overview)

-   <span data-ttu-id="7c5ed-160">**Soluzione di monitoraggio di contenitore in Log Analitica**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-160">**Container Monitoring solution in Log Analytics**</span></span>

[https://docs.microsoft.com/azure/log-analytics/log-analytics-containers](https://docs.microsoft.com/azure/log-analytics/log-analytics-containers)

-   <span data-ttu-id="7c5ed-161">**Panoramica di monitoraggio di Azure**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-161">**Overview of Azure Monitor**</span></span>

[https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitoring-overview-azure-monitor)

-   <span data-ttu-id="7c5ed-162">**Che cos'è Operations Management Suite (OMS)?**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-162">**What is Operations Management Suite (OMS)?**</span></span>

[https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview](https://docs.microsoft.com/azure/operations-management-suite/operations-management-suite-overview)

-   <span data-ttu-id="7c5ed-163">**Monitoraggio di contenitori di Windows Server nell'infrastruttura di servizio con OMS**</span><span class="sxs-lookup"><span data-stu-id="7c5ed-163">**Monitoring Windows Server containers in Service Fabric with OMS**</span></span>

[https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-containers-windowsserver](https://docs.microsoft.com/azure/service-fabric/service-fabric-diagnostics-containers-windowsserver)

>[!div class="step-by-step"]
<span data-ttu-id="7c5ed-164">[Precedente](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
[Successivo](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)</span><span class="sxs-lookup"><span data-stu-id="7c5ed-164">[Previous](build-resilient-services-ready-for-the-cloud-embrace-transient-failures-in-the-cloud.md)
[Next](modernize-your-apps-lifecycle-with-ci-cd-pipelines-and-devops-tools-in-the-cloud.md)</span></span>