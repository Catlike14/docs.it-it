---
title: Ottimizzazione delle prestazioni nel controllo DataGridView Windows Form
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- DataGridView control [Windows Forms], performance tuning
- performance [Windows Forms], DataGridView control
- performance tuning [Windows Forms], data grids
ms.assetid: 6ccbff28-a0ff-41e4-b601-61b31b61851d
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: da0171bf4fa056de2dd06c2f7e431ea55a8dab1a
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="performance-tuning-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="ea21d-102">Ottimizzazione delle prestazioni nel controllo DataGridView Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-102">Performance Tuning in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="ea21d-103">Quando si lavora con grandi quantità di dati, il `DataGridView` controllo può utilizzare una grande quantità di memoria in overhead, se non si utilizza con attenzione.</span><span class="sxs-lookup"><span data-stu-id="ea21d-103">When working with large amounts of data, the `DataGridView` control can consume a large amount of memory in overhead, unless you use it carefully.</span></span> <span data-ttu-id="ea21d-104">Nei client con memoria limitata, è possibile evitare alcuni questo overhead, evitando di funzionalità che hanno un costo elevato della memoria.</span><span class="sxs-lookup"><span data-stu-id="ea21d-104">On clients with limited memory, you can avoid some of this overhead by avoiding features that have a high memory cost.</span></span> <span data-ttu-id="ea21d-105">È inoltre possibile gestire alcune o tutte le operazioni di manutenzione dati e il recupero di attività manualmente utilizzando la modalità virtuale per personalizzare l'utilizzo della memoria per il proprio scenario.</span><span class="sxs-lookup"><span data-stu-id="ea21d-105">You can also manage some or all of the data maintenance and retrieval tasks yourself using virtual mode in order to customize the memory usage for your scenario.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ea21d-106">In questa sezione</span><span class="sxs-lookup"><span data-stu-id="ea21d-106">In This Section</span></span>  
 [<span data-ttu-id="ea21d-107">Procedure consigliate per ridimensionare il controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-107">Best Practices for Scaling the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/best-practices-for-scaling-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="ea21d-108">Viene descritto come utilizzare il `DataGridView` controllo in modo da evitare possibili problemi legati all'utilizzo e le prestazioni della memoria necessaria quando si lavora con grandi quantità di dati.</span><span class="sxs-lookup"><span data-stu-id="ea21d-108">Describes how to use the `DataGridView` control in a way that avoids unnecessary memory usage and performance penalties when working with large amounts of data.</span></span>  
  
 [<span data-ttu-id="ea21d-109">Modo virtuale nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-109">Virtual Mode in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/virtual-mode-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="ea21d-110">Viene descritto come utilizzare la modalità virtuale per integrare o sostituire il meccanismo di associazione dati standard.</span><span class="sxs-lookup"><span data-stu-id="ea21d-110">Describes how to use virtual mode to supplement or replace the standard data-binding mechanism.</span></span>  
  
 [<span data-ttu-id="ea21d-111">Procedura dettagliata: Implementazione della modalità virtuale nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-111">Walkthrough: Implementing Virtual Mode in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/implementing-virtual-mode-wf-datagridview-control.md)  
 <span data-ttu-id="ea21d-112">Viene descritto come implementare i gestori per diversi eventi in modalità virtuale.</span><span class="sxs-lookup"><span data-stu-id="ea21d-112">Describes how to implement handlers for several virtual-mode events.</span></span> <span data-ttu-id="ea21d-113">Viene inoltre illustrato come implementare il rollback a livello di riga e il commit di modifiche dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ea21d-113">Also demonstrates how to implement row-level rollback and commit for user edits.</span></span>  
  
 [<span data-ttu-id="ea21d-114">Implementazione del modo virtuale con caricamento dati JIT nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-114">Implementing Virtual Mode with Just-In-Time Data Loading in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)  
 <span data-ttu-id="ea21d-115">Viene descritto come caricare dati su richiesta, è utile quando si dispone di più dati per visualizzare la memoria disponibile client possa memorizzare.</span><span class="sxs-lookup"><span data-stu-id="ea21d-115">Describes how to load data on demand, which is useful when you have more data to display than the available client memory can store.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="ea21d-116">Riferimenti</span><span class="sxs-lookup"><span data-stu-id="ea21d-116">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="ea21d-117">Fornisce la documentazione di riferimento per il controllo <xref:System.Windows.Forms.DataGridView>.</span><span class="sxs-lookup"><span data-stu-id="ea21d-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>  
 <span data-ttu-id="ea21d-118">Fornisce la documentazione di riferimento per la <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> proprietà.</span><span class="sxs-lookup"><span data-stu-id="ea21d-118">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ea21d-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ea21d-119">See Also</span></span>  
 [<span data-ttu-id="ea21d-120">Controllo DataGridView</span><span class="sxs-lookup"><span data-stu-id="ea21d-120">DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/datagridview-control-windows-forms.md)  
 [<span data-ttu-id="ea21d-121">Modalità di visualizzazione di dati nel controllo DataGridView di Windows Form</span><span class="sxs-lookup"><span data-stu-id="ea21d-121">Data Display Modes in the Windows Forms DataGridView Control</span></span>](../../../../docs/framework/winforms/controls/data-display-modes-in-the-windows-forms-datagridview-control.md)
