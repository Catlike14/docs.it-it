---
title: "Procedura: creare un'interfaccia di tipo Esplora risorse in un Windows Form"
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Explorer [Windows Forms], creating with Windows Forms
- SplitContainer control [Windows Forms], Explorer-style interface
- forms [Windows Forms], Windows Explorer type
ms.assetid: 9a3d5f4f-5dda-4350-9ad5-57ce5976dc47
ms.openlocfilehash: 249210d2bcb7a9ef2c5bf1aed00bcfe138193aab
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/02/2018
ms.locfileid: "43456707"
---
# <a name="how-to-create-a-windows-explorerstyle-interface-on-a-windows-form"></a><span data-ttu-id="27991-102">Procedura: creare un'interfaccia di tipo Esplora risorse in un Windows Form</span><span class="sxs-lookup"><span data-stu-id="27991-102">How to: Create a Windows Explorer–Style Interface on a Windows Form</span></span>
<span data-ttu-id="27991-103">Windows Explorer è una soluzione di interfaccia utente comune per le applicazioni a causa di relativa familiarità pronto.</span><span class="sxs-lookup"><span data-stu-id="27991-103">Windows Explorer is a common user-interface choice for applications because of its ready familiarity.</span></span>  
  
 <span data-ttu-id="27991-104">Windows Explorer è costituita essenzialmente da un <xref:System.Windows.Forms.TreeView> controllo e un <xref:System.Windows.Forms.ListView> controllo in due pannelli separati.</span><span class="sxs-lookup"><span data-stu-id="27991-104">Windows Explorer is, essentially, a <xref:System.Windows.Forms.TreeView> control and a <xref:System.Windows.Forms.ListView> control on separate panels.</span></span> <span data-ttu-id="27991-105">I pannelli vengono effettuati ridimensionabili da una barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="27991-105">The panels are made resizable by a splitter.</span></span> <span data-ttu-id="27991-106">Questa disposizione dei controlli in modo efficace per la visualizzazione e le informazioni cercate.</span><span class="sxs-lookup"><span data-stu-id="27991-106">This arrangement of controls is very effective for displaying and browsing information.</span></span>  
  
 <span data-ttu-id="27991-107">I passaggi seguenti mostrano come disporre i controlli in un Windows form simile a Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="27991-107">The following steps show how to arrange controls in a Windows Explorer-like form.</span></span> <span data-ttu-id="27991-108">Non illustrano come aggiungere la funzionalità per l'esplorazione del file dell'applicazione Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="27991-108">They do not show how to add the file-browsing functionality of the Windows Explorer application.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="27991-109">Le finestre di dialogo e i comandi di menu visualizzati potrebbero essere diversi da quelli descritti nella Guida a seconda delle impostazioni attive o dell'edizione del programma.</span><span class="sxs-lookup"><span data-stu-id="27991-109">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="27991-110">Per modificare le impostazioni, scegliere **Importa/Esporta impostazioni** dal menu **Strumenti** .</span><span class="sxs-lookup"><span data-stu-id="27991-110">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="27991-111">Per altre informazioni, vedere [Personalizzare l'IDE di Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).</span><span class="sxs-lookup"><span data-stu-id="27991-111">For more information, see [Personalize the Visual Studio IDE](/visualstudio/ide/personalizing-the-visual-studio-ide).</span></span>  
  
### <a name="to-create-a-windows-explorer-style-windows-form"></a><span data-ttu-id="27991-112">Per creare un modulo di Windows di tipo Esplora risorse di Windows</span><span class="sxs-lookup"><span data-stu-id="27991-112">To create a Windows Explorer-style Windows Form</span></span>  
  
