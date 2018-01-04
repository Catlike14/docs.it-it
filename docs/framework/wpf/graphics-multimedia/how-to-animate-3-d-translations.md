---
title: 'Procedura: aggiungere un''animazione alle traslazioni tridimensionali'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- animation [WPF], 3-D translations
- 3-D translations [WPF], animating
ms.assetid: d4eece1f-0cd2-4a2c-8370-293354c380e4
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: d49ad52906787eed9ab115adeb763b89b2ea38e0
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-animate-3-d-translations"></a><span data-ttu-id="ce061-102">Procedura: aggiungere un'animazione alle traslazioni tridimensionali</span><span class="sxs-lookup"><span data-stu-id="ce061-102">How to: Animate 3-D Translations</span></span>
<span data-ttu-id="ce061-103">In questo argomento viene illustrato come aggiungere un'animazione a una trasformazione conversione impostata su un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modello.</span><span class="sxs-lookup"><span data-stu-id="ce061-103">This topic demonstrates how to animate a translation transformation set on a [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] model.</span></span>  
  
 <span data-ttu-id="ce061-104">Il codice seguente viene illustrata l'applicazione di un <xref:System.Windows.Media.Media3D.TranslateTransform3D> dell'oggetto per il <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> proprietà di un <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span><span class="sxs-lookup"><span data-stu-id="ce061-104">The code below shows the application of a <xref:System.Windows.Media.Media3D.TranslateTransform3D> object to the <xref:System.Windows.Media.Media3D.Model3D.Transform%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D>.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline1)]  
  
 <span data-ttu-id="ce061-105">Il <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> proprietà di questo <xref:System.Windows.Media.Media3D.TranslateTransform3D> oggetto animato utilizzando il codice riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="ce061-105">The <xref:System.Windows.Media.Media3D.TranslateTransform3D.OffsetX%2A> property of this <xref:System.Windows.Media.Media3D.TranslateTransform3D> object is animated using the code below.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationInline2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationinline2)]  
  
## <a name="example"></a><span data-ttu-id="ce061-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="ce061-106">Example</span></span>  
 <span data-ttu-id="ce061-107">Il codice seguente viene illustrato l'esempio completo.</span><span class="sxs-lookup"><span data-stu-id="ce061-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#Translation3DAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/Translation3DAnimationExample.xaml#translation3danimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="ce061-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ce061-108">See Also</span></span>  
 [<span data-ttu-id="ce061-109">Cenni preliminari sull'animazione</span><span class="sxs-lookup"><span data-stu-id="ce061-109">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)  
 [<span data-ttu-id="ce061-110">Creare una scena tridimensionale</span><span class="sxs-lookup"><span data-stu-id="ce061-110">Create a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [<span data-ttu-id="ce061-111">Panoramica sulla grafica tridimensionale</span><span class="sxs-lookup"><span data-stu-id="ce061-111">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)  
 [<span data-ttu-id="ce061-112">Cenni preliminari sulle trasformazioni</span><span class="sxs-lookup"><span data-stu-id="ce061-112">Transforms Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
