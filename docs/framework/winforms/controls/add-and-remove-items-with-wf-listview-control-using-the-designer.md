---
title: 'Procedura: aggiungere e rimuovere elementi nel controllo ListView Windows Form mediante la finestra di progettazione'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView control [Windows Forms], populating
- ListView control [Windows Forms], adding list items
ms.assetid: 217611ee-fd11-4d39-9a54-a37c3e781be1
ms.openlocfilehash: 0480c8980f0eba17229fff0c1e947cac5216fb9e
ms.sourcegitcommit: 8c28ab17c26bf08abbd004cc37651985c68841b8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/07/2018
ms.locfileid: "48847750"
---
# <a name="how-to-add-and-remove-items-with-the-windows-forms-listview-control-using-the-designer"></a>Procedura: aggiungere e rimuovere elementi nel controllo ListView Windows Form mediante la finestra di progettazione
Il processo di aggiunta di un elemento a un form Windows <xref:System.Windows.Forms.ListView> controllo consiste principalmente nella definizione dell'elemento e assegnazione di proprietà. È possibile aggiungere o rimuovere elementi elenco in qualsiasi momento.  
  
 La procedura seguente richiede un **applicazione di Windows** progetto con un form contenente un <xref:System.Windows.Forms.ListView> controllo. Per informazioni sulla configurazione di un progetto di questo tipo, vedere [procedura: creare un progetto di applicazione Windows](https://msdn.microsoft.com/library/b2f93fed-c635-4705-8d0e-cf079a264efa) e [procedura: aggiungere i controlli Windows Form](../../../../docs/framework/winforms/controls/how-to-add-controls-to-windows-forms.md).  
  
> [!NOTE]
>  Le finestre di dialogo e i comandi di menu visualizzati potrebbero essere diversi da quelli descritti nella Guida a seconda delle impostazioni attive o dell'edizione del programma. Per modificare le impostazioni, scegliere **Importa/Esporta impostazioni** dal menu **Strumenti** . Per altre informazioni, vedere [Personalizzare l'IDE di Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-add-or-remove-items-using-the-designer"></a>Per aggiungere o rimuovere elementi tramite la finestra di progettazione  
  
1.  Selezionare il controllo <xref:System.Windows.Forms.ListView>.  
  
2.  Nel **delle proprietà** finestra, fare clic sul **puntini di sospensione** (![schermata di VisualStudioEllipsesButton](../../../../docs/framework/winforms/media/vbellipsesbutton.png "vbEllipsesButton")) accanto alla il <xref:System.Windows.Forms.ListView.Items%2A> proprietà.  
  
     Il **Editor della raccolta ListViewItem** viene visualizzata.  
  
3.  Per aggiungere un elemento, scegliere il **Add** pulsante. È quindi possibile impostare le proprietà del nuovo elemento, ad esempio la <xref:System.Windows.Forms.ListView.Text%2A> e <xref:System.Windows.Forms.ListViewItem.ImageIndex%2A> proprietà.  
  
4.  Per rimuovere un elemento, selezionarlo e scegliere il **rimuovere** pulsante.  
  
## <a name="see-also"></a>Vedere anche  
 [Panoramica del controllo ListView](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)  
 [Procedura: Aggiungere colonne al controllo ListView di Windows Form](../../../../docs/framework/winforms/controls/how-to-add-columns-to-the-windows-forms-listview-control.md)  
 [Procedura: Visualizzare elementi secondari nelle colonne con il controllo ListView di Windows Form](../../../../docs/framework/winforms/controls/how-to-display-subitems-in-columns-with-the-windows-forms-listview-control.md)  
 [Procedura: Visualizzare icone per il controllo ListView di Windows Form](../../../../docs/framework/winforms/controls/how-to-display-icons-for-the-windows-forms-listview-control.md)  
 [Procedura: Aggiungere informazioni personalizzate a un controllo TreeView o ListView (Windows Form)](../../../../docs/framework/winforms/controls/add-custom-information-to-a-treeview-or-listview-control-wf.md)  
 [Procedura: Raggruppare elementi in un controllo ListView di Windows Form](../../../../docs/framework/winforms/controls/how-to-group-items-in-a-windows-forms-listview-control.md)
