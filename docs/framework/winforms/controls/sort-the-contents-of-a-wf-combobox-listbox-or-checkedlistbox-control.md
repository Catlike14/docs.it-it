---
title: 'Procedura: ordinare il contenuto di un controllo ComboBox, ListBox o CheckedListBox Windows Form'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- CheckedListBox control [Windows Forms], sorting
- ComboBox control [Windows Forms], sorting contents
- combo boxes [Windows Forms], sorting contents
- list boxes [Windows Forms], sorting contents
- ListBox control [Windows Forms], sorting contents
ms.assetid: c268e387-3d1d-4d86-a940-19f6673c8d06
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 4f266af44f954cb8416e1f7672f6642ab7c6995b
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-sort-the-contents-of-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="fab55-102">Procedura: ordinare il contenuto di un controllo ComboBox, ListBox o CheckedListBox Windows Form</span><span class="sxs-lookup"><span data-stu-id="fab55-102">How to: Sort the Contents of a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="fab55-103">Controlli Windows Form ordinamento non viene eseguito quando sono associati a dati.</span><span class="sxs-lookup"><span data-stu-id="fab55-103">Windows Forms controls do not sort when they are data-bound.</span></span> <span data-ttu-id="fab55-104">Per visualizzare i dati ordinati, utilizzare un'origine dati che supporta l'ordinamento e quindi chiedere l'origine dati di ordinamento.</span><span class="sxs-lookup"><span data-stu-id="fab55-104">To display sorted data, use a data source that supports sorting and then have the data source sort it.</span></span> <span data-ttu-id="fab55-105">Origini dati che supportano l'ordinamento sono viste di dati, gestori di visualizzazioni dati e matrici ordinate.</span><span class="sxs-lookup"><span data-stu-id="fab55-105">Data sources that support sorting are data views, data view managers, and sorted arrays.</span></span>  
  
 <span data-ttu-id="fab55-106">Se il controllo non è associato a dati, è possibile ordinarli.</span><span class="sxs-lookup"><span data-stu-id="fab55-106">If the control is not data-bound, you can sort it.</span></span>  
  
### <a name="to-sort-the-list"></a><span data-ttu-id="fab55-107">Per ordinare l'elenco</span><span class="sxs-lookup"><span data-stu-id="fab55-107">To sort the list</span></span>  
  
1.  <span data-ttu-id="fab55-108">Impostare la proprietà `Sorted` su `true`.</span><span class="sxs-lookup"><span data-stu-id="fab55-108">Set the `Sorted` property to `true`.</span></span>  
  
     <span data-ttu-id="fab55-109">Questa impostazione Riposiziona tutti gli elementi dell'elenco in base all'ordinamento.</span><span class="sxs-lookup"><span data-stu-id="fab55-109">This setting repositions all existing list items in sorted order.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fab55-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fab55-110">See Also</span></span>  
 <xref:System.Windows.Forms.ComboBox>  
 <xref:System.Windows.Forms.ListBox>  
 <xref:System.Windows.Forms.CheckedListBox>  
 [<span data-ttu-id="fab55-111">Data binding in Windows Form</span><span class="sxs-lookup"><span data-stu-id="fab55-111">Windows Forms Data Binding</span></span>](../../../../docs/framework/winforms/windows-forms-data-binding.md)  
 [<span data-ttu-id="fab55-112">Procedura: Aggiungere e rimuovere elementi da un controllo ComboBox, ListBox o CheckedListBox di Windows Form</span><span class="sxs-lookup"><span data-stu-id="fab55-112">How to: Add and Remove Items from a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>](../../../../docs/framework/winforms/controls/add-and-remove-items-from-a-wf-combobox.md)  
 [<span data-ttu-id="fab55-113">Quando usare un controllo ComboBox Windows Form anziché un controllo ListBox</span><span class="sxs-lookup"><span data-stu-id="fab55-113">When to Use a Windows Forms ComboBox Instead of a ListBox</span></span>](../../../../docs/framework/winforms/controls/when-to-use-a-windows-forms-combobox-instead-of-a-listbox.md)  
 [<span data-ttu-id="fab55-114">Controlli Windows Form usati per elencare opzioni</span><span class="sxs-lookup"><span data-stu-id="fab55-114">Windows Forms Controls Used to List Options</span></span>](../../../../docs/framework/winforms/controls/windows-forms-controls-used-to-list-options.md)
