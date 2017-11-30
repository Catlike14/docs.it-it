---
title: Conversione dei tipi di .NET Framework in stringhe
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: dc2e2b65-f623-4dc3-938b-d2a054d6832c
caps.latest.revision: "3"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: c3abe140e62f112a15a1ad1b1b2a79c14364b26d
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="converting-net-framework-types-to-strings"></a><span data-ttu-id="2982b-102">Conversione dei tipi di .NET Framework in stringhe</span><span class="sxs-lookup"><span data-stu-id="2982b-102">Converting .NET Framework Types to Strings</span></span>
<span data-ttu-id="2982b-103">Se si desidera convertire un tipo .NET Framework in una stringa, utilizzare il **ToString** metodo.</span><span class="sxs-lookup"><span data-stu-id="2982b-103">If you want to convert a .NET Framework type to a string, use the **ToString** method.</span></span> <span data-ttu-id="2982b-104">Il **ToString** metodo restituisce una rappresentazione di stringa del tipo passato.</span><span class="sxs-lookup"><span data-stu-id="2982b-104">The **ToString** method returns a string representation of the type passed in.</span></span> <span data-ttu-id="2982b-105">Nella tabella seguente sono elencati i tipi .NET Framework che restituiscono una stringa in un formato corrispondente alle specifiche XML Schema (XSD).</span><span class="sxs-lookup"><span data-stu-id="2982b-105">The following table lists the .NET Framework types that return a string in a format that maps to the XML Schema (XSD) specifications.</span></span>  
  
|<span data-ttu-id="2982b-106">Tipo .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2982b-106">.NET Framework type</span></span>|<span data-ttu-id="2982b-107">Tipo di stringa restituito</span><span class="sxs-lookup"><span data-stu-id="2982b-107">String type returned</span></span>|  
|-------------------------|--------------------------|  
|<span data-ttu-id="2982b-108">Boolean</span><span class="sxs-lookup"><span data-stu-id="2982b-108">Boolean</span></span>|<span data-ttu-id="2982b-109">"true", "false"</span><span class="sxs-lookup"><span data-stu-id="2982b-109">"true", "false"</span></span>|  
|<span data-ttu-id="2982b-110">Single.PositiveInfinity</span><span class="sxs-lookup"><span data-stu-id="2982b-110">Single.PositiveInfinity</span></span>|<span data-ttu-id="2982b-111">"INF"</span><span class="sxs-lookup"><span data-stu-id="2982b-111">"INF"</span></span>|  
|<span data-ttu-id="2982b-112">Single.NegativeInfinity</span><span class="sxs-lookup"><span data-stu-id="2982b-112">Single.NegativeInfinity</span></span>|<span data-ttu-id="2982b-113">"-INF"</span><span class="sxs-lookup"><span data-stu-id="2982b-113">"-INF"</span></span>|  
|<span data-ttu-id="2982b-114">Double.PositiveInfinity</span><span class="sxs-lookup"><span data-stu-id="2982b-114">Double.PositiveInfinity</span></span>|<span data-ttu-id="2982b-115">"INF"</span><span class="sxs-lookup"><span data-stu-id="2982b-115">"INF"</span></span>|  
|<span data-ttu-id="2982b-116">Double.NegativeInfinity</span><span class="sxs-lookup"><span data-stu-id="2982b-116">Double.NegativeInfinity</span></span>|<span data-ttu-id="2982b-117">"-INF"</span><span class="sxs-lookup"><span data-stu-id="2982b-117">"-INF"</span></span>|  
|<span data-ttu-id="2982b-118">DateTime</span><span class="sxs-lookup"><span data-stu-id="2982b-118">DateTime</span></span>|<span data-ttu-id="2982b-119">Il formato è yyyy-MM-ddTHH:mm:sszzzzzz e i relativi subset.</span><span class="sxs-lookup"><span data-stu-id="2982b-119">Format is yyyy-MM-ddTHH:mm:sszzzzzz and its subsets.</span></span>|  
|<span data-ttu-id="2982b-120">TimeSpan</span><span class="sxs-lookup"><span data-stu-id="2982b-120">Timespan</span></span>|<span data-ttu-id="2982b-121">Il formato è PnYnMnTnHnMnSad esempio, `P2Y10M15DT10H30M20S` corrisponde a una durata di 2 anni, 10 mesi, 15 giorni, 10 ore, 30 minuti e 20 secondi.</span><span class="sxs-lookup"><span data-stu-id="2982b-121">Format is PnYnMnTnHnMnS, for example, `P2Y10M15DT10H30M20S` is a duration of 2 years, 10 months, 15 days, 10hours, 30 minutes and 20 seconds.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="2982b-122">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="2982b-122">See Also</span></span>  
 [<span data-ttu-id="2982b-123">Conversione di tipi di dati XML</span><span class="sxs-lookup"><span data-stu-id="2982b-123">Conversion of XML Data Types</span></span>](../../../../docs/standard/data/xml/conversion-of-xml-data-types.md)  
 [<span data-ttu-id="2982b-124">Conversione di stringhe in tipi di dati .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2982b-124">Converting Strings to .NET Framework Data Types</span></span>](../../../../docs/standard/data/xml/converting-strings-to-dotnet-data-types.md)
