---
title: Panoramica di .NET Core SDK
description: Informazioni su .NET Core SDK, ovvero un set di librerie e strumenti usati per creare progetti .NET Core.
keywords: .NET, .NET Core
author: blackdwarf
ms.author: mairaw
ms.date: 06/20/2016
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: 26bc9822-e42b-48ec-b0d6-499dc604add7
ms.workload: dotnetcore
ms.openlocfilehash: f32f4c50f5b3fef8f38560ea3516265f7a4ac008
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/23/2017
---
# <a name="net-core-sdk-overview"></a>Panoramica di .NET Core SDK 

## <a name="introduction"></a>Introduzione
.NET Core SDK è un set di librerie e strumenti che consente agli sviluppatori di creare applicazioni e librerie .NET Core. Si tratta del pacchetto che gli sviluppatori acquisteranno con maggiore probabilità. 

Contiene i componenti seguenti:

1. Strumenti da riga di comando .NET usati per la compilazione delle applicazioni
2. .NET Core (librerie e runtime) che consentono la compilazione e l'esecuzione delle applicazioni
3. Driver `dotnet` per l'esecuzione dei [comandi dell'interfaccia della riga di comando](tools/index.md) e delle applicazioni


## <a name="acquiring-the-net-core-sdk"></a>Acquisizione di .NET Core SDK
Come per qualsiasi strumento, è innanzitutto necessario eseguire l'installazione nel computer. A seconda dello scenario, per installare l'SDK è possibile usare programmi nativi oppure lo script della shell di installazione.

I programmi di installazione nativi sono principalmente destinati ai computer degli sviluppatori. L'SDK viene distribuito mediante il meccanismo di installazione nativo di ogni piattaforma supportata, ad esempio i pacchetti DEB in Ubuntu o i bundle MSI in Windows. Questi programmi di installazione installano e configurano l'ambiente in base alle esigenze per consentire all'utente di usare l'SDK immediatamente dopo l'installazione. Tuttavia, richiedono anche privilegi amministrativi sul computer. È possibile visualizzare le istruzioni di installazione in [.NET Core installation guide](https://aka.ms/dotnetcoregs) (Guida all'installazione di .NET Core).

Al contrario, gli script di installazione non richiedono privilegi amministrativi. Tuttavia, non installano tutti i prerequisiti nel computer ed è quindi necessario installarli manualmente. Gli script sono progettati principalmente per configurare i server di compilazione o possono essere usati quando si vuole installare gli strumenti senza privilegi amministrativi (tenendo conto della precedente precisazione relativa ai prerequisiti). È possibile trovare altre informazioni nell'[argomento di riferimento dello script di installazione](tools/dotnet-install-script.md). Se si è interessati alla procedura per configurare l'SDK nel server di compilazione con integrazione continua (CI, Continuous Integration), è possibile vedere il documento sull'uso dell'[SDK con server CI](tools/using-ci-with-cli.md). 

Per impostazione predefinita, l'SDK viene installato in modalità side-by-side (SxS). Ciò significa che più versioni degli strumenti dell'interfaccia della riga di comando possono coesistere in un determinato momento su un singolo computer. Il modo in cui viene identificata la versione corretta è illustrato più dettagliatamente nella sezione [Driver](tools/index.md#driver) dell'argomento relativo agli strumenti della riga di comando di .NET Core.
