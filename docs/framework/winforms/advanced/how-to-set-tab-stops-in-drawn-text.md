---
title: 'Procedura: impostare punti di tabulazione nel testo disegnato'
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
helpviewer_keywords:
- text [Windows Forms], drawing with tab stops
- tabs [Windows Forms], drawn text
ms.assetid: 64878f98-39ba-4303-b63f-0859ab682eeb
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: e561e8096780301230071e869dac482a6a908a5e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-set-tab-stops-in-drawn-text"></a><span data-ttu-id="7d4da-102">Procedura: impostare punti di tabulazione nel testo disegnato</span><span class="sxs-lookup"><span data-stu-id="7d4da-102">How to: Set Tab Stops in Drawn Text</span></span>
<span data-ttu-id="7d4da-103">È possibile impostare punti di tabulazione per il testo chiamando il <xref:System.Drawing.StringFormat.SetTabStops%2A> metodo di un <xref:System.Drawing.StringFormat> oggetto e quindi passando il <xref:System.Drawing.StringFormat> dell'oggetto per il <xref:System.Drawing.Graphics.DrawString%2A> metodo la <xref:System.Drawing.Graphics> classe.</span><span class="sxs-lookup"><span data-stu-id="7d4da-103">You can set tab stops for text by calling the <xref:System.Drawing.StringFormat.SetTabStops%2A> method of a <xref:System.Drawing.StringFormat> object and then passing that <xref:System.Drawing.StringFormat> object to the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="7d4da-104">Il <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> fa uso non supporta l'aggiunta di punti di tabulazione al testo disegnato, sebbene sia possibile espandere una scheda esistente viene interrotto il <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> flag.</span><span class="sxs-lookup"><span data-stu-id="7d4da-104">The <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> does not support adding tab stops to drawn text, although you can expand existing tab stops using the <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> flag.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d4da-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="7d4da-105">Example</span></span>  
 <span data-ttu-id="7d4da-106">Nell'esempio seguente imposta punti di tabulazione in corrispondenza di 150, 250 e 350.</span><span class="sxs-lookup"><span data-stu-id="7d4da-106">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="7d4da-107">Quindi, il codice visualizza un elenco dei nomi e i punteggi di test.</span><span class="sxs-lookup"><span data-stu-id="7d4da-107">Then, the code displays a tabbed list of names and test scores.</span></span>  
  
 <span data-ttu-id="7d4da-108">Nella figura seguente mostra il testo a schede.</span><span class="sxs-lookup"><span data-stu-id="7d4da-108">The following illustration shows the tabbed text.</span></span>  
  
 <span data-ttu-id="7d4da-109">![Tipi di carattere testo](../../../../docs/framework/winforms/advanced/media/fontstext4.png "fontstext4")</span><span class="sxs-lookup"><span data-stu-id="7d4da-109">![Fonts Text](../../../../docs/framework/winforms/advanced/media/fontstext4.png "fontstext4")</span></span>  
  
 <span data-ttu-id="7d4da-110">Il codice seguente passa due argomenti per il <xref:System.Drawing.StringFormat.SetTabStops%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="7d4da-110">The following code passes two arguments to the <xref:System.Drawing.StringFormat.SetTabStops%2A> method.</span></span> <span data-ttu-id="7d4da-111">Il secondo argomento è una matrice che contiene gli offset di tabulazione.</span><span class="sxs-lookup"><span data-stu-id="7d4da-111">The second argument is an array that contains tab offsets.</span></span> <span data-ttu-id="7d4da-112">Il primo argomento passato a <xref:System.Drawing.StringFormat.SetTabStops%2A> è 0, che indica che il primo offset nella matrice viene misurato dalla posizione 0, il bordo sinistro del rettangolo di delimitazione.</span><span class="sxs-lookup"><span data-stu-id="7d4da-112">The first argument passed to <xref:System.Drawing.StringFormat.SetTabStops%2A> is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#41](../../../../samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.FontsAndText#41](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="7d4da-113">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="7d4da-113">Compiling the Code</span></span>  
  
-   <span data-ttu-id="7d4da-114">L'esempio precedente è progettato per l'uso con Windows Form e richiede <xref:System.Windows.Forms.PaintEventArgs> `e`, un parametro di <xref:System.Windows.Forms.PaintEventHandler>.</span><span class="sxs-lookup"><span data-stu-id="7d4da-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d4da-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7d4da-115">See Also</span></span>  
 [<span data-ttu-id="7d4da-116">Uso di tipi di carattere e testo</span><span class="sxs-lookup"><span data-stu-id="7d4da-116">Using Fonts and Text</span></span>](../../../../docs/framework/winforms/advanced/using-fonts-and-text.md)  
 [<span data-ttu-id="7d4da-117">Procedura: Creare testo con GDI</span><span class="sxs-lookup"><span data-stu-id="7d4da-117">How to: Draw Text with GDI</span></span>](../../../../docs/framework/winforms/advanced/how-to-draw-text-with-gdi.md)
