---
title: 'Procedura: animare lo spessore di un bordo utilizzando frame chiave'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: a601fd6779a4d912166366652435aff9ae37613f
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2018
ms.locfileid: "43421410"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a>Procedura: animare lo spessore di un bordo utilizzando frame chiave
In questo esempio illustra come animare la <xref:System.Windows.Controls.Control.BorderThickness%2A> proprietà di un <xref:System.Windows.Controls.Border>.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente usa il <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> classe per animare la <xref:System.Windows.Controls.Control.BorderThickness%2A> proprietà di un <xref:System.Windows.Controls.Border>. Questa animazione usa tre fotogrammi chiave nel modo seguente:  
  
1.  Il primo mezzo secondo viene usata un'istanza del <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> classe per aumentare gradualmente lo spessore del bordo. L'esempio Usa <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> per creare un aumento lineare uniforme tra i valori.  
  
2.  Alla fine del successivo mezzo secondo viene usata un'istanza del <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> classe per aumentare rapidamente lo spessore del bordo. Fotogrammi chiave discreti come quelli derivati da <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> creano salti improvvisi tra valori, vale a dire, lo spostamento dell'animazione è a scatti.  
  
3.  I due secondi finali viene usata un'istanza del <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> classe per diminuire gradualmente lo spessore del bordo. I fotogrammi chiave spline come quelli derivati da <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> creano una transizione variabile tra i valori a seconda dei valori del <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> proprietà. In questo fotogramma chiave l'animazione inizia a spostarsi lentamente, quindi accelera in modo esponenziale verso la fine del segmento temporale.  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](../../../../samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 Per l'esempio completo, vedere [Esempio di animazione con fotogrammi chiave](https://go.microsoft.com/fwlink/?LinkID=160012).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>  
 <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>  
 <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>  
 [Cenni preliminari sulle animazioni con fotogrammi chiave](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animations-overview.md)  
 [Procedure relative ai fotogrammi chiave](../../../../docs/framework/wpf/graphics-multimedia/key-frame-animation-how-to-topics.md)  
 [Animare un valore BorderThickness](../../../../docs/framework/wpf/controls/how-to-animate-a-borderthickness-value.md)
