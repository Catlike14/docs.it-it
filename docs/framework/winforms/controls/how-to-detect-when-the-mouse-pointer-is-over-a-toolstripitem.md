---
title: 'Procedura: rilevare quando il puntatore del mouse si trova sopra un ToolStripItem'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], detecting mouse movement
- ToolStrip control [Windows Forms], detecting mouse movement
- ToolStripItem class [Windows Forms], detecting mouse movement
- mouse [Windows Forms], detecting movement on toolbars
ms.assetid: d38b5082-aba7-4f6c-841b-bd9714e307fd
ms.openlocfilehash: 15a7562efd9a86a029754610ffd9e77c372d1ac2
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33530497"
---
# <a name="how-to-detect-when-the-mouse-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="3fba5-102">Procedura: rilevare quando il puntatore del mouse si trova sopra un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="3fba5-102">How to: Detect When the Mouse Pointer Is Over a ToolStripItem</span></span>
<span data-ttu-id="3fba5-103">Utilizzare la procedura seguente per rilevare quando il puntatore del mouse si trova su un <xref:System.Windows.Forms.ToolStripItem>.</span><span class="sxs-lookup"><span data-stu-id="3fba5-103">Use the following procedure to detect when the mouse pointer is over a <xref:System.Windows.Forms.ToolStripItem>.</span></span>  
  
### <a name="to-detect-when-the-pointer-is-over-a-toolstripitem"></a><span data-ttu-id="3fba5-104">Per rilevare quando il puntatore si trova sopra un ToolStripItem</span><span class="sxs-lookup"><span data-stu-id="3fba5-104">To detect when the pointer is over a ToolStripItem</span></span>  
  
-   <span data-ttu-id="3fba5-105">Utilizzare il <xref:System.Windows.Forms.ToolStripItem.Selected%2A> proprietà per gli elementi in cui <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> è `true`.</span><span class="sxs-lookup"><span data-stu-id="3fba5-105">Use the <xref:System.Windows.Forms.ToolStripItem.Selected%2A> property for items in which <xref:System.Windows.Forms.ToolStripItem.CanSelect%2A> is `true`.</span></span>  
  
     <span data-ttu-id="3fba5-106">Ciò impedirà la necessità di sincronizzare il <xref:System.Windows.Forms.ToolStripItem.MouseEnter> e <xref:System.Windows.Forms.ToolStripItem.MouseLeave> eventi.</span><span class="sxs-lookup"><span data-stu-id="3fba5-106">This will prevent you from having to synchronize the <xref:System.Windows.Forms.ToolStripItem.MouseEnter> and <xref:System.Windows.Forms.ToolStripItem.MouseLeave> events.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3fba5-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3fba5-107">See Also</span></span>  
 <xref:System.Windows.Forms.ToolStripItem>  
 <xref:System.Windows.Forms.ToolStripItem.Selected%2A>  
 [<span data-ttu-id="3fba5-108">Panoramica sul controllo ToolStrip</span><span class="sxs-lookup"><span data-stu-id="3fba5-108">ToolStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/toolstrip-control-overview-windows-forms.md)
