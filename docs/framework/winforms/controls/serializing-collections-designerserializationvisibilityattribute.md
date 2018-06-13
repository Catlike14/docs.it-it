---
title: 'Procedura dettagliata: serializzazione di raccolte di tipi standard tramite DesignerSerializationVisibilityAttribute'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- serialization [Windows Forms], collections
- standard types [Windows Forms], collections
- collections [Windows Forms], serializing
- collections [Windows Forms], standard types
ms.assetid: 020c9df4-fdc5-4dae-815a-963ecae5668c
ms.openlocfilehash: a502ecc30911f2296bf48eaa195f5b6452b7588a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33541298"
---
# <a name="walkthrough-serializing-collections-of-standard-types-with-the-designerserializationvisibilityattribute"></a><span data-ttu-id="047d2-102">Procedura dettagliata: serializzazione di raccolte di tipi standard tramite DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="047d2-102">Walkthrough: Serializing Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>
<span data-ttu-id="047d2-103">I controlli personalizzati talvolta espongono un insieme come una proprietà.</span><span class="sxs-lookup"><span data-stu-id="047d2-103">Your custom controls will sometimes expose a collection as a property.</span></span> <span data-ttu-id="047d2-104">Questa procedura dettagliata viene illustrato come utilizzare la <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> classe per controllare la modalità di serializzazione di una raccolta in fase di progettazione.</span><span class="sxs-lookup"><span data-stu-id="047d2-104">This walkthrough demonstrates how to use the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> class to control how a collection is serialized at design time.</span></span> <span data-ttu-id="047d2-105">L'applicazione di <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valore alla proprietà della raccolta assicura che la proprietà sarà serializzata.</span><span class="sxs-lookup"><span data-stu-id="047d2-105">Applying the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value to your collection property ensures that the property will be serialized.</span></span>  
  
 <span data-ttu-id="047d2-106">Per copiare il codice in questo argomento come elenco singolo, vedere [procedura: serializzare le raccolte di tipi Standard DesignerSerializationVisibilityAttribute](http://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9).</span><span class="sxs-lookup"><span data-stu-id="047d2-106">To copy the code in this topic as a single listing, see [How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute](http://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9).</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="047d2-107">Le finestre di dialogo e i comandi di menu visualizzati potrebbero essere diversi da quelli descritti nella Guida a seconda delle impostazioni attive o dell'edizione del programma.</span><span class="sxs-lookup"><span data-stu-id="047d2-107">The dialog boxes and menu commands you see might differ from those described in Help depending on your active settings or edition.</span></span> <span data-ttu-id="047d2-108">Per modificare le impostazioni, scegliere **Importa/Esporta impostazioni** dal menu **Strumenti** .</span><span class="sxs-lookup"><span data-stu-id="047d2-108">To change your settings, choose **Import and Export Settings** on the **Tools** menu.</span></span> <span data-ttu-id="047d2-109">Per altre informazioni, vedere [Personalizzazione delle impostazioni di sviluppo in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span><span class="sxs-lookup"><span data-stu-id="047d2-109">For more information, see [Customizing Development Settings in Visual Studio](http://msdn.microsoft.com/library/22c4debb-4e31-47a8-8f19-16f328d7dcd3).</span></span>  
  
## <a name="prerequisites"></a><span data-ttu-id="047d2-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="047d2-110">Prerequisites</span></span>  
 <span data-ttu-id="047d2-111">Per completare questa procedura dettagliata, è necessario:</span><span class="sxs-lookup"><span data-stu-id="047d2-111">In order to complete this walkthrough, you will need:</span></span>  
  
-   <span data-ttu-id="047d2-112">Disporre di autorizzazioni sufficienti creare ed eseguire progetti di applicazione Windows Form nel computer in cui è installato Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="047d2-112">Sufficient permissions to be able to create and run Windows Forms application projects on the computer where Visual Studio is installed.</span></span>  
  
## <a name="creating-a-control-that-has-a-serializable-collection"></a><span data-ttu-id="047d2-113">Creazione di un controllo che contiene una raccolta serializzabile</span><span class="sxs-lookup"><span data-stu-id="047d2-113">Creating a Control That Has a Serializable Collection</span></span>  
 <span data-ttu-id="047d2-114">Il primo passaggio consiste nel creare un controllo che contiene una raccolta serializzabile come una proprietà.</span><span class="sxs-lookup"><span data-stu-id="047d2-114">The first step is to create a control that has a serializable collection as a property.</span></span> <span data-ttu-id="047d2-115">È possibile modificare il contenuto di questa raccolta tramite il **Editor della raccolta**, che è possibile accedere dal **proprietà** finestra.</span><span class="sxs-lookup"><span data-stu-id="047d2-115">You can edit the contents of this collection using the **Collection Editor**, which you can access from the **Properties** window.</span></span>  
  
#### <a name="to-create-a-control-with-a-serializable-collection"></a><span data-ttu-id="047d2-116">Per creare un controllo con una raccolta serializzabile</span><span class="sxs-lookup"><span data-stu-id="047d2-116">To create a control with a serializable collection</span></span>  
  
1.  <span data-ttu-id="047d2-117">Creare un progetto libreria di controlli Windows denominato `SerializationDemoControlLib`.</span><span class="sxs-lookup"><span data-stu-id="047d2-117">Create a Windows Control Library project called `SerializationDemoControlLib`.</span></span> <span data-ttu-id="047d2-118">Per ulteriori informazioni, vedere [modello libreria di controlli Windows](http://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4).</span><span class="sxs-lookup"><span data-stu-id="047d2-118">For more information, see [Windows Control Library Template](http://msdn.microsoft.com/library/722f4e2d-1310-4ed5-8f33-593337ab66b4).</span></span>  
  
2.  <span data-ttu-id="047d2-119">Rinominare `UserControl1` a `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-119">Rename `UserControl1` to `SerializationDemoControl`.</span></span> <span data-ttu-id="047d2-120">Per ulteriori informazioni, vedere [procedura: rinominare gli identificatori](http://msdn.microsoft.com/library/2430f732-2b70-4516-8cf6-a7bb71cc9724).</span><span class="sxs-lookup"><span data-stu-id="047d2-120">For more information, see [How to: Rename Identifiers](http://msdn.microsoft.com/library/2430f732-2b70-4516-8cf6-a7bb71cc9724).</span></span>  
  
3.  <span data-ttu-id="047d2-121">Nel **proprietà** finestra, impostare il valore della <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> proprietà `10`.</span><span class="sxs-lookup"><span data-stu-id="047d2-121">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Padding.All%2A?displayProperty=nameWithType> property to `10`.</span></span>  
  
4.  <span data-ttu-id="047d2-122">Sul posto un <xref:System.Windows.Forms.TextBox> controllo il `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-122">Place a <xref:System.Windows.Forms.TextBox> control in the `SerializationDemoControl`.</span></span>  
  
5.  <span data-ttu-id="047d2-123">Selezionare il controllo <xref:System.Windows.Forms.TextBox>.</span><span class="sxs-lookup"><span data-stu-id="047d2-123">Select the <xref:System.Windows.Forms.TextBox> control.</span></span> <span data-ttu-id="047d2-124">Nel **proprietà** finestra, impostare le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="047d2-124">In the **Properties** window, set the following properties.</span></span>  
  
    |<span data-ttu-id="047d2-125">Proprietà</span><span class="sxs-lookup"><span data-stu-id="047d2-125">Property</span></span>|<span data-ttu-id="047d2-126">Modificare in</span><span class="sxs-lookup"><span data-stu-id="047d2-126">Change to</span></span>|  
    |--------------|---------------|  
    |<span data-ttu-id="047d2-127">**Multiline**</span><span class="sxs-lookup"><span data-stu-id="047d2-127">**Multiline**</span></span>|`true`|  
    |<span data-ttu-id="047d2-128">**Ancoraggio**</span><span class="sxs-lookup"><span data-stu-id="047d2-128">**Dock**</span></span>|<xref:System.Windows.Forms.DockStyle.Fill>|  
    |<span data-ttu-id="047d2-129">**Barre di scorrimento**</span><span class="sxs-lookup"><span data-stu-id="047d2-129">**ScrollBars**</span></span>|<xref:System.Windows.Forms.ScrollBars.Vertical>|  
    |<span data-ttu-id="047d2-130">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="047d2-130">**ReadOnly**</span></span>|`true`|  
  
6.  <span data-ttu-id="047d2-131">Nel **Editor di codice**, dichiarare un campo di matrice di stringa denominato `stringsValue` in `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-131">In the **Code Editor**, declare a string array field named `stringsValue` in `SerializationDemoControl`.</span></span>  
  
     [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#4)]
     [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#4)]
     [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#4)]  
  
7.  <span data-ttu-id="047d2-132">Definire il `Strings` proprietà il `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-132">Define the `Strings` property on the `SerializationDemoControl`.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="047d2-133">Il <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> valore viene utilizzato per attivare la serializzazione della raccolta.</span><span class="sxs-lookup"><span data-stu-id="047d2-133">The <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content> value is used to enable serialization of the collection.</span></span>  
  
 [!code-cpp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/cpp/form1.cpp#5)]
 [!code-csharp[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/CS/form1.cs#5)]
 [!code-vb[System.ComponentModel.DesignerSerializationVisibilityAttribute#5](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.DesignerSerializationVisibilityAttribute/VB/form1.vb#5)]  
  
1.  <span data-ttu-id="047d2-134">Per compilare il progetto ed eseguire il controllo in **UserControl Test Container**, premere F5.</span><span class="sxs-lookup"><span data-stu-id="047d2-134">Press F5 to build the project and run your control in the **UserControl Test Container**.</span></span>  
  
2.  <span data-ttu-id="047d2-135">Trovare il `Strings` proprietà il <xref:System.Windows.Forms.PropertyGrid> del **UserControl Test Container**.</span><span class="sxs-lookup"><span data-stu-id="047d2-135">Find the `Strings` property in the <xref:System.Windows.Forms.PropertyGrid> of the **UserControl Test Container**.</span></span> <span data-ttu-id="047d2-136">Fare clic su di `Strings` proprietà, quindi fare clic sui puntini di sospensione (![schermata VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) per aprire il **Editor raccolta di stringhe**.</span><span class="sxs-lookup"><span data-stu-id="047d2-136">Click the `Strings` property, then click the ellipsis (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) button to open the **String Collection Editor**.</span></span>  
  
3.  <span data-ttu-id="047d2-137">Immettere più stringhe nel **Editor raccolta di stringhe**.</span><span class="sxs-lookup"><span data-stu-id="047d2-137">Enter several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="047d2-138">È necessario separarli premendo INVIO alla fine di ogni stringa.</span><span class="sxs-lookup"><span data-stu-id="047d2-138">Separate them by pressing the ENTER key at the end of each string.</span></span> <span data-ttu-id="047d2-139">Fare clic su **OK** dopo aver terminato le stringhe.</span><span class="sxs-lookup"><span data-stu-id="047d2-139">Click **OK** when you are finished entering strings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="047d2-140">Vengono visualizzate le stringhe immesse nel <xref:System.Windows.Forms.TextBox> del `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-140">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>  
  
## <a name="serializing-a-collection-property"></a><span data-ttu-id="047d2-141">La serializzazione di una proprietà di raccolta</span><span class="sxs-lookup"><span data-stu-id="047d2-141">Serializing a Collection Property</span></span>  
 <span data-ttu-id="047d2-142">Per testare il comportamento di serializzazione del controllo, verrà posizionato in un form e modificare il contenuto della raccolta con il **Editor della raccolta**.</span><span class="sxs-lookup"><span data-stu-id="047d2-142">To test the serialization behavior of your control, you will place it on a form and change the contents of the collection with the **Collection Editor**.</span></span> <span data-ttu-id="047d2-143">È possibile osservare lo stato di raccolta serializzata in un file speciale della finestra di progettazione, in cui il **Progettazione Windows Form** genera codice.</span><span class="sxs-lookup"><span data-stu-id="047d2-143">You can see the serialized collection state by looking at a special designer file, into which the **Windows Forms Designer** emits code.</span></span>  
  
#### <a name="to-serialize-a-collection"></a><span data-ttu-id="047d2-144">Per serializzare una raccolta</span><span class="sxs-lookup"><span data-stu-id="047d2-144">To serialize a collection</span></span>  
  
1.  <span data-ttu-id="047d2-145">Aggiungere un progetto applicazione Windows alla soluzione.</span><span class="sxs-lookup"><span data-stu-id="047d2-145">Add a Windows Application project to the solution.</span></span> <span data-ttu-id="047d2-146">Denominare il progetto `SerializationDemoControlTest`.</span><span class="sxs-lookup"><span data-stu-id="047d2-146">Name the project `SerializationDemoControlTest`.</span></span>  
  
2.  <span data-ttu-id="047d2-147">Nel **della casella degli strumenti**, individuare la scheda **Componenti SerializationDemoControlLib**.</span><span class="sxs-lookup"><span data-stu-id="047d2-147">In the **Toolbox**, find the tab named **SerializationDemoControlLib Components**.</span></span> <span data-ttu-id="047d2-148">In questa scheda, si trova il `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-148">In this tab, you will find the `SerializationDemoControl`.</span></span> <span data-ttu-id="047d2-149">Per altre informazioni, vedere [Procedura dettagliata: compilare automaticamente la casella degli strumenti con componenti personalizzati](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span><span class="sxs-lookup"><span data-stu-id="047d2-149">For more information, see [Walkthrough: Automatically Populating the Toolbox with Custom Components](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md).</span></span>  
  
3.  <span data-ttu-id="047d2-150">Sul posto un `SerializationDemoControl` sul form.</span><span class="sxs-lookup"><span data-stu-id="047d2-150">Place a `SerializationDemoControl` on your form.</span></span>  
  
4.  <span data-ttu-id="047d2-151">Trovare il `Strings` proprietà il **proprietà** finestra.</span><span class="sxs-lookup"><span data-stu-id="047d2-151">Find the `Strings` property in the **Properties** window.</span></span> <span data-ttu-id="047d2-152">Fare clic su di `Strings` proprietà, quindi fare clic sui puntini di sospensione (![schermata VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) per aprire il **Editor raccolta di stringhe**.</span><span class="sxs-lookup"><span data-stu-id="047d2-152">Click the `Strings` property, then click the ellipsis (![VisualStudioEllipsesButton screenshot](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) button to open the **String Collection Editor**.</span></span>  
  
5.  <span data-ttu-id="047d2-153">Digitare diverse stringhe nel **Editor raccolta di stringhe**.</span><span class="sxs-lookup"><span data-stu-id="047d2-153">Type several strings in the **String Collection Editor**.</span></span> <span data-ttu-id="047d2-154">È necessario separarli premendo INVIO alla fine di ogni stringa.</span><span class="sxs-lookup"><span data-stu-id="047d2-154">Separate them by pressing the ENTER key at the end of each string.</span></span> <span data-ttu-id="047d2-155">Fare clic su **OK** dopo aver terminato le stringhe.</span><span class="sxs-lookup"><span data-stu-id="047d2-155">Click **OK** when you are finished entering strings.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="047d2-156">Vengono visualizzate le stringhe immesse nel <xref:System.Windows.Forms.TextBox> del `SerializationDemoControl`.</span><span class="sxs-lookup"><span data-stu-id="047d2-156">The strings you typed appear in the <xref:System.Windows.Forms.TextBox> of the `SerializationDemoControl`.</span></span>  
  
1.  <span data-ttu-id="047d2-157">In **Esplora soluzioni** fare clic sul pulsante **Mostra tutti i file**.</span><span class="sxs-lookup"><span data-stu-id="047d2-157">In **Solution Explorer**, click the **Show All Files** button.</span></span>  
  
2.  <span data-ttu-id="047d2-158">Aprire il **Form1** nodo.</span><span class="sxs-lookup"><span data-stu-id="047d2-158">Open the **Form1** node.</span></span> <span data-ttu-id="047d2-159">In cui è presente un file denominato **Form1. Designer.cs** o **Form1**.</span><span class="sxs-lookup"><span data-stu-id="047d2-159">Beneath it is a file called **Form1.Designer.cs** or **Form1.Designer.vb**.</span></span> <span data-ttu-id="047d2-160">Si tratta del file in cui il **Progettazione Windows Form** genera codice che rappresenta lo stato in fase di progettazione del form e i relativi controlli figlio.</span><span class="sxs-lookup"><span data-stu-id="047d2-160">This is the file into which the **Windows Forms Designer** emits code representing the design-time state of your form and its child controls.</span></span> <span data-ttu-id="047d2-161">Aprire il file nell'**editor di codice**.</span><span class="sxs-lookup"><span data-stu-id="047d2-161">Open this file in the **Code Editor**.</span></span>  
  
3.  <span data-ttu-id="047d2-162">Aprire l'area denominata **codice generato da Progettazione Windows Form** e individuare la sezione **serializationDemoControl1**.</span><span class="sxs-lookup"><span data-stu-id="047d2-162">Open the region called **Windows Form Designer generated code** and find the section labeled **serializationDemoControl1**.</span></span> <span data-ttu-id="047d2-163">Sotto l'etichetta è il codice che rappresenta lo stato serializzato del controllo.</span><span class="sxs-lookup"><span data-stu-id="047d2-163">Beneath this label is the code representing the serialized state of your control.</span></span> <span data-ttu-id="047d2-164">Le stringhe digitato nel passaggio 5 vengono visualizzate in un'assegnazione di `Strings` proprietà.</span><span class="sxs-lookup"><span data-stu-id="047d2-164">The strings you typed in step 5 appear in an assignment to the `Strings` property.</span></span> <span data-ttu-id="047d2-165">Gli esempi di codice seguente in c# e Visual Basic, Mostra codice simile a ciò che viene visualizzato se digitato le stringhe "rosso", "arancione" e "giallo".</span><span class="sxs-lookup"><span data-stu-id="047d2-165">The following code examples in C# and Visual Basic, show code similar to what you will see if you typed the strings "red", "orange", and "yellow".</span></span>  
  
    ```csharp  
    this.serializationDemoControl1.Strings = new string[] {  
            "red",  
            "orange",  
            "yellow"};  
    ```  
    
    ```vb  
    Me.serializationDemoControl1.Strings = New String() {"red", "orange", "yellow"}  
    ```
  
4.  <span data-ttu-id="047d2-166">Nel **Editor di codice**, modificare il valore della <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> sul `Strings` proprietà <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span><span class="sxs-lookup"><span data-stu-id="047d2-166">In the **Code Editor**, change the value of the <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute> on the `Strings` property to <xref:System.ComponentModel.DesignerSerializationVisibility.Hidden>.</span></span>  
  
    ```csharp  
    [DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)]  
    ```  
    ```vb  
    <DesignerSerializationVisibility(DesignerSerializationVisibility.Hidden)> _  
    ```  
  
5. <span data-ttu-id="047d2-167">Ricompilare la soluzione e ripetere i passaggi 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="047d2-167">Rebuild the solution and repeat steps 3 and 4.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="047d2-168">In questo caso, il **Progettazione Windows Form** alcuna assegnazione genera la `Strings` proprietà.</span><span class="sxs-lookup"><span data-stu-id="047d2-168">In this case, the **Windows Forms Designer** emits no assignment to the `Strings` property.</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="047d2-169">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="047d2-169">Next Steps</span></span>  
 <span data-ttu-id="047d2-170">Una volta che in grado di serializzare una raccolta di tipi standard, è consigliabile integrare in modo più specifico i controlli personalizzati nell'ambiente di progettazione.</span><span class="sxs-lookup"><span data-stu-id="047d2-170">Once you know how to serialize a collection of standard types, consider integrating your custom controls more deeply into the design-time environment.</span></span> <span data-ttu-id="047d2-171">Gli argomenti seguenti viene descritto come migliorare l'integrazione in fase di progettazione di controlli personalizzati:</span><span class="sxs-lookup"><span data-stu-id="047d2-171">The following topics describe how to enhance the design-time integration of your custom controls:</span></span>  
  
-   [<span data-ttu-id="047d2-172">Architettura della fase di progettazione</span><span class="sxs-lookup"><span data-stu-id="047d2-172">Design-Time Architecture</span></span>](http://msdn.microsoft.com/library/4881917b-628f-4689-b872-472e4f8a4e3a)  
  
-   [<span data-ttu-id="047d2-173">Attributi nei controlli Windows Forms</span><span class="sxs-lookup"><span data-stu-id="047d2-173">Attributes in Windows Forms Controls</span></span>](../../../../docs/framework/winforms/controls/attributes-in-windows-forms-controls.md)  
  
-   [<span data-ttu-id="047d2-174">Panoramica di serializzazione della finestra di progettazione</span><span class="sxs-lookup"><span data-stu-id="047d2-174">Designer Serialization Overview</span></span>](http://msdn.microsoft.com/library/c342635a-aa5f-4281-915b-b013738af15a)  
  
-   [<span data-ttu-id="047d2-175">Procedura dettagliata: Creazione di un controllo Windows Form che usufruisca delle funzionalità offerte da Visual Studio in fase di progettazione</span><span class="sxs-lookup"><span data-stu-id="047d2-175">Walkthrough: Creating a Windows Forms Control That Takes Advantage of Visual Studio Design-Time Features</span></span>](../../../../docs/framework/winforms/controls/creating-a-wf-control-design-time-features.md)  
  
## <a name="see-also"></a><span data-ttu-id="047d2-176">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="047d2-176">See Also</span></span>  
 <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute>  
 [<span data-ttu-id="047d2-177">Panoramica di serializzazione della finestra di progettazione</span><span class="sxs-lookup"><span data-stu-id="047d2-177">Designer Serialization Overview</span></span>](http://msdn.microsoft.com/library/c342635a-aa5f-4281-915b-b013738af15a)  
 [<span data-ttu-id="047d2-178">Procedura: serializzare le raccolte di tipi Standard tramite DesignerSerializationVisibilityAttribute</span><span class="sxs-lookup"><span data-stu-id="047d2-178">How to: Serialize Collections of Standard Types with the DesignerSerializationVisibilityAttribute</span></span>](http://msdn.microsoft.com/library/7829fcdd-8205-405f-8231-a1282a9835c9)  
 [<span data-ttu-id="047d2-179">Procedura dettagliata: Compilare automaticamente la casella degli strumenti con componenti personalizzati</span><span class="sxs-lookup"><span data-stu-id="047d2-179">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>](../../../../docs/framework/winforms/controls/walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
