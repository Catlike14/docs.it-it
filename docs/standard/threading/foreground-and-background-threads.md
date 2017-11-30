---
title: Thread in primo piano e in background
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- threading [.NET Framework], foreground
- threading [.NET Framework], background
- foreground threads
- background threads
ms.assetid: cfe0d632-dd35-47e0-91ad-f742a444005e
caps.latest.revision: "12"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 42ad427fc2c1175c0d9b333aa418aea039f11a35
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="foreground-and-background-threads"></a><span data-ttu-id="6e463-102">Thread in primo piano e in background</span><span class="sxs-lookup"><span data-stu-id="6e463-102">Foreground and Background Threads</span></span>
<span data-ttu-id="6e463-103">Un thread gestito è un thread in background o un thread in primo piano.</span><span class="sxs-lookup"><span data-stu-id="6e463-103">A managed thread is either a background thread or a foreground thread.</span></span> <span data-ttu-id="6e463-104">Thread in background sono identiche a thread in foreground con un'unica eccezione: un thread in background non mantiene l'ambiente di esecuzione gestito.</span><span class="sxs-lookup"><span data-stu-id="6e463-104">Background threads are identical to foreground threads with one exception: a background thread does not keep the managed execution environment running.</span></span> <span data-ttu-id="6e463-105">Una volta tutti i thread in primo piano sono stati interrotti in un processo gestito (in cui il file .exe è un assembly gestito), il sistema di tutti i thread in background e viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="6e463-105">Once all foreground threads have been stopped in a managed process (where the .exe file is a managed assembly), the system stops all background threads and shuts down.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="6e463-106">Quando il runtime interrompe un thread in background, perché si sta arrestando il processo, viene generata alcuna eccezione nel thread.</span><span class="sxs-lookup"><span data-stu-id="6e463-106">When the runtime stops a background thread because the process is shutting down, no exception is thrown in the thread.</span></span> <span data-ttu-id="6e463-107">Tuttavia, quando i thread vengono interrotti perché il <xref:System.AppDomain.Unload%2A?displayProperty=nameWithType> metodo scarica il dominio dell'applicazione, un <xref:System.Threading.ThreadAbortException> viene generata nel thread di sfondo e primo piano.</span><span class="sxs-lookup"><span data-stu-id="6e463-107">However, when threads are stopped because the <xref:System.AppDomain.Unload%2A?displayProperty=nameWithType> method unloads the application domain, a <xref:System.Threading.ThreadAbortException> is thrown in both foreground and background threads.</span></span>  
  
 <span data-ttu-id="6e463-108">Utilizzare il <xref:System.Threading.Thread.IsBackground%2A?displayProperty=nameWithType> proprietà per determinare se un thread è uno sfondo o un thread in primo piano o per modificare il relativo stato.</span><span class="sxs-lookup"><span data-stu-id="6e463-108">Use the <xref:System.Threading.Thread.IsBackground%2A?displayProperty=nameWithType> property to determine whether a thread is a background or a foreground thread, or to change its status.</span></span> <span data-ttu-id="6e463-109">Un thread può essere cambiato in un thread in background in qualsiasi momento impostando il relativo <xref:System.Threading.Thread.IsBackground%2A> proprietà `true`.</span><span class="sxs-lookup"><span data-stu-id="6e463-109">A thread can be changed to a background thread at any time by setting its <xref:System.Threading.Thread.IsBackground%2A> property to `true`.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="6e463-110">Lo stato di primo piano o di sfondo di un thread non incidono sul risultato di un'eccezione non gestita nel thread.</span><span class="sxs-lookup"><span data-stu-id="6e463-110">The foreground or background status of a thread does not affect the outcome of an unhandled exception in the thread.</span></span> <span data-ttu-id="6e463-111">In .NET Framework versione 2.0, un'eccezione non gestita in primo piano o in background thread comporta la terminazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6e463-111">In the .NET Framework version 2.0, an unhandled exception in either foreground or background threads results in termination of the application.</span></span> <span data-ttu-id="6e463-112">Vedere [eccezioni in thread gestiti](../../../docs/standard/threading/exceptions-in-managed-threads.md).</span><span class="sxs-lookup"><span data-stu-id="6e463-112">See [Exceptions in Managed Threads](../../../docs/standard/threading/exceptions-in-managed-threads.md).</span></span>  
  
 <span data-ttu-id="6e463-113">Thread che appartengono al pool di thread gestiti (ovvero, i thread la cui <xref:System.Threading.Thread.IsThreadPoolThread%2A> proprietà `true`) sono thread in background.</span><span class="sxs-lookup"><span data-stu-id="6e463-113">Threads that belong to the managed thread pool (that is, threads whose <xref:System.Threading.Thread.IsThreadPoolThread%2A> property is `true`) are background threads.</span></span> <span data-ttu-id="6e463-114">Tutti i thread che accedono all'ambiente di esecuzione gestita dal codice non gestito sono contrassegnati come thread in background.</span><span class="sxs-lookup"><span data-stu-id="6e463-114">All threads that enter the managed execution environment from unmanaged code are marked as background threads.</span></span> <span data-ttu-id="6e463-115">Tutti i thread generati creando e avviando un nuovo <xref:System.Threading.Thread> oggetto sono thread per impostazione predefinita in primo piano.</span><span class="sxs-lookup"><span data-stu-id="6e463-115">All threads generated by creating and starting a new <xref:System.Threading.Thread> object are by default foreground threads.</span></span>  
  
 <span data-ttu-id="6e463-116">Se si utilizza un thread per monitorare un'attività, ad esempio una connessione socket, impostare il relativo <xref:System.Threading.Thread.IsBackground%2A> proprietà `true` in modo che il thread non impedisce l'interruzione del processo.</span><span class="sxs-lookup"><span data-stu-id="6e463-116">If you use a thread to monitor an activity, such as a socket connection, set its <xref:System.Threading.Thread.IsBackground%2A> property to `true` so that the thread does not prevent your process from terminating.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6e463-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6e463-117">See Also</span></span>  
 <xref:System.Threading.Thread.IsBackground%2A?displayProperty=nameWithType>  
 <xref:System.Threading.Thread>  
 <xref:System.Threading.ThreadAbortException>
