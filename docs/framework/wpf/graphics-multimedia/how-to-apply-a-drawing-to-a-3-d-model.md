---
title: 'Procedura: applicare un disegno a un modello tridimensionale'
ms.date: 03/30/2017
helpviewer_keywords:
- drawings [WPF], applying to 3-D models
- 3-D models [WPF], applying drawings to
ms.assetid: 68357577-b7fc-446e-8be9-a8cc7df3a350
ms.openlocfilehash: 26a84d963cac3b5c23617bfaa23279021e29c07a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559064"
---
# <a name="how-to-apply-a-drawing-to-a-3-d-model"></a><span data-ttu-id="f39db-102">Procedura: applicare un disegno a un modello tridimensionale</span><span class="sxs-lookup"><span data-stu-id="f39db-102">How to: Apply a Drawing to a 3-D Model</span></span>
<span data-ttu-id="f39db-103">In questo esempio viene illustrato come utilizzare un <xref:System.Windows.Media.DrawingBrush> come il <xref:System.Windows.Media.Media3D.Material> applicato a un [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] modello.</span><span class="sxs-lookup"><span data-stu-id="f39db-103">This example shows how to use a <xref:System.Windows.Media.DrawingBrush> as the <xref:System.Windows.Media.Media3D.Material> applied to a [!INCLUDE[TLA#tla_3d](../../../../includes/tlasharptla-3d-md.md)] model.</span></span>  
  
 <span data-ttu-id="f39db-104">Il codice seguente definisce un <xref:System.Windows.Media.DrawingGroup> come contenuto di un <xref:System.Windows.Media.DrawingBrush>.</span><span class="sxs-lookup"><span data-stu-id="f39db-104">The following code defines a <xref:System.Windows.Media.DrawingGroup> as the content of a <xref:System.Windows.Media.DrawingBrush>.</span></span>  <span data-ttu-id="f39db-105">Il <xref:System.Windows.Media.DrawingBrush> è impostato come il <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> proprietà del <xref:System.Windows.Media.Media3D.DiffuseMaterial> applicato a un [!INCLUDE[TLA2#tla_3d](../../../../includes/tla2sharptla-3d-md.md)] piano.</span><span class="sxs-lookup"><span data-stu-id="f39db-105">The <xref:System.Windows.Media.DrawingBrush> is set as the <xref:System.Windows.Media.Media3D.DiffuseMaterial.Brush%2A> property of the <xref:System.Windows.Media.Media3D.DiffuseMaterial> applied to a [!INCLUDE[TLA2#tla_3d](../../../../includes/tla2sharptla-3d-md.md)] plane.</span></span>  
  
 <span data-ttu-id="f39db-106">**Nota:** è spesso opportuno definire oggetti complessi e i valori come il disegno sotto come risorse che possono essere riutilizzate e semplificano il codice.</span><span class="sxs-lookup"><span data-stu-id="f39db-106">**Note:** It is often desirable to define complex objects and values like the drawing below as resources which can be reused and simplify your code.</span></span> <span data-ttu-id="f39db-107">Vedere [risorse XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md) per ulteriori informazioni.</span><span class="sxs-lookup"><span data-stu-id="f39db-107">See [XAML Resources](../../../../docs/framework/wpf/advanced/xaml-resources.md) for more information.</span></span>  
  
 [!code-xaml[3DGallery_snip#ApplyDrawingToMaterialInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialinline1)]  
  
## <a name="example"></a><span data-ttu-id="f39db-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="f39db-108">Example</span></span>  
 <span data-ttu-id="f39db-109">Il codice seguente viene illustrato l'esempio completo.</span><span class="sxs-lookup"><span data-stu-id="f39db-109">The following code shows the entire sample.</span></span>  
  
 [!code-xaml[3DGallery_snip#ApplyDrawingToMaterialExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_snip/CS/ApplyDrawingToMaterialExample.xaml#applydrawingtomaterialexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="f39db-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f39db-110">See Also</span></span>  
 [<span data-ttu-id="f39db-111">Risorse XAML</span><span class="sxs-lookup"><span data-stu-id="f39db-111">XAML Resources</span></span>](../../../../docs/framework/wpf/advanced/xaml-resources.md)  
 [<span data-ttu-id="f39db-112">Creare una scena tridimensionale</span><span class="sxs-lookup"><span data-stu-id="f39db-112">Create a 3-D Scene</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)  
 [<span data-ttu-id="f39db-113">Cenni preliminari sugli oggetti Drawing</span><span class="sxs-lookup"><span data-stu-id="f39db-113">Drawing Objects Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/drawing-objects-overview.md)  
 [<span data-ttu-id="f39db-114">Panoramica sulla grafica tridimensionale</span><span class="sxs-lookup"><span data-stu-id="f39db-114">3-D Graphics Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
