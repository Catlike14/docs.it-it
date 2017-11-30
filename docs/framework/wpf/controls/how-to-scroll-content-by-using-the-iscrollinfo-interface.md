---
title: 'Procedura: scorrere il contenuto mediante l''interfaccia IScrollInfo'
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
- ScrollViewer control [WPF], scrolling content
- scrolling content [WPF]
- IScrollInfo interface [WPF]
ms.assetid: d8700bef-a3f8-4c12-9de2-fc3b79f32cd3
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 1895507c30ad5267d4c2b1afff3acf004e872d40
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-scroll-content-by-using-the-iscrollinfo-interface"></a><span data-ttu-id="fb6b5-102">Procedura: scorrere il contenuto mediante l'interfaccia IScrollInfo</span><span class="sxs-lookup"><span data-stu-id="fb6b5-102">How to: Scroll Content by Using the IScrollInfo Interface</span></span>
<span data-ttu-id="fb6b5-103">In questo esempio viene illustrato come scorrere il contenuto utilizzando il <xref:System.Windows.Controls.Primitives.IScrollInfo> interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-103">This example shows how to scroll content by using the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fb6b5-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="fb6b5-104">Example</span></span>  
 <span data-ttu-id="fb6b5-105">L'esempio seguente illustra le funzionalità del <xref:System.Windows.Controls.Primitives.IScrollInfo> interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-105">The following example demonstrates the features of the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface.</span></span> <span data-ttu-id="fb6b5-106">Nell'esempio viene creato un <xref:System.Windows.Controls.StackPanel> elemento [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] annidato in un elemento padre <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-106">The example creates a <xref:System.Windows.Controls.StackPanel> element in [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)] that is nested in a parent <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="fb6b5-107">Gli elementi figlio del <xref:System.Windows.Controls.StackPanel> è possibile scorrere in modo logico utilizzando i metodi definiti per il <xref:System.Windows.Controls.Primitives.IScrollInfo> interfaccia ed eseguire il cast all'istanza di <xref:System.Windows.Controls.StackPanel> (`sp1`) nel codice.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-107">The child elements of the <xref:System.Windows.Controls.StackPanel> can be scrolled logically by using the methods defined by the <xref:System.Windows.Controls.Primitives.IScrollInfo> interface and cast to the instance of <xref:System.Windows.Controls.StackPanel> (`sp1`) in code.</span></span>  
  
 [!code-xaml[IScrollInfoMethods#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="fb6b5-108">Ogni <xref:System.Windows.Controls.Button> nel [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] file attiva un metodo personalizzato associato che controlla il comportamento di scorrimento in <xref:System.Windows.Controls.StackPanel>.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-108">Each <xref:System.Windows.Controls.Button> in the [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] file triggers an associated custom method that controls scrolling behavior in <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="fb6b5-109">Nell'esempio seguente viene illustrato come utilizzare il <xref:System.Windows.Controls.Primitives.IScrollInfo.LineUp%2A> e <xref:System.Windows.Controls.Primitives.IScrollInfo.LineDown%2A> metodi; viene inoltre genericamente illustrato come utilizzare tutti i metodi di posizionamento che la <xref:System.Windows.Controls.Primitives.IScrollInfo> classe definisce.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-109">The following example shows how to use the <xref:System.Windows.Controls.Primitives.IScrollInfo.LineUp%2A> and <xref:System.Windows.Controls.Primitives.IScrollInfo.LineDown%2A> methods; it also generically shows how to use all the positioning methods that the <xref:System.Windows.Controls.Primitives.IScrollInfo> class defines.</span></span>  
  
 [!code-csharp[IScrollInfoMethods#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/IScrollInfoMethods/CSharp/Window1.xaml.cs#3)]
 [!code-vb[IScrollInfoMethods#3](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/IScrollInfoMethods/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="fb6b5-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fb6b5-110">See Also</span></span>  
 <xref:System.Windows.Controls.ScrollViewer>  
 <xref:System.Windows.Controls.Primitives.IScrollInfo>  
 <xref:System.Windows.Controls.StackPanel>  
 [<span data-ttu-id="fb6b5-111">Panoramica sull'elemento ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="fb6b5-111">ScrollViewer Overview</span></span>](../../../../docs/framework/wpf/controls/scrollviewer-overview.md)  
 [<span data-ttu-id="fb6b5-112">Procedure relative</span><span class="sxs-lookup"><span data-stu-id="fb6b5-112">How-to Topics</span></span>](../../../../docs/framework/wpf/controls/scrollviewer-how-to-topics.md)  
 [<span data-ttu-id="fb6b5-113">Cenni preliminari sugli elementi Panel</span><span class="sxs-lookup"><span data-stu-id="fb6b5-113">Panels Overview</span></span>](../../../../docs/framework/wpf/controls/panels-overview.md)
