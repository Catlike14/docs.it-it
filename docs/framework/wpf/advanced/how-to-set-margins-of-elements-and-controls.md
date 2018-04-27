---
title: 'Procedura: impostare i margini di elementi e controlli'
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-wpf
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- setting [WPF], Margin property
- properties [WPF], Margin property
- Margin property [WPF], setting
ms.assetid: 70ebee01-6f87-4352-8dd4-402c65eaaed6
caps.latest.revision: 9
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: f32107074239e9713feaa9e0b9b7e1f89869d111
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2018
---
# <a name="how-to-set-margins-of-elements-and-controls"></a><span data-ttu-id="1ed05-102">Procedura: impostare i margini di elementi e controlli</span><span class="sxs-lookup"><span data-stu-id="1ed05-102">How to: Set Margins of Elements and Controls</span></span>
<span data-ttu-id="1ed05-103">In questo esempio viene illustrato come impostare il <xref:System.Windows.FrameworkElement.Margin%2A> proprietà modificando i valori di proprietà esistenti per il margine nel code-behind.</span><span class="sxs-lookup"><span data-stu-id="1ed05-103">This example describes how to set the <xref:System.Windows.FrameworkElement.Margin%2A> property, by changing any existing property value for the margin in code-behind.</span></span> <span data-ttu-id="1ed05-104">Il <xref:System.Windows.FrameworkElement.Margin%2A> è una proprietà del <xref:System.Windows.FrameworkElement> elemento di base e pertanto viene ereditata da un'ampia gamma di controlli e altri elementi.</span><span class="sxs-lookup"><span data-stu-id="1ed05-104">The <xref:System.Windows.FrameworkElement.Margin%2A> property is a property of the <xref:System.Windows.FrameworkElement> base element, and is thus inherited by a variety of controls and other elements.</span></span>  
  
 <span data-ttu-id="1ed05-105">Questo esempio è scritto in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], con un code-behind del file che il [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] fa riferimento a.</span><span class="sxs-lookup"><span data-stu-id="1ed05-105">This example is written in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], with a code-behind file that the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] refers to.</span></span> <span data-ttu-id="1ed05-106">Il code-behind è visualizzato in c# e una versione di Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1ed05-106">The code-behind is shown in both a C# and a Microsoft Visual Basic version.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1ed05-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="1ed05-107">Example</span></span>  
 [!code-xaml[FEMarginProgrammatic#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml#xaml)]  
  
 [!code-csharp[FEMarginProgrammatic#Handler](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEMarginProgrammatic/CSharp/default.xaml.cs#handler)]
 [!code-vb[FEMarginProgrammatic#Handler](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/FEMarginProgrammatic/VisualBasic/default.xaml.vb#handler)]
