---
title: "Procedura: implementare l'interfaccia ITypedList"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ITypedList interface
- BindingList(Of T) class
- data binding [Windows Forms], implementing
- IBindingList interface
ms.assetid: 834cc15c-50bc-4a8b-a610-313d6a217357
ms.openlocfilehash: 181879d3e41e0dd140c79a4c63d52e6999acf86d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33538067"
---
# <a name="how-to-implement-the-itypedlist-interface"></a><span data-ttu-id="44a5c-102">Procedura: implementare l'interfaccia ITypedList</span><span class="sxs-lookup"><span data-stu-id="44a5c-102">How to: Implement the ITypedList Interface</span></span>
<span data-ttu-id="44a5c-103">Implementare il <xref:System.ComponentModel.ITypedList> interfaccia per abilitare l'individuazione dello schema per un elenco associabile.</span><span class="sxs-lookup"><span data-stu-id="44a5c-103">Implement the <xref:System.ComponentModel.ITypedList> interface to enable discovery of the schema for a bindable list.</span></span>  
  
## <a name="example"></a><span data-ttu-id="44a5c-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="44a5c-104">Example</span></span>  
 <span data-ttu-id="44a5c-105">Esempio di codice seguente viene illustrato come implementare il <xref:System.ComponentModel.ITypedList> interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44a5c-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="44a5c-106">Un tipo generico denominato `SortableBindingList` deriva il <xref:System.ComponentModel.BindingList%601> classe e implementa il <xref:System.ComponentModel.ITypedList> interfaccia.</span><span class="sxs-lookup"><span data-stu-id="44a5c-106">A generic type named `SortableBindingList` derives from the <xref:System.ComponentModel.BindingList%601> class and implements the <xref:System.ComponentModel.ITypedList> interface.</span></span> <span data-ttu-id="44a5c-107">Una classe semplice denominata `Customer` fornisce i dati, che sono associati all'intestazione di un <xref:System.Windows.Forms.DataGridView> controllo.</span><span class="sxs-lookup"><span data-stu-id="44a5c-107">A simple class named `Customer` provides data, which is bound to the header of a <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 [!code-csharp[System.ComponentModel.ITypedList#1](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/SortableBindingList.cs#1)]
 [!code-vb[System.ComponentModel.ITypedList#1](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/SortableBindingList.vb#1)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#10](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Customer.cs#10)]
 [!code-vb[System.ComponentModel.ITypedList#10](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Customer.vb#10)]  
  
 [!code-csharp[System.ComponentModel.ITypedList#100](../../../samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.ITypedList/CS/Form1.cs#100)]
 [!code-vb[System.ComponentModel.ITypedList#100](../../../samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.ITypedList/VB/Form1.vb#100)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="44a5c-108">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="44a5c-108">Compiling the Code</span></span>  
 <span data-ttu-id="44a5c-109">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="44a5c-109">This example requires:</span></span>  
  
-   <span data-ttu-id="44a5c-110">Riferimenti agli assembly System.Drawing e System.Windows.Forms.</span><span class="sxs-lookup"><span data-stu-id="44a5c-110">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44a5c-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="44a5c-111">See Also</span></span>  
 <xref:System.ComponentModel.ITypedList>  
 <xref:System.ComponentModel.BindingList%601>  
 <xref:System.ComponentModel.IBindingList>  
 [<span data-ttu-id="44a5c-112">Data binding e Windows Forms</span><span class="sxs-lookup"><span data-stu-id="44a5c-112">Data Binding and Windows Forms</span></span>](../../../docs/framework/winforms/data-binding-and-windows-forms.md)
