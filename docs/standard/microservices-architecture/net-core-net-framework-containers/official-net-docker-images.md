---
title: Immagini Docker .NET ufficiale
description: Architettura di Microservizi .NET per le applicazioni nei contenitori .NET | Immagini Docker .NET ufficiale
keywords: Docker, microservizi, ASP.NET, contenitore
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 10/18/2017
ms.prod: .net-core
ms.technology: dotnet-docker
ms.topic: article
ms.openlocfilehash: 6f14bd0cf55a552f3881d755ebe7389f000975d8
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2017
---
# <a name="official-net-docker-images"></a><span data-ttu-id="7f487-104">Immagini Docker .NET ufficiale</span><span class="sxs-lookup"><span data-stu-id="7f487-104">Official .NET Docker images</span></span>

<span data-ttu-id="7f487-105">Le immagini Docker .NET ufficiale sono immagini Docker creati e ottimizzati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7f487-105">The Official .NET Docker images are Docker images created and optimized by Microsoft.</span></span> <span data-ttu-id="7f487-106">Sono disponibili pubblicamente in repository Microsoft su [Hub Docker](https://hub.docker.com/u/microsoft/).</span><span class="sxs-lookup"><span data-stu-id="7f487-106">They are publicly available in the Microsoft repositories on [Docker Hub](https://hub.docker.com/u/microsoft/).</span></span> <span data-ttu-id="7f487-107">Ogni archivio può contenere più immagini, a seconda delle versioni di .NET e il sistema operativo e le versioni (Linux Debian, Alpine Linux, Windows Nano Server, Windows Server Core e così via).</span><span class="sxs-lookup"><span data-stu-id="7f487-107">Each repository can contain multiple images, depending on .NET versions, and depending on the OS and versions (Linux Debian, Linux Alpine, Windows Nano Server, Windows Server Core, etc.).</span></span>

<span data-ttu-id="7f487-108">La visione Microsoft per i repository .NET è repository granulare e sono specifici, in un repository rappresenta uno scenario specifico o un carico di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7f487-108">Microsoft’s vision for .NET repositories is to have granular and focused repos, where a repo represents a specific scenario or workload.</span></span> <span data-ttu-id="7f487-109">Ad esempio, il [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) immagini devono essere utilizzate quando usando ASP.NET Core in Docker, poiché tali immagini ASP.NET Core offrono ulteriori ottimizzazioni contenitori in questo caso è possibile avviare più velocemente.</span><span class="sxs-lookup"><span data-stu-id="7f487-109">For instance, the [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) images should be used when using ASP.NET Core on Docker, because those ASP.NET Core images provide additional optimizations so containers can start faster.</span></span>

<span data-ttu-id="7f487-110">D'altra parte, le immagini di .NET Core (microsoft/dotnet) sono progettate per le applicazioni di console basate su .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f487-110">On the other hand, the .NET Core images (microsoft/dotnet) are intended for console apps based on .NET Core.</span></span> <span data-ttu-id="7f487-111">Ad esempio, i processi batch, i processi Web di Azure e altri scenari di console devono utilizzare .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f487-111">For example, batch processes, Azure WebJobs, and other console scenarios should use .NET Core.</span></span> <span data-ttu-id="7f487-112">Tali immagini non includono lo stack ASP.NET Core, risultante in un'immagine contenitore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="7f487-112">Those images do not include the ASP.NET Core stack, resulting in a smaller container image.</span></span>

<span data-ttu-id="7f487-113">La maggior parte dei repository di immagini forniscono tag completo che consentono di selezionare non solo una versione di framework specifico, ma anche per scegliere un sistema operativo (versione di Windows o Linux distro).</span><span class="sxs-lookup"><span data-stu-id="7f487-113">Most image repos provide extensive tagging to help you select not just a specific framework version, but also to choose an OS (Linux distro or Windows version).</span></span>

