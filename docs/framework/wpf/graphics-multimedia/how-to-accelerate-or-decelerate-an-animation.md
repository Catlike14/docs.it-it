---
title: 'Procedura: accelerare o decelerare un''animazione'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- decelerating animation [WPF]
- accelerating animation [WPF]
- animation [WPF], accelerating
- animation [WPF], decelerating
ms.assetid: 4f383b2c-f94d-4a4e-9a06-f56f5dae95f9
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c06518e3eada30bd4e22549a9ee3c8f16070f5ec
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-accelerate-or-decelerate-an-animation"></a><span data-ttu-id="bf11c-102">Procedura: accelerare o decelerare un'animazione</span><span class="sxs-lookup"><span data-stu-id="bf11c-102">How to: Accelerate or Decelerate an Animation</span></span>
<span data-ttu-id="bf11c-103">In questo esempio viene illustrato come creare un'animazione accelerare e decelerazione nel tempo.</span><span class="sxs-lookup"><span data-stu-id="bf11c-103">This example demonstrates how to make an animation accelerate and decelerate over time.</span></span> <span data-ttu-id="bf11c-104">Nell'esempio seguente, molti rettangoli sono animati da animazioni con diversi <xref:System.Windows.Media.Animation.Timeline.AccelerationRatio%2A> e <xref:System.Windows.Media.Animation.Timeline.DecelerationRatio%2A> impostazioni.</span><span class="sxs-lookup"><span data-stu-id="bf11c-104">In the following example, several rectangles are animated by animations with different <xref:System.Windows.Media.Animation.Timeline.AccelerationRatio%2A> and <xref:System.Windows.Media.Animation.Timeline.DecelerationRatio%2A> settings.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bf11c-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="bf11c-105">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/AccelDecelExample.xaml#1)]  
  
 <span data-ttu-id="bf11c-106">Codice è stato omesso da questo esempio.</span><span class="sxs-lookup"><span data-stu-id="bf11c-106">Code has been omitted from this example.</span></span> <span data-ttu-id="bf11c-107">Per il codice completo, vedere il [esempio di comportamento](http://go.microsoft.com/fwlink/?LinkID=159970).</span><span class="sxs-lookup"><span data-stu-id="bf11c-107">For the complete code, see the [Animation Timing Behavior Sample](http://go.microsoft.com/fwlink/?LinkID=159970).</span></span>
