---
title: "Procedura: archiviare più formati di dati in un oggetto dati"
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
- DataObject class [WPF], storing multiple formats
- DataFormats class [WPF], storing multiple formats
- drag-and-drop [WPF], storing multiple formats
ms.assetid: 941ace29-29c4-4c26-b75b-ea7d06aa0d69
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: b7019385e9c6acd8baf74dac163b75b10307a7f1
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-store-multiple-data-formats-in-a-data-object"></a><span data-ttu-id="65fe3-102">Procedura: archiviare più formati di dati in un oggetto dati</span><span class="sxs-lookup"><span data-stu-id="65fe3-102">How to: Store Multiple Data Formats in a Data Object</span></span>
<span data-ttu-id="65fe3-103">Nell'esempio seguente viene illustrato come utilizzare il <xref:System.Windows.DataObject.SetData%28System.String%2CSystem.Object%29> metodo per aggiungere dati a un oggetto dati in più formati.</span><span class="sxs-lookup"><span data-stu-id="65fe3-103">The following example shows how to use the <xref:System.Windows.DataObject.SetData%28System.String%2CSystem.Object%29> method to add data to a data object in multiple formats.</span></span>  
  
## <a name="example"></a><span data-ttu-id="65fe3-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="65fe3-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="65fe3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65fe3-105">Description</span></span>  
  
### <a name="code"></a><span data-ttu-id="65fe3-106">Codice</span><span class="sxs-lookup"><span data-stu-id="65fe3-106">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_storemultipleformats)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_StoreMultipleFormats](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_storemultipleformats)]  
  
## <a name="see-also"></a><span data-ttu-id="65fe3-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="65fe3-107">See Also</span></span>  
 <xref:System.Windows.IDataObject>  
 [<span data-ttu-id="65fe3-108">Cenni preliminari sul trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="65fe3-108">Drag and Drop Overview</span></span>](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
