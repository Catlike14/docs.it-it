---
title: Stili e modelli di ScrollViewer
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ScrollViewer
- states [WPF], ScrollViewer
- styles [WPF], ScrollViewer
- templates [WPF], ScrollViewer
- ControlTemplate [WPF], ScrollViewer
- ScrollViewer [WPF], styles and templates
ms.assetid: dffdd822-ae69-4946-abaf-710860cd65b2
ms.openlocfilehash: 5ad3738972ae9b33764d3b710077f6d4a0526a13
ms.sourcegitcommit: 43924acbdbb3981d103e11049bbe460457d42073
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="scrollviewer-styles-and-templates"></a><span data-ttu-id="59b07-102">Stili e modelli di ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="59b07-102">ScrollViewer Styles and Templates</span></span>
<span data-ttu-id="59b07-103">In questo argomento vengono descritti gli stili e modelli per il <xref:System.Windows.Controls.ScrollViewer> controllo.</span><span class="sxs-lookup"><span data-stu-id="59b07-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span> <span data-ttu-id="59b07-104">È possibile modificare il valore predefinito <xref:System.Windows.Controls.ControlTemplate> per fornire al controllo un aspetto univoco.</span><span class="sxs-lookup"><span data-stu-id="59b07-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="59b07-105">Per altre informazioni, vedere [Personalizzazione dell'aspetto di un controllo esistente mediante la creazione di un oggetto ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span><span class="sxs-lookup"><span data-stu-id="59b07-105">For more information, see [Customizing the Appearance of an Existing Control by Creating a ControlTemplate](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md).</span></span>  
  
## <a name="scrollviewer-parts"></a><span data-ttu-id="59b07-106">Parti del controllo ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="59b07-106">ScrollViewer Parts</span></span>  
 <span data-ttu-id="59b07-107">La tabella seguente elenca le parti denominate la <xref:System.Windows.Controls.ScrollViewer> controllo.</span><span class="sxs-lookup"><span data-stu-id="59b07-107">The following table lists the named parts for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="59b07-108">Parte</span><span class="sxs-lookup"><span data-stu-id="59b07-108">Part</span></span>|<span data-ttu-id="59b07-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="59b07-109">Type</span></span>|<span data-ttu-id="59b07-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b07-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="59b07-111">PART_ScrollContentPresenter</span><span class="sxs-lookup"><span data-stu-id="59b07-111">PART_ScrollContentPresenter</span></span>|<xref:System.Windows.Controls.ScrollContentPresenter>|<span data-ttu-id="59b07-112">Il segnaposto di contenuto di <xref:System.Windows.Controls.ScrollViewer>.</span><span class="sxs-lookup"><span data-stu-id="59b07-112">The placeholder for content in the <xref:System.Windows.Controls.ScrollViewer>.</span></span>|  
|<span data-ttu-id="59b07-113">PART_HorizontalScrollBar</span><span class="sxs-lookup"><span data-stu-id="59b07-113">PART_HorizontalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="59b07-114">Il <xref:System.Windows.Controls.Primitives.ScrollBar> consente di scorrere orizzontalmente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="59b07-114">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content horizontally.</span></span>|  
|<span data-ttu-id="59b07-115">PART_VerticalScrollBar</span><span class="sxs-lookup"><span data-stu-id="59b07-115">PART_VerticalScrollBar</span></span>|<xref:System.Windows.Controls.Primitives.ScrollBar>|<span data-ttu-id="59b07-116">Il <xref:System.Windows.Controls.Primitives.ScrollBar> consente di scorrere verticalmente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="59b07-116">The <xref:System.Windows.Controls.Primitives.ScrollBar> used to scroll the content vertically.</span></span>|  
  
## <a name="scrollviewer-states"></a><span data-ttu-id="59b07-117">Stati del controllo ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="59b07-117">ScrollViewer States</span></span>  
 <span data-ttu-id="59b07-118">Nella tabella seguente sono elencati gli stati visivi per la <xref:System.Windows.Controls.ScrollViewer> controllo.</span><span class="sxs-lookup"><span data-stu-id="59b07-118">The following table lists the visual states for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
|<span data-ttu-id="59b07-119">Nome VisualState</span><span class="sxs-lookup"><span data-stu-id="59b07-119">VisualState Name</span></span>|<span data-ttu-id="59b07-120">Nome VisualStateGroup</span><span class="sxs-lookup"><span data-stu-id="59b07-120">VisualStateGroup Name</span></span>|<span data-ttu-id="59b07-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b07-121">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="59b07-122">Valido</span><span class="sxs-lookup"><span data-stu-id="59b07-122">Valid</span></span>|<span data-ttu-id="59b07-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="59b07-123">ValidationStates</span></span>|<span data-ttu-id="59b07-124">Il controllo Usa il <xref:System.Windows.Controls.Validation> classe e <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> proprietà associata è `false`.</span><span class="sxs-lookup"><span data-stu-id="59b07-124">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="59b07-125">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="59b07-125">InvalidFocused</span></span>|<span data-ttu-id="59b07-126">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="59b07-126">ValidationStates</span></span>|<span data-ttu-id="59b07-127">Il <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> proprietà associata è `true` ha il controllo ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="59b07-127">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="59b07-128">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="59b07-128">InvalidUnfocused</span></span>|<span data-ttu-id="59b07-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="59b07-129">ValidationStates</span></span>|<span data-ttu-id="59b07-130">Il <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> proprietà associata è `true` ha il controllo non è attivo.</span><span class="sxs-lookup"><span data-stu-id="59b07-130">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="scrollviewer-controltemplate-example"></a><span data-ttu-id="59b07-131">Esempio di ControlTemplate del controllo ScrollViewer</span><span class="sxs-lookup"><span data-stu-id="59b07-131">ScrollViewer ControlTemplate Example</span></span>  
 <span data-ttu-id="59b07-132">Nell'esempio seguente viene illustrato come definire un <xref:System.Windows.Controls.ControlTemplate> per il <xref:System.Windows.Controls.ScrollViewer> controllo.</span><span class="sxs-lookup"><span data-stu-id="59b07-132">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ScrollViewer> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ScrollViewer](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollviewer.xaml#scrollviewer)]  
  
 <span data-ttu-id="59b07-133">L'esempio precedente usa una o più delle seguenti risorse.</span><span class="sxs-lookup"><span data-stu-id="59b07-133">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="59b07-134">Per l'esempio completo, vedere [Esempio di applicazione di stili con ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="59b07-134">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="59b07-135">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="59b07-135">See Also</span></span>  
 <xref:System.Windows.FrameworkElement.Style%2A>  
 <xref:System.Windows.Controls.ControlTemplate>  
 [<span data-ttu-id="59b07-136">Stili e modelli di Control</span><span class="sxs-lookup"><span data-stu-id="59b07-136">Control Styles and Templates</span></span>](../../../../docs/framework/wpf/controls/control-styles-and-templates.md)  
 [<span data-ttu-id="59b07-137">Personalizzazione dei controlli</span><span class="sxs-lookup"><span data-stu-id="59b07-137">Control Customization</span></span>](../../../../docs/framework/wpf/controls/control-customization.md)  
 [<span data-ttu-id="59b07-138">Applicazione di stili e modelli</span><span class="sxs-lookup"><span data-stu-id="59b07-138">Styling and Templating</span></span>](../../../../docs/framework/wpf/controls/styling-and-templating.md)  
 [<span data-ttu-id="59b07-139">Personalizzazione dell'aspetto di un controllo esistente mediante la creazione di un oggetto ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="59b07-139">Customizing the Appearance of an Existing Control by Creating a ControlTemplate</span></span>](../../../../docs/framework/wpf/controls/customizing-the-appearance-of-an-existing-control.md)
