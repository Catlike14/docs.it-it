---
title: 'Procedura: abilitare la visualizzazione affiancata in un controllo ListView di Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- tile view feature
- tiling
- Windows Forms, controls
- ListView control [Windows Forms], tile view
ms.assetid: c20e67a3-2d94-413d-9fcf-ecbd0fe251da
ms.openlocfilehash: 4eb418bbd2d399c57ce4a8235130a9939be56ce4
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43519522"
---
# <a name="how-to-enable-tile-view-in-a-windows-forms-listview-control"></a>Procedura: abilitare la visualizzazione affiancata in un controllo ListView di Windows Form
La funzionalità di visualizzazione affiancata del controllo <xref:System.Windows.Forms.ListView>, è possibile fornire un equilibrio visivo tra informazioni grafiche e testuali. Le informazioni testuali visualizzate per un elemento nella visualizzazione affiancata corrisponde alle informazioni della colonna definite per la visualizzazione dettagli. La visualizzazione affiancata viene usata in combinazione con le funzionalità di raggruppamento o segno di inserimento nel controllo <xref:System.Windows.Forms.ListView>.  
  
 La visualizzazione affiancata usa un'icona di 32 x 32 pixel e alcune righe di testo, come illustrato nelle immagini seguenti.  
  
 ![Visualizzazione affiancata in un controllo ListView](../../../../docs/framework/winforms/controls/media/listviewtile.gif "ListViewTile")  
Icone e testo di visualizzazione affiancata  
  
 Per abilitare la visualizzazione affiancata, impostare la proprietà <xref:System.Windows.Forms.ListView.View%2A> su <xref:System.Windows.Forms.View.Tile>. È possibile regolare la dimensione dei riquadri impostando la proprietà <xref:System.Windows.Forms.ListView.TileSize%2A> e il numero di righe di testo visualizzate nel riquadro regolando la raccolta <xref:System.Windows.Forms.ListView.Columns%2A>.  
  
> [!NOTE]
>  La visualizzazione affiancata è disponibile solo in [!INCLUDE[WinXpFamily](../../../../includes/winxpfamily-md.md)] quando l'applicazione chiama il metodo <xref:System.Windows.Forms.Application.EnableVisualStyles%2A?displayProperty=nameWithType>. Nei sistemi operativi precedenti, qualsiasi codice correlato alla visualizzazione affiancata non ha alcun effetto e il controllo <xref:System.Windows.Forms.ListView> viene visualizzato nella visualizzazione Icone grandi. Per altre informazioni, vedere <xref:System.Windows.Forms.ListView.View%2A?displayProperty=nameWithType>.  
  
### <a name="to-set-tile-view-programmatically"></a>Per impostare la visualizzazione affiancata a livello di codice  
  
1.  Usare l'enumerazione <xref:System.Windows.Forms.View> del controllo <xref:System.Windows.Forms.ListView>.  
  
    ```vb  
    ListView1.View = View.Tile  
    ```  
  
    ```csharp  
    listView1.View = View.Tile;  
    ```  
  
## <a name="example"></a>Esempio  
 L'esempio di codice completo seguente illustra la visualizzazione affiancata con riquadri modificati in modo da visualizzare tre righe di testo. La dimensione dei riquadri è stata modificata per evitare il ritorno a capo.  
  
 [!code-cpp[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CPP/listviewtilingexample.cpp#1)]
 [!code-csharp[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/CS/listviewtilingexample.cs#1)]
 [!code-vb[System.Windows.Forms.ListView.Tiling#1](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ListView.Tiling/VB/listviewtilingexample.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
 L'esempio presenta i requisiti seguenti:  
  
-   Riferimenti agli assembly System e System.Windows.Forms.  
  
-   Un file di icona denominato book.ico nella stessa directory del file eseguibile.  
  
 Per informazioni sulla compilazione di questo esempio dalla riga di comando per Visual Basic o Visual c#, vedere [compilazione dalla riga di comando](~/docs/visual-basic/reference/command-line-compiler/building-from-the-command-line.md) oppure [con la creazione della riga di comando csc.exe](~/docs/csharp/language-reference/compiler-options/command-line-building-with-csc-exe.md). È anche possibile compilare questo esempio in Visual Studio incollando il codice in un nuovo progetto.  Vedere anche [Procedura: Compilare ed eseguire un esempio di codice Windows Form completo tramite Visual Studio](https://msdn.microsoft.com/library/Bb129228\(v=vs.110\)).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Forms.ListView>  
 <xref:System.Windows.Forms.ListView.TileSize%2A>  
 [Controllo ListView](../../../../docs/framework/winforms/controls/listview-control-windows-forms.md)  
 [Panoramica del controllo ListView](../../../../docs/framework/winforms/controls/listview-control-overview-windows-forms.md)  
 [Funzionalità di Windows XP e controlli di Windows Forms](https://msdn.microsoft.com/library/bc7fab94-fce9-4bf1-a8ad-a5837c91c3c0)
