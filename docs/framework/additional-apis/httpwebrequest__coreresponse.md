---
title: Campo HttpWebRequest._CoreResponse
ms.date: 01/29/2018
topic_type:
- apiref
api_name:
- System.Net.HttpWebRequest._CoreResponse
api_location:
- System.dll
api_type:
- Assembly
author: stevewhims
ms.openlocfilehash: 3627c9bf0d72ccec3a0d6d9c7c89b62f83dcd4b4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33356199"
---
# <a name="httpwebrequestcoreresponse-field"></a><span data-ttu-id="0e165-102">HttpWebRequest. \_CoreResponse campo</span><span class="sxs-lookup"><span data-stu-id="0e165-102">HttpWebRequest.\_CoreResponse Field</span></span>

<span data-ttu-id="0e165-103">`HttpWebRequest._CoreResponse` è un oggetto (entrambi una [CoreResponseData](coreresponsedata.md) o un <xref:System.Exception>) contenente il risultato dell'analisi delle risposte HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e165-103">`HttpWebRequest._CoreResponse` is an object (either a [CoreResponseData](coreresponsedata.md) or an <xref:System.Exception>) containing the result of HTTP response parsing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e165-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e165-104">Syntax</span></span>
  
```csharp
private object _CoreResponse
```

> [!WARNING]
> <span data-ttu-id="0e165-105">Questa API non deve essere utilizzata direttamente nel codice.</span><span class="sxs-lookup"><span data-stu-id="0e165-105">This API is not meant to be used directly in your code.</span></span> <span data-ttu-id="0e165-106">Utilizzare invece un <xref:System.Diagnostics.DiagnosticSource> per associare il codice di rete.</span><span class="sxs-lookup"><span data-stu-id="0e165-106">Instead, you should use a <xref:System.Diagnostics.DiagnosticSource> to hook networking code.</span></span> <span data-ttu-id="0e165-107">Vedere [manuale dell'utente DiagnosticSource](https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.DiagnosticSource/src/DiagnosticSourceUsersGuide.md).</span><span class="sxs-lookup"><span data-stu-id="0e165-107">See [DiagnosticSource User's Guide](https://github.com/dotnet/corefx/blob/master/src/System.Diagnostics.DiagnosticSource/src/DiagnosticSourceUsersGuide.md).</span></span>
> 
> <span data-ttu-id="0e165-108">Microsoft non supporta l'utilizzo di questa classe in un'applicazione di produzione in qualsiasi circostanza.</span><span class="sxs-lookup"><span data-stu-id="0e165-108">Microsoft does not support the use of this class in a production application under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e165-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e165-109">Requirements</span></span>

<span data-ttu-id="0e165-110">**Namespace:** <xref:System.Net></span><span class="sxs-lookup"><span data-stu-id="0e165-110">**Namespace:** <xref:System.Net></span></span>

<span data-ttu-id="0e165-111">**Assembly:** System (System. dll)</span><span class="sxs-lookup"><span data-stu-id="0e165-111">**Assembly:** System (in System.dll)</span></span>

<span data-ttu-id="0e165-112">**Versioni di .NET framework:** disponibile dalla 2.0.</span><span class="sxs-lookup"><span data-stu-id="0e165-112">**.NET Framework versions:** Available since 2.0.</span></span>
