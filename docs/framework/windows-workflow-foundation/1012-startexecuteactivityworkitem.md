---
title: 1012 - StartExecuteActivityWorkItem
ms.date: 03/30/2017
ms.assetid: 29e9b1c6-c5d7-4b58-b59d-a06a923d3c80
ms.openlocfilehash: d6b330bc454c39584e5027f757fd9d9d3434d941
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33510380"
---
# <a name="1012---startexecuteactivityworkitem"></a><span data-ttu-id="313be-102">1012 - StartExecuteActivityWorkItem</span><span class="sxs-lookup"><span data-stu-id="313be-102">1012 - StartExecuteActivityWorkItem</span></span>
## <a name="properties"></a><span data-ttu-id="313be-103">Proprietà</span><span class="sxs-lookup"><span data-stu-id="313be-103">Properties</span></span>  
  
|||  
|-|-|  
|<span data-ttu-id="313be-104">ID</span><span class="sxs-lookup"><span data-stu-id="313be-104">ID</span></span>|<span data-ttu-id="313be-105">1012</span><span class="sxs-lookup"><span data-stu-id="313be-105">1012</span></span>|  
|<span data-ttu-id="313be-106">Parole chiave</span><span class="sxs-lookup"><span data-stu-id="313be-106">Keywords</span></span>|<span data-ttu-id="313be-107">WFRuntime</span><span class="sxs-lookup"><span data-stu-id="313be-107">WFRuntime</span></span>|  
|<span data-ttu-id="313be-108">Livello</span><span class="sxs-lookup"><span data-stu-id="313be-108">Level</span></span>|<span data-ttu-id="313be-109">Dettagliato</span><span class="sxs-lookup"><span data-stu-id="313be-109">Verbose</span></span>|  
|<span data-ttu-id="313be-110">Canale</span><span class="sxs-lookup"><span data-stu-id="313be-110">Channel</span></span>|<span data-ttu-id="313be-111">Microsoft-Windows-Application Server-Applications/Debug</span><span class="sxs-lookup"><span data-stu-id="313be-111">Microsoft-Windows-Application Server-Applications/Debug</span></span>|  
  
## <a name="description"></a><span data-ttu-id="313be-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="313be-112">Description</span></span>  
 <span data-ttu-id="313be-113">Indica che viene avviata l'esecuzione di ExecuteActivityWorkItem.</span><span class="sxs-lookup"><span data-stu-id="313be-113">Indicates an ExecuteActivityWorkItem is starting execution.</span></span>  
  
## <a name="message"></a><span data-ttu-id="313be-114">Messaggio</span><span class="sxs-lookup"><span data-stu-id="313be-114">Message</span></span>  
 <span data-ttu-id="313be-115">Avvio dell'esecuzione di ExecuteActivityWorkItem per l'attività '%1', DisplayName: '%2', InstanceId: '%3'.</span><span class="sxs-lookup"><span data-stu-id="313be-115">Starting execution of an ExecuteActivityWorkItem for Activity '%1', DisplayName: '%2', InstanceId: '%3'.</span></span>  
  
## <a name="details"></a><span data-ttu-id="313be-116">Dettagli</span><span class="sxs-lookup"><span data-stu-id="313be-116">Details</span></span>  
  
|<span data-ttu-id="313be-117">Nome elemento dati</span><span class="sxs-lookup"><span data-stu-id="313be-117">Data Item Name</span></span>|<span data-ttu-id="313be-118">Tipo elemento dati</span><span class="sxs-lookup"><span data-stu-id="313be-118">Data Item Type</span></span>|<span data-ttu-id="313be-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="313be-119">Description</span></span>|  
|--------------------|--------------------|-----------------|  
|<span data-ttu-id="313be-120">Attività</span><span class="sxs-lookup"><span data-stu-id="313be-120">Activity</span></span>|<span data-ttu-id="313be-121">xs:string</span><span class="sxs-lookup"><span data-stu-id="313be-121">xs:string</span></span>|<span data-ttu-id="313be-122">Il nome del tipo di attività.</span><span class="sxs-lookup"><span data-stu-id="313be-122">The type name of the activity.</span></span>|  
|<span data-ttu-id="313be-123">DisplayName</span><span class="sxs-lookup"><span data-stu-id="313be-123">DisplayName</span></span>|<span data-ttu-id="313be-124">xs:string</span><span class="sxs-lookup"><span data-stu-id="313be-124">xs:string</span></span>|<span data-ttu-id="313be-125">Nome visualizzato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="313be-125">The display name of the activity.</span></span>|  
|<span data-ttu-id="313be-126">InstanceId</span><span class="sxs-lookup"><span data-stu-id="313be-126">InstanceId</span></span>|<span data-ttu-id="313be-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="313be-127">xs:string</span></span>|<span data-ttu-id="313be-128">L'ID dell'istanza dell'attività.</span><span class="sxs-lookup"><span data-stu-id="313be-128">The instance id of the activity.</span></span>|  
|<span data-ttu-id="313be-129">AppDomain</span><span class="sxs-lookup"><span data-stu-id="313be-129">AppDomain</span></span>|<span data-ttu-id="313be-130">xs:string</span><span class="sxs-lookup"><span data-stu-id="313be-130">xs:string</span></span>|<span data-ttu-id="313be-131">Stringa restituita da AppDomain.CurrentDomain.FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="313be-131">The string returned by AppDomain.CurrentDomain.FriendlyName.</span></span>|
