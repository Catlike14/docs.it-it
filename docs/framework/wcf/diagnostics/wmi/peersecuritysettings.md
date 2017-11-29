---
title: PeerSecuritySettings
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 24ae0d35-f3a3-419b-afd6-686e22aae27b
caps.latest.revision: "7"
author: BrucePerlerMS
ms.author: bruceper
manager: mbaldwin
ms.openlocfilehash: 02cd483f2f7ec5e599b286b672d051a0e8d57940
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="peersecuritysettings"></a><span data-ttu-id="8f0fa-102">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="8f0fa-102">PeerSecuritySettings</span></span>
<span data-ttu-id="8f0fa-103">PeerSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="8f0fa-103">PeerSecuritySettings</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="8f0fa-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f0fa-104">Syntax</span></span>  
  
```  
class PeerSecuritySettings  
{  
  string Mode;  
  PeerTransportSecuritySettings Transport;  
};  
```  
  
## <a name="methods"></a><span data-ttu-id="8f0fa-105">Metodi</span><span class="sxs-lookup"><span data-stu-id="8f0fa-105">Methods</span></span>  
 <span data-ttu-id="8f0fa-106">La classe PeerSecuritySettings non definisce metodi.</span><span class="sxs-lookup"><span data-stu-id="8f0fa-106">The PeerSecuritySettings class does not define any methods.</span></span>  
  
## <a name="properties"></a><span data-ttu-id="8f0fa-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8f0fa-107">Properties</span></span>  
 <span data-ttu-id="8f0fa-108">La classe PeerSecuritySettings ha le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="8f0fa-108">The PeerSecuritySettings class has the following properties:</span></span>  
  
### <a name="mode"></a><span data-ttu-id="8f0fa-109">Modalità</span><span class="sxs-lookup"><span data-stu-id="8f0fa-109">Mode</span></span>  
 <span data-ttu-id="8f0fa-110">Tipo di dati: stringa</span><span class="sxs-lookup"><span data-stu-id="8f0fa-110">Data type: string</span></span>  
  
 <span data-ttu-id="8f0fa-111">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f0fa-111">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f0fa-112">Se un endpoint configurato con l'associazione utilizza meccanismi di sicurezza a livello di messaggio o di trasporto.</span><span class="sxs-lookup"><span data-stu-id="8f0fa-112">Whether message-level and transport-level security are used by an endpoint configured with the binding.</span></span>  
  
### <a name="transport"></a><span data-ttu-id="8f0fa-113">Trasporto</span><span class="sxs-lookup"><span data-stu-id="8f0fa-113">Transport</span></span>  
 <span data-ttu-id="8f0fa-114">Tipo di dati: PeerTransportSecuritySettings</span><span class="sxs-lookup"><span data-stu-id="8f0fa-114">Data type: PeerTransportSecuritySettings</span></span>  
  
 <span data-ttu-id="8f0fa-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8f0fa-115">Access type: Read-only</span></span>  
  
 <span data-ttu-id="8f0fa-116">Impostazioni di sicurezza del trasporto.</span><span class="sxs-lookup"><span data-stu-id="8f0fa-116">Transport security settings.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="8f0fa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f0fa-117">Requirements</span></span>  
  
|<span data-ttu-id="8f0fa-118">MOF</span><span class="sxs-lookup"><span data-stu-id="8f0fa-118">MOF</span></span>|<span data-ttu-id="8f0fa-119">Dichiarato in Servicemodel.mof.</span><span class="sxs-lookup"><span data-stu-id="8f0fa-119">Declared in Servicemodel.mof.</span></span>|  
|---------|-----------------------------------|  
|<span data-ttu-id="8f0fa-120">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8f0fa-120">Namespace</span></span>|<span data-ttu-id="8f0fa-121">Definito in root\ServiceModel</span><span class="sxs-lookup"><span data-stu-id="8f0fa-121">Defined in root\ServiceModel</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="8f0fa-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f0fa-122">See Also</span></span>  
 <xref:System.ServiceModel.PeerSecuritySettings>
