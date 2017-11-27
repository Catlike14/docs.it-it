---
title: 'Procedura: impostare il titolo di una finestra da una pagina'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- windows [WPF], setting title from a page
- title of window [WPF], setting from a page
- pages [WPF], setting window title from
ms.assetid: fecf0d19-3eb6-4f8c-a44f-ff1b6f2b34b3
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 412771e3f43bc3755bdf9236743310ac8060165c
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2017
---
# <a name="how-to-set-the-title-of-a-window-from-a-page"></a><span data-ttu-id="5bf67-102">Procedura: impostare il titolo di una finestra da una pagina</span><span class="sxs-lookup"><span data-stu-id="5bf67-102">How to: Set the Title of a Window from a Page</span></span>
<span data-ttu-id="5bf67-103">In questo esempio viene illustrato come impostare il titolo della finestra in cui un <xref:System.Windows.Controls.Page> è ospitato.</span><span class="sxs-lookup"><span data-stu-id="5bf67-103">This example shows how to set the title of the window in which a <xref:System.Windows.Controls.Page> is hosted.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bf67-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="5bf67-104">Example</span></span>  
 <span data-ttu-id="5bf67-105">Una pagina è possibile modificare il titolo della finestra che la ospita impostando il <xref:System.Windows.Controls.Page.WindowTitle%2A> proprietà, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5bf67-105">A page can change the title of the window that is hosting it by setting the <xref:System.Windows.Controls.Page.WindowTitle%2A> property, like so:</span></span>  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowTitleXAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowTitlePage.xaml#setpagewindowtitlexaml)]  
  
> [!NOTE]
>  <span data-ttu-id="5bf67-106">L'impostazione di <xref:System.Windows.Controls.Page.Title%2A> non modifica il valore del titolo della finestra proprietà di una pagina.</span><span class="sxs-lookup"><span data-stu-id="5bf67-106">Setting the <xref:System.Windows.Controls.Page.Title%2A> property of a page does not change the value of the window title.</span></span> <span data-ttu-id="5bf67-107">In alternativa, <xref:System.Windows.Controls.Page.Title%2A> specifica il nome di una voce di pagina nella cronologia di navigazione.</span><span class="sxs-lookup"><span data-stu-id="5bf67-107">Instead, <xref:System.Windows.Controls.Page.Title%2A> specifies the name of a page entry in navigation history.</span></span>
