---
title: 'Procedura: creare uno StackPanel'
ms.date: 03/30/2017
helpviewer_keywords:
- StackPanel control [WPF], creating
ms.assetid: e7ce65cb-720a-4bb6-95b6-286b74488a58
ms.openlocfilehash: 30f24d8dba7c09271a5957822439af6b64e05aca
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33553027"
---
# <a name="how-to-create-a-stackpanel"></a>Procedura: creare uno StackPanel
In questo esempio viene illustrato come creare un <xref:System.Windows.Controls.StackPanel>.  
  
## <a name="example"></a>Esempio  
 Oggetto <xref:System.Windows.Controls.StackPanel> consente di sovrapposizione di elementi in una direzione specificata. Utilizzando le proprietà definite su <xref:System.Windows.Controls.StackPanel>, il contenuto può fluire in verticale, ovvero l'impostazione predefinita, orizzontalmente o verticalmente.  
  
 Nell'esempio riportato in uno stack verticale cinque <xref:System.Windows.Controls.TextBlock> controlli, ognuno con un altro <xref:System.Windows.Controls.Border> e <xref:System.Windows.Controls.Border.Background%2A>, utilizzando <xref:System.Windows.Controls.StackPanel>. Gli elementi figlio che non hanno alcuna specificato <xref:System.Windows.FrameworkElement.Width%2A> adattata per riempire la finestra padre; tuttavia, gli elementi figlio che dispone di un oggetto specificato <xref:System.Windows.FrameworkElement.Width%2A>, è centrato all'interno della finestra.  
  
 La direzione predefinita dello stack in un <xref:System.Windows.Controls.StackPanel> è verticale. Al controllo di flusso contenuto in un <xref:System.Windows.Controls.StackPanel>, utilizzare il <xref:System.Windows.Controls.StackPanel.Orientation%2A> proprietà. È possibile controllare l'allineamento orizzontale tramite la <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> proprietà.  
  
```xaml  
<Page xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" WindowTitle="StackPanel Sample">  
  <StackPanel>  
    <Border Background="SkyBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="12">Stacked Item #1</TextBlock>  
    </Border>  
    <Border Width="400" Background="CadetBlue" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="14">Stacked Item #2</TextBlock>  
    </Border>  
    <Border Background="LightGoldenRodYellow" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="16">Stacked Item #3</TextBlock>  
    </Border>  
    <Border Width="200" Background="PaleGreen" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="18">Stacked Item #4</TextBlock>  
    </Border>  
    <Border Background="White" BorderBrush="Black" BorderThickness="1">  
      <TextBlock Foreground="Black" FontSize="20">Stacked Item #5</TextBlock>  
    </Border>  
  </StackPanel>  
</Page>  
```  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Controls.StackPanel>  
 [Cenni preliminari sugli elementi Panel](../../../../docs/framework/wpf/controls/panels-overview.md)  
 [Procedure relative alle proprietà](../../../../docs/framework/wpf/controls/stackpanel-how-to-topics.md)
