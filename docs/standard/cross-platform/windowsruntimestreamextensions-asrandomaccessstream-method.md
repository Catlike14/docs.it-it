---
title: Metodo WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
api_name: System.IO.WindowsRuntimeStreamExtensions.AsRandomAccessStream
api_location: System.Runtime.WindowsRuntime.dll
ms.assetid: dcc72283-caed-49ee-b45d-ccaf94e97129
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: be93ddc0f3bf0a5079f31bfa0ff5caa882342c37
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="windowsruntimestreamextensionsasrandomaccessstreamsystemiostream-method"></a><span data-ttu-id="4002c-102">Metodo WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream)</span><span class="sxs-lookup"><span data-stu-id="4002c-102">WindowsRuntimeStreamExtensions.AsRandomAccessStream(System.IO.Stream) Method</span></span>
<span data-ttu-id="4002c-103">[Supportato in .NET Framework 4.5.1 e versioni successive]</span><span class="sxs-lookup"><span data-stu-id="4002c-103">[Supported in the .NET Framework 4.5.1 and later versions]</span></span>  
  
 <span data-ttu-id="4002c-104">Converte il flusso specificato in un flusso di accesso casuale.</span><span class="sxs-lookup"><span data-stu-id="4002c-104">Converts the specified stream to a random access stream.</span></span>  
  
 <span data-ttu-id="4002c-105">**Namespace:**<xref:System.IO?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="4002c-105">**Namespace:** <xref:System.IO?displayProperty=nameWithType></span></span>  
 <span data-ttu-id="4002c-106">**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span><span class="sxs-lookup"><span data-stu-id="4002c-106">**Assembly:** System.Runtime.WindowsRuntime (in System.Runtime.WindowsRuntime.dll)</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="4002c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4002c-107">Syntax</span></span>  
  
```csharp  
[CLSCompliantAttribute(false)]  
public static  IRandomAccessStream AsRandomAccessStream(Stream stream)  
```  
  
```vb  
'Declaration  
<ExtensionAttribute> _  
<CLSCompliantAttribute(False)> _  
Public Shared Function AsRandomAccessStream ( _  
        stream As Stream) As IRandomAccessStream  
```  
  
#### <a name="parameters"></a><span data-ttu-id="4002c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4002c-108">Parameters</span></span>  
 `stream`  
  
 <span data-ttu-id="4002c-109">Tipo: <xref:System.IO.Stream?displayProperty=nameWithType></span><span class="sxs-lookup"><span data-stu-id="4002c-109">Type: <xref:System.IO.Stream?displayProperty=nameWithType></span></span>  
<span data-ttu-id="4002c-110">Flusso da convertire.</span><span class="sxs-lookup"><span data-stu-id="4002c-110">The stream to convert.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="4002c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4002c-111">Return Value</span></span>  
 <span data-ttu-id="4002c-112">Tipo: [Windows.Storage.Streams.RandomAccessStream](http://msdn.microsoft.com/library/windows/apps/windows.storage.streams.randomaccessstream.aspx)</span><span class="sxs-lookup"><span data-stu-id="4002c-112">Type: [Windows.Storage.Streams.RandomAccessStream](http://msdn.microsoft.com/library/windows/apps/windows.storage.streams.randomaccessstream.aspx)</span></span>  
<span data-ttu-id="4002c-113">Oggetto [!INCLUDE[wrt](../../../includes/wrt-md.md)] flusso ad accesso casuale, che rappresenta il flusso convertito.</span><span class="sxs-lookup"><span data-stu-id="4002c-113">A [!INCLUDE[wrt](../../../includes/wrt-md.md)] random access stream, which represents the converted stream.</span></span>  
  
## <a name="exceptions"></a><span data-ttu-id="4002c-114">Eccezioni</span><span class="sxs-lookup"><span data-stu-id="4002c-114">Exceptions</span></span>  
  
|<span data-ttu-id="4002c-115">Eccezione</span><span class="sxs-lookup"><span data-stu-id="4002c-115">Exception</span></span>|<span data-ttu-id="4002c-116">Condizione</span><span class="sxs-lookup"><span data-stu-id="4002c-116">Condition</span></span>|  
|---------------|---------------|  
|<xref:System.NotSupportedException>|<span data-ttu-id="4002c-117">Il flusso da convertire non supporta la ricerca.</span><span class="sxs-lookup"><span data-stu-id="4002c-117">The stream to convert does not support seeking.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4002c-118">Note</span><span class="sxs-lookup"><span data-stu-id="4002c-118">Remarks</span></span>  
 <span data-ttu-id="4002c-119">Questo metodo di estensione è disponibile solo quando si sviluppano applicazioni Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002c-119">This extension method is available only when you develop Windows Store apps.</span></span> <span data-ttu-id="4002c-120">Questo metodo fornisce un modo conveniente per lavorare con i flussi nelle applicazioni Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4002c-120">This method provides a convenient way of working with streams in Windows Store apps.</span></span> <span data-ttu-id="4002c-121">Il flusso .NET Framework da convertire deve supportare la ricerca.</span><span class="sxs-lookup"><span data-stu-id="4002c-121">The .NET Framework stream you want to convert must support seeking.</span></span> <span data-ttu-id="4002c-122">Per altre informazioni, vedere il metodo <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="4002c-122">For more information, see the <xref:System.IO.Stream.Seek%2A?displayProperty=nameWithType> method.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="4002c-123">Questa API è supportata in .NET Framework 4.5.1 e nelle versioni successive, ma non nella versione 4.5.</span><span class="sxs-lookup"><span data-stu-id="4002c-123">This API is supported in the .NET Framework 4.5.1 and later versions, but not in version 4.5.</span></span>  
  
## <a name="version-information"></a><span data-ttu-id="4002c-124">Informazioni sulla versione</span><span class="sxs-lookup"><span data-stu-id="4002c-124">Version Information</span></span>  
 <span data-ttu-id="4002c-125">**.NET per applicazioni Windows Store**</span><span class="sxs-lookup"><span data-stu-id="4002c-125">**.NET for Windows Store apps**</span></span>  
  
 <span data-ttu-id="4002c-126">Supportato in: Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4002c-126">Supported in: Windows 8.1</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4002c-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4002c-127">See Also</span></span>  
 <!--zz <xref:System.IO.WindowsRuntimeStreamExtensions>--> `System.IO.WindowsRuntimeStreamExtensions`  
 [<span data-ttu-id="4002c-128">Procedura: Eseguire la conversione tra flussi di .NET Framework e flussi di Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="4002c-128">How to: Convert Between .NET Framework Streams and Windows Runtime Streams</span></span>](../../../docs/standard/io/how-to-convert-between-dotnet-streams-and-winrt-streams.md)
