---
title: "Funzionalità non supportata"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: e480cfb5-697e-42c8-bed5-9264c945c4f9
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 6dd8ccebd278fdc36c536c49f7f1d4262b2de8c1
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="unsupported-functionality"></a><span data-ttu-id="31732-102">Funzionalità non supportata</span><span class="sxs-lookup"><span data-stu-id="31732-102">Unsupported Functionality</span></span>
<span data-ttu-id="31732-103">In LINQ to SQL non è possibile esporre la funzionalità SQL seguente tramite la conversione di costrutti CLR (Common Language Runtime) e .NET Framework esistenti:</span><span class="sxs-lookup"><span data-stu-id="31732-103">In LINQ to SQL, the following SQL functionality cannot be exposed through translation of existing common language runtime (CLR) and .NET Framework constructs:</span></span>  
  
-   `STDDEV`  
  
-   `LIKE`  
  
     <span data-ttu-id="31732-104">Sebbene `LIKE` non sia supportato tramite conversione diretta, una funzionalità analoga esiste nella classe <xref:System.Data.Linq.SqlClient.SqlMethods>.</span><span class="sxs-lookup"><span data-stu-id="31732-104">Although `LIKE` is not supported through direct translation, similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span> <span data-ttu-id="31732-105">Per altre informazioni, vedere <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="31732-105">For more information, see <xref:System.Data.Linq.SqlClient.SqlMethods.Like%2A?displayProperty=nameWithType>.</span></span>  
  
-   `DATEDIFF`  
  
     <span data-ttu-id="31732-106">LINQ to SQL dispone di un supporto limitato per `DATEDIFF`.</span><span class="sxs-lookup"><span data-stu-id="31732-106">LINQ to SQL has limited support for `DATEDIFF`.</span></span> <span data-ttu-id="31732-107">Una funzionalità analoga è presente nella classe <xref:System.Data.Linq.SqlClient.SqlMethods>.</span><span class="sxs-lookup"><span data-stu-id="31732-107">Similar functionality exists in the <xref:System.Data.Linq.SqlClient.SqlMethods> class.</span></span>  
  
-   `ROUND`  
  
     <span data-ttu-id="31732-108">LINQ to SQL dispone di un supporto limitato per `ROUND`.</span><span class="sxs-lookup"><span data-stu-id="31732-108">LINQ to SQL has limited support for `ROUND`.</span></span> <span data-ttu-id="31732-109">Per ulteriori informazioni, vedere [metodi System. Math](system-math-methods.md).</span><span class="sxs-lookup"><span data-stu-id="31732-109">For more information, see [System.Math Methods](system-math-methods.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="31732-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="31732-110">See Also</span></span>  
 [<span data-ttu-id="31732-111">Funzioni e tipi di dati</span><span class="sxs-lookup"><span data-stu-id="31732-111">Data Types and Functions</span></span>](data-types-and-functions.md)