1.  <span data-ttu-id="27991-113">Creare un nuovo progetto applicazione Windows (**File** > **New** > **progetto** > **Visual C#** oppure **Visual Basic** > **Desktop classico** > **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="27991-113">Create a new Windows Application project (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>  
  
2.  <span data-ttu-id="27991-114">Dal **casella degli strumenti**:</span><span class="sxs-lookup"><span data-stu-id="27991-114">From the **Toolbox**:</span></span>  
  
    1.  <span data-ttu-id="27991-115">Trascinare un <xref:System.Windows.Forms.SplitContainer> controllo nel form.</span><span class="sxs-lookup"><span data-stu-id="27991-115">Drag a <xref:System.Windows.Forms.SplitContainer> control onto your form.</span></span>  
  
    2.  <span data-ttu-id="27991-116">Trascinare un <xref:System.Windows.Forms.TreeView> controllo in **SplitterPanel1** (il pannello del <xref:System.Windows.Forms.SplitContainer> controllo contrassegnato **Panel1**).</span><span class="sxs-lookup"><span data-stu-id="27991-116">Drag a <xref:System.Windows.Forms.TreeView> control into **SplitterPanel1** (the panel of the <xref:System.Windows.Forms.SplitContainer> control marked **Panel1**).</span></span>  
  
    3.  <span data-ttu-id="27991-117">Trascinare un <xref:System.Windows.Forms.ListView> controllo in **pannello SplitterPanel2** (il pannello del <xref:System.Windows.Forms.SplitContainer> controllo contrassegnato **Panel2**).</span><span class="sxs-lookup"><span data-stu-id="27991-117">Drag a <xref:System.Windows.Forms.ListView> control into **SplitterPanel2** (the panel of the <xref:System.Windows.Forms.SplitContainer> control marked **Panel2**).</span></span>  
  
3.  <span data-ttu-id="27991-118">Selezionare tutti i tre controlli premendo il tasto CTRL e facendo clic su essi, a sua volta.</span><span class="sxs-lookup"><span data-stu-id="27991-118">Select all three controls by pressing the CTRL key and clicking them in turn.</span></span> <span data-ttu-id="27991-119">Quando si seleziona il <xref:System.Windows.Forms.SplitContainer> controllo, fare clic sulla barra di divisione, anziché i pannelli.</span><span class="sxs-lookup"><span data-stu-id="27991-119">When you select the <xref:System.Windows.Forms.SplitContainer> control, click the splitter bar, rather than the panels.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="27991-120">Non usare la **Seleziona tutto** comando le **modificare** menu.</span><span class="sxs-lookup"><span data-stu-id="27991-120">Do not use the **Select All** command on the **Edit** menu.</span></span> <span data-ttu-id="27991-121">Se in questo caso, la proprietà necessaria nel passaggio successivo non compariranno nella **proprietà** finestra.</span><span class="sxs-lookup"><span data-stu-id="27991-121">If you do so, the property needed in the next step will not appear in the **Properties** window.</span></span>  
  
4.  <span data-ttu-id="27991-122">Nel **le proprietà** impostare nella finestra di <xref:System.Windows.Forms.SplitContainer.Dock%2A> proprietà <xref:System.Windows.Forms.DockStyle.Fill>.</span><span class="sxs-lookup"><span data-stu-id="27991-122">In the **Properties** window, set the <xref:System.Windows.Forms.SplitContainer.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>  
  
5.  <span data-ttu-id="27991-123">Premere F5 per eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27991-123">Press F5 to run the application.</span></span>  
  
     <span data-ttu-id="27991-124">Viene visualizzata un'interfaccia utente di due parti, simile a quella della finestra di esplorazione di Windows.</span><span class="sxs-lookup"><span data-stu-id="27991-124">The form displays a two-part user interface, similar to that of the Windows Explorer.</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="27991-125">Quando si trascina la barra di divisione, i pannelli vengono ridimensionati.</span><span class="sxs-lookup"><span data-stu-id="27991-125">When you drag the splitter, the panels resize themselves.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="27991-126">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="27991-126">See Also</span></span>  
 <xref:System.Windows.Forms.SplitContainer>  
 [<span data-ttu-id="27991-127">Procedura: Creare un'interfaccia utente a più riquadri con Windows Form</span><span class="sxs-lookup"><span data-stu-id="27991-127">How to: Create a Multipane User Interface with Windows Forms</span></span>](../../../../docs/framework/winforms/controls/how-to-create-a-multipane-user-interface-with-windows-forms.md)  
 [<span data-ttu-id="27991-128">Procedura: Definire il ridimensionamento e il posizionamento in una finestra divisa</span><span class="sxs-lookup"><span data-stu-id="27991-128">How to: Define Resize and Positioning Behavior in a Split Window</span></span>](../../../../docs/framework/winforms/controls/how-to-define-resize-and-positioning-behavior-in-a-split-window.md)  
 [<span data-ttu-id="27991-129">Procedura: Suddividere una finestra orizzontalmente</span><span class="sxs-lookup"><span data-stu-id="27991-129">How to: Split a Window Horizontally</span></span>](../../../../docs/framework/winforms/controls/how-to-split-a-window-horizontally.md)  
 [<span data-ttu-id="27991-130">Controllo SplitContainer</span><span class="sxs-lookup"><span data-stu-id="27991-130">SplitContainer Control</span></span>](../../../../docs/framework/winforms/controls/splitcontainer-control-windows-forms.md)