<span data-ttu-id="7f487-114">Per ulteriori informazioni sulle immagini Docker .NET ufficiale fornito da Microsoft, vedere il [riepilogo immagini Docker .NET](https://aka.ms/dotnetdockerimages).</span><span class="sxs-lookup"><span data-stu-id="7f487-114">For further information about the official .NET Docker images provided by Microsoft, see the [.NET Docker Images summary](https://aka.ms/dotnetdockerimages).</span></span>

## <a name="net-core-and-docker-image-optimizations-for-development-versus-production"></a><span data-ttu-id="7f487-115">Ottimizzazioni di immagine .NET core e Docker per lo sviluppo e produzione</span><span class="sxs-lookup"><span data-stu-id="7f487-115">.NET Core and Docker image optimizations for development versus production</span></span>

<span data-ttu-id="7f487-116">Quando si compila immagini Docker per gli sviluppatori, Microsoft è incentrata su scenari principali seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f487-116">When building Docker images for developers, Microsoft focused on the following main scenarios:</span></span>

-   <span data-ttu-id="7f487-117">Le immagini utilizzate per *sviluppare* e creazione di applicazioni .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f487-117">Images used to *develop* and build .NET Core apps.</span></span>

-   <span data-ttu-id="7f487-118">Le immagini utilizzate per *eseguire* app .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7f487-118">Images used to *run* .NET Core apps.</span></span>

<span data-ttu-id="7f487-119">Perché più immagini?</span><span class="sxs-lookup"><span data-stu-id="7f487-119">Why multiple images?</span></span> <span data-ttu-id="7f487-120">Durante lo sviluppo, compilazione e l'esecuzione di applicazioni nei contenitori, è in genere in base alla priorità.</span><span class="sxs-lookup"><span data-stu-id="7f487-120">When developing, building, and running containerized applications, you usually have different priorities.</span></span> <span data-ttu-id="7f487-121">Fornendo immagini differenti per queste attività distinte, Microsoft consente di ottimizzare i processi di sviluppo, compilazione e distribuzione di applicazioni separati.</span><span class="sxs-lookup"><span data-stu-id="7f487-121">By providing different images for these separate tasks, Microsoft helps optimize the separate processes of developing, building, and deploying apps.</span></span>

### <a name="during-development-and-build"></a><span data-ttu-id="7f487-122">Durante lo sviluppo e compilazione</span><span class="sxs-lookup"><span data-stu-id="7f487-122">During development and build</span></span>

<span data-ttu-id="7f487-123">Durante lo sviluppo, aspetto importante è la velocità con cui è possibile scorrere le modifiche e la possibilità di eseguire il debug delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="7f487-123">During development, what is important is how fast you can iterate changes, and the ability to debug the changes.</span></span> <span data-ttu-id="7f487-124">Le dimensioni dell'immagine non sono importante quanto la possibilità di apportare modifiche al codice e visualizzare rapidamente le modifiche.</span><span class="sxs-lookup"><span data-stu-id="7f487-124">The size of the image is not as important as the ability to make changes to your code and see the changes quickly.</span></span> <span data-ttu-id="7f487-125">Alcuni strumenti e i "contenitori agente di compilazione" Usa lo sviluppo immagine ASP.NET di base (microsoft/aspnetcore-compilazione) durante lo sviluppo e processo di compilazione.</span><span class="sxs-lookup"><span data-stu-id="7f487-125">Some tools and "build-agent containers", use the development ASP.NET Core image (microsoft/aspnetcore-build) during development and build proces.</span></span> <span data-ttu-id="7f487-126">Quando si compila in un contenitore Docker, gli aspetti importanti sono gli elementi necessari per compilare l'app.</span><span class="sxs-lookup"><span data-stu-id="7f487-126">When building inside a Docker container, the important aspects are the elements that are needed in order to compile your app.</span></span> <span data-ttu-id="7f487-127">Ciò include il compilatore e Gulp ed eventuali altre dipendenze di .NET, più dipendenze, lo sviluppo web quali npm, Bower.</span><span class="sxs-lookup"><span data-stu-id="7f487-127">This includes the compiler and any other .NET dependencies, plus web development dependencies like npm, Gulp, and Bower.</span></span>

<span data-ttu-id="7f487-128">Perché questo tipo di immagine di compilazione è importante?</span><span class="sxs-lookup"><span data-stu-id="7f487-128">Why is this type of build image important?</span></span> <span data-ttu-id="7f487-129">Non si distribuirla questa immagine nell'ambiente di produzione.</span><span class="sxs-lookup"><span data-stu-id="7f487-129">You do not deploy this image to production.</span></span> <span data-ttu-id="7f487-130">Si tratta invece di un'immagine da utilizzare per compilare il contenuto che si inserisce in un'immagine di produzione.</span><span class="sxs-lookup"><span data-stu-id="7f487-130">Instead, it is an image you use to build the content you place into a production image.</span></span> <span data-ttu-id="7f487-131">Questa immagine potrebbe essere utilizzata in un ambiente di integrazione continua (CI) o di un ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="7f487-131">This image would be used in your continuous integration (CI) environment or build environment.</span></span> <span data-ttu-id="7f487-132">Ad esempio, anziché l'installazione manuale di tutte le dipendenze dell'applicazione direttamente su un agente di compilazione host (ad esempio VM), l'agente di compilazione creerebbe un'istanza di un'immagine di compilazione .NET Core con tutte le dipendenze necessarie per compilare l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f487-132">For instance, rather than manually installing all your application dependencies directly on a build agent host (a VM, for example), the build agent would instantiate a .NET Core build image with all the dependencies required to build the application.</span></span> <span data-ttu-id="7f487-133">Per l'agente di compilazione è necessario soltanto sapere come eseguire questa immagine Docker.</span><span class="sxs-lookup"><span data-stu-id="7f487-133">Your build agent only needs to know how to run this Docker image.</span></span> <span data-ttu-id="7f487-134">Questo semplifica l'ambiente CI e rende molto più prevedibili.</span><span class="sxs-lookup"><span data-stu-id="7f487-134">This simplifies your CI environment and makes it much more predictable.</span></span>

### <a name="in-production"></a><span data-ttu-id="7f487-135">Nell'ambiente di produzione</span><span class="sxs-lookup"><span data-stu-id="7f487-135">In production</span></span>

<span data-ttu-id="7f487-136">È importante nell'ambiente di produzione è la velocità con cui è possibile distribuire e avviare i contenitori basati su un'immagine .NET Core di produzione.</span><span class="sxs-lookup"><span data-stu-id="7f487-136">What is important in production is how fast you can deploy and start your containers based on a production .NET Core image.</span></span> <span data-ttu-id="7f487-137">Pertanto, in base l'immagine solo runtime [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) è ridotto in modo che è possibile spostare rapidamente in rete dal Registro di sistema Docker per gli host Docker.</span><span class="sxs-lookup"><span data-stu-id="7f487-137">Therefore, the runtime-only image based on [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) is small so that it can travel quickly across the network from your Docker registry to your Docker hosts.</span></span> <span data-ttu-id="7f487-138">Il contenuto è pronto per l'esecuzione, consentendo l'ora più veloce dall'avvio del contenitore per l'elaborazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="7f487-138">The contents are ready to run, enabling the fastest time from starting the container to processing results.</span></span> <span data-ttu-id="7f487-139">Nel modello di Docker, non è necessario per la compilazione da C\# il codice, come quando si esegue la compilazione dotnet o dotnet pubblicare quando utilizza il contenitore della build.</span><span class="sxs-lookup"><span data-stu-id="7f487-139">In the Docker model, there is no need for compilation from C\# code, as there is when you run dotnet build or dotnet publish when using the build container.</span></span>

<span data-ttu-id="7f487-140">In questa immagine ottimizzata vengono inseriti solo i file binari e altri contenuti necessari per eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7f487-140">In this optimized image you put only the binaries and other content needed to run the application.</span></span> <span data-ttu-id="7f487-141">Ad esempio, di pubblicare il contenuto creato da dotnet contiene solo i file binari compilati .NET, immagini, js e file CSS.</span><span class="sxs-lookup"><span data-stu-id="7f487-141">For example, the content created by dotnet publish contains only the compiled .NET binaries, images, .js, and .css files.</span></span> <span data-ttu-id="7f487-142">Nel corso del tempo, si noterà immagini che contengono pacchetti preJit.</span><span class="sxs-lookup"><span data-stu-id="7f487-142">Over time, you will see images that contain pre-jitted packages.</span></span>

<span data-ttu-id="7f487-143">Anche se sono presenti più versioni di .NET Core e ASP.NET Core immagini, condividono uno o più livelli, tra cui il livello di base.</span><span class="sxs-lookup"><span data-stu-id="7f487-143">Although there are multiple versions of the .NET Core and ASP.NET Core images, they all share one or more layers, including the base layer.</span></span> <span data-ttu-id="7f487-144">Pertanto, la quantità di spazio su disco necessario per archiviare un'immagine è di piccole dimensioni è costituito solo il delta tra l'immagine personalizzata e l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="7f487-144">Therefore, the amount of disk space needed to store an image is small; it consists only of the delta between your custom image and its base image.</span></span> <span data-ttu-id="7f487-145">Il risultato è che è più veloce effettuare il pull dell'immagine dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7f487-145">The result is that it is quick to pull the image from your registry.</span></span>

<span data-ttu-id="7f487-146">Quando si Esplora il repository di immagini .NET hub Docker, sono disponibili più versioni di immagine classificati o contrassegnato con tag.</span><span class="sxs-lookup"><span data-stu-id="7f487-146">When you explore the .NET image repositories at Docker Hub, you will find multiple image versions classified or marked with tags.</span></span> <span data-ttu-id="7f487-147">Questi tag utili per decidere quale utilizzare, a seconda della versione che è necessario, ad esempio quelli riportati nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="7f487-147">These tags help to decide which one to use, depending on the version you need, like those in the following table:</span></span>

-   <span data-ttu-id="7f487-148">Microsoft /**aspnetcore:2.0**</span><span class="sxs-lookup"><span data-stu-id="7f487-148">microsoft/**aspnetcore:2.0**</span></span>

        ASP.NET Core, with runtime only and ASP.NET Core optimizations, on Linux and Windows (multi-arch)

-   <span data-ttu-id="7f487-149">Microsoft /**aspnetcore-compilazione: 2.0**</span><span class="sxs-lookup"><span data-stu-id="7f487-149">microsoft/**aspnetcore-build:2.0**</span></span>

        ASP.NET Core, with SDKs included, on Linux and Windows (multi-arch)


>[!div class="step-by-step"]
<span data-ttu-id="7f487-150">[Precedente] (net-contenitore-os-targets.md) [Avanti] (... /Architect-microservice-Container-Applications/index.MD)</span><span class="sxs-lookup"><span data-stu-id="7f487-150">[Previous] (net-container-os-targets.md) [Next] (../architect-microservice-container-applications/index.md)</span></span>