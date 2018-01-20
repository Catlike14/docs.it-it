---
title: 'Procedura: aggiungere colonne al controllo ListView Windows Form utilizzando la finestra di progettazione'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- ListView control [Windows Forms], adding column headers
- columns [Windows Forms], adding to ListView controls
ms.assetid: 5b1a8b4d-587e-479a-95c1-f9b90884f13a
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 971d3918fd6085bea85e43183ea67745d40e51b8
ms.sourcegitcommit: c0dd436f6f8f44dc80dc43b07f6841a00b74b23f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/19/2018
---
# <a name="how-to-add-columns-to-the-windows-forms-listview-control-using-the-designer"></a><span data-ttu-id="519bc-102">Procedura: aggiungere colonne al controllo ListView Windows Form utilizzando la finestra di progettazione</span><span class="sxs-lookup"><span data-stu-id="519bc-102">How to: Add Columns to the Windows Forms ListView Control Using the Designer</span></span>
<span data-ttu-id="519bc-103">Windows Form <xref:System.Windows.Forms.ListView> controllo può visualizzare più colonne per ogni elenco elemento quando si trova il **dettagli** visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="519bc-103">The Windows Forms <xref:System.Windows.Forms.ListView> control can display multiple columns for each list item when in the **Details** view.</span></span> <span data-ttu-id="519bc-104">È possibile utilizzare le colonne per visualizzare diversi tipi di informazioni su ogni elemento di elenco.</span><span class="sxs-lookup"><span data-stu-id="519bc-104">You can use the columns to display several types of information about each list item.</span></span> <span data-ttu-id="519bc-105">Ad esempio, un elenco di file potrebbe visualizzare il nome del file, il tipo di file, dimensioni e data che dell'ultima modifica il file.</span><span class="sxs-lookup"><span data-stu-id="519bc-105">For example, a list of files could display the file name, file type, size, and date the file was last modified.</span></span> <span data-ttu-id="519bc-106">Per informazioni sulla compilazione delle colonne dopo la creazione, vedere [procedura: visualizzare elementi secondari nelle colonne con il controllo ListView Windows Form](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md).</span><span class="sxs-lookup"><span data-stu-id="519bc-106">For information on populating the columns once they are created, see [How to: Display Subitems in Columns with the Windows Forms ListView Control](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md).</span></span>  
  
 <span data-ttu-id="519bc-107">La procedura seguente richiede un **applicazione Windows** progetto con un form contenente un <xref:System.Windows.Forms.ListView> controllo.</span><span class="sxs-lookup"><span data-stu-id="519bc-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.ListView> control.</span></span> <span data-ttu-id="519bc-108">Per informazioni sull'impostazione di un progetto, vedere [procedura: creare un progetto di applicazione Windows](http://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) e [procedura: aggiungere controlli a un Windows Form](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="519bc-108">For information about setting up such a project, see [How to: Create a Windows Application Project](http://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) and [How to: Add Controls to Windows Forms](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="519bc-109">Le finestre di dialogo e i comandi di menu visualizzati potrebbero essere diversi da quelli descritti nella Guida a seconda delle impostazioni attive o dell'edizione del programma.</span><span class="sxs-lookup"><span data-stu-id="519bc-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="519bc-110">Per modificare le impostazioni, scegliere **Importa/Esporta impostazioni** dal menu **Strumenti** .</span><span class="sxs-lookup"><span data-stu-id="519bc-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="519bc-111">Per altre informazioni, vedere [Personalizzazione delle impostazioni di sviluppo in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span><span class="sxs-lookup"><span data-stu-id="519bc-111">For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span></span>  
  
### <a name="to-add-columns-in-the-designer"></a><span data-ttu-id="519bc-112">Per aggiungere colonne nella finestra di progettazione</span><span class="sxs-lookup"><span data-stu-id="519bc-112">To add columns in the designer</span></span>  
  
1.  <span data-ttu-id="519bc-113">Nel **proprietà** finestra, impostare il controllo <xref:System.Windows.Forms.ListView.View%2A> proprietà <xref:System.Windows.Forms.View.Details>.</span><span class="sxs-lookup"><span data-stu-id="519bc-113">In the **Properties** window, set the control's <xref:System.Windows.Forms.ListView.View%2A> property to <xref:System.Windows.Forms.View.Details>.</span></span>  
  
2.  <span data-ttu-id="519bc-114">Nel **proprietà** finestra, fare clic su di **i puntini di sospensione** pulsante (![schermata VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) accanto a il <xref:System.Windows.Forms.ListView.Columns%2A> proprietà.</span><span class="sxs-lookup"><span data-stu-id="519bc-114">In the **Properties** window, click the **Ellipsis** button (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) next to the <xref:System.Windows.Forms.ListView.Columns%2A> property.</span></span>  
  
     <span data-ttu-id="519bc-115">Il **insieme ColumnHeader** viene visualizzato.</span><span class="sxs-lookup"><span data-stu-id="519bc-115">The **ColumnHeader Collection Editor** appears.</span></span>  
  
3.  <span data-ttu-id="519bc-116">Utilizzare il **Aggiungi** pulsante per aggiungere nuove colonne.</span><span class="sxs-lookup"><span data-stu-id="519bc-116">Use the **Add** button to add new columns.</span></span> <span data-ttu-id="519bc-117">È quindi possibile selezionare l'intestazione di colonna e impostare il testo (la didascalia della colonna), l'allineamento del testo e larghezza.</span><span class="sxs-lookup"><span data-stu-id="519bc-117">You can then select the column header and set its text (the caption of the column), text alignment, and width.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="519bc-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="519bc-118">See Also</span></span>  
 [<span data-ttu-id="519bc-119">Panoramica del controllo ListView</span><span class="sxs-lookup"><span data-stu-id="519bc-119">ListView Control Overview</span></span>](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)  
 [<span data-ttu-id="519bc-120">Procedura: Aggiungere e rimuovere elementi con il controllo ListView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="519bc-120">How to: Add and Remove Items with the Windows Forms ListView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-add-and-remove-items-with-the-windows-forms-listview-control.md)  
 [<span data-ttu-id="519bc-121">Procedura: Visualizzare elementi secondari nelle colonne con il controllo ListView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="519bc-121">How to: Display Subitems in Columns with the Windows Forms ListView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)  
 [<span data-ttu-id="519bc-122">Procedura: Visualizzare icone per il controllo ListView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="519bc-122">How to: Display Icons for the Windows Forms ListView Control</span></span>](../../../../docs/framework/winforms/controls/how-to-display-icons-for-the-windows-forms-listview-control.md)  
 [<span data-ttu-id="519bc-123">Procedura: Aggiungere informazioni personalizzate a un controllo TreeView o ListView (Windows Form)</span><span class="sxs-lookup"><span data-stu-id="519bc-123">How to: Add Custom Information to a TreeView or ListView Control (Windows Forms)</span></span>](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)
