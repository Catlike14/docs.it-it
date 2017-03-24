---
title: Comando dotnet-nuget-push | Microsoft Docs
description: Il comando dotnet-nuget-push effettua il push di un pacchetto nel server e lo pubblica.
keywords: dotnet-nuget-push, interfaccia della riga di comando, comando dell&quot;interfaccia della riga di comando, .NET Core
author: karann-msft
ms.author: mairaw
ms.date: 03/06/2017
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: f54d9adf-94f8-41cc-bb52-42f7ca3be6ff
translationtype: Human Translation
ms.sourcegitcommit: 195664ae6409be02ca132900d9c513a7b412acd4
ms.openlocfilehash: 54ffd79cc9306ffcc5793990c3dc2e7534ed3f4b
ms.lasthandoff: 03/07/2017

---
#<a name="dotnet-nuget-push"></a>dotnet-nuget-push

## <a name="name"></a>Nome

`dotnet-nuget-push`: effettua il push di un pacchetto nel server e lo pubblica. 

## <a name="synopsis"></a>Riepilogo

```
dotnet nuget push [<package>] [-s|--source] [-ss|--symbol-source] [-t|--timeout] [-k|--api-key] [-sk|--symbol-api-key] [-d|--disable-buffering] [-n|--no-symbols] [--force-english-output] [-v|--verbosity]
dotnet nuget push [-h|--help]
```

## <a name="description"></a>Descrizione

Il comando `dotnet nuget push` effettua il push di un pacchetto nel server e lo pubblica. Il comando di push usa dettagli del server e delle credenziali presenti nel file di configurazione o nella catena di file di configurazione NuGet. Per altre informazioni sui file di configurazione, vedere [Configuring NuGet Behavior](https://docs.microsoft.com/nuget/consume-packages/configuring-nuget-behavior) (Configurazione del comportamento di NuGet). La configurazione predefinita di NuGet si ottiene caricando *%AppData%\NuGet\NuGet.config* (Windows) o *$HOME/.local/share* (Linux/macOS) e quindi caricando qualsiasi file *nuget.config* o *.nuget\nuget.config* a partire dalla directory radice dell'unità fino alla directory corrente.

## <a name="options"></a>Opzioni

`-h|--help`

Stampa una breve guida per il comando.  

`-s|--source <SOURCE>`

Specifica l'URL del server. Questa opzione è obbligatoria, a meno che il valore di configurazione `DefaultPushSource` non sia impostato nel file di configurazione NuGet.

`--symbols-source <SOURCE>`

Specifica l'URL del server di simboli.

`-t|--timeout <TIMEOUT>`

Specifica il timeout (in secondi) per il push a un server. Il valore predefinito è 300 secondi (5 minuti). Se si specifica 0, viene comunque restituito il valore predefinito.

`-k|--api-key <API_KEY>`

Chiave API per il server.

`--symbol-api-key <API_KEY>`

Chiave API per il server di simboli.

`-d|--disable-buffering`

Disabilita la memorizzazione nel buffer quando si effettua il push a un server HTTP(S) per ridurre l'utilizzo della memoria.

`-n|--no-symbols`

Non effettua il push dei simboli (anche se presenti).

`--force-english-output`

Forza la visualizzazione in inglese di tutto l'output registrato. Oltre a consentire la generazione di output in inglese in computer non configurati per questa lingua, la coerenza tra le diverse piattaforme offerta da questa opzione risulta utile per gli strumenti automatici che ricercano testo nei log.

`--verbosity <LEVEL>`

Visualizza la quantità di dettagli nell'output. Il livello può essere `normal`, `quiet` o `detailed`.

## <a name="examples"></a>Esempi

Effettua il push di foo.nupkg all'origine push predefinita, specificando la chiave API:

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a`

Effettua il push di foo.nupkg all'origine push personalizzata `http://customsource`, specificando la chiave API:

`dotnet nuget push foo.nupkg -k 4003d786-cc37-4004-bfdf-c4f3e8ef9b3a -s http://customsource/` 

Effettua il push di foo.nupkg all'origine push predefinita:

`dotnet nuget push foo.nupkg` 

Effettua il push di foo.symbols.nupkg all'origine simboli predefinita:

`dotnet nuget push foo.symbols.nupkg`

Effettua il push di foo.nupkg all'origine push predefinita, specificando un timeout di 360 secondi:

`dotnet nuget push foo.nupkg --timeout 360`

Effettua il push di tutti i file con estensione .nupkg presenti nella directory corrente all'origine push predefinita:

`dotnet nuget push *.nupkg`

Effettua il push di tutti i file con estensione .nupkg presenti nella directory corrente all'origine push predefinita, specificando un file di configurazione personalizzato *./config/My.Config*:

`dotnet nuget push *.nupkg --config-file ./config/My.Config`

Effettua il push di tutti i file con estensione .nupkg presenti nella directory corrente all'origine push predefinita con il massimo livello di dettaglio:

`dotnet nuget push *.nupkg --verbosity detailed`

