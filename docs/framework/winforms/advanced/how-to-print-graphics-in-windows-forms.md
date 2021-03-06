---
title: 'Procedura: stampare grafica in Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], printing
- printing [Windows Forms], graphics
ms.assetid: 32b891e6-52ff-4fea-a9ff-2ce5db20a4c6
ms.openlocfilehash: 8281e1e0a3d350c3b81e26bbe59c098536ef064e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33521498"
---
# <a name="how-to-print-graphics-in-windows-forms"></a>Procedura: stampare grafica in Windows Form
Spesso, è possibile stampare grafica nell'applicazione basata su Windows. La <xref:System.Drawing.Graphics> classe fornisce metodi per disegnare oggetti in un dispositivo, ad esempio un monitor o una stampante.  
  
### <a name="to-print-graphics"></a>Per stampare la grafica  
  
1.  Aggiungere un <xref:System.Drawing.Printing.PrintDocument> componente al form.  
  
2.  Nel <xref:System.Drawing.Printing.PrintDocument.PrintPage> gestore dell'evento, utilizzare il <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> proprietà del <xref:System.Drawing.Printing.PrintPageEventArgs> classe per indicare la stampante nella quale tipo di grafica da stampare.  
  
     Esempio di codice seguente viene illustrato un gestore eventi utilizzato per creare un'ellisse blu all'interno di un rettangolo di delimitazione. Il rettangolo è il percorso e delle dimensioni seguenti: a partire da 100, 150 con una larghezza pari a 250 e un'altezza pari a 250.  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillEllipse(Brushes.Blue, New Rectangle(100, 150, 250, 250))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,   
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Blue,   
         new Rectangle(100, 150, 250, 250));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Blue,  
             Rectangle(100, 150, 250, 250));  
       }  
    ```  
  
     (Visual c# e [!INCLUDE[vcprvc](../../../../includes/vcprvc-md.md)]) inserire il codice seguente nel costruttore del form per registrare il gestore dell'evento.  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    this->printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Drawing.Graphics>  
 <xref:System.Drawing.Brush>  
 [Supporto per la stampa in Windows Forms](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)
