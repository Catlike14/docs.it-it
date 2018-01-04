---
title: 'Procedura: animare un valore Boolean utilizzando fotogrammi chiave'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Booleans [WPF], animating with key frames
- animation [WPF], Booleans with key frames
- key frames [WPF], animating Booleans with
ms.assetid: 4b0fac96-6231-4fcf-9775-4dd673ddc785
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 910210b8360956b9e92b613fad52e7bfc7f5e49e
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-animate-a-boolean-by-using-key-frames"></a><span data-ttu-id="01b1f-102">Procedura: animare un valore Boolean utilizzando fotogrammi chiave</span><span class="sxs-lookup"><span data-stu-id="01b1f-102">How to: Animate a Boolean by Using Key Frames</span></span>
<span data-ttu-id="01b1f-103">In questo esempio viene illustrato come animare il valore della proprietà booleana un <xref:System.Windows.Controls.Button> controllo utilizzando fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="01b1f-103">This example shows how to animate the Boolean property value of a <xref:System.Windows.Controls.Button> control by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01b1f-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="01b1f-104">Example</span></span>  
 <span data-ttu-id="01b1f-105">L'esempio seguente usa il <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames> classe da cui iniziare l'animazione di <xref:System.Windows.UIElement.IsEnabled%2A> proprietà di un <xref:System.Windows.Controls.Button> controllo.</span><span class="sxs-lookup"><span data-stu-id="01b1f-105">The following example uses the <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames> class to animate the <xref:System.Windows.UIElement.IsEnabled%2A> property of a <xref:System.Windows.Controls.Button> control.</span></span> <span data-ttu-id="01b1f-106">Tutti i fotogrammi chiave in questo esempio utilizzano un'istanza di <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> classe.</span><span class="sxs-lookup"><span data-stu-id="01b1f-106">All the key frames in this example use an instance of the <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> class.</span></span> <span data-ttu-id="01b1f-107">Fotogrammi chiave discreti come <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> creare improvvisi tra due valori, ovvero, si scatti dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="01b1f-107">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteBooleanKeyFrame> create sudden jumps between values, that is, the movement of the animation is jerky.</span></span>  
  
 [!code-csharp[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/BooleanAnimationUsingKeyFramesExample.cs#booleananimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/booleananimationusingkeyframesexample.vb#booleananimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#BooleanAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/BooleanAnimationUsingKeyFramesExample.xaml#booleananimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="01b1f-108">Per l'esempio completo, vedere [Esempio di animazione con fotogrammi chiave](http://go.microsoft.com/fwlink/?LinkID=160012).</span><span class="sxs-lookup"><span data-stu-id="01b1f-108">For the complete sample, see [KeyFrame Animation Sample](http://go.microsoft.com/fwlink/?LinkID=160012).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01b1f-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="01b1f-109">See Also</span></span>  
 <xref:System.Windows.Media.Animation.BooleanAnimationUsingKeyFrames>  
 <xref:System.Windows.UIElement.IsEnabled%2A>  
 <xref:System.Windows.Controls.Button>  
 [<span data-ttu-id="01b1f-110">Cenni preliminari sulle animazioni con fotogrammi chiave</span><span class="sxs-lookup"><span data-stu-id="01b1f-110">Key-Frame Animations Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [<span data-ttu-id="01b1f-111">Procedure relative ai fotogrammi chiave</span><span class="sxs-lookup"><span data-stu-id="01b1f-111">Key-Frame How-to Topics</span></span>](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)
