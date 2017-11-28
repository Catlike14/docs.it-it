---
title: 'Procedura: disabilitare l''aggiunta e l''eliminazione di elementi DataRepeater (Visual Studio)'
ms.date: 07/20/2015
ms.prod: .net
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataRepeater, disabling delete
- DataRepeater, disabling add
ms.assetid: 298d8f60-ddfe-4361-ab66-cf76d0df5220
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 1b15fe6fb5190855126ffa60ac488aaa74ad9b5a
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-disable-adding-and-deleting-datarepeater-items-visual-studio"></a><span data-ttu-id="4b678-102">Procedura: disabilitare l'aggiunta e l'eliminazione di elementi DataRepeater (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="4b678-102">How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)</span></span>
<span data-ttu-id="4b678-103">Per impostazione predefinita, gli utenti possono aggiungere ed eliminare elementi in un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> controllo.</span><span class="sxs-lookup"><span data-stu-id="4b678-103">By default, users can add and delete items in a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span> <span data-ttu-id="4b678-104">Gli utenti possono aggiungere un nuovo elemento premendo CTRL + N quando un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> ha lo stato attivo o facendo clic di **AddNewItem** pulsante il <xref:System.Windows.Forms.BindingNavigator> controllo.</span><span class="sxs-lookup"><span data-stu-id="4b678-104">Users can add a new item by pressing CTRL+N when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **AddNewItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span> <span data-ttu-id="4b678-105">Gli utenti possono eliminare un elemento premendo CANC quando un <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> ha lo stato attivo o facendo clic di **DeleteItem** pulsante il <xref:System.Windows.Forms.BindingNavigator> controllo.</span><span class="sxs-lookup"><span data-stu-id="4b678-105">Users can delete an item by pressing DELETE when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem%2A> has focus or by clicking the **DeleteItem** button on the <xref:System.Windows.Forms.BindingNavigator> control.</span></span>  
  
 <span data-ttu-id="4b678-106">È possibile disabilitare l'aggiunta e/o l'eliminazione in fase di progettazione o in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b678-106">You can disable adding and/or deleting at design time or at run time.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-design-time"></a><span data-ttu-id="4b678-107">Per disabilitare l'aggiunta ed eliminazione in fase di progettazione</span><span class="sxs-lookup"><span data-stu-id="4b678-107">To disable adding and deleting at design time</span></span>  
  
1.  <span data-ttu-id="4b678-108">In Progettazione Windows Form, selezionare il <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> controllo.</span><span class="sxs-lookup"><span data-stu-id="4b678-108">In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> control.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="4b678-109">È necessario selezionare la sezione inferiore del controllo.</span><span class="sxs-lookup"><span data-stu-id="4b678-109">You must select the lower section of the control.</span></span> <span data-ttu-id="4b678-110">Se si seleziona l'area del modello di elemento, verrà visualizzato un set diverso di proprietà.</span><span class="sxs-lookup"><span data-stu-id="4b678-110">If you select the item template section, a different set of properties will be displayed.</span></span>  
  
2.  <span data-ttu-id="4b678-111">Nella finestra Proprietà impostare il <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A> proprietà **False**.</span><span class="sxs-lookup"><span data-stu-id="4b678-111">In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems%2A> property to **False**.</span></span>  
  
3.  <span data-ttu-id="4b678-112">Impostare il <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A> proprietà **False**.</span><span class="sxs-lookup"><span data-stu-id="4b678-112">Set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems%2A> property to **False**.</span></span>  
  
4.  <span data-ttu-id="4b678-113">In Progettazione Windows Form, selezionare il <xref:System.Windows.Forms.BindingNavigator> controllare e quindi scegliere il **AddNewItem** pulsante (il pulsante con un segno più).</span><span class="sxs-lookup"><span data-stu-id="4b678-113">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **AddNewItem** button (the button with a plus sign on it).</span></span>  
  
5.  <span data-ttu-id="4b678-114">Nella finestra Proprietà impostare il <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> proprietà **False**.</span><span class="sxs-lookup"><span data-stu-id="4b678-114">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
6.  <span data-ttu-id="4b678-115">In Progettazione Windows Form, selezionare il <xref:System.Windows.Forms.BindingNavigator> controllare e quindi scegliere il **DeleteItem** pulsante (il pulsante con una X rossa su di esso).</span><span class="sxs-lookup"><span data-stu-id="4b678-115">In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator> control, and then click the **DeleteItem** button (the button with a red X on it).</span></span>  
  
7.  <span data-ttu-id="4b678-116">Nella finestra Proprietà impostare il <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> proprietà **False**.</span><span class="sxs-lookup"><span data-stu-id="4b678-116">In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> property to **False**.</span></span>  
  
