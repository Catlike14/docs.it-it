---
title: "Proprietà dei controlli Windows Form"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
caps.latest.revision: "11"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 8d645a321319bf54ca0cc4f142c343420eb1f30e
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="properties-in-windows-forms-controls"></a><span data-ttu-id="033ad-102">Proprietà dei controlli Windows Form</span><span class="sxs-lookup"><span data-stu-id="033ad-102">Properties in Windows Forms Controls</span></span>
<span data-ttu-id="033ad-103">Un controllo Windows Form eredita molte proprietà della classe base <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="033ad-103">A Windows Forms control inherits many properties form the base class <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="033ad-104">Queste sono incluse proprietà, ad esempio <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>e molti altri.</span><span class="sxs-lookup"><span data-stu-id="033ad-104">These include properties such as <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>, and many others.</span></span> <span data-ttu-id="033ad-105">Per informazioni dettagliate sulle proprietà ereditate, vedere <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="033ad-105">For details about inherited properties, see <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="033ad-106">È possibile eseguire l'override delle proprietà ereditate dal controllo nonché definirne di nuove.</span><span class="sxs-lookup"><span data-stu-id="033ad-106">You can override inherited properties in your control as well as define new properties.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="033ad-107">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="033ad-107">In This Section</span></span>  
 [<span data-ttu-id="033ad-108">Definizione di una proprietà</span><span class="sxs-lookup"><span data-stu-id="033ad-108">Defining a Property</span></span>](../../../../docs/framework/winforms/controls/defining-a-property-in-windows-forms-controls.md)  
 <span data-ttu-id="033ad-109">Viene illustrato come implementare una proprietà per un controllo o un componente personalizzato e come integrare la proprietà nell'ambiente di progettazione.</span><span class="sxs-lookup"><span data-stu-id="033ad-109">Shows how to implement a property for a custom control or component and shows how to integrate the property into the design environment.</span></span>  
  
 [<span data-ttu-id="033ad-110">Definizione dei valori predefiniti utilizzando i metodi ShouldSerialize e Reset</span><span class="sxs-lookup"><span data-stu-id="033ad-110">Defining Default Values with the ShouldSerialize and Reset Methods</span></span>](../../../../docs/framework/winforms/controls/defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 <span data-ttu-id="033ad-111">Viene illustrato come definire valori di proprietà predefiniti per un controllo o un componente personalizzato.</span><span class="sxs-lookup"><span data-stu-id="033ad-111">Shows how to define default property values for a custom control or component.</span></span>  
  
 [<span data-ttu-id="033ad-112">Eventi di modifica delle proprietà</span><span class="sxs-lookup"><span data-stu-id="033ad-112">Property-Changed Events</span></span>](../../../../docs/framework/winforms/controls/property-changed-events.md)  
 <span data-ttu-id="033ad-113">Viene descritto come attivare le notifiche di modifiche alle proprietà quando un valore di una proprietà viene modificato.</span><span class="sxs-lookup"><span data-stu-id="033ad-113">Describes how to enable property-change notifications when a property value changes.</span></span>  
  
 [<span data-ttu-id="033ad-114">Procedura: esporre le proprietà dei controlli costitutivi</span><span class="sxs-lookup"><span data-stu-id="033ad-114">How to: Expose Properties of Constituent Controls</span></span>](../../../../docs/framework/winforms/controls/how-to-expose-properties-of-constituent-controls.md)  
 <span data-ttu-id="033ad-115">Viene illustrato come esporre le proprietà dei controlli che fanno parte di un controllo composito personalizzato.</span><span class="sxs-lookup"><span data-stu-id="033ad-115">Shows how to expose properties of constituent controls in a custom composite control.</span></span>  
  
 [<span data-ttu-id="033ad-116">Implementazione dei metodi nei controlli personalizzati</span><span class="sxs-lookup"><span data-stu-id="033ad-116">Method Implementation in Custom Controls</span></span>](../../../../docs/framework/winforms/controls/method-implementation-in-custom-controls.md)  
 <span data-ttu-id="033ad-117">Viene descritto come implementare metodi nei controlli e nei componenti personalizzati.</span><span class="sxs-lookup"><span data-stu-id="033ad-117">Describes how to implement methods in custom controls and components.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="033ad-118">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="033ad-118">Reference</span></span>  
 <xref:System.Windows.Forms.UserControl>  
 <span data-ttu-id="033ad-119">Viene descritta la classe base per l'implementazione dei controlli compositi.</span><span class="sxs-lookup"><span data-stu-id="033ad-119">Documents the base class for implementing composite controls.</span></span>  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 <span data-ttu-id="033ad-120">Viene descritto l'attributo che specifica il <xref:System.ComponentModel.TypeConverter> da usare per un tipo di proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="033ad-120">Documents the attribute that specifies the <xref:System.ComponentModel.TypeConverter> to use for a custom property type.</span></span>  
  
 <xref:System.ComponentModel.EditorAttribute>  
 <span data-ttu-id="033ad-121">Viene descritto l'attributo che specifica il <xref:System.Drawing.Design.UITypeEditor> da utilizzare per una proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="033ad-121">Documents the attribute that specifies the <xref:System.Drawing.Design.UITypeEditor> to use for a custom property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="033ad-122">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="033ad-122">Related Sections</span></span>  
 [<span data-ttu-id="033ad-123">Attributi nei controlli Windows Forms</span><span class="sxs-lookup"><span data-stu-id="033ad-123">Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/attributes-in-windows-forms-controls.md)  
 <span data-ttu-id="033ad-124">Descrive gli attributi che è possibile applicare alle proprietà o ad altri membri e componenti dei controlli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="033ad-124">Describes the attributes you can apply to properties or other members of your custom controls and components.</span></span>  
  
 [<span data-ttu-id="033ad-125">Attributi per componenti in fase di progettazione</span><span class="sxs-lookup"><span data-stu-id="033ad-125">Design-Time Attributes for Components</span></span>](http://msdn.microsoft.com/library/12050fe3-9327-4509-9e21-4ee2494b95c3)  
 <span data-ttu-id="033ad-126">Elenca gli attributi dei metadati da applicare ai componenti e ai controlli in modo che vengano visualizzati correttamente in fase di progettazione nelle finestre di progettazione visiva.</span><span class="sxs-lookup"><span data-stu-id="033ad-126">Lists metadata attributes to apply to components and controls so that they are displayed correctly at design time in visual designers.</span></span>  
  
 [<span data-ttu-id="033ad-127">Estensione del supporto in fase di progettazione</span><span class="sxs-lookup"><span data-stu-id="033ad-127">Extending Design-Time Support</span></span>](http://msdn.microsoft.com/library/d6ac8a6a-42fd-4bc8-bf33-b212811297e2)  
 <span data-ttu-id="033ad-128">Descrive come implementare classi, quali editor e finestre di progettazione, che forniscono supporto in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="033ad-128">Describes how to implement classes such as editors and designers that provide design-time support.</span></span>
