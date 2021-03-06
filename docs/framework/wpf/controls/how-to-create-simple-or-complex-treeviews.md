---
title: 'Procedura: creare controlli TreeView semplici o complessi'
ms.date: 03/30/2017
helpviewer_keywords:
- TreeView control [WPF], creating
- Control class [WPF], TreeView [WPF], creating
ms.assetid: 1defbb78-b8e7-4c0e-b650-576453ac828d
ms.openlocfilehash: 54e9218ea1460a0c29d8b9d7b9c740c18ac7ab24
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33552998"
---
# <a name="how-to-create-simple-or-complex-treeviews"></a>Procedura: creare controlli TreeView semplici o complessi
In questo esempio viene illustrato come creare semplici o complesse <xref:System.Windows.Controls.TreeView> controlli.  
  
 Oggetto <xref:System.Windows.Controls.TreeView> è costituito da una gerarchia di <xref:System.Windows.Controls.TreeViewItem> controlli che possono contenere semplici stringhe di testo e contenuto anche più complesso, ad esempio <xref:System.Windows.Controls.Button> controlli o <xref:System.Windows.Controls.StackPanel> con contenuto incorporato. È possibile definire in modo esplicito il <xref:System.Windows.Controls.TreeView> contenuto o un'origine dati può fornire il contenuto. In questo argomento vengono forniti esempi di questi concetti.  
  
## <a name="example"></a>Esempio  
 Il <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> proprietà del <xref:System.Windows.Controls.TreeViewItem> il contenuto che il <xref:System.Windows.Controls.TreeView> Visualizza per quell'elemento. Oggetto <xref:System.Windows.Controls.TreeViewItem> può anche avere <xref:System.Windows.Controls.TreeViewItem> controlli come elementi figlio ed è possono definire gli elementi figlio tramite la <xref:System.Windows.Controls.ItemsControl.Items%2A> proprietà.  
  
 Nell'esempio seguente viene illustrato come definire in modo esplicito <xref:System.Windows.Controls.TreeViewItem> contenuto impostando il <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> proprietà in una stringa di testo.  
  
 [!code-xaml[TreeViewSimple#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#1)]  
  
 Nell'esempio seguente viene illustrato come definire gli elementi figlio di un <xref:System.Windows.Controls.TreeViewItem> definendo <xref:System.Windows.Controls.ItemsControl.Items%2A> che sono <xref:System.Windows.Controls.Button> controlli.  
  
 [!code-xaml[TreeViewSimple#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#3)]  
  
 Nell'esempio seguente viene illustrato come creare un <xref:System.Windows.Controls.TreeView> in cui un <xref:System.Windows.Data.XmlDataProvider> fornisce <xref:System.Windows.Controls.TreeViewItem> contenuto e un <xref:System.Windows.HierarchicalDataTemplate> definisce l'aspetto del contenuto.  
  
 [!code-xaml[TreeViewSimple#6](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#6)]  
  
 [!code-xaml[TreeViewSimple#7](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#7)]  
  
 [!code-xaml[TreeViewSimple#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#5)]  
  
 Nell'esempio seguente viene illustrato come creare un <xref:System.Windows.Controls.TreeView> in cui il <xref:System.Windows.Controls.TreeViewItem> contenuto contiene <xref:System.Windows.Controls.DockPanel> controlli con contenuto incorporato.  
  
 [!code-xaml[TreeViewSimple#9](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeViewSimple/CS/Window1.xaml#9)]  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Controls.TreeView>  
 <xref:System.Windows.Controls.TreeViewItem>  
 [Panoramica sul controllo TreeView](../../../../docs/framework/wpf/controls/treeview-overview.md)  
 [Procedure relative alle proprietà](../../../../docs/framework/wpf/controls/treeview-how-to-topics.md)
