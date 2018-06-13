---
title: 'Procedura: recuperare dati in un formato dati particolare'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], retrieving data
- DataFormats class [WPF], retrieving data
- DataObject class [WPF], retrieving data
ms.assetid: a625acf3-1144-44cd-add7-456aefc3859f
ms.openlocfilehash: 405fff1b586207249fbabafb28791ffa2901cf49
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33545107"
---
# <a name="how-to-retrieve-data-in-a-particular-data-format"></a><span data-ttu-id="a849f-102">Procedura: recuperare dati in un formato dati particolare</span><span class="sxs-lookup"><span data-stu-id="a849f-102">How to: Retrieve Data in a Particular Data Format</span></span>
<span data-ttu-id="a849f-103">Nell'esempio seguente viene illustrato come recuperare i dati da un oggetto dati in un formato specificato.</span><span class="sxs-lookup"><span data-stu-id="a849f-103">The following examples show how to retrieve data from a data object in a specified format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a849f-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="a849f-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="a849f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a849f-105">Description</span></span>  
 <span data-ttu-id="a849f-106">Il codice di esempio seguente usa il <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> eseguire l'overload per controllare innanzitutto se formattare una data specificata è disponibile (in modo nativo o tramite conversione automatica); se il formato specificato non è disponibile, l'esempio recupera i dati utilizzando il <xref:System.Windows.DataObject.GetData%28System.String%29> metodo.</span><span class="sxs-lookup"><span data-stu-id="a849f-106">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%29> overload to first check if a specified data format is available (natively or by auto-convert); if the specified format is available, the example retrieves the data by using the <xref:System.Windows.DataObject.GetData%28System.String%29> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="a849f-107">Codice</span><span class="sxs-lookup"><span data-stu-id="a849f-107">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat)]  
  
## <a name="example"></a><span data-ttu-id="a849f-108">Esempio</span><span class="sxs-lookup"><span data-stu-id="a849f-108">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="a849f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a849f-109">Description</span></span>  
 <span data-ttu-id="a849f-110">Il codice di esempio seguente usa il <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> overload per verificare se un formato dati specificato è disponibile in modo nativo (formati di dati convertibili automaticamente sono filtrati); se il formato specificato non è disponibile, l'esempio recupera i dati utilizzando il <xref:System.Windows.DataObject.GetData%28System.String%29>metodo.</span><span class="sxs-lookup"><span data-stu-id="a849f-110">The following example code uses the <xref:System.Windows.DataObject.GetDataPresent%28System.String%2CSystem.Boolean%29> overload to first check if a specified data format is available natively (auto-convertible data formats are filtered); if the specified format is available, the example retrieves the data by using the <xref:System.Windows.DataObject.GetData%28System.String%29> method.</span></span>  
  
### <a name="code"></a><span data-ttu-id="a849f-111">Codice</span><span class="sxs-lookup"><span data-stu-id="a849f-111">Code</span></span>  
 [!code-csharp[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/CSharp/Window1.xaml.cs#_dragdrop_getspecificdataformat_native)]
 [!code-vb[DragDrop_DragDropMiscCode#_DragDrop_GetSpecificDataFormat_Native](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DragDrop_DragDropMiscCode/visualbasic/window1.xaml.vb#_dragdrop_getspecificdataformat_native)]  
  
## <a name="see-also"></a><span data-ttu-id="a849f-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a849f-112">See Also</span></span>  
 <xref:System.Windows.IDataObject>  
 [<span data-ttu-id="a849f-113">Cenni preliminari sul trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="a849f-113">Drag and Drop Overview</span></span>](../../../../docs/framework/wpf/advanced/drag-and-drop-overview.md)
