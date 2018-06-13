---
title: 'Procedura: creare una forma composta'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- shapes [WPF], composite
- composite shapes [WPF]
- graphics [WPF], composite shapes
ms.assetid: 8e5c7ef4-d7ed-4c43-afc9-ca01325c300b
ms.openlocfilehash: 6bb2a8a32938682af52343b971b840dbed16bcef
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33559970"
---
# <a name="how-to-create-a-composite-shape"></a><span data-ttu-id="4049f-102">Procedura: creare una forma composta</span><span class="sxs-lookup"><span data-stu-id="4049f-102">How to: Create a Composite Shape</span></span>
<span data-ttu-id="4049f-103">In questo esempio viene illustrato come creare forme composte tramite <xref:System.Windows.Media.Geometry> oggetti e visualizzarle utilizzando un <xref:System.Windows.Shapes.Path> elemento.</span><span class="sxs-lookup"><span data-stu-id="4049f-103">This example shows how to create composite shapes using <xref:System.Windows.Media.Geometry> objects and display them using a <xref:System.Windows.Shapes.Path> element.</span></span> <span data-ttu-id="4049f-104">Nell'esempio seguente, un <xref:System.Windows.Media.LineGeometry>, <xref:System.Windows.Media.EllipseGeometry>e un <xref:System.Windows.Media.RectangleGeometry> vengono utilizzati con un <xref:System.Windows.Media.GeometryGroup> per creare una forma composta.</span><span class="sxs-lookup"><span data-stu-id="4049f-104">In the following example, a <xref:System.Windows.Media.LineGeometry>, <xref:System.Windows.Media.EllipseGeometry>, and a <xref:System.Windows.Media.RectangleGeometry> are used with a <xref:System.Windows.Media.GeometryGroup> to create a composite shape.</span></span> <span data-ttu-id="4049f-105">Quindi vengono tracciate le geometrie utilizzando un <xref:System.Windows.Shapes.Path> elemento.</span><span class="sxs-lookup"><span data-stu-id="4049f-105">The geometries are then drawn using a <xref:System.Windows.Shapes.Path> element.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4049f-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="4049f-106">Example</span></span>  
 [!code-xaml[GeometrySample#19](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#19)]  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/CompositeShapeExample.cs#compositeshapecodeexampleinline1)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/compositeshapeexample.vb#compositeshapecodeexampleinline1)]  
  
 <span data-ttu-id="4049f-107">La figura seguente mostra la forma creata nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="4049f-107">The following illustration shows the shape created in the previous example.</span></span>  
  
 <span data-ttu-id="4049f-108">![Geometria composta creata con GeometryGroup](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")</span><span class="sxs-lookup"><span data-stu-id="4049f-108">![A composite geometry created using a GeometryGroup](../../../../docs/framework/wpf/graphics-multimedia/media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")</span></span>  
<span data-ttu-id="4049f-109">Geometria composta</span><span class="sxs-lookup"><span data-stu-id="4049f-109">Composite Geometry</span></span>  
  
 <span data-ttu-id="4049f-110">Le forme più complesse, ad esempio poligoni e forme con segmenti curvi, possono essere create tramite un <xref:System.Windows.Media.PathGeometry>.</span><span class="sxs-lookup"><span data-stu-id="4049f-110">More complex shapes, such as polygons and shapes with curved segments, may be created using a <xref:System.Windows.Media.PathGeometry>.</span></span> <span data-ttu-id="4049f-111">Per un esempio che illustra come creare una forma utilizzando un <xref:System.Windows.Media.PathGeometry>, vedere [creare una forma con PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md).</span><span class="sxs-lookup"><span data-stu-id="4049f-111">For an example showing how to create a shape using a <xref:System.Windows.Media.PathGeometry>, see [Create a Shape by Using a PathGeometry](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-shape-by-using-a-pathgeometry.md).</span></span>  <span data-ttu-id="4049f-112">Sebbene in questo esempio viene eseguito il rendering di una forma sullo schermo utilizzando un <xref:System.Windows.Shapes.Path> elemento <xref:System.Windows.Media.Geometry> gli oggetti possono essere utilizzati anche per descrivere il contenuto di un <xref:System.Windows.Media.GeometryDrawing> o un <xref:System.Windows.Media.DrawingContext>.</span><span class="sxs-lookup"><span data-stu-id="4049f-112">Although this example renders a shape to the screen using a <xref:System.Windows.Shapes.Path> element, <xref:System.Windows.Media.Geometry> objects may also be used to describe the contents of a <xref:System.Windows.Media.GeometryDrawing> or a <xref:System.Windows.Media.DrawingContext>.</span></span> <span data-ttu-id="4049f-113">Potrebbe inoltre essere utilizzati per il ritaglio e hit testing.</span><span class="sxs-lookup"><span data-stu-id="4049f-113">They may also be used for clipping and hit-testing.</span></span>  
  
 <span data-ttu-id="4049f-114">Questo esempio fa parte di un esempio più esaustivo. Per l'esempio completo, vedere la pagina [Geometries Sample (esempio di geometrie)](http://go.microsoft.com/fwlink/?LinkID=159989).</span><span class="sxs-lookup"><span data-stu-id="4049f-114">This example is part of larger sample; for the complete sample, see the [Geometries Sample](http://go.microsoft.com/fwlink/?LinkID=159989).</span></span>
