---
title: Visual Studio Tools per Docker
description: Uso di Visual Studio Tools per Docker
keywords: .NET, .NET Core, Docker, ASP.NET Core, Visual Studio
author: spboyer
ms.author: shboyer
ms.date: 04/27/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-docker
ms.devlang: dotnet
ms.assetid: 1f3b9a68-4dea-4b60-8cb3-f46164eedbbf
ms.translationtype: HT
ms.sourcegitcommit: 9bb17207ba72bb22f5d6db55e9d1bd77e3013445
ms.openlocfilehash: 113d470a55fd92704de0e6def392a6e0a1a3a118
ms.contentlocale: it-it
ms.lasthandoff: 08/25/2017

---

# <a name="visual-studio-tools-for-docker"></a><span data-ttu-id="bd0af-104">Visual Studio Tools per Docker</span><span class="sxs-lookup"><span data-stu-id="bd0af-104">Visual Studio Tools for Docker</span></span>

<span data-ttu-id="bd0af-105">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) con [Docker per Windows](https://docs.docker.com/docker-for-windows/install/) supporta la compilazione, il debug e l'esecuzione delle applicazioni web e console .NET Framework e .NET Core tramite i contenitori Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="bd0af-105">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) with [Docker for Windows](https://docs.docker.com/docker-for-windows/install/) supports building, debugging, and running .NET Framework and .NET Core web and console applications using Windows and Linux containers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bd0af-106">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="bd0af-106">Prerequisites</span></span>

- <span data-ttu-id="bd0af-107">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) con carico di lavoro .NET Core</span><span class="sxs-lookup"><span data-stu-id="bd0af-107">[Microsoft Visual Studio 2017](https://www.visualstudio.com/) with .NET Core workload</span></span>
- [<span data-ttu-id="bd0af-108">Docker per Windows</span><span class="sxs-lookup"><span data-stu-id="bd0af-108">Docker for Windows</span></span>](https://docs.docker.com/docker-for-windows/install/)

## <a name="installation-and-setup"></a><span data-ttu-id="bd0af-109">Installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="bd0af-109">Installation and setup</span></span>

<span data-ttu-id="bd0af-110">Installare [Microsoft Visual Studio 2017](https://docs.microsoft.com/en-us/visualstudio/install/install-visual-studio) con il carico di lavoro di .NET Core.</span><span class="sxs-lookup"><span data-stu-id="bd0af-110">Install [Microsoft Visual Studio 2017](https://docs.microsoft.com/en-us/visualstudio/install/install-visual-studio) with the .NET Core workload.</span></span>

<span data-ttu-id="bd0af-111">Per l'installazione Docker, vedere le informazioni riportate in [Docker for Windows: What to know before you install](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install) (Docker per Windows: informazioni da conoscere prima dell'installazione) e installare [Docker per Windows](https://docs.docker.com/docker-for-windows/install/).</span><span class="sxs-lookup"><span data-stu-id="bd0af-111">For Docker installation, review the information at [Docker for Windows: What to know before you install](https://docs.docker.com/docker-for-windows/install/#what-to-know-before-you-install) and install [Docker For Windows](https://docs.docker.com/docker-for-windows/install/).</span></span>

<span data-ttu-id="bd0af-112">Un'attività di configurazione necessaria è l'impostazione di **[Shared Drives](https://docs.docker.com/docker-for-windows/#shared-drives)** (Unità condivise) in Docker for Windows.</span><span class="sxs-lookup"><span data-stu-id="bd0af-112">A required configuration is to setup **[Shared Drives](https://docs.docker.com/docker-for-windows/#shared-drives)** in Docker for Windows.</span></span> <span data-ttu-id="bd0af-113">Questa impostazione è necessaria per il mapping dei volumi e il supporto del debug.</span><span class="sxs-lookup"><span data-stu-id="bd0af-113">The setting is required for the volume mapping and debugging support.</span></span>

<span data-ttu-id="bd0af-114">Fare clic con il pulsante destro del mouse sull'icona di Docker sulla barra delle applicazioni, scegliere **Settings** (Impostazioni) e quindi selezionare **Shared Drives** (Unità condivise).</span><span class="sxs-lookup"><span data-stu-id="bd0af-114">Right click the Docker icon in the System Tray, click **Settings** and select **Shared Drives**.</span></span> <span data-ttu-id="bd0af-115">Selezionare l'unità in cui Docker archivierà i file e applicherà le modifiche.</span><span class="sxs-lookup"><span data-stu-id="bd0af-115">Select the drive where Docker will store your files and apply changes.</span></span>

![Shared Drives (Unità condivise)](./media/visual-studio-tools-for-docker/settings-shared-drives-win.png)

## <a name="create-an-aspnet-web-application-and-add-docker-support"></a><span data-ttu-id="bd0af-117">Creare un'applicazione Web ASP.NET e aggiungere il supporto per Docker</span><span class="sxs-lookup"><span data-stu-id="bd0af-117">Create an ASP.NET Web Application and add Docker Support</span></span>

<span data-ttu-id="bd0af-118">Creare una nuova applicazione Web ASP.NET Core usando Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bd0af-118">Using Visual Studio, create a new ASP.NET Core Web Application.</span></span> <span data-ttu-id="bd0af-119">Quando l'applicazione è caricata, selezionare **Add Docker Support** (Aggiungi supporto Docker) dal menu **Progetto** oppure fare clic con il pulsante destro del mouse in Esplora soluzioni e scegliere **Aggiungi** > **Docker Support** (Supporto Docker).</span><span class="sxs-lookup"><span data-stu-id="bd0af-119">When the application is loaded, either select **Add Docker Support** from the **Project Menu** or right click the project from the Solution Explorer and select **Add** > **Docker Support**.</span></span>

<span data-ttu-id="bd0af-120">Menu Progetto</span><span class="sxs-lookup"><span data-stu-id="bd0af-120">Project Menu</span></span>

![Progetto, Add Docker Support (Aggiungi supporto Docker)](./media/visual-studio-tools-for-docker/project-add-docker-support.png)

<span data-ttu-id="bd0af-122">Menu di scelta rapida Progetto</span><span class="sxs-lookup"><span data-stu-id="bd0af-122">Project Context Menu</span></span>

![Fare clic con il pulsante destro del mouse su Add Docker Support (Aggiungi supporto Docker)](./media/visual-studio-tools-for-docker/right-click-add-docker-support.png)

<span data-ttu-id="bd0af-124">Quando si aggiunge il supporto di Docker al progetto, è possibile scegliere i contenitori Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="bd0af-124">When you add Docker support to your project, you can choose either Windows or Linux containers.</span></span> <span data-ttu-id="bd0af-125">L'host Docker deve eseguire lo stesso tipo di contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-125">(The Docker host must be running the same container type.</span></span> <span data-ttu-id="bd0af-126">Se è necessario modificare il tipo di contenitore nell'istanza di Docker in esecuzione, fare clic con il pulsante destro del mouse sull'icona di **Docker** sulla barra delle applicazioni e scegliere **Switch to Windows containers** (Passa ai contenitori Windows) o **Switch to Linux containers** (Passa ai contenitori Linux).</span><span class="sxs-lookup"><span data-stu-id="bd0af-126">If you need change the container type in the running Docker instance, right click the **Docker** icon in the System Tray, and choose **Switch to Windows containers** or **Switch to Linux containers**.)</span></span> 

<span data-ttu-id="bd0af-127">Al progetto verranno aggiunti i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="bd0af-127">The following files are added to the project.</span></span>

- <span data-ttu-id="bd0af-128">**Dockerfile**: il file Docker per applicazioni ASP.NET Core è basato sull'immagine [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore).</span><span class="sxs-lookup"><span data-stu-id="bd0af-128">**Dockerfile**: the Docker file for ASP.NET Core applications is based on the [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore) image.</span></span> <span data-ttu-id="bd0af-129">Questa immagine include i pacchetti NuGet ASP.NET Core che sono stati compilati PreJit migliorando le prestazioni di avvio.</span><span class="sxs-lookup"><span data-stu-id="bd0af-129">This image includes the ASP.NET Core NuGet packages, which have been pre-jitted improving startup performance.</span></span> <span data-ttu-id="bd0af-130">Quando si compilano applicazioni .NET Core Console, il file Dockerfile FROM farà riferimento all'immagine [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet) più recente.</span><span class="sxs-lookup"><span data-stu-id="bd0af-130">When building .NET Core Console Applications, the Dockerfile FROM will reference the most recent [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet) image.</span></span>   
- <span data-ttu-id="bd0af-131">**docker-compose.yml**: file Compose Docker di base usato per definire la raccolta di immagini da compilare ed eseguire con docker-compose build/run.</span><span class="sxs-lookup"><span data-stu-id="bd0af-131">**docker-compose.yml**: base Docker Compose file used to define the collection of images to be built and run with docker-compose build/run.</span></span>   
- <span data-ttu-id="bd0af-132">**docker-compose.dev.debug.yml**: file Compose Docker aggiuntivo da usare per modifiche iterative quando la configurazione viene impostata per il debug.</span><span class="sxs-lookup"><span data-stu-id="bd0af-132">**docker-compose.dev.debug.yml**: additional docker-compose file with for iterative changes when your configuration is set to debug.</span></span> <span data-ttu-id="bd0af-133">Visual Studio chiamerà -f docker-compose.yml -f docker-compose.dev.debug.yml per unire questi elementi.</span><span class="sxs-lookup"><span data-stu-id="bd0af-133">Visual Studio will call -f docker-compose.yml -f docker-compose.dev.debug.yml to merge these together.</span></span> <span data-ttu-id="bd0af-134">Questo file Compose viene usato dagli strumenti di sviluppo di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bd0af-134">This compose file is used by Visual Studio development tools.</span></span>   
- <span data-ttu-id="bd0af-135">**docker-compose.dev.release.yml**: file Compose Docker aggiuntivo usato per il debug della definizione della versione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-135">**docker-compose.dev.release.yml**: additional Docker Compose file to debug your release definition.</span></span> <span data-ttu-id="bd0af-136">Monterà il debugger su un volume in modo che il contenuto dell'immagine di produzione non venga modificato.</span><span class="sxs-lookup"><span data-stu-id="bd0af-136">It will volume mount the debugger so it doesn't change the contents of the production image.</span></span>  

<span data-ttu-id="bd0af-137">Il file docker-compose.yml contiene il nome dell'immagine creata quando si esegue il progetto.</span><span class="sxs-lookup"><span data-stu-id="bd0af-137">The docker-compose.yml file contains the name of the image that is created when project is run.</span></span> 

```
version '2'

services:
  hellodockertools:
    image:  user/hellodockertools${TAG}
    build:
      context: .
      dockerfile: Dockerfile
    ports:
      - "80"
``` 

<span data-ttu-id="bd0af-138">In questo esempio `image: user/hellodockertools${TAG}` genera l'immagine `user/hellodockertools:dev` quando l'applicazione viene eseguita in modalità **Debug** e `user/hellodockertools:latest` viene eseguito in modalità **Versione**.</span><span class="sxs-lookup"><span data-stu-id="bd0af-138">In this example, `image: user/hellodockertools${TAG}` generates the image `user/hellodockertools:dev` when the application is run in **Debug** mode and `user/hellodockertools:latest` in **Release** mode respectively.</span></span> 

<span data-ttu-id="bd0af-139">Se si prevede di effettuare il push dell'immagine nel Registro di sistema, sarà necessario modificare `user` specificando il proprio nome utente Docker Hub,</span><span class="sxs-lookup"><span data-stu-id="bd0af-139">You will want to change the `user` to your Docker Hub username if you plan to push the image to the registry.</span></span> <span data-ttu-id="bd0af-140">ad esempio `spboyer/hellodockertools`. In alternativa, modificare l'URL del Registro di sistema privato `privateregistry.domain.com/` in base alla configurazione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-140">For example, `spboyer/hellodockertools`, or change to your private registry url `privateregistry.domain.com/` depending on your configuration.</span></span>

### <a name="debugging"></a><span data-ttu-id="bd0af-141">Debug</span><span class="sxs-lookup"><span data-stu-id="bd0af-141">Debugging</span></span>

<span data-ttu-id="bd0af-142">Selezionare **Docker** dall'elenco a discesa Debug nella barra degli strumenti e usare F5 per avviare il debug dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-142">Select **Docker** from the debug dropdown in the toolbar and use F5 to start debugging the application.</span></span> 

- <span data-ttu-id="bd0af-143">Se non è già presente nella cache, viene acquisita l'immagine microsoft/aspnetcore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-143">The microsoft/aspnetcore image is acquired (if not already in your cache)</span></span>
- <span data-ttu-id="bd0af-144">ASPNETCORE_ENVIRONMENT viene impostato su Sviluppo all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-144">ASPNETCORE_ENVIRONMENT is set to Development within the container</span></span>
- <span data-ttu-id="bd0af-145">La porta 80 viene impostata come EXPOSED e mappata a una porta assegnata in modo dinamico per localhost.</span><span class="sxs-lookup"><span data-stu-id="bd0af-145">PORT 80 is EXPOSED and mapped to a dynamically assigned port for localhost.</span></span> <span data-ttu-id="bd0af-146">La porta è determinata dall'host Docker ed è possibile eseguirvi query con docker ps.</span><span class="sxs-lookup"><span data-stu-id="bd0af-146">The port is determined by the docker host and can be queried with docker ps.</span></span> 
- <span data-ttu-id="bd0af-147">L'applicazione viene copiata nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-147">Your application is copied to the container</span></span>
- <span data-ttu-id="bd0af-148">Usando la porta assegnata in modo dinamico, viene avviato il browser predefinito con il debugger collegato al contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-148">Default browser is launched with the debugger attached to the container, using the dynamically assigned port.</span></span> 

<span data-ttu-id="bd0af-149">La risultante immagine Docker compilata è l'immagine `dev` dell'applicazione con le immagini `microsoft/aspnetcore` come immagine di base.</span><span class="sxs-lookup"><span data-stu-id="bd0af-149">The resulting Docker image built is the `dev` image of your application with the `microsoft/aspnetcore` images as the base image.</span></span>
<span data-ttu-id="bd0af-150">Nota: nell'immagine dev non è presente il contenuto dell'applicazione poiché le configurazioni Debug usano il montaggio su volume per garantire un'esperienza iterativa.</span><span class="sxs-lookup"><span data-stu-id="bd0af-150">Note: the dev image is empty of your app contents as Debug confgurations use volume mounting to provide the iterative experience.</span></span> <span data-ttu-id="bd0af-151">Per effettuare il push di un'immagine, usare la configurazione Versione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-151">To push an image, use the Release configuration.</span></span>

```console
REPOSITORY                  TAG         IMAGE ID            CREATED         SIZE
spboyer/hellodockertools    dev         0b6e2e44b3df        4 minutes ago   268.9 MB
microsoft/aspnetcore        1.0.1       189ad4312ce7        5 days ago      268.9 MB
```

<span data-ttu-id="bd0af-152">L'applicazione viene eseguita usando il contenitore che è possibile visualizzare eseguendo il comando `docker ps`.</span><span class="sxs-lookup"><span data-stu-id="bd0af-152">The application is running using the container which you can see by running the `docker ps` command.</span></span>

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   4 minutes ago       Up 4 minutes        0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="edit-and-continue"></a><span data-ttu-id="bd0af-153">Modifica e continuazione</span><span class="sxs-lookup"><span data-stu-id="bd0af-153">Edit and Continue</span></span>

<span data-ttu-id="bd0af-154">Le modifiche apportate ai file statici e/o ai file di modello razor (.cshtml) vengono aggiornate automaticamente senza la necessità di eseguire un passaggio di compilazione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-154">Changes to static files and/or razor template files (.cshtml) are automatically updated without the need of a compilation step.</span></span> <span data-ttu-id="bd0af-155">Dopo aver apportato una modifica, salvarla e fare clic sul pulsante di aggiornamento nel browser per visualizzare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bd0af-155">Make the change, save and tap refresh in the browser to view the update.</span></span>  

<span data-ttu-id="bd0af-156">Le modifiche ai file del codice richiedono la compilazione e il riavvio di Kestrel all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-156">Modifications to code files require compiling and a restart of Kestrel within the container.</span></span> <span data-ttu-id="bd0af-157">Dopo aver apportato una modifica, premere CTRL+F5 per eseguire il processo e avviare l'applicazione all'interno del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-157">After making the change, use CTRL + F5 to perform the process and start the application within the container.</span></span> <span data-ttu-id="bd0af-158">Il contenitore Docker non viene ricompilato o arrestato. Usando `docker ps` nella riga di comando è possibile vedere che il contenitore originale è ancora in esecuzione come 10 minuti fa.</span><span class="sxs-lookup"><span data-stu-id="bd0af-158">The Docker container is not rebuilt or stopped; using `docker ps` in the command line you can see that the original container is still running as of 10 minutes ago.</span></span> 

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   10 minutes ago      Up 10 minutes       0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="publishing-docker-images"></a><span data-ttu-id="bd0af-159">Pubblicazione di immagini Docker</span><span class="sxs-lookup"><span data-stu-id="bd0af-159">Publishing Docker images</span></span>

<span data-ttu-id="bd0af-160">Dopo il completamento del ciclo di sviluppo e debug dell'applicazione, Visual Studio Tools per Docker consente di creare l'immagine di produzione dell'applicazione stessa.</span><span class="sxs-lookup"><span data-stu-id="bd0af-160">Once you have completed the develop and debug cycle of your application, the Visual Studio Tools for Docker will help you create the production image of your application.</span></span> <span data-ttu-id="bd0af-161">Selezionare **Versione** dall'elenco a discesa Debug ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-161">Change the debug dropdown to **Release** and build the application.</span></span> <span data-ttu-id="bd0af-162">Gli strumenti realizzeranno l'immagine con il tag `:latest`. È possibile effettuare il push dell'immagine nel Registro di sistema privato o in Docker Hub.</span><span class="sxs-lookup"><span data-stu-id="bd0af-162">The tooling will produce the image with the `:latest` tag which you can push to your private registry or Docker Hub.</span></span> 

<span data-ttu-id="bd0af-163">Usando `docker images` è possibile visualizzare l'elenco delle immagini.</span><span class="sxs-lookup"><span data-stu-id="bd0af-163">Using the `docker images` you can see the list of images.</span></span>

```console
REPOSITORY                 TAG                 IMAGE ID            CREATED             SIZE
spboyer/hellodockertools   latest              8184ae38ba91        5 seconds ago       278.4 MB
spboyer/hellodockertools   dev                 0b6e2e44b3df        About an hour ago   268.9 MB
microsoft/aspnetcore       1.0.1               189ad4312ce7        5 days ago          268.9 MB
```

<span data-ttu-id="bd0af-164">È possibile aspettarsi che l'immagine di produzione o della versione abbia dimensioni minori rispetto all'immagine **dev**. Tuttavia, grazie all'uso del mapping dei volumi, il debugger e l'applicazione sono stati eseguiti nel computer locale e non nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="bd0af-164">There may be an expectation for the production or release image to be smaller in size by comparison to the **dev** image, however through the use of the volume mapping; the debugger and application were actually being run from your local machine and not within the container.</span></span> <span data-ttu-id="bd0af-165">L'immagine con il tag **latest** integra l'intero codice dell'applicazione necessario per eseguire l'applicazione stessa in un computer host. La differenza corrisponde pertanto alle dimensioni del codice dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bd0af-165">The **latest** image has packaged the entire application code needed to run the application on a host machine, therefore the delta is the size of your application code.</span></span>

