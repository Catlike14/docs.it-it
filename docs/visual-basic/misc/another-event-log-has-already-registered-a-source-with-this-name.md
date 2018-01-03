---
title: "Un altro log eventi ha già registrato un'origine con questo nome"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 0f04afd5d061a44f572d95abfb0173ad6fa2ac27
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2017
---
# <a name="another-event-log-has-already-registered-a-source-with-this-name"></a><span data-ttu-id="acbe2-102">Un altro log eventi ha già registrato un'origine con questo nome</span><span class="sxs-lookup"><span data-stu-id="acbe2-102">Another event log has already registered a source with this name</span></span>
<span data-ttu-id="acbe2-103">Si è provato a scrivere una voce in un log eventi ma l'origine specificata è stata registrata in un altro log eventi.</span><span class="sxs-lookup"><span data-stu-id="acbe2-103">An attempt was made to write an entry to an event log where the specified source is registered with another event log.</span></span>  
  
 <span data-ttu-id="acbe2-104">Per consentire al componente <xref:System.Diagnostics.EventLog.Source%2A> di scrivere voci in un log, è necessario impostare la proprietà <xref:System.Diagnostics.EventLog> sull'istanza del componente.</span><span class="sxs-lookup"><span data-stu-id="acbe2-104">You must set the <xref:System.Diagnostics.EventLog.Source%2A> property of your <xref:System.Diagnostics.EventLog> component instance before your component writes an entry to a log.</span></span> <span data-ttu-id="acbe2-105">Quando si esegue questa operazione, viene controllato che l'origine specificata sia registrata nel log eventi in cui viene scritto il componente e, se necessario, viene chiamata la proprietà <xref:System.Diagnostics.EventLog.CreateEventSource%2A> .</span><span class="sxs-lookup"><span data-stu-id="acbe2-105">When this happens, the system checks that the source you specified is registered with the event log to which the component is writing, and calls <xref:System.Diagnostics.EventLog.CreateEventSource%2A> if needed.</span></span>  
  
## <a name="to-correct-this-error"></a><span data-ttu-id="acbe2-106">Per correggere l'errore</span><span class="sxs-lookup"><span data-stu-id="acbe2-106">To correct this error</span></span>  
  
1.  <span data-ttu-id="acbe2-107">Rimuovere l'associazione tra l'origine e il primo log usando il metodo <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> o <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> .</span><span class="sxs-lookup"><span data-stu-id="acbe2-107">Remove the association of the source with the first log using the <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> or the <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> method.</span></span>  
  
2.  <span data-ttu-id="acbe2-108">Registrare l'origine nel nuovo log.</span><span class="sxs-lookup"><span data-stu-id="acbe2-108">Register the source with the new log.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="acbe2-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="acbe2-109">See Also</span></span>  
 [<span data-ttu-id="acbe2-110">My</span><span class="sxs-lookup"><span data-stu-id="acbe2-110">My.Application.Log</span></span>](xref:Microsoft.VisualBasic.ApplicationServices.ApplicationBase.Log)  

