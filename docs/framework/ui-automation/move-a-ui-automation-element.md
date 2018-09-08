---
title: Spostare un elemento di automazione interfaccia utente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- moving elements
- elements, moving
- UI Automation, moving elements
ms.assetid: 4042cb44-e27e-4a03-ac36-9be1eed65b47
author: Xansky
ms.author: mhopkins
manager: markl
ms.openlocfilehash: cb239adc6dfb11c83fb983a41ea40ad8bf714038
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/08/2018
ms.locfileid: "44196881"
---
# <a name="move-a-ui-automation-element"></a><span data-ttu-id="ff7c3-102">Spostare un elemento di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="ff7c3-102">Move a UI Automation Element</span></span>
> [!NOTE]
>  <span data-ttu-id="ff7c3-103">Questa documentazione è destinata agli sviluppatori di .NET Framework che vogliono usare le classi gestite di [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] definite nello spazio dei nomi <xref:System.Windows.Automation>.</span><span class="sxs-lookup"><span data-stu-id="ff7c3-103">This documentation is intended for .NET Framework developers who want to use the managed [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] classes defined in the <xref:System.Windows.Automation> namespace.</span></span> <span data-ttu-id="ff7c3-104">Per informazioni aggiornate sulle [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], vedere [Windows Automation API: automazione dell'interfaccia utente](https://go.microsoft.com/fwlink/?LinkID=156746).</span><span class="sxs-lookup"><span data-stu-id="ff7c3-104">For the latest information about [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)], see [Windows Automation API: UI Automation](https://go.microsoft.com/fwlink/?LinkID=156746).</span></span>  
  
 <span data-ttu-id="ff7c3-105">In questo esempio viene illustrato come spostare un elemento [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] in una posizione dello schermo specificata.</span><span class="sxs-lookup"><span data-stu-id="ff7c3-105">This example demonstrates how to move a [!INCLUDE[TLA2#tla_uiautomation](../../../includes/tla2sharptla-uiautomation-md.md)] element to a specified screen location.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff7c3-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff7c3-106">Example</span></span>  
 <span data-ttu-id="ff7c3-107">Nell'esempio seguente vengono usati i pattern di controllo <xref:System.Windows.Automation.WindowPattern> e <xref:System.Windows.Automation.TransformPattern> per spostare a livello di codice un'applicazione di destinazione [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)] target application to discrete screen locations e track the <xref:System.Windows.Automation.AutomationElement.BoundingRectangleProperty> <xref:System.Windows.Automation.AutomationElement.AutomationPropertyChangedEvent>.</span><span class="sxs-lookup"><span data-stu-id="ff7c3-107">The following example uses the <xref:System.Windows.Automation.WindowPattern> and <xref:System.Windows.Automation.TransformPattern> control patterns to programmatically move a [!INCLUDE[TLA#tla_win32](../../../includes/tlasharptla-win32-md.md)] target application to discrete screen locations and track the <xref:System.Windows.Automation.AutomationElement.BoundingRectangleProperty> <xref:System.Windows.Automation.AutomationElement.AutomationPropertyChangedEvent>.</span></span>  
  
 [!code-csharp[WindowMove#1301](../../../samples/snippets/csharp/VS_Snippets_Wpf/WindowMove/CSharp/WindowMove.cs#1301)]
 [!code-vb[WindowMove#1301](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WindowMove/VisualBasic/windowmove.vb#1301)]  
[!code-csharp[WindowMove#1300](../../../samples/snippets/csharp/VS_Snippets_Wpf/WindowMove/CSharp/WindowMove.cs#1300)]
[!code-vb[WindowMove#1300](../../../samples/snippets/visualbasic/VS_Snippets_Wpf/WindowMove/VisualBasic/windowmove.vb#1300)]  
  
## <a name="see-also"></a><span data-ttu-id="ff7c3-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff7c3-108">See Also</span></span>  
 [<span data-ttu-id="ff7c3-109">Esempio WindowPattern</span><span class="sxs-lookup"><span data-stu-id="ff7c3-109">WindowPattern Sample</span></span>](https://msdn.microsoft.com/library/598b695c-8baf-406e-bbfb-2a1c7842a1de)
