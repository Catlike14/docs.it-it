---
title: 'Procedura: Eseguire l''override di una selezione proxy globale'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
ms.assetid: 0da481a9-b414-4230-beb0-e3ceba882fe5
caps.latest.revision: "8"
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: dc9f8f4e958d1988cecd769431e99d70ff2a4cfd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-override-a-global-proxy-selection"></a><span data-ttu-id="e8828-102">Procedura: Eseguire l'override di una selezione proxy globale</span><span class="sxs-lookup"><span data-stu-id="e8828-102">How to: Override a Global Proxy Selection</span></span>
<span data-ttu-id="e8828-103">Questo esempio invia un oggetto **WebRequest** a www.contoso.com che esegue l'override della selezione del proxy globale con un server proxy denominato `alternateproxy` sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="e8828-103">This example sends a **WebRequest** to www.contoso.com that overrides the global proxy selection with a proxy server named `alternateproxy` on port 80.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e8828-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="e8828-104">Example</span></span>  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
req.Proxy = new WebProxy("http://alternateproxy:80/");  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com/")  
req.Proxy = New WebProxy("http://alternateproxy:80/")  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e8828-105">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="e8828-105">Compiling the Code</span></span>  
 <span data-ttu-id="e8828-106">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e8828-106">This example requires:</span></span>  
  
-   <span data-ttu-id="e8828-107">Riferimenti allo spazio dei nomi **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="e8828-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8828-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e8828-108">See Also</span></span>  
 [<span data-ttu-id="e8828-109">Uso di protocolli applicativi</span><span class="sxs-lookup"><span data-stu-id="e8828-109">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)  
 [<span data-ttu-id="e8828-110">Accesso a Internet con un proxy</span><span class="sxs-lookup"><span data-stu-id="e8828-110">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
