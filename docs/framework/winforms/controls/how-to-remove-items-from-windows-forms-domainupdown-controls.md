---
title: 'Procedura: rimuovere elementi dai controlli DomainUpDown Windows Form'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DomainUpDown control [Windows Forms], removing items from
- spin button control [Windows Forms], removing items
ms.assetid: e70f5cbc-b497-41a9-975a-344c00e56ed2
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 17972aa9cb1626793ab04d317bb66d2774899cfc
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-remove-items-from-windows-forms-domainupdown-controls"></a><span data-ttu-id="8421a-102">Procedura: rimuovere elementi dai controlli DomainUpDown Windows Form</span><span class="sxs-lookup"><span data-stu-id="8421a-102">How to: Remove Items from Windows Forms DomainUpDown Controls</span></span>
<span data-ttu-id="8421a-103">È possibile rimuovere elementi da Windows Form <xref:System.Windows.Forms.DomainUpDown> controllo chiamando la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> o <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> metodo la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe.</span><span class="sxs-lookup"><span data-stu-id="8421a-103">You can remove items from the Windows Forms <xref:System.Windows.Forms.DomainUpDown> control by calling the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> or <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method of the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> class.</span></span> <span data-ttu-id="8421a-104">Il <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> metodo rimuove un elemento specifico, mentre il <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> metodo rimuove un elemento in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8421a-104">The <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> method removes a specific item, while the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method removes an item by its position.</span></span>  
  
### <a name="to-remove-an-item"></a><span data-ttu-id="8421a-105">Per rimuovere un elemento</span><span class="sxs-lookup"><span data-stu-id="8421a-105">To remove an item</span></span>  
  
-   <span data-ttu-id="8421a-106">Utilizzare il <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> metodo la <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> classe per rimuovere un elemento in base al nome.</span><span class="sxs-lookup"><span data-stu-id="8421a-106">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A> method of the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection> class to remove an item by name.</span></span>  
  
    ```vb  
    DomainUpDown1.Items.Remove("noodles")  
    ```  
  
    ```csharp  
    domainUpDown1.Items.Remove("noodles");  
    ```  
  
    ```cpp  
    domainUpDown1->Items->Remove("noodles");  
    ```  
  
     <span data-ttu-id="8421a-107">oppure</span><span class="sxs-lookup"><span data-stu-id="8421a-107">-or-</span></span>  
  
-   <span data-ttu-id="8421a-108">Utilizzare il <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> metodo per rimuovere un elemento in base alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8421a-108">Use the <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A> method to remove an item by its position.</span></span>  
  
    ```vb  
    ' Removes the first item in the list.  
    DomainUpDown1.Items.RemoveAt(0)  
    ```  
  
    ```csharp  
    // Removes the first item in the list.  
    domainUpDown1.Items.RemoveAt(0);  
    ```  
  
    ```cpp  
    // Removes the first item in the list.  
    domainUpDown1->Items->RemoveAt(0);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="8421a-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8421a-109">See Also</span></span>  
 <xref:System.Windows.Forms.DomainUpDown>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.Remove%2A?displayProperty=nameWithType>  
 <xref:System.Windows.Forms.DomainUpDown.DomainUpDownItemCollection.RemoveAt%2A?displayProperty=nameWithType>  
 [<span data-ttu-id="8421a-110">Controllo DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="8421a-110">DomainUpDown Control</span></span>](../../../../docs/framework/winforms/controls/domainupdown-control-windows-forms.md)  
 [<span data-ttu-id="8421a-111">Panoramica sul controllo DomainUpDown</span><span class="sxs-lookup"><span data-stu-id="8421a-111">DomainUpDown Control Overview</span></span>](../../../../docs/framework/winforms/controls/domainupdown-control-overview-windows-forms.md)
