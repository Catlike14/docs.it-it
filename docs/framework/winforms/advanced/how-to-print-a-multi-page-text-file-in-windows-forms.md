---
title: 'Procedura: stampare un file di testo con più pagine in Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- printing [Windows Forms], printing multiple pages
- text [Windows Forms], printing Windows Forms
- Windows Forms, printing text
- printing [Windows Forms], text
ms.assetid: 362427f8-03d4-4826-b49f-60ab066ad322
ms.openlocfilehash: b8cfba338bb318139bedf5595df8bad666c201bd
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/07/2018
ms.locfileid: "44084424"
---
# <a name="how-to-print-a-multi-page-text-file-in-windows-forms"></a>Procedura: stampare un file di testo con più pagine in Windows Form
La stampa di testo è un'operazione molto comune nelle applicazioni per Windows. La classe <xref:System.Drawing.Graphics> fornisce metodi per visualizzare oggetti (grafica o testo) su una periferica, ad esempio un monitor o una stampante.  
  
> [!NOTE]
>  I metodi <xref:System.Windows.Forms.TextRenderer.DrawText%2A> dell'oggetto <xref:System.Windows.Forms.TextRenderer> non sono supportati per la stampa. È consigliabile usare sempre i metodi <xref:System.Drawing.Graphics.DrawString%2A> dell'oggetto <xref:System.Drawing.Graphics>, come illustrato nell'esempio di codice seguente, per visualizzare il testo a scopo di stampa.  
  
### <a name="to-print-text"></a>Per stampare il test  
  
1.  Aggiungere un componente <xref:System.Drawing.Printing.PrintDocument> e una stringa al form.  
  
     [!code-csharp[System.Drawing.Printing.PrintExamples#8](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/CS/Form1.cs#8)]
     [!code-vb[System.Drawing.Printing.PrintExamples#8](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/VB/Form1.vb#8)]  
  
2.  Se si stampa un documento, impostare la proprietà <xref:System.Drawing.Printing.PrintDocument.DocumentName%2A> sul documento da stampare, quindi aprire e leggere il contenuto del documento fino alla stringa aggiunta in precedenza.  
  
     [!code-csharp[System.Drawing.Printing.PrintExamples#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/CS/Form1.cs#1)]
     [!code-vb[System.Drawing.Printing.PrintExamples#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/VB/Form1.vb#1)]  
  
3.  Nel gestore dell'evento <xref:System.Drawing.Printing.PrintDocument.PrintPage>, usare la proprietà <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> della classe <xref:System.Drawing.Printing.PrintPageEventArgs> e il contenuto del documento per calcolare la lunghezza delle righe e le righe per pagina. Dopo la generazione di ogni pagina, controllare se si tratta dell'ultima pagina e impostare la proprietà <xref:System.Drawing.Printing.PrintPageEventArgs.HasMorePages%2A> della classe <xref:System.Drawing.Printing.PrintPageEventArgs> di conseguenza. L'evento <xref:System.Drawing.Printing.PrintDocument.PrintPage> viene generato finché la proprietà <xref:System.Drawing.Printing.PrintPageEventArgs.HasMorePages%2A> non assume valore `false`. Assicurarsi inoltre che l'evento <xref:System.Drawing.Printing.PrintDocument.PrintPage> sia associato al relativo metodo di gestione degli eventi.  
  
     Nell'esempio di codice seguente il gestore eventi viene usato per stampare il contenuto del file "testPage.txt" con lo stesso tipo di carattere usato nel form.  
  
     [!code-csharp[System.Drawing.Printing.PrintExamples#2](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/CS/Form1.cs#2)]
     [!code-vb[System.Drawing.Printing.PrintExamples#2](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/VB/Form1.vb#2)]  
  
4.  Eseguire una chiamata al metodo <xref:System.Drawing.Printing.PrintDocument.Print%2A> per generare l'evento <xref:System.Drawing.Printing.PrintDocument.PrintPage>.  
  
     [!code-csharp[System.Drawing.Printing.PrintExamples#5](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/CS/Form1.cs#5)]
     [!code-vb[System.Drawing.Printing.PrintExamples#5](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/VB/Form1.vb#5)]  
  
## <a name="example"></a>Esempio  
 [!code-csharp[System.Drawing.Printing.PrintExamples#0](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/CS/Form1.cs#0)]
 [!code-vb[System.Drawing.Printing.PrintExamples#0](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Printing.PrintExamples/VB/Form1.vb#0)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Un file di testo denominato testPage.txt contenente il testo da stampare, situato nella radice dell'unità C:\\. Modificare il codice per stampare un file diverso.  
  
-   Riferimenti agli assembly System, System.Windows.Forms e System.Drawing.  
  
-   Per informazioni sulla compilazione di questo esempio dalla riga di comando per Visual Basic o Visual c#, vedere [compilazione dalla riga di comando](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oppure [con la creazione della riga di comando csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). È anche possibile compilare questo esempio in Visual Studio incollando il codice in un nuovo progetto.  Vedere anche [Procedura: Compilare ed eseguire un esempio di codice Windows Form completo tramite Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Drawing.Graphics>  
 <xref:System.Drawing.Brush>  
 [Supporto per la stampa in Windows Forms](../../../../docs/framework/winforms/advanced/windows-forms-print-support.md)
