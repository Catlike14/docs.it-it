---
title: 'Procedura: rispondere alla selezione dei pulsanti di Windows Form'
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
- buttons [Windows Forms], responding to Click events
- events [Windows Forms], Click events
- Click event [Windows Forms], Button control
- MouseDown event
- Button control [Windows Forms], click response
- double-clicks
- examples [Windows Forms], controls
- Click event [Windows Forms], responding to
ms.assetid: 7a4951bd-369c-4662-b246-28ad83eda484
caps.latest.revision: "14"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 923eb7d1b1b5b442ce897619253a958019b239a7
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-respond-to-windows-forms-button-clicks"></a><span data-ttu-id="c70ce-102">Procedura: rispondere alla selezione dei pulsanti di Windows Form</span><span class="sxs-lookup"><span data-stu-id="c70ce-102">How to: Respond to Windows Forms Button Clicks</span></span>
<span data-ttu-id="c70ce-103">L'utilizzo di base di un Windows Form <xref:System.Windows.Forms.Button> controllo consiste nell'esecuzione di codice quando si fa clic sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="c70ce-103">The most basic use of a Windows Forms <xref:System.Windows.Forms.Button> control is to run some code when the button is clicked.</span></span>  
  
 <span data-ttu-id="c70ce-104">Fare clic su un <xref:System.Windows.Forms.Button> controllo genera anche un numero di altri eventi, ad esempio il <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseDown>, e <xref:System.Windows.Forms.Control.MouseUp> eventi.</span><span class="sxs-lookup"><span data-stu-id="c70ce-104">Clicking a <xref:System.Windows.Forms.Button> control also generates a number of other events, such as the <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseDown>, and <xref:System.Windows.Forms.Control.MouseUp> events.</span></span> <span data-ttu-id="c70ce-105">Se si prevede di collegare gestori eventi per questi eventi correlati, assicurarsi che le relative azioni non sono in conflitto.</span><span class="sxs-lookup"><span data-stu-id="c70ce-105">If you intend to attach event handlers for these related events, be sure that their actions do not conflict.</span></span> <span data-ttu-id="c70ce-106">Ad esempio, se facendo clic sul pulsante Cancella le informazioni che l'utente è tipizzata in una casella di testo, posizionando il puntatore del mouse sul pulsante dovrebbe non visualizzare una descrizione comandi che contiene queste informazioni ora-inesistente.</span><span class="sxs-lookup"><span data-stu-id="c70ce-106">For example, if clicking the button clears information that the user has typed in a text box, pausing the mouse pointer over the button should not display a tool tip with that now-nonexistent information.</span></span>  
  
 <span data-ttu-id="c70ce-107">Se l'utente tenta di fare doppio clic su di <xref:System.Windows.Forms.Button> (controllo), verranno elaborati separatamente ogni clic; vale a dire, il controllo non supporta l'evento di doppio clic.</span><span class="sxs-lookup"><span data-stu-id="c70ce-107">If the user attempts to double-click the <xref:System.Windows.Forms.Button> control, each click will be processed separately; that is, the control does not support the double-click event.</span></span>  
  
### <a name="to-respond-to-a-button-click"></a><span data-ttu-id="c70ce-108">Per rispondere a un clic del pulsante</span><span class="sxs-lookup"><span data-stu-id="c70ce-108">To respond to a button click</span></span>  
  
-   <span data-ttu-id="c70ce-109">Il pulsante `Click` <xref:System.EventHandler> scrivere il codice da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c70ce-109">In the button's `Click` <xref:System.EventHandler> write the code to run.</span></span> <span data-ttu-id="c70ce-110">`Button1_Click`deve essere associato al controllo.</span><span class="sxs-lookup"><span data-stu-id="c70ce-110">`Button1_Click` must be bound to the control.</span></span> <span data-ttu-id="c70ce-111">Per ulteriori informazioni, vedere [procedura: creare gestori eventi in fase di esecuzione per Windows Form](../../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c70ce-111">For more information, see [How to: Create Event Handlers at Run Time for Windows Forms](../../../../docs/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms.md).</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click  
       MessageBox.Show("Button1 was clicked")  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       MessageBox.Show("button1 was clicked");  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          MessageBox::Show("button1 was clicked");  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="c70ce-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c70ce-112">See Also</span></span>  
 [<span data-ttu-id="c70ce-113">Panoramica sul controllo Button</span><span class="sxs-lookup"><span data-stu-id="c70ce-113">Button Control Overview</span></span>](../../../../docs/framework/winforms/controls/button-control-overview-windows-forms.md)  
 [<span data-ttu-id="c70ce-114">Modalità di selezione di un controllo Button di Windows Form</span><span class="sxs-lookup"><span data-stu-id="c70ce-114">Ways to Select a Windows Forms Button Control</span></span>](../../../../docs/framework/winforms/controls/ways-to-select-a-windows-forms-button-control.md)  
 [<span data-ttu-id="c70ce-115">Controllo Button</span><span class="sxs-lookup"><span data-stu-id="c70ce-115">Button Control</span></span>](../../../../docs/framework/winforms/controls/button-control-windows-forms.md)
