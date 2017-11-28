---
title: 'Procedura: posizionare un menu di scelta rapida personalizzato in un controllo RichTextBox'
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
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 1c0a4fd8d2df15dcca2d9d1751f3089922d9a5ad
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a><span data-ttu-id="6a353-102">Procedura: posizionare un menu di scelta rapida personalizzato in un controllo RichTextBox</span><span class="sxs-lookup"><span data-stu-id="6a353-102">How to: Position a Custom Context Menu in a RichTextBox</span></span>
<span data-ttu-id="6a353-103">In questo esempio viene descritto come posizionare un menu di scelta rapida personalizzato per un <xref:System.Windows.Controls.RichTextBox>.</span><span class="sxs-lookup"><span data-stu-id="6a353-103">This example shows how to position a custom context menu for a <xref:System.Windows.Controls.RichTextBox>.</span></span>  
  
 <span data-ttu-id="6a353-104">Quando si implementa un menu contestuale personalizzato per un oggetto **RichTextBox**, si è responsabili della gestione del posizionamento del menu contestuale.</span><span class="sxs-lookup"><span data-stu-id="6a353-104">When you implement a custom context menu for a **RichTextBox**, you are responsible for handling the placement of the context menu.</span></span>  <span data-ttu-id="6a353-105">Per impostazione predefinita, un menu contestuale personalizzato si apre al centro dell'oggetto **RichTextBox**.</span><span class="sxs-lookup"><span data-stu-id="6a353-105">By default, a custom context menu is opened at the center of the **RichTextBox**.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6a353-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a353-106">Example</span></span>  
 <span data-ttu-id="6a353-107">Per eseguire l'override del comportamento di selezione host predefinito, aggiungere un listener per il <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> evento.</span><span class="sxs-lookup"><span data-stu-id="6a353-107">To override the default placement behavior, add a listener for the <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> event.</span></span>  <span data-ttu-id="6a353-108">L'esempio seguente illustra come eseguire questa operazione a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="6a353-108">The following example shows how to do this programmatically.</span></span>  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a><span data-ttu-id="6a353-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="6a353-109">Example</span></span>  
 <span data-ttu-id="6a353-110">Nell'esempio seguente viene illustrata un'implementazione corrispondente <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> listener di eventi.</span><span class="sxs-lookup"><span data-stu-id="6a353-110">The following example shows an implementation the corresponding <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> event listener.</span></span>  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](../../../../samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a><span data-ttu-id="6a353-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="6a353-111">See Also</span></span>  
 [<span data-ttu-id="6a353-112">Cenni preliminari sul controllo RichTextBox</span><span class="sxs-lookup"><span data-stu-id="6a353-112">RichTextBox Overview</span></span>](../../../../docs/framework/wpf/controls/richtextbox-overview.md)  
 [<span data-ttu-id="6a353-113">Cenni preliminari sulla classe TextBox</span><span class="sxs-lookup"><span data-stu-id="6a353-113">TextBox Overview</span></span>](../../../../docs/framework/wpf/controls/textbox-overview.md)
