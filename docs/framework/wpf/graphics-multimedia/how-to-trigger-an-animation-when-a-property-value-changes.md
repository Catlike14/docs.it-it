---
title: "Procedura: attivare un'animazione quando il valore di una proprietà viene modificato"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- animation [WPF], starting when property values change
- triggering animation [WPF]
- Storyboards [WPF], starting when property values change
ms.assetid: 12399c21-0300-4f4f-9e3a-d92d9907e5f5
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 4d722be0f0367f7e6e98ef1c8451ce58ee28fedd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-trigger-an-animation-when-a-property-value-changes"></a><span data-ttu-id="f5703-102">Procedura: attivare un'animazione quando il valore di una proprietà viene modificato</span><span class="sxs-lookup"><span data-stu-id="f5703-102">How to: Trigger an Animation When a Property Value Changes</span></span>
<span data-ttu-id="f5703-103">In questo esempio viene illustrato come utilizzare un <xref:System.Windows.Trigger> per avviare un <xref:System.Windows.Media.Animation.Storyboard> quando si modifica un valore di proprietà.</span><span class="sxs-lookup"><span data-stu-id="f5703-103">This example shows how to use a <xref:System.Windows.Trigger> to start a <xref:System.Windows.Media.Animation.Storyboard> when a property value changes.</span></span> <span data-ttu-id="f5703-104">È possibile utilizzare un <xref:System.Windows.Trigger> all'interno di un <xref:System.Windows.Style>, <xref:System.Windows.Controls.ControlTemplate>, o <xref:System.Windows.DataTemplate>.</span><span class="sxs-lookup"><span data-stu-id="f5703-104">You can use a <xref:System.Windows.Trigger> inside a <xref:System.Windows.Style>, <xref:System.Windows.Controls.ControlTemplate>, or <xref:System.Windows.DataTemplate>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f5703-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="f5703-105">Example</span></span>  
 <span data-ttu-id="f5703-106">Nell'esempio seguente viene utilizzato un <xref:System.Windows.Trigger> per animare la <xref:System.Windows.UIElement.Opacity%2A> di un <xref:System.Windows.Controls.Button> quando relativo <xref:System.Windows.UIElement.IsMouseOver%2A> proprietà diventa `true`.</span><span class="sxs-lookup"><span data-stu-id="f5703-106">The following example uses a <xref:System.Windows.Trigger> to animate the <xref:System.Windows.UIElement.Opacity%2A> of a <xref:System.Windows.Controls.Button> when its <xref:System.Windows.UIElement.IsMouseOver%2A> property becomes `true`.</span></span>  
  
 [!code-xaml[AnimatePropertyStoryboards#PropertyTriggerExample](../../../../samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/PropertyTriggerExample.xaml#propertytriggerexample)]  
  
 <span data-ttu-id="f5703-107">Le animazioni applicate tramite proprietà <xref:System.Windows.Trigger> oggetti si comportano in modo più complesso rispetto a <xref:System.Windows.EventTrigger> animazioni o a quelle avviate tramite <xref:System.Windows.Media.Animation.Storyboard> metodi.</span><span class="sxs-lookup"><span data-stu-id="f5703-107">Animations applied by property <xref:System.Windows.Trigger> objects behave in a more complex fashion than <xref:System.Windows.EventTrigger> animations or animations started using <xref:System.Windows.Media.Animation.Storyboard> methods.</span></span>  <span data-ttu-id="f5703-108">Essi "handoff" con le animazioni definite da altri <xref:System.Windows.Trigger> oggetti, ma possono essere combinate con <xref:System.Windows.EventTrigger> e le animazioni basate su metodo.</span><span class="sxs-lookup"><span data-stu-id="f5703-108">They "handoff" with animations defined by other <xref:System.Windows.Trigger> objects, but compose with <xref:System.Windows.EventTrigger> and method-triggered animations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5703-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f5703-109">See Also</span></span>  
 <xref:System.Windows.Trigger>  
 [<span data-ttu-id="f5703-110">Cenni preliminari sulle tecniche di animazione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f5703-110">Property Animation Techniques Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/property-animation-techniques-overview.md)  
 [<span data-ttu-id="f5703-111">Cenni preliminari sugli storyboard</span><span class="sxs-lookup"><span data-stu-id="f5703-111">Storyboards Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/storyboards-overview.md)
