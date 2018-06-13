---
title: "Procedura: Eseguire l'override di una selezione proxy globale"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 0da481a9-b414-4230-beb0-e3ceba882fe5
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: c10cff979a18d8e07a1e7089f96157e4c38f040e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33393906"
---
# <a name="how-to-override-a-global-proxy-selection"></a><span data-ttu-id="2172c-102">Procedura: Eseguire l'override di una selezione proxy globale</span><span class="sxs-lookup"><span data-stu-id="2172c-102">How to: Override a Global Proxy Selection</span></span>
<span data-ttu-id="2172c-103">Questo esempio invia un oggetto **WebRequest** a www.contoso.com che esegue l'override della selezione del proxy globale con un server proxy denominato `alternateproxy` sulla porta 80.</span><span class="sxs-lookup"><span data-stu-id="2172c-103">This example sends a **WebRequest** to www.contoso.com that overrides the global proxy selection with a proxy server named `alternateproxy` on port 80.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2172c-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="2172c-104">Example</span></span>  
  
```csharp  
WebRequest req = WebRequest.Create("http://www.contoso.com/");  
req.Proxy = new WebProxy("http://alternateproxy:80/");  
```  
  
```vb  
Dim req As WebRequest = WebRequest.Create("http://www.contoso.com/")  
req.Proxy = New WebProxy("http://alternateproxy:80/")  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="2172c-105">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="2172c-105">Compiling the Code</span></span>  
 <span data-ttu-id="2172c-106">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="2172c-106">This example requires:</span></span>  
  
-   <span data-ttu-id="2172c-107">Riferimenti allo spazio dei nomi **System.Net**.</span><span class="sxs-lookup"><span data-stu-id="2172c-107">References to the **System.Net** namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2172c-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2172c-108">See Also</span></span>  
 [<span data-ttu-id="2172c-109">Uso di protocolli applicativi</span><span class="sxs-lookup"><span data-stu-id="2172c-109">Using Application Protocols</span></span>](../../../docs/framework/network-programming/using-application-protocols.md)  
 [<span data-ttu-id="2172c-110">Accesso a Internet con un proxy</span><span class="sxs-lookup"><span data-stu-id="2172c-110">Accessing the Internet Through a Proxy</span></span>](../../../docs/framework/network-programming/accessing-the-internet-through-a-proxy.md)
