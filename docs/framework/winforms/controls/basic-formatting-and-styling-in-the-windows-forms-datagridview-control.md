---
title: Formattazione e stile di base nel controllo DataGridView Windows Form
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting and styling
- data grids [Windows Forms], formatting
ms.assetid: b9b90836-1f56-4aa9-8db8-edc78fe830e8
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 1c6ae9c4159f8f9eafd73608e4fc3f4a646c1eaa
ms.sourcegitcommit: c2e216692ef7576a213ae16af2377cd98d1a67fa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/22/2017
---
# <a name="basic-formatting-and-styling-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="7161b-102">Formattazione e stile di base nel controllo DataGridView Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-102">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="7161b-103">Il `DataGridView` controllo rende più semplice definire l'aspetto delle celle di base e la formattazione di valori di cella.</span><span class="sxs-lookup"><span data-stu-id="7161b-103">The `DataGridView` control makes it easy to define the basic appearance of cells and the display formatting of cell values.</span></span> <span data-ttu-id="7161b-104">È possibile definire l'aspetto e la formattazione di stili per le singole celle, per le celle in colonne e righe specifiche o per tutte le celle nel controllo impostando le proprietà del `DataGridViewCellStyle` accessibili tramite diversi oggetti `DataGridView` le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="7161b-104">You can define appearance and formatting styles for individual cells, for cells in specific columns and rows, or for all cells in the control by setting the properties of the `DataGridViewCellStyle` objects accessed through various `DataGridView` control properties.</span></span> <span data-ttu-id="7161b-105">Inoltre, è possibile modificare gli stili in modo dinamico in base a fattori, ad esempio il valore di cella gestendo il `CellFormatting` evento.</span><span class="sxs-lookup"><span data-stu-id="7161b-105">Additionally, you can modify these styles dynamically based on factors such as the cell value by handling the `CellFormatting` event.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7161b-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7161b-106">In This Section</span></span>  
 [<span data-ttu-id="7161b-107">Procedura: Modificare gli stili dei bordi e delle linee della griglia nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-107">How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/change-the-border-and-gridline-styles-in-the-datagrid.md)  
 <span data-ttu-id="7161b-108">Viene descritto come impostare `DataGridView` le proprietà che definiscono l'aspetto del bordo del controllo e linee di separazione tra le celle.</span><span class="sxs-lookup"><span data-stu-id="7161b-108">Describes how to set `DataGridView` properties that define the appearance of the control border and the boundary lines between cells.</span></span>  
  
 [<span data-ttu-id="7161b-109">Stili delle celle nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-109">Cell Styles in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/cell-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-110">Viene descritto il `DataGridViewCellStyle` classe e l'interagiscono tra le proprietà di tale tipo per definire la modalità di visualizzazione delle celle nel controllo.</span><span class="sxs-lookup"><span data-stu-id="7161b-110">Describes the `DataGridViewCellStyle` class and how properties of that type interact to define how cells are displayed in the control.</span></span>  
  
 [<span data-ttu-id="7161b-111">Procedura: Impostare stili di cella predefiniti per il controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-111">How to: Set Default Cell Styles for the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-112">Viene descritto come utilizzare `DataGridViewCellStyle` proprietà per definire l'aspetto predefinito di celle, righe e colonne specifiche in tutto il controllo.</span><span class="sxs-lookup"><span data-stu-id="7161b-112">Describes how to use `DataGridViewCellStyle` properties to define the default appearance of cells in specific rows and columns and in the entire control.</span></span>  
  
 [<span data-ttu-id="7161b-113">Procedura: Formattare i dati nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-113">How to: Format Data in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-format-data-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-114">Viene descritto come formattare i valori visualizzati nelle celle utilizzando `DataGridViewCellStyle` proprietà.</span><span class="sxs-lookup"><span data-stu-id="7161b-114">Describes how to format cell display values using `DataGridViewCellStyle` properties.</span></span>  
  
 [<span data-ttu-id="7161b-115">Procedura: Impostare gli stili di carattere e colore nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-115">How to: Set Font and Color Styles in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-font-and-color-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-116">Viene descritto come utilizzare il `DefaultCellStyle` proprietà da impostare base visualizzare caratteristiche per tutte le celle nel controllo.</span><span class="sxs-lookup"><span data-stu-id="7161b-116">Describes how to use the `DefaultCellStyle` property to set basic display characteristics for all cells in the control.</span></span>  
  
 [<span data-ttu-id="7161b-117">Procedura: Impostare stili di righe alterne per il controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-117">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-118">Viene descritto come creare un effetto registro nel controllo con righe alterne che vengono visualizzate in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="7161b-118">Describes how to create a ledger-like effect in the control using alternating rows that are displayed differently.</span></span>  
  
 [<span data-ttu-id="7161b-119">Procedura: Usare il modello di riga per personalizzare le righe nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-119">How to: Use the Row Template to Customize Rows in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/use-the-row-template-to-customize-rows-in-the-datagrid.md)  
 <span data-ttu-id="7161b-120">Viene descritto come utilizzare il `RowTemplate` proprietà per impostare le proprietà di riga che verranno utilizzate per tutte le righe nel controllo.</span><span class="sxs-lookup"><span data-stu-id="7161b-120">Describes how to use the `RowTemplate` property to set row properties that will be used for all rows in the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="7161b-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7161b-121">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="7161b-122">Fornisce la documentazione di riferimento per il controllo <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="7161b-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewCellStyle>  
 <span data-ttu-id="7161b-123">Fornisce la documentazione di riferimento per la <xref:System.Windows.Forms.DataGridViewCellStyle> classe.</span><span class="sxs-lookup"><span data-stu-id="7161b-123">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewCellStyle> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.CellFormatting>  
 <span data-ttu-id="7161b-124">Fornisce la documentazione di riferimento per il <xref:System.Windows.Forms.DataGridView.CellFormatting> evento.</span><span class="sxs-lookup"><span data-stu-id="7161b-124">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.CellFormatting> event.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.RowTemplate%2A>  
 <span data-ttu-id="7161b-125">Fornisce la documentazione di riferimento per la <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> proprietà.</span><span class="sxs-lookup"><span data-stu-id="7161b-125">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="7161b-126">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="7161b-126">Related Sections</span></span>  
 [<span data-ttu-id="7161b-127">Personalizzazione del controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-127">Customizing the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/customizing-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7161b-128">Fornisce argomenti che descrivono come disegnare celle e righe personalizzate di <xref:System.Windows.Forms.DataGridView> e come creare tipi di cella, colonna e riga derivati.</span><span class="sxs-lookup"><span data-stu-id="7161b-128">Provides topics that describe custom painting <xref:System.Windows.Forms.DataGridView> cells and rows, and creating derived cell, column, and row types.</span></span>  
  
 [<span data-ttu-id="7161b-129">Funzionalità di base per colonna, riga e cella nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="7161b-129">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/basic-column-row-and-cell-features-wf-datagridview-control.md)  
 <span data-ttu-id="7161b-130">Fornisce argomenti che descrivono comunemente usate le proprietà di cella, riga e colonna.</span><span class="sxs-lookup"><span data-stu-id="7161b-130">Provides topics that describe commonly used cell, row, and column properties.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7161b-131">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7161b-131">See Also</span></span>  
 [<span data-ttu-id="7161b-132">Controllo DataGridView</span><span class="sxs-lookup"><span data-stu-id="7161b-132">DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)
