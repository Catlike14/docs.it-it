---
title: 'Procedura dettagliata: hosting di controlli Windows Form in WPF tramite XAML'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: hosting Windows Forms control in WPF [WPF]
ms.assetid: 1aef42cb-4cfb-44b4-9a7a-c02632d3d9c7
caps.latest.revision: "34"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 5fe01b4ef9aebe697138e925935b73bd4770e86a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="walkthrough-hosting-a-windows-forms-control-in-wpf-by-using-xaml"></a><span data-ttu-id="210cc-102">Procedura dettagliata: hosting di controlli Windows Form in WPF tramite XAML</span><span class="sxs-lookup"><span data-stu-id="210cc-102">Walkthrough: Hosting a Windows Forms Control in WPF by Using XAML</span></span>
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]<span data-ttu-id="210cc-103"> offre numerosi controlli con un insieme di funzionalità completo.</span><span class="sxs-lookup"><span data-stu-id="210cc-103"> provides many controls with a rich feature set.</span></span> <span data-ttu-id="210cc-104">Tuttavia, può talvolta si desidera utilizzare [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] ai controlli del [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pagine.</span><span class="sxs-lookup"><span data-stu-id="210cc-104">However, you may sometimes want to use [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls on your [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pages.</span></span> <span data-ttu-id="210cc-105">Ad esempio, è possibile un investimento sostanziale esistente [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controlli o si può disporre di un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controllo che fornisce funzionalità univoche.</span><span class="sxs-lookup"><span data-stu-id="210cc-105">For example, you may have a substantial investment in existing [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] controls, or you may have a [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] control that provides unique functionality.</span></span>  
  
 <span data-ttu-id="210cc-106">Questa procedura dettagliata viene illustrato come ospitare un controllo Windows Form <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control per un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] pagina tramite [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span><span class="sxs-lookup"><span data-stu-id="210cc-106">This walkthrough shows you how to host a Windows Forms <xref:System.Windows.Forms.MaskedTextBox?displayProperty=nameWithType> control on a [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page by using [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)].</span></span>  
  
 <span data-ttu-id="210cc-107">Per un elenco di codice completo delle attività illustrate in questa procedura dettagliata, vedere [ospita un controllo Windows Form in WPF by Using XAML Sample](http://go.microsoft.com/fwlink/?LinkID=160000).</span><span class="sxs-lookup"><span data-stu-id="210cc-107">For a complete code listing of the tasks shown in this walkthrough, see [Hosting a Windows Forms Control in WPF by Using XAML Sample](http://go.microsoft.com/fwlink/?LinkID=160000).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="210cc-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="210cc-108">Prerequisites</span></span>  
 <span data-ttu-id="210cc-109">Per completare la procedura dettagliata, è necessario disporre dei componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="210cc-109">You need the following components to complete this walkthrough:</span></span>  
  
-   [!INCLUDE[vs_dev10_long](../../../../includes/vs-dev10-long-md.md)]<span data-ttu-id="210cc-110">.</span><span class="sxs-lookup"><span data-stu-id="210cc-110">.</span></span>  
  
## <a name="hosting-the-windows-forms-control"></a><span data-ttu-id="210cc-111">Hosting del controllo Windows Forms</span><span class="sxs-lookup"><span data-stu-id="210cc-111">Hosting the Windows Forms Control</span></span>  
  
#### <a name="to-host-the-maskedtextbox-control"></a><span data-ttu-id="210cc-112">Per ospitare il controllo MaskedTextBox</span><span class="sxs-lookup"><span data-stu-id="210cc-112">To host the MaskedTextBox control</span></span>  
  
1.  <span data-ttu-id="210cc-113">Creare un progetto di applicazione WPF denominato `HostingWfInWpfWithXaml`.</span><span class="sxs-lookup"><span data-stu-id="210cc-113">Create a WPF Application project named `HostingWfInWpfWithXaml`.</span></span>  
  
2.  <span data-ttu-id="210cc-114">Aggiungere riferimenti agli assembly indicati di seguito.</span><span class="sxs-lookup"><span data-stu-id="210cc-114">Add references to the following assemblies.</span></span>  
  
    -   <span data-ttu-id="210cc-115">WindowsFormsIntegration</span><span class="sxs-lookup"><span data-stu-id="210cc-115">WindowsFormsIntegration</span></span>  
  
    -   <span data-ttu-id="210cc-116">System.Windows.Forms</span><span class="sxs-lookup"><span data-stu-id="210cc-116">System.Windows.Forms</span></span>  
  
3.  <span data-ttu-id="210cc-117">Aprire MainWindow. XAML nel [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="210cc-117">Open MainWindow.xaml in the [!INCLUDE[wpfdesigner_current_short](../../../../includes/wpfdesigner-current-short-md.md)].</span></span>  
  
4.  <span data-ttu-id="210cc-118">Nel <xref:System.Windows.Window> elemento, aggiungere il seguente mapping dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="210cc-118">In the <xref:System.Windows.Window> element, add the following namespace mapping.</span></span> <span data-ttu-id="210cc-119">Il `wf` mapping dello spazio dei nomi stabilisce un riferimento all'assembly che contiene il [!INCLUDE[TLA2#tla_winforms](../../../../includes/tla2sharptla-winforms-md.md)] controllo.</span><span class="sxs-lookup"><span data-stu-id="210cc-119">The `wf` namespace mapping establishes a reference to the assembly that contains the [!INCLUDE[TLA2#tla_winforms](../../../../includes/tla2sharptla-winforms-md.md)] control.</span></span>  
  
    ```xaml  
    xmlns:wf="clr-namespace:System.Windows.Forms;assembly=System.Windows.Forms"  
    ```  
  
5.  <span data-ttu-id="210cc-120">Nel <xref:System.Windows.Controls.Grid> elemento aggiungere il codice XAML seguente.</span><span class="sxs-lookup"><span data-stu-id="210cc-120">In the <xref:System.Windows.Controls.Grid> element add the following XAML.</span></span>  
  
     <span data-ttu-id="210cc-121">Il <xref:System.Windows.Forms.MaskedTextBox> controllo viene creato come elemento figlio di <xref:System.Windows.Forms.Integration.WindowsFormsHost> controllo.</span><span class="sxs-lookup"><span data-stu-id="210cc-121">The <xref:System.Windows.Forms.MaskedTextBox> control is created as a child of the <xref:System.Windows.Forms.Integration.WindowsFormsHost> control.</span></span>  
  
     [!code-xaml[HostingWfInWpfWithXaml#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/HostingWfInWpfWithXaml/CSharp/HostingWfInWpf/Window1.xaml#3)]  
  
6.  <span data-ttu-id="210cc-122">Premere F5 per compilare ed eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="210cc-122">Press F5 to build and run the application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="210cc-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="210cc-123">See Also</span></span>  
 <xref:System.Windows.Forms.Integration.ElementHost>  
 <xref:System.Windows.Forms.Integration.WindowsFormsHost>  
 [<span data-ttu-id="210cc-124">WPF Designer</span><span class="sxs-lookup"><span data-stu-id="210cc-124">WPF Designer</span></span>](http://msdn.microsoft.com/en-us/c6c65214-8411-4e16-b254-163ed4099c26)  
 [<span data-ttu-id="210cc-125">Procedura dettagliata: hosting di controlli Windows Form in WPF</span><span class="sxs-lookup"><span data-stu-id="210cc-125">Walkthrough: Hosting a Windows Forms Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-control-in-wpf.md)  
 [<span data-ttu-id="210cc-126">Procedura dettagliata: Hosting di controlli Windows Form compositi in WPF</span><span class="sxs-lookup"><span data-stu-id="210cc-126">Walkthrough: Hosting a Windows Forms Composite Control in WPF</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)  
 [<span data-ttu-id="210cc-127">Procedura dettaglia: hosting di un controllo WPF composito in Windows Form</span><span class="sxs-lookup"><span data-stu-id="210cc-127">Walkthrough: Hosting a WPF Composite Control in Windows Forms</span></span>](../../../../docs/framework/wpf/advanced/walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)  
 [<span data-ttu-id="210cc-128">Controlli Windows Form e controlli WPF equivalenti</span><span class="sxs-lookup"><span data-stu-id="210cc-128">Windows Forms Controls and Equivalent WPF Controls</span></span>](../../../../docs/framework/wpf/advanced/windows-forms-controls-and-equivalent-wpf-controls.md)  
 [<span data-ttu-id="210cc-129">Hosting di un controllo Windows Form in WPF tramite XAML Sample</span><span class="sxs-lookup"><span data-stu-id="210cc-129">Hosting a Windows Forms Control in WPF by Using XAML Sample</span></span>](http://go.microsoft.com/fwlink/?LinkID=160000)
