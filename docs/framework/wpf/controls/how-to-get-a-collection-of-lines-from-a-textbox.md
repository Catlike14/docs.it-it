---
title: 'Procedura: ottenere una raccolta di righe da un controllo TextBox'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- lines [WPF], getting collection of
- TextBox control [WPF], getting collection of lines
ms.assetid: a12f529d-b926-47f6-92bf-cad5f17b532a
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: bb771cdb4d12ebaa5160ec16ca57ba6acf011222
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-get-a-collection-of-lines-from-a-textbox"></a>Procedura: ottenere una raccolta di righe da un controllo TextBox
In questo esempio viene illustrato come ottenere una raccolta di righe di testo da un <xref:System.Windows.Controls.TextBox>.  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene illustrato un semplice metodo che accetta un <xref:System.Windows.Controls.TextBox> come argomento e restituisce un <xref:System.Collections.Specialized.StringCollection> contenente le righe di testo di **TextBox**.  Il <xref:System.Windows.Controls.TextBox.LineCount%2A> proprietà viene utilizzata per determinare il numero di righe incluse nel **TextBox**e <xref:System.Windows.Controls.TextBox.GetLineText%2A> metodo viene quindi utilizzato per estrarre ciascuna riga e aggiungerlo alla raccolta di righe.  
  
 [!code-csharp[TextBox_MiscCode#_TextBox_GetLines](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TextBox_MiscCode/CSharp/Window1.xaml.cs#_textbox_getlines)]  
  
## <a name="see-also"></a>Vedere anche  
 [Cenni preliminari sulla classe TextBox](../../../../docs/framework/wpf/controls/textbox-overview.md)  
 [Cenni preliminari sul controllo RichTextBox](../../../../docs/framework/wpf/controls/richtextbox-overview.md)
