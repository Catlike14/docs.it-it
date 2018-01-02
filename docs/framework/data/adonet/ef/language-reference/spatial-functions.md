---
title: Funzioni spaziali
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 90cb177d-88a0-45be-97e8-3b306283c6e0
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.workload: dotnet
ms.openlocfilehash: c482c2f79c6416a4e748599c896280b426d31ce2
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="spatial-functions"></a><span data-ttu-id="d1700-102">Funzioni spaziali</span><span class="sxs-lookup"><span data-stu-id="d1700-102">Spatial Functions</span></span>
<span data-ttu-id="d1700-103">Nessun formato letterale per i tipi spaziali.</span><span class="sxs-lookup"><span data-stu-id="d1700-103">There is no literal format for spatial types.</span></span> <span data-ttu-id="d1700-104">Tuttavia, è possibile usare le funzioni canoniche di Entity Framework che si chiamano tramite stringhe in formato Well-Known Text.</span><span class="sxs-lookup"><span data-stu-id="d1700-104">However, you can use canonical Entity Framework functions that you call using strings in Well-Known Text format.</span></span> <span data-ttu-id="d1700-105">Ad esempio, la seguente chiamata di funzione crea un punto di geometria:</span><span class="sxs-lookup"><span data-stu-id="d1700-105">For example, the following function call creates a geometry point:</span></span>  
  
```  
GeometryFromText('POINT (43 -73)')  
```  
  
 <span data-ttu-id="d1700-106">Il [metodi SpatialEdmFunctions](http://msdn.microsoft.com/library/hh749531.aspx) pagina vengono elencati tutti i metodi canonici spaziali di Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="d1700-106">The [SpatialEdmFunctions Methods](http://msdn.microsoft.com/library/hh749531.aspx) page lists all spatial canonical Entity Framework methods.</span></span> <span data-ttu-id="d1700-107">Fare clic su un metodo per visualizzare i parametri che devono essere passati a una funzione.</span><span class="sxs-lookup"><span data-stu-id="d1700-107">Click on a method of interest to see what parameters should be passed to a function.</span></span>
