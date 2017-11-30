---
title: 'Procedura: convertire un elemento'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: graphics [WPF], translations
ms.assetid: 461c8273-15df-42f6-8672-89ba22887cc0
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 222aebe0ffe3d2bb1d84002a2ad94b0b92ede15b
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-translate-an-element"></a><span data-ttu-id="a8beb-102">Procedura: convertire un elemento</span><span class="sxs-lookup"><span data-stu-id="a8beb-102">How to: Translate an Element</span></span>
<span data-ttu-id="a8beb-103">In questo esempio viene illustrato come quale traslare (spostare) un elemento utilizzando un <xref:System.Windows.Media.TranslateTransform>.</span><span class="sxs-lookup"><span data-stu-id="a8beb-103">This example shows how to translate (move) an element by using a <xref:System.Windows.Media.TranslateTransform>.</span></span>  
  
 <span data-ttu-id="a8beb-104">La <xref:System.Windows.Media.TranslateTransform> classe è particolarmente utile per lo spostamento degli elementi all'interno di riquadri che non supportano il posizionamento assoluto.</span><span class="sxs-lookup"><span data-stu-id="a8beb-104">The <xref:System.Windows.Media.TranslateTransform> class is especially useful for moving elements inside panels that do not support absolute positioning.</span></span> <span data-ttu-id="a8beb-105">Ad esempio, applicando un <xref:System.Windows.Media.TranslateTransform> per il <xref:System.Windows.UIElement.RenderTransform%2A> proprietà di un elemento, è possibile spostare un elemento all'interno di un <xref:System.Windows.Controls.StackPanel> o <xref:System.Windows.Controls.DockPanel>.</span><span class="sxs-lookup"><span data-stu-id="a8beb-105">For example, by applying a <xref:System.Windows.Media.TranslateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of an element, you can move an element within a <xref:System.Windows.Controls.StackPanel> or <xref:System.Windows.Controls.DockPanel>.</span></span>  
  
 <span data-ttu-id="a8beb-106">Utilizzare il <xref:System.Windows.Media.TranslateTransform.X%2A> proprietà del <xref:System.Windows.Media.TranslateTransform> per specificare la quantità, in pixel, per spostare l'elemento lungo l'asse x.</span><span class="sxs-lookup"><span data-stu-id="a8beb-106">Use the <xref:System.Windows.Media.TranslateTransform.X%2A> property of the <xref:System.Windows.Media.TranslateTransform> to specify the amount, in pixels, to move the element along the x-axis.</span></span> <span data-ttu-id="a8beb-107">Utilizzare il <xref:System.Windows.Media.TranslateTransform.Y%2A> proprietà per specificare la quantità, in pixel, per spostare l'elemento lungo l'asse y.</span><span class="sxs-lookup"><span data-stu-id="a8beb-107">Use the <xref:System.Windows.Media.TranslateTransform.Y%2A> property to specify the amount, in pixels, to move the element along the y-axis.</span></span> <span data-ttu-id="a8beb-108">Infine, applicare il <xref:System.Windows.Media.TranslateTransform> per il <xref:System.Windows.UIElement.RenderTransform%2A> proprietà dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a8beb-108">Finally, apply the <xref:System.Windows.Media.TranslateTransform> to the <xref:System.Windows.UIElement.RenderTransform%2A> property of the element.</span></span>  
  
 <span data-ttu-id="a8beb-109">Nell'esempio seguente viene utilizzato un <xref:System.Windows.Media.TranslateTransform> per spostare un pixel elemento 50 a destra e di 50 pixel in basso.</span><span class="sxs-lookup"><span data-stu-id="a8beb-109">The following example uses a <xref:System.Windows.Media.TranslateTransform> to move an element 50 pixels to the right and 50 pixels down.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a8beb-110">Esempio</span><span class="sxs-lookup"><span data-stu-id="a8beb-110">Example</span></span>  
 [!code-xaml[transformsSample#53](../../../../samples/snippets/csharp/VS_Snippets_Wpf/transformsSample/CS/TranslateTransformExample.xaml#53)]  
  
 <span data-ttu-id="a8beb-111">Per l'esempio completo, vedere [2-D Transforms Sample (Esempio di trasformazioni 2D)](http://go.microsoft.com/fwlink/?LinkID=158252).</span><span class="sxs-lookup"><span data-stu-id="a8beb-111">For the complete sample, see [2-D Transforms Sample](http://go.microsoft.com/fwlink/?LinkID=158252).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a8beb-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a8beb-112">See Also</span></span>  
 [<span data-ttu-id="a8beb-113">Cenni preliminari sulle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="a8beb-113">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
