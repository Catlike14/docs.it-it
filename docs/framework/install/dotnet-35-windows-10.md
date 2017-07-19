---
title: Installare .NET Framework 3.5 in Windows 10, Windows 8.1 e Windows 8 | Microsoft Docs
description: Informazioni sull'installazione di .NET Framework 3.5 in Windows 10, Windows 8.1 e Windows 8
author: rlander
keywords: .NET Framework, Installare
ms.date: 04/20/2017
ms.topic: article
ms.prod: .net-framework
ms.technology: vs-ide-deployment
ms.devlang: dotnet
ms.assetid: 67cda1d5-c6g4-4eb5-93e6-4f478de07ff7
ms.translationtype: Human Translation
ms.sourcegitcommit: 4437ce5d344cf06d30e31911def6287999fc6ffc
ms.openlocfilehash: 137436a073c050ed431b231204a3aca31c98c01a
ms.contentlocale: it-it
ms.lasthandoff: 06/02/2017

---

# <a name="install-the-net-framework-35-on-windows-10-windows-81-and-windows-8"></a>Installare .NET Framework 3.5 in Windows 10, Windows 8.1 e Windows 8

Le istruzioni seguenti sono utili nel caso in cui sia necessario installare .NET Framework 3.5 per eseguire un'applicazione in Windows 10, Windows 8.1 e Windows 8 e si applicano anche alle versioni precedenti di Windows.

## <a name="install-the-net-framework-35-on-demand"></a>Installare .NET Framework 3.5 su richiesta

Se si tenta di eseguire un'applicazione che richiede .NET Framework 3.5, potrebbe essere visualizzata la finestra di dialogo di configurazione seguente. Scegliere **Installa la funzionalità** per abilitare .NET Framework 3.5. Per questa opzione è necessaria una connessione Internet.

![Finestra di dialogo di installazione di .NET Framework](./media/dotnet-framework-installation-dialog.jpg)

## <a name="enable-the-net-framework-35-in-control-panel"></a>Abilitare .NET Framework 3.5 dal Pannello di controllo

.NET Framework 3.5 può essere abilitato dal Pannello di controllo di Windows. Per questa opzione è necessaria una connessione Internet.

1. Premere il tasto Windows ![Logo Windows](https://i-msdn.sec.s-msft.com/dynimg/IC721376.jpeg) sulla tastiera, digitare "Funzionalità Windows" e premere INVIO. Viene visualizzata la finestra di dialogo **Attivazione o disattivazione delle funzionalità Windows**.

2. Selezionare la casella di controllo **.NET Framework 3.5 (include .NET 2.0 e 3.0)**, selezionare OK e riavviare il computer, se richiesto.

   ![Installazione di .NET tramite il Pannello di controllo](./media/dotnet-control-panel.png)

   Non è necessario selezionare gli elementi figlio per l'**attivazione HTTP di Windows Communication Foundation (WCF)** e per l'**attivazione non HTTP di Windows Communication Foundation (WCF)**, a meno che, in qualità di sviluppatore o amministratore del server, non si richieda questa funzionalità.

