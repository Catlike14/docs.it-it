---
title: 'Procedura: ruotare l''input penna'
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
- ink [WPF], rotating
- rotating ink [WPF]
ms.assetid: fac36cc9-dd01-41ca-9bde-9d33e3790bbe
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 0bfb3663d5fff7a1611732a016a6d17f143082e2
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-rotate-ink"></a><span data-ttu-id="50dd4-102">Procedura: ruotare l'input penna</span><span class="sxs-lookup"><span data-stu-id="50dd4-102">How to: Rotate Ink</span></span>
## <a name="example"></a><span data-ttu-id="50dd4-103">Esempio</span><span class="sxs-lookup"><span data-stu-id="50dd4-103">Example</span></span>  
 <span data-ttu-id="50dd4-104">Nell'esempio seguente consente di copiare l'input penna da un <xref:System.Windows.Controls.InkCanvas> per un <xref:System.Windows.Controls.Canvas> che contiene un <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="50dd4-104">The following example copies the ink from an <xref:System.Windows.Controls.InkCanvas> to a <xref:System.Windows.Controls.Canvas> that contains an <xref:System.Windows.Controls.InkPresenter>.</span></span>  <span data-ttu-id="50dd4-105">Quando l'applicazione input penna viene copiato, anche ruotato di 90 gradi in senso orario.</span><span class="sxs-lookup"><span data-stu-id="50dd4-105">When the application copies the ink, it also rotates the ink 90 degrees clockwise.</span></span>  
  
 [!code-xaml[HowToRotateInk#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToRotateInk/CSharp/Window1.xaml#1)]  
  
 [!code-csharp[HowToRotateInk#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HowToRotateInk/CSharp/Window1.xaml.cs#2)]  
  
## <a name="example"></a><span data-ttu-id="50dd4-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="50dd4-106">Example</span></span>  
 <span data-ttu-id="50dd4-107">L'esempio seguente è un oggetto personalizzato <xref:System.Windows.Documents.Adorner> che ruota i tratti su un <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="50dd4-107">The following example is a custom <xref:System.Windows.Documents.Adorner> that rotates the strokes on an <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-csharp[AdornerForStrokes#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/RotatingAdornerForStrokes.cs#1)]
 [!code-vb[AdornerForStrokes#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornerForStrokes/VisualBasic/RotatingAdornerForStrokes.vb#1)]  
  
 <span data-ttu-id="50dd4-108">L'esempio seguente è un [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file che definisce un <xref:System.Windows.Controls.InkPresenter> e la popola con input penna.</span><span class="sxs-lookup"><span data-stu-id="50dd4-108">The following example is a [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] file that defines an <xref:System.Windows.Controls.InkPresenter> and populates it with ink.</span></span> <span data-ttu-id="50dd4-109">Il `Window_Loaded` lo strumento decorativo personalizzato al gestore eventi aggiunge il <xref:System.Windows.Controls.InkPresenter>.</span><span class="sxs-lookup"><span data-stu-id="50dd4-109">The `Window_Loaded` event handler adds the custom adorner to the <xref:System.Windows.Controls.InkPresenter>.</span></span>  
  
 [!code-xaml[AdornerForStrokes#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[AdornerForStrokes#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/AdornerForStrokes/CSharp/Window1.xaml.cs#3)]
 [!code-vb[AdornerForStrokes#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/AdornerForStrokes/VisualBasic/Window1.xaml.vb#3)]
