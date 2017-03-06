---
title: Visual Studio Tools per Docker
description: Uso di Visual Studio Tools per Docker
keywords: .NET, .NET Core, Docker, ASP.NET Core, Visual Studio 2015
author: spboyer
ms.author: shboyer
ms.date: 09/16/2016
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-docker
ms.devlang: dotnet
ms.assetid: 1f3b9a68-4dea-4b60-8cb3-f46164eedbbf
translationtype: Human Translation
ms.sourcegitcommit: 90fe68f7f3c4b46502b5d3770b1a2d57c6af748a
ms.openlocfilehash: d3ea05484650d64284affa70c7377df929e44bfc
ms.lasthandoff: 03/02/2017

---

# <a name="visual-studio-tools-for-docker"></a>Visual Studio Tools per Docker 
Lo sviluppo e il debug di un'applicazione in un contenitore Docker può richiedere l'esecuzione di attività di configurazione con diversi strumenti. [Visual Studio Tools per Docker](https://visualstudiogallery.msdn.microsoft.com/0f5b2caa-ea00-41c8-b8a2-058c7da0b3e4) consente di superare gli ostacoli e individuare i bug usando F5 per eseguire il debug dell'applicazione direttamente in un contenitore Docker ospitato localmente. 

> [!NOTE]
>La versione corrente è destinata ai contenitori Docker Linux. La versione per i contenitori Windows sarà disponibile a breve.

## <a name="prerequisites"></a>Prerequisiti
- [Microsoft Visual Studio 2015 Update 3](https://www.visualstudio.com/downloads/download-visual-studio-vs)
- [.NET Core 1.0.1 - VS 2015 Tooling Preview 2](https://go.microsoft.com/fwlink/?LinkID=827546)
- [Docker for Windows](https://www.docker.com/products/docker#/windows) per eseguire localmente i contenitori Docker

## <a name="installation-and-setup"></a>Installazione e configurazione
Scaricare e installare [Visual Studio Tools per Docker](https://aka.ms/DockerToolsForVS) da [Visual Studio Gallery](http://visualstudiogallery.msdn.microsoft.com/). In alternativa, è possibile cercarlo in **Estensioni e aggiornamenti** all'interno di Visual Studio. 

Un'attività di configurazione necessaria è l'impostazione di **[Shared Drives](https://docs.docker.com/docker-for-windows/#/shared-drives)** (Unità condivise) in Docker for Windows. Questa impostazione è necessaria per il mapping dei volumi e il supporto del debug.

Fare clic con il pulsante destro del mouse sull'icona Docker sulla barra delle applicazioni, scegliere Settings (Impostazioni) e quindi selezionare Shared Drives (Unità condivise).

![Shared Drives (Unità condivise)](./media/visual-studio-tools-for-docker/settings-shared-drives-win.png) 

## <a name="create-an-aspnet-web-application-and-add-docker-support"></a>Creare un'applicazione Web ASP.NET e aggiungere il supporto per Docker

Creare una nuova applicazione Web ASP.NET Core usando Visual Studio. Quando l'applicazione è caricata, selezionare **Add Docker Support** (Aggiungi supporto Docker) dal menu **Progetto** oppure fare clic con il pulsante destro del mouse in Esplora soluzioni e scegliere **Aggiungi** > **Docker Support** (Supporto Docker).

Menu Progetto

![Progetto, Add Docker Support (Aggiungi supporto Docker)](./media/visual-studio-tools-for-docker/project-add-docker-support.png)

Menu di scelta rapida Progetto

![Fare clic con il pulsante destro del mouse su Add Docker Support (Aggiungi supporto Docker)](./media/visual-studio-tools-for-docker/right-click-add-docker-support.png)

Al progetto verranno aggiunti i file seguenti:

- **Dockerfile**: il file Docker per applicazioni ASP.NET Core è basato sull'immagine [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore). Questa immagine include i pacchetti NuGet ASP.NET Core che sono stati compilati PreJit migliorando le prestazioni di avvio. Quando si compilano applicazioni .NET Core Console, il file Dockerfile FROM farà riferimento all'immagine [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet) più recente.
- **docker-compose.yml**: file Compose Docker di base usato per definire la raccolta di immagini da compilare ed eseguire con docker-compose build/run.  
- **docker-compose.dev.debug.yml**: file Compose Docker aggiuntivo da usare per modifiche iterative quando la configurazione viene impostata per il debug. Visual Studio chiamerà -f docker-compose.yml -f docker-compose.dev.debug.yml per unire questi elementi. Questo file Compose viene usato dagli strumenti di sviluppo di Visual Studio.   
- **docker-compose.dev.release.yml**: file Compose Docker aggiuntivo usato per il debug della definizione della versione. Monterà il debugger su un volume in modo che il contenuto dell'immagine di produzione non venga modificato.  

Il file docker-compose.yml contiene il nome dell'immagine creata quando si esegue il progetto. 

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

In questo esempio `image: user/hellodockertools${TAG}` genera l'immagine `user/hellodockertools:dev` quando l'applicazione viene eseguita in modalità **Debug** e `user/hellodockertools:latest` viene eseguito in modalità **Versione**. 

Se si prevede di effettuare il push dell'immagine nel Registro di sistema, sarà necessario modificare `user` specificando il proprio nome utente Docker Hub, ad esempio `spboyer/hellodockertools`. In alternativa, modificare l'URL del Registro di sistema privato `privateregistry.domain.com/` in base alla configurazione.

### <a name="debugging"></a>Debug
Selezionare **Docker** dall'elenco a discesa Debug nella barra degli strumenti e usare F5 per avviare il debug dell'applicazione. 

- Se non è già presente nella cache, viene acquisita l'immagine microsoft/aspnetcore.
- ASPNETCORE_ENVIRONMENT viene impostato su Sviluppo all'interno del contenitore.
- La porta 80 viene impostata come EXPOSED e mappata a una porta assegnata in modo dinamico per localhost. La porta è determinata dall'host Docker ed è possibile eseguirvi query con docker ps. 
- L'applicazione viene copiata nel contenitore.
- Usando la porta assegnata in modo dinamico, viene avviato il browser predefinito con il debugger collegato al contenitore. 

La risultante immagine Docker compilata è l'immagine `dev` dell'applicazione con le immagini `microsoft/aspnetcore` come immagine di base.
Nota: nell'immagine dev non è presente il contenuto dell'applicazione poiché le configurazioni Debug usano il montaggio su volume per garantire un'esperienza iterativa. Per effettuare il push di un'immagine, usare la configurazione Versione.

```console
REPOSITORY                  TAG         IMAGE ID            CREATED         SIZE
spboyer/hellodockertools    dev         0b6e2e44b3df        4 minutes ago   268.9 MB
microsoft/aspnetcore        1.0.1       189ad4312ce7        5 days ago      268.9 MB
```

L'applicazione viene eseguita usando il contenitore che è possibile visualizzare eseguendo il comando `docker ps`.

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   4 minutes ago       Up 4 minutes        0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="edit-and-continue"></a>Modifica e continuazione
Le modifiche apportate ai file statici e/o ai file di modello razor (.cshtml) vengono aggiornate automaticamente senza la necessità di eseguire un passaggio di compilazione. Dopo aver apportato una modifica, salvarla e fare clic sul pulsante di aggiornamento nel browser per visualizzare l'aggiornamento.  

Le modifiche ai file del codice richiedono la compilazione e il riavvio di Kestrel all'interno del contenitore. Dopo aver apportato una modifica, premere CTRL+F5 per eseguire il processo e avviare l'applicazione all'interno del contenitore. Il contenitore Docker non viene ricompilato o arrestato. Usando `docker ps` nella riga di comando è possibile vedere che il contenitore originale è ancora in esecuzione come 10 minuti fa. 

```console
CONTAINER ID        IMAGE                          COMMAND               CREATED             STATUS              PORTS                   NAMES
3f240cf686c9        spboyer/hellodockertools:dev   "tail -f /dev/null"   10 minutes ago      Up 10 minutes       0.0.0.0:32769->80/tcp   hellodockertools_hellodockertools_1
```

### <a name="publishing-docker-images"></a>Pubblicazione di immagini Docker 
Dopo il completamento del ciclo di sviluppo e debug dell'applicazione, Visual Studio Tools per Docker consente di creare l'immagine di produzione dell'applicazione stessa. Selezionare **Versione** dall'elenco a discesa Debug ed eseguire l'applicazione. Gli strumenti realizzeranno l'immagine con il tag `:latest`. È possibile effettuare il push dell'immagine nel Registro di sistema privato o in Docker Hub. 

Usando `docker images` è possibile visualizzare l'elenco delle immagini.

```console
REPOSITORY                 TAG                 IMAGE ID            CREATED             SIZE
spboyer/hellodockertools   latest              8184ae38ba91        5 seconds ago       278.4 MB
spboyer/hellodockertools   dev                 0b6e2e44b3df        About an hour ago   268.9 MB
microsoft/aspnetcore       1.0.1               189ad4312ce7        5 days ago          268.9 MB
```

È possibile aspettarsi che l'immagine di produzione o della versione abbia dimensioni minori rispetto all'immagine **dev**. Tuttavia, grazie all'uso del mapping dei volumi, il debugger e l'applicazione sono stati eseguiti nel computer locale e non nel contenitore. L'immagine con il tag **latest** integra l'intero codice dell'applicazione necessario per eseguire l'applicazione stessa in un computer host. La differenza corrisponde pertanto alle dimensioni del codice dell'applicazione.