8.  <span data-ttu-id="4b678-117">Nella barra dei componenti, selezionare il <xref:System.Windows.Forms.BindingSource> a cui il <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> è associato.</span><span class="sxs-lookup"><span data-stu-id="4b678-117">In the Component Tray, select the <xref:System.Windows.Forms.BindingSource> to which the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater> is bound.</span></span>  
  
9. <span data-ttu-id="4b678-118">Nella finestra Proprietà impostare il <xref:System.Windows.Forms.BindingSource.AllowNew%2A> proprietà **False**.</span><span class="sxs-lookup"><span data-stu-id="4b678-118">In the Properties window, set the <xref:System.Windows.Forms.BindingSource.AllowNew%2A> property to **False**.</span></span>  
  
10. <span data-ttu-id="4b678-119">In Progettazione Windows Form, fare doppio clic su di **DeleteItem** pulsante per aprire l'Editor di codice.</span><span class="sxs-lookup"><span data-stu-id="4b678-119">In the Windows Forms Designer, double-click the **DeleteItem** button to open the Code Editor.</span></span>  
  
11. <span data-ttu-id="4b678-120">Nell'elenco a discesa degli eventi, selezionare il `BindingNavigatorDeleteItem_EnabledChanged` evento.</span><span class="sxs-lookup"><span data-stu-id="4b678-120">In the Events drop-down list, select the `BindingNavigatorDeleteItem_EnabledChanged` event.</span></span>  
  
12. <span data-ttu-id="4b678-121">Aggiungere il codice seguente al gestore eventi `BindingNavigatorDeleteItem_EnabledChanged` :</span><span class="sxs-lookup"><span data-stu-id="4b678-121">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="4b678-122">Questo passaggio è necessario affinché <xref:System.Windows.Forms.BindingSource> abiliti il pulsante **DeleteItem** pulsante a ogni modifica del record corrente.</span><span class="sxs-lookup"><span data-stu-id="4b678-122">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
### <a name="to-disable-adding-and-deleting-at-run-time"></a><span data-ttu-id="4b678-123">Per disabilitare l'aggiunta ed eliminazione in fase di esecuzione</span><span class="sxs-lookup"><span data-stu-id="4b678-123">To disable adding and deleting at run time</span></span>  
  
1.  <span data-ttu-id="4b678-124">In Progettazione Windows Form, fare doppio clic sul form per aprire l'editor di codice.</span><span class="sxs-lookup"><span data-stu-id="4b678-124">In the Windows Forms Designer, double-click the form to open the Code Editor.</span></span>  
  
2.  <span data-ttu-id="4b678-125">Aggiungere il codice seguente all'evento `Form_Load` :</span><span class="sxs-lookup"><span data-stu-id="4b678-125">Add the following code to the `Form_Load` event:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#2](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_2.vb)]  
  
3.  <span data-ttu-id="4b678-126">Aggiungere il codice seguente al gestore eventi `BindingNavigatorDeleteItem_EnabledChanged` :</span><span class="sxs-lookup"><span data-stu-id="4b678-126">Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:</span></span>  
  
     [!code-csharp[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/CSharp/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.cs)]
     [!code-vb[VbPowerPacksDataRepeaterDisableAddDelete#1](../../../visual-basic/developing-apps/windows-forms/codesnippet/VisualBasic/how-to-disable-adding-and-deleting-datarepeater-items-visual-studio_1.vb)]  
  
    > [!NOTE]
    >  <span data-ttu-id="4b678-127">Questo passaggio è necessario affinché <xref:System.Windows.Forms.BindingSource> abiliti il pulsante **DeleteItem** pulsante a ogni modifica del record corrente.</span><span class="sxs-lookup"><span data-stu-id="4b678-127">This step is necessary because the <xref:System.Windows.Forms.BindingSource> will enable the **DeleteItem** button every time that the current record changes.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4b678-128">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4b678-128">See Also</span></span>  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater>  
 [<span data-ttu-id="4b678-129">Introduzione al controllo DataRepeater</span><span class="sxs-lookup"><span data-stu-id="4b678-129">Introduction to the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/introduction-to-the-datarepeater-control-visual-studio.md)  
 [<span data-ttu-id="4b678-130">Risoluzione dei problemi relativi al controllo DataRepeater</span><span class="sxs-lookup"><span data-stu-id="4b678-130">Troubleshooting the DataRepeater Control</span></span>](../../../visual-basic/developing-apps/windows-forms/troubleshooting-the-datarepeater-control-visual-studio.md)
