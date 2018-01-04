---
title: ServiceAppDomain
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: f28e5186-a66d-46c1-abe9-b50e07f8cb4f
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 5d948d1c77fc3f188694062ca9dcb3058f408c45
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="serviceappdomain"></a><span data-ttu-id="919ed-102">ServiceAppDomain</span><span class="sxs-lookup"><span data-stu-id="919ed-102">ServiceAppDomain</span></span>
<span data-ttu-id="919ed-103">Esegue il mapping di un servizio a un dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ed-103">Maps a service to an application domain.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="919ed-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="919ed-104">Syntax</span></span>  
  
```  
class ServiceAppDomain  
{  
  Service ref;  
  AppDomainInfo ref;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="919ed-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="919ed-105">Methods</span></span>  
 <span data-ttu-id="919ed-106">La classe ServiceAppDomain non definisce metodi.</span><span class="sxs-lookup"><span data-stu-id="919ed-106">The ServiceAppDomain class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="919ed-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="919ed-107">Properties</span></span>  
 <span data-ttu-id="919ed-108">La classe ServiceAppDomain presenta le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="919ed-108">The ServiceAppDomain class has the following properties:</span></span>  
  
### <a name="ref"></a><span data-ttu-id="919ed-109">ref</span><span class="sxs-lookup"><span data-stu-id="919ed-109">ref</span></span>  
 <span data-ttu-id="919ed-110">Tipo di dati: servizio</span><span class="sxs-lookup"><span data-stu-id="919ed-110">Data type: Service</span></span>  
<span data-ttu-id="919ed-111">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="919ed-111">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="919ed-112">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="919ed-112">Access type: Read-only</span></span>  
  
 <span data-ttu-id="919ed-113">Il servizio di questo dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ed-113">The service of this application domain.</span></span>  
  
### <a name="ref"></a><span data-ttu-id="919ed-114">ref</span><span class="sxs-lookup"><span data-stu-id="919ed-114">ref</span></span>  
 <span data-ttu-id="919ed-115">Tipo di dati: AppDomainInfo</span><span class="sxs-lookup"><span data-stu-id="919ed-115">Data type: AppDomainInfo</span></span>  
<span data-ttu-id="919ed-116">Qualificatori: chiave</span><span class="sxs-lookup"><span data-stu-id="919ed-116">Qualifiers: Key</span></span>  
  
 <span data-ttu-id="919ed-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="919ed-117">Access type: Read-only</span></span>  
  
 <span data-ttu-id="919ed-118">Contiene proprietà del dominio applicazione.</span><span class="sxs-lookup"><span data-stu-id="919ed-118">Contains properties of the application domain.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="919ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="919ed-119">Requirements</span></span>  
  
|<span data-ttu-id="919ed-120">MOF</span><span class="sxs-lookup"><span data-stu-id="919ed-120">MOF</span></span>|<span data-ttu-id="919ed-121">Dichiarato in Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="919ed-121">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="919ed-122">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="919ed-122">Namespace</span></span>|<span data-ttu-id="919ed-123">Definito in root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="919ed-123">Defined in root\ServiceModel</span></span>|
