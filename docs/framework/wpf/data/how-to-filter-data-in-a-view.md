---
title: 'Procedura: filtrare i dati in una visualizzazione'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- views [WPF], filtering data
- filtering data in views [WPF]
- data binding [WPF], filtering data in views
ms.assetid: c76e8606-4cc4-45a8-9110-e2ec66dc6afd
caps.latest.revision: "16"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 17b7fc68319552a7b31d5eaf7826146de5c41aa5
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-filter-data-in-a-view"></a><span data-ttu-id="724b8-102">Procedura: filtrare i dati in una visualizzazione</span><span class="sxs-lookup"><span data-stu-id="724b8-102">How to: Filter Data in a View</span></span>
<span data-ttu-id="724b8-103">In questo esempio viene illustrato come filtrare i dati in una vista.</span><span class="sxs-lookup"><span data-stu-id="724b8-103">This example shows how to filter data in a view.</span></span>  
  
## <a name="example"></a><span data-ttu-id="724b8-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="724b8-104">Example</span></span>  
 <span data-ttu-id="724b8-105">Per creare un filtro, definire un metodo che fornisce la logica di filtro.</span><span class="sxs-lookup"><span data-stu-id="724b8-105">To create a filter, define a method that provides the filtering logic.</span></span> <span data-ttu-id="724b8-106">Il metodo viene utilizzato come un callback e accetta un parametro di tipo `object`.</span><span class="sxs-lookup"><span data-stu-id="724b8-106">The method is used as a callback and accepts a parameter of type `object`.</span></span> <span data-ttu-id="724b8-107">Il metodo seguente restituisce tutti i `Order` gli oggetti con il `filled` proprietà è impostata su "No", per escludere il resto degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="724b8-107">The following method returns all the `Order` objects with the `filled` property set to "No", filtering out the rest of the objects.</span></span>  
  
 [!code-csharp[SortFilter#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#2)]
 [!code-vb[SortFilter#2](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#2)]  
  
 <span data-ttu-id="724b8-108">È quindi possibile applicare il filtro, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="724b8-108">You can then apply the filter, as shown in the following example.</span></span> <span data-ttu-id="724b8-109">In questo esempio, `myCollectionView` è un <xref:System.Windows.Data.ListCollectionView> oggetto.</span><span class="sxs-lookup"><span data-stu-id="724b8-109">In this example, `myCollectionView` is a <xref:System.Windows.Data.ListCollectionView> object.</span></span>  
  
 [!code-csharp[SortFilter#Filter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#filter)]
 [!code-vb[SortFilter#Filter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#filter)]  
  
 <span data-ttu-id="724b8-110">Per rimuovere il filtro, è possibile impostare il <xref:System.Windows.Data.CollectionView.Filter%2A> proprietà `null`:</span><span class="sxs-lookup"><span data-stu-id="724b8-110">To undo filtering, you can set the <xref:System.Windows.Data.CollectionView.Filter%2A> property to `null`:</span></span>  
  
 [!code-csharp[SortFilter#Unfilter](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SortFilter/CSharp/Page1.xaml.cs#unfilter)]
 [!code-vb[SortFilter#Unfilter](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/SortFilter/VisualBasic/Page1.xaml.vb#unfilter)]  
  
 <span data-ttu-id="724b8-111">Per informazioni su come creare o ottenere una visualizzazione, vedere [ottenere la visualizzazione predefinita di una raccolta di dati](../../../../docs/framework/wpf/data/how-to-get-the-default-view-of-a-data-collection.md).</span><span class="sxs-lookup"><span data-stu-id="724b8-111">For information about how to create or obtain a view, see [Get the Default View of a Data Collection](../../../../docs/framework/wpf/data/how-to-get-the-default-view-of-a-data-collection.md).</span></span> <span data-ttu-id="724b8-112">Per un esempio completo, vedere [ordinamento e filtro di elementi in una visualizzazione](http://go.microsoft.com/fwlink/?LinkID=160040).</span><span class="sxs-lookup"><span data-stu-id="724b8-112">For the complete example, see [Sorting and Filtering Items in a View Sample](http://go.microsoft.com/fwlink/?LinkID=160040).</span></span>  
  
 <span data-ttu-id="724b8-113">Se l'oggetto visualizzazione proviene da un <xref:System.Windows.Data.CollectionViewSource> dell'oggetto, si applica la logica di filtro impostando un gestore eventi per il <xref:System.Windows.Data.CollectionViewSource.Filter> evento.</span><span class="sxs-lookup"><span data-stu-id="724b8-113">If your view object comes from a <xref:System.Windows.Data.CollectionViewSource> object, you apply filtering logic by setting an event handler for the <xref:System.Windows.Data.CollectionViewSource.Filter> event.</span></span> <span data-ttu-id="724b8-114">Nell'esempio seguente, `listingDataView` è un'istanza di <xref:System.Windows.Data.CollectionViewSource>.</span><span class="sxs-lookup"><span data-stu-id="724b8-114">In the following example, `listingDataView` is an instance of <xref:System.Windows.Data.CollectionViewSource>.</span></span>  
  
 [!code-csharp[DataBindingLab#10](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#10)]
 [!code-vb[DataBindingLab#10](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#10)]  
  
 <span data-ttu-id="724b8-115">Nell'esempio viene illustrata l'implementazione dell'esempio `ShowOnlyBargainsFilter` gestore eventi del filtro.</span><span class="sxs-lookup"><span data-stu-id="724b8-115">The following shows the implementation of the example `ShowOnlyBargainsFilter` filter event handler.</span></span> <span data-ttu-id="724b8-116">Questo gestore eventi viene utilizzato il <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> proprietà da filtrare `AuctionItem` gli oggetti che hanno un `CurrentPrice` di $25 o superiore.</span><span class="sxs-lookup"><span data-stu-id="724b8-116">This event handler uses the <xref:System.Windows.Data.FilterEventArgs.Accepted%2A> property to filter out `AuctionItem` objects that have a `CurrentPrice` of $25 or greater.</span></span>  
  
 [!code-csharp[DataBindingLab#5](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/MainWindow.xaml.cs#5)]
 [!code-vb[DataBindingLab#5](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/MainWindow.xaml.vb#5)]  
  
## <a name="see-also"></a><span data-ttu-id="724b8-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="724b8-117">See Also</span></span>  
 <xref:System.Windows.Data.CollectionView.CanFilter%2A>  
 <xref:System.Windows.Data.BindingListCollectionView.CustomFilter%2A>  
 [<span data-ttu-id="724b8-118">Panoramica sul data binding</span><span class="sxs-lookup"><span data-stu-id="724b8-118">Data Binding Overview</span></span>](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [<span data-ttu-id="724b8-119">Ordinare i dati in una visualizzazione</span><span class="sxs-lookup"><span data-stu-id="724b8-119">Sort Data in a View</span></span>](../../../../docs/framework/wpf/data/how-to-sort-data-in-a-view.md)  
 [<span data-ttu-id="724b8-120">Procedure relative alle proprietà</span><span class="sxs-lookup"><span data-stu-id="724b8-120">How-to Topics</span></span>](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
