---
title: Cenni preliminari sul componente PageSetupDialog (Windows Form)
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: 4e7b4548f5a178ed7b819dbc2edc37bb95e3e0f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33534225"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a><span data-ttu-id="7bf29-102">Cenni preliminari sul componente PageSetupDialog (Windows Form)</span><span class="sxs-lookup"><span data-stu-id="7bf29-102">PageSetupDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="7bf29-103">Windows Form <xref:System.Windows.Forms.PageSetupDialog> componente è una finestra di dialogo preconfigurata che consentono di impostare i dettagli della pagina per la stampa nelle applicazioni basate su Windows.</span><span class="sxs-lookup"><span data-stu-id="7bf29-103">The Windows Forms <xref:System.Windows.Forms.PageSetupDialog> component is a pre-configured dialog box used to set page details for printing in Windows-based applications.</span></span> <span data-ttu-id="7bf29-104">Utilizzarlo all'interno dell'applicazione basate su Windows come una soluzione semplice per gli utenti per impostare preferenze della pagina anziché configurare la propria finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7bf29-104">Use it within your Windows-based application as a simple solution for users to set page preferences in lieu of configuring your own dialog box.</span></span> <span data-ttu-id="7bf29-105">È possibile abilitare l'impostazione bordo e i margini, intestazioni e piè di pagina e l'orientamento verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="7bf29-105">You can enable users to set border and margin adjustments, headers and footers, and portrait or landscape orientation.</span></span> <span data-ttu-id="7bf29-106">Basandosi sulle finestre di dialogo standard di Windows è quindi possibile creare applicazioni le cui funzionalità di base sono immediatamente familiari agli utenti.</span><span class="sxs-lookup"><span data-stu-id="7bf29-106">By relying on standard Windows dialog boxes, you create applications whose basic functionality is immediately familiar to users.</span></span>  
  
## <a name="key-properties-and-methods"></a><span data-ttu-id="7bf29-107">Metodi e proprietà chiave</span><span class="sxs-lookup"><span data-stu-id="7bf29-107">Key Properties and Methods</span></span>  
 <span data-ttu-id="7bf29-108">Utilizzare il <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> metodo per visualizzare la finestra di dialogo in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7bf29-108">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog at run time.</span></span> <span data-ttu-id="7bf29-109">Questo componente è è possibile impostare proprietà relative a una singola pagina (<xref:System.Drawing.Printing.PrintDocument> classe) o a qualsiasi documento (<xref:System.Drawing.Printing.PageSettings> classe).</span><span class="sxs-lookup"><span data-stu-id="7bf29-109">This component has properties you can set that relate to either a single page (<xref:System.Drawing.Printing.PrintDocument> class) or any document (<xref:System.Drawing.Printing.PageSettings> class).</span></span> <span data-ttu-id="7bf29-110">Inoltre, il <xref:System.Windows.Forms.PageSetupDialog> componente può essere utilizzato per determinare le impostazioni della stampante specifiche, che vengono archiviate nel <xref:System.Drawing.Printing.PrinterSettings> classe.</span><span class="sxs-lookup"><span data-stu-id="7bf29-110">Additionally, the <xref:System.Windows.Forms.PageSetupDialog> component can be used to determine specific printer settings, which are stored in the <xref:System.Drawing.Printing.PrinterSettings> class.</span></span>  
  
 <span data-ttu-id="7bf29-111">Quando viene aggiunto a un modulo, il <xref:System.Windows.Forms.PageSetupDialog> componente viene visualizzato nella barra delle applicazioni nella parte inferiore della finestra di progettazione Windows Form.</span><span class="sxs-lookup"><span data-stu-id="7bf29-111">When it is added to a form, the <xref:System.Windows.Forms.PageSetupDialog> component appears in the tray at the bottom of the Windows Forms Designer.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bf29-112">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="7bf29-112">See Also</span></span>  
 <xref:System.Windows.Forms.PageSetupDialog>  
 [<span data-ttu-id="7bf29-113">Componente PageSetupDialog</span><span class="sxs-lookup"><span data-stu-id="7bf29-113">PageSetupDialog Component</span></span>](../../../../docs/framework/winforms/controls/pagesetupdialog-component-windows-forms.md)
