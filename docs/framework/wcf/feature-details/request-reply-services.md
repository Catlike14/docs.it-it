---
title: Servizi request/reply
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- Windows Communication Foundation [WCF], request-reply services
- contracts [WCF], request-reply services
- WCF [WCF], request-reply services
- request-reply contracts [WCF]
ms.assetid: 2fa710f1-47f4-4598-b063-3ab3bd22ebba
caps.latest.revision: "7"
author: Erikre
ms.author: erikre
manager: erikre
ms.openlocfilehash: a38a90d4e9ec249f91e8bfda88c646c006890d8d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="request-reply-services"></a><span data-ttu-id="56cc3-102">Servizi request/reply</span><span class="sxs-lookup"><span data-stu-id="56cc3-102">Request-Reply Services</span></span>
<span data-ttu-id="56cc3-103">I servizi request/reply sono il tipo predefinito di contratto dell'operazione in [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)].</span><span class="sxs-lookup"><span data-stu-id="56cc3-103">Request-reply services are the default type of operation contract in [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)].</span></span> <span data-ttu-id="56cc3-104">I client effettuano chiamate alle operazioni del servizio e attendono una risposta dal servizio.</span><span class="sxs-lookup"><span data-stu-id="56cc3-104">Clients make calls to service operations and wait for a response from the service.</span></span> <span data-ttu-id="56cc3-105">È possibile effettuare chiamate a un'operazione del servizio in modo sincrono o asincrono. Nel primo caso, il client si blocca finché non riceve una risposta dal servizio o la chiamata scade, mentre nel secondo caso il client esegue una chiamata all'operazione del servizio, continua a funzionare e riceve la risposta dal servizio su un altro thread.</span><span class="sxs-lookup"><span data-stu-id="56cc3-105">You can perform calls to a service operation either synchronously, where the client blocks until it receives a response from the service or the call times, or asynchronously, where the client makes a call to the service operation, continues working, and receives the response from the service on another thread.</span></span>  
  
 <span data-ttu-id="56cc3-106">Per creare un contratto di servizio request/reply, definirlo e applicare la classe <xref:System.ServiceModel.OperationContractAttribute> a ogni operazione, come illustrato nel codice di esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="56cc3-106">To create a request-reply service contract, define your service contract, and apply the <xref:System.ServiceModel.OperationContractAttribute> class to each operation, as shown in the following sample code.</span></span>  
  
```  
[ServiceContract(Namespace="http://Microsoft.ServiceModel.Samples")]  
public interface IRequestReplyCalculator  
{  
    [OperationContract]  
    double Add(double n1, double n2);  
}  
```  
  
 <span data-ttu-id="56cc3-107">Non è necessario impostare la proprietà <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> su `false` perché questo è il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="56cc3-107">You do not have to set the  <xref:System.ServiceModel.OperationContractAttribute.IsOneWay%2A> property to `false` because this is the default behavior.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="56cc3-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="56cc3-108">See Also</span></span>  
 [<span data-ttu-id="56cc3-109">Servizi unidirezionali</span><span class="sxs-lookup"><span data-stu-id="56cc3-109">One-Way Services</span></span>](../../../../docs/framework/wcf/feature-details/one-way-services.md)  
 [<span data-ttu-id="56cc3-110">Servizi duplex</span><span class="sxs-lookup"><span data-stu-id="56cc3-110">Duplex Services</span></span>](../../../../docs/framework/wcf/feature-details/duplex-services.md)
