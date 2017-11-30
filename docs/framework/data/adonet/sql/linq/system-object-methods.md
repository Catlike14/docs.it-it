---
title: Metodi System.Object
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 5397fca0-689e-443e-802f-e1cbdc866427
caps.latest.revision: "2"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: 6998c2b00a2b8e83bc79ae7ba1dd01ea549cf5df
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="systemobject-methods"></a><span data-ttu-id="ae26d-102">Metodi System.Object</span><span class="sxs-lookup"><span data-stu-id="ae26d-102">System.Object Methods</span></span>
[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)]<span data-ttu-id="ae26d-103">supporta i seguenti <xref:System.Object> metodi.</span><span class="sxs-lookup"><span data-stu-id="ae26d-103"> supports the following <xref:System.Object> methods.</span></span>  
  
|||  
|-|-|  
|<xref:System.Object.Equals%28System.Object%29?displayProperty=nameWithType>|<xref:System.Object.Equals%28System.Object%2CSystem.Object%29?displayProperty=nameWithType>|  
|<xref:System.Object.ToString?displayProperty=nameWithType>||  
  
 <span data-ttu-id="ae26d-104">In [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] non sono supportati i metodi <xref:System.Object> riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="ae26d-104">[!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] does not support the following <xref:System.Object> methods.</span></span>  
  
|||  
|-|-|  
|<xref:System.Object.GetHashCode?displayProperty=nameWithType>|<xref:System.Object.ReferenceEquals%28System.Object%2CSystem.Object%29?displayProperty=nameWithType>|  
|<xref:System.Object.MemberwiseClone?displayProperty=nameWithType>|<xref:System.Object.GetType?displayProperty=nameWithType>|  
|<span data-ttu-id="ae26d-105"><xref:System.Object.ToString?displayProperty=nameWithType> per i tipi binari, ad esempio `BINARY`, `VARBINARY`, `IMAGE` e `TIMESTAMP`.</span><span class="sxs-lookup"><span data-stu-id="ae26d-105"><xref:System.Object.ToString?displayProperty=nameWithType> for binary types such as `BINARY`, `VARBINARY`, `IMAGE`, and `TIMESTAMP`.</span></span>||  
  
## <a name="differences-from-net"></a><span data-ttu-id="ae26d-106">Differenze rispetto a .NET</span><span class="sxs-lookup"><span data-stu-id="ae26d-106">Differences from .NET</span></span>  
 <span data-ttu-id="ae26d-107">L'output di <xref:System.Object.ToString?displayProperty=nameWithType> per doppia utilizza SQL `CONVERT`(nvarchar (30), @x, 2) in SQL.</span><span class="sxs-lookup"><span data-stu-id="ae26d-107">The output of <xref:System.Object.ToString?displayProperty=nameWithType> for double uses SQL `CONVERT`(NVARCHAR(30), @x, 2) on SQL.</span></span> <span data-ttu-id="ae26d-108">In SQL vengono sempre usate 16 cifre e la notazione scientifica in questo caso, ad esempio "0.000000000000000e+000" per 0.</span><span class="sxs-lookup"><span data-stu-id="ae26d-108">SQL always uses 16 digits and scientific notation in this case (for example, "0.000000000000000e+000" for 0).</span></span> <span data-ttu-id="ae26d-109">Di conseguenza, la conversione di <xref:System.Object.ToString?displayProperty=nameWithType> non genera la stessa stringa di <xref:System.Convert.ToString%2A?displayProperty=nameWithType> in .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ae26d-109">As a result, <xref:System.Object.ToString?displayProperty=nameWithType> conversion does not produce the same string as <xref:System.Convert.ToString%2A?displayProperty=nameWithType> in the .NET Framework.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ae26d-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ae26d-110">See Also</span></span>  
 [<span data-ttu-id="ae26d-111">Funzioni e tipi di dati</span><span class="sxs-lookup"><span data-stu-id="ae26d-111">Data Types and Functions</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
