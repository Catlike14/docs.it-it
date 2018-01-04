---
title: 'Procedura: applicare un oggetto Material alle parti anteriore e posteriore di un oggetto tridimensionale'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- 3-D objects [WPF], applying Material class
- Material class [WPF], applying to both sides of 3-D object
- classes [WPF], Material
ms.assetid: d93c8ad6-4939-4d29-9544-4d16d98093c1
caps.latest.revision: "5"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c5ead8805c3d16bc16e259bdf90a19f05500563c
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-apply-material-to-the-front-and-back-of-a-3-d-object"></a><span data-ttu-id="db841-102">Procedura: applicare un oggetto Material alle parti anteriore e posteriore di un oggetto tridimensionale</span><span class="sxs-lookup"><span data-stu-id="db841-102">How to: Apply Material to the Front and Back of a 3-D Object</span></span>
<span data-ttu-id="db841-103">Nell'esempio seguente viene illustrato come applicare un <xref:System.Windows.Media.Media3D.Material> nella parte anteriore e posteriore di un oggetto 3D dell'oggetto e animare l'oggetto per visualizzare entrambi i lati dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="db841-103">The following example shows how to apply a <xref:System.Windows.Media.Media3D.Material> to the front and back of a 3-D object and animate the object to show both sides of the object.</span></span> <span data-ttu-id="db841-104">Il <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> proprietà di un <xref:System.Windows.Media.Media3D.GeometryModel3D> viene utilizzato per applicare un colore rosso <xref:System.Windows.Media.Brush> per il lato anteriore dell'oggetto e <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> proprietà del <xref:System.Windows.Media.Media3D.GeometryModel3D> viene utilizzato per applicare un blu <xref:System.Windows.Media.Brush> al lato posteriore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="db841-104">The <xref:System.Windows.Media.Media3D.GeometryModel3D.Material%2A> property of a <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a red <xref:System.Windows.Media.Brush> to the front side of the object and the <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> property of the <xref:System.Windows.Media.Media3D.GeometryModel3D> is used to apply a blue <xref:System.Windows.Media.Brush> to the back side of the object.</span></span> <span data-ttu-id="db841-105">Il codice riportato di seguito viene illustrata l'applicazione dei materiali all'oggetto:</span><span class="sxs-lookup"><span data-stu-id="db841-105">The code below shows the application of the materials to the object:</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexampleinline1)]  
  
## <a name="example"></a><span data-ttu-id="db841-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="db841-106">Example</span></span>  
 <span data-ttu-id="db841-107">Il codice seguente viene illustrato l'esempio completo.</span><span class="sxs-lookup"><span data-stu-id="db841-107">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[Animation3DGallery_snip#BackMaterialAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/BackMaterialAnimationExample.xaml#backmaterialanimationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="db841-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="db841-108">See Also</span></span>  
 [<span data-ttu-id="db841-109">Creare una scena tridimensionale</span><span class="sxs-lookup"><span data-stu-id="db841-109">Create a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [<span data-ttu-id="db841-110">Panoramica sulla grafica tridimensionale</span><span class="sxs-lookup"><span data-stu-id="db841-110">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)  
 [<span data-ttu-id="db841-111">Animare le proprietà Material in una scena tridimensionale</span><span class="sxs-lookup"><span data-stu-id="db841-111">Animate Material Properties in a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-material-properties-in-a-3-d-scene.md)  
 [<span data-ttu-id="db841-112">Applicare materiale con componente emissiva a un oggetto tridimensionale</span><span class="sxs-lookup"><span data-stu-id="db841-112">Apply Emissive Material to a 3-D Object</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-apply-emissive-material-to-a-3-d-object.md)
