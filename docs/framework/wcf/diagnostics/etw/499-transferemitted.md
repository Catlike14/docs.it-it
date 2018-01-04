---
title: 499 - TransferEmitted
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 07a26434-a7a0-40fc-b5d0-3520a04328ae
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: b1034ae6bd6072a3849d72fafcad55c61e500439
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="499---transferemitted"></a><span data-ttu-id="d2d88-102">499 - TransferEmitted</span><span class="sxs-lookup"><span data-stu-id="d2d88-102">499 - TransferEmitted</span></span>
## <a name="properties"></a><span data-ttu-id="d2d88-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2d88-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="d2d88-104">Id</span><span class="sxs-lookup"><span data-stu-id="d2d88-104">ID</span></span>|<span data-ttu-id="d2d88-105">499</span><span class="sxs-lookup"><span data-stu-id="d2d88-105">499</span></span>|  
|<span data-ttu-id="d2d88-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="d2d88-106">Keywords</span></span>|<span data-ttu-id="d2d88-107">Troubleshooting, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging</span><span class="sxs-lookup"><span data-stu-id="d2d88-107">Troubleshooting, UserEvents, EndToEndMonitoring, ServiceModel, WFTracking, ServiceHost, WCFMessageLogging</span></span>|  
|<span data-ttu-id="d2d88-108">Livello</span><span class="sxs-lookup"><span data-stu-id="d2d88-108">Level</span></span>|<span data-ttu-id="d2d88-109">LogAlways</span><span class="sxs-lookup"><span data-stu-id="d2d88-109">LogAlways</span></span>|  
|<span data-ttu-id="d2d88-110">Canale</span><span class="sxs-lookup"><span data-stu-id="d2d88-110">Channel</span></span>|<span data-ttu-id="d2d88-111">Microsoft-Windows-Application Server-Applications/Analytic</span><span class="sxs-lookup"><span data-stu-id="d2d88-111">Microsoft-Windows-Application Server-Applications/Analytic</span></span>|  
  
## <a name="description"></a><span data-ttu-id="d2d88-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2d88-112">Description</span></span>  
 <span data-ttu-id="d2d88-113">Questo evento viene generato quando si verifica l'evento di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="d2d88-113">This event is emitted when the transfer event takes place.</span></span>  
  
## <a name="message"></a><span data-ttu-id="d2d88-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="d2d88-114">Message</span></span>  
 <span data-ttu-id="d2d88-115">Emissione evento di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="d2d88-115">Transfer event emitted.</span></span>  
  
## <a name="details"></a><span data-ttu-id="d2d88-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="d2d88-116">Details</span></span>  
  
|<span data-ttu-id="d2d88-117">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="d2d88-117">Data Item Name</span></span>|<span data-ttu-id="d2d88-118">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="d2d88-118">Data Item Type</span></span>|<span data-ttu-id="d2d88-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2d88-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="d2d88-120">HostReference</span><span class="sxs-lookup"><span data-stu-id="d2d88-120">HostReference</span></span>|`xs:string`|<span data-ttu-id="d2d88-121">Per i servizi ospitati su Web, questo campo identifica in modo univoco il servizio nella gerarchia Web.</span><span class="sxs-lookup"><span data-stu-id="d2d88-121">For Web-hosted services, this field uniquely identifies the service in the Web hierarchy.</span></span> <span data-ttu-id="d2d88-122">Il formato viene definito come ' nome sito Web dell'applicazione virtuale percorso &#124; Percorso virtuale servizio &#124; ServiceName'.</span><span class="sxs-lookup"><span data-stu-id="d2d88-122">Its format is defined as 'Web Site Name Application Virtual Path&#124;Service Virtual Path&#124;ServiceName'.</span></span> <span data-ttu-id="d2d88-123">Esempio: ' Default Web Site/CalculatorApplication &#124;/CalculatorService.svc &#124; CalculatorService'.</span><span class="sxs-lookup"><span data-stu-id="d2d88-123">Example: 'Default Web Site/CalculatorApplication&#124;/CalculatorService.svc&#124;CalculatorService'.</span></span>|  
|<span data-ttu-id="d2d88-124">AppDomain</span><span class="sxs-lookup"><span data-stu-id="d2d88-124">AppDomain</span></span>|`xs:string`|<span data-ttu-id="d2d88-125">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="d2d88-125">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
