---
title: Pulizia delle risorse non gestite
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Close method
- Dispose method
- garbage collector
- garbage collection, unmanaged resources
- cleanup operations
- explicit cleanups
- unmanaged resource cleanup
- Finalize method
ms.assetid: a17b0066-71c2-4ba4-9822-8e19332fc213
caps.latest.revision: "19"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c94a449edbbe38c4028e27fd946b66a054badf51
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="cleaning-up-unmanaged-resources"></a>Pulizia delle risorse non gestite
Per la maggior parte degli oggetti creati dall'app, è possibile basarsi su. Garbage collector del NET di gestione della memoria. Se però si creano oggetti che includono risorse non gestite, sarà necessario rilasciare esplicitamente queste ultime quando si smette di utilizzarle. Il tipo più comune di risorsa non gestita è rappresentato dagli oggetti che eseguono il wrapping di risorse del sistema operativo, quali file, finestre, connessioni di rete o connessioni di database. Benché il Garbage Collector sia in grado di tenere traccia della durata di un oggetto in cui è incapsulata una risorsa non gestita, non dispone di dati sufficienti per effettuare il rilascio e la pulizia della risorsa non gestita.  
  
 Se i tipi utilizzano risorse non gestite, è necessario effettuare le operazioni seguenti:  
  
-   Implementare il [modello dispose](../../../docs/standard/design-guidelines/dispose-pattern.md). A tale scopo è necessario fornire un'implementazione <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> per abilitare il rilascio deterministico delle risorse non gestite. Un consumer del tipo in uso chiama <xref:System.IDisposable.Dispose%2A> quando l'oggetto e le risorse che utilizza non sono più necessari. Il metodo <xref:System.IDisposable.Dispose%2A> rilascia immediatamente le risorse non gestite.  
  
-   Impostare il rilascio delle risorse non gestite nel caso in cui un consumer del tipo in uso ometta di chiamare <xref:System.IDisposable.Dispose%2A>. Questo risultato può essere raggiunto in due modi:  
  
    -   Utilizzare un handle sicuro per eseguire il wrapping della risorsa non gestita. Questa è la tecnica consigliata. Gli handle sicuri derivano dalla classe <xref:System.Runtime.InteropServices.SafeHandle?displayProperty=nameWithType> e includono un metodo <xref:System.Object.Finalize%2A> affidabile. L'utilizzo di un handle sicuro richiede semplicemente l'implementazione dell'interfaccia <xref:System.IDisposable> e la chiamata del metodo <xref:System.Runtime.InteropServices.SafeHandle.Dispose%2A> dell'handle sicuro nell'implementazione <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType>. Il finalizzatore dell'handle sicuro viene chiamato automaticamente dal Garbage Collector se non viene chiamato il metodo <xref:System.IDisposable.Dispose%2A>.  
  
         -oppure-  
  
    -   Eseguire l'override del metodo <xref:System.Object.Finalize%2A?displayProperty=nameWithType>. La finalizzazione abilita il rilascio non deterministico delle risorse non gestite quando il consumer di un tipo non riesce a chiamare <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> per l'eliminazione deterministica. Tuttavia, poiché la finalizzazione dell'oggetto può essere un'operazione complessa e soggetta a errori, è consigliabile utilizzare un handle sicuro anziché fornire il proprio finalizzatore.  
  
 I consumer del tipo in uso possono quindi chiamare l'implementazione <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> direttamente per liberare la memoria utilizzata dalle risorse non gestite. Quando si implementa correttamente un metodo <xref:System.IDisposable.Dispose%2A>, il metodo <xref:System.Object.Finalize%2A> o il proprio override del metodo <xref:System.Object.Finalize%2A?displayProperty=nameWithType> diventa una misura di protezione per la pulizia delle risorse nel caso in cui il metodo <xref:System.IDisposable.Dispose%2A> non venga chiamato.  
  
## <a name="in-this-section"></a>Contenuto della sezione  
 [Implementazione di un metodo Dispose](../../../docs/standard/garbage-collection/implementing-dispose.md)  
 Viene descritto come implementare il [modello dispose](../../../docs/standard/design-guidelines/dispose-pattern.md) per il rilascio delle risorse non gestite.  
  
 [Uso di oggetti che implementano IDisposable](../../../docs/standard/garbage-collection/using-objects.md)  
 Viene descritto in che modo i consumer di un tipo assicurano la chiamata della relativa implementazione <xref:System.IDisposable.Dispose%2A>. A tale scopo, si consiglia l'utilizzo dell'istruzione `using` in C# o l'istruzione `Using` in Visual Basic.  
  
## <a name="reference"></a>Riferimento  
 <xref:System.IDisposable?displayProperty=nameWithType>  
 Viene definito il metodo <xref:System.IDisposable.Dispose%2A> per il rilascio delle risorse non gestite.  
  
 <xref:System.Object.Finalize%2A?displayProperty=nameWithType>  
 Provvede alla finalizzazione dell'oggetto se le risorse non gestite non vengono rilasciate dal metodo <xref:System.IDisposable.Dispose%2A>.  
  
 <xref:System.GC.SuppressFinalize%2A?displayProperty=nameWithType>  
 Elimina la finalizzazione. Questo metodo viene abitualmente chiamato da un metodo `Dispose` per impedire l'esecuzione di un finalizzatore.
