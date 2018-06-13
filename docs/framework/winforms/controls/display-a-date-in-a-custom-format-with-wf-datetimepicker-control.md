---
title: 'Procedura: visualizzare una data in un formato personalizzato con il controllo DateTimePicker di Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- DateTimePicker control [Windows Forms], display styles
- examples [Windows Forms], DateTimePicker control
- dates [Windows Forms], displaying in DateTimePicker control
ms.assetid: 39767691-2d2b-46b6-a663-b7901e581a6e
ms.openlocfilehash: 2f563b5de9b80dab2af00290e8a6b3b309410a9e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33526009"
---
# <a name="how-to-display-a-date-in-a-custom-format-with-the-windows-forms-datetimepicker-control"></a><span data-ttu-id="4d834-102">Procedura: visualizzare una data in un formato personalizzato con il controllo DateTimePicker di Windows Form</span><span class="sxs-lookup"><span data-stu-id="4d834-102">How to: Display a Date in a Custom Format with the Windows Forms DateTimePicker Control</span></span>
<span data-ttu-id="4d834-103">Windows Form <xref:System.Windows.Forms.DateTimePicker> controllo offre flessibilità nella formattazione la visualizzazione di date e ore nel controllo.</span><span class="sxs-lookup"><span data-stu-id="4d834-103">The Windows Forms <xref:System.Windows.Forms.DateTimePicker> control gives you flexibility in formatting the display of dates and times in the control.</span></span> <span data-ttu-id="4d834-104">Il <xref:System.Windows.Forms.DateTimePicker.Format%2A> proprietà consente di selezionare uno dei formati predefiniti elencati nella <xref:System.Windows.Forms.DateTimePickerFormat>.</span><span class="sxs-lookup"><span data-stu-id="4d834-104">The <xref:System.Windows.Forms.DateTimePicker.Format%2A> property allows you to select from predefined formats, listed in the <xref:System.Windows.Forms.DateTimePickerFormat>.</span></span> <span data-ttu-id="4d834-105">Se nessuna di esse soddisfa le proprie esigenze, è possibile creare un formato personalizzato utilizzando i caratteri di formato elencati <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.</span><span class="sxs-lookup"><span data-stu-id="4d834-105">If none of these is adequate for your purposes, you can create your own format style using format characters listed in <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A>.</span></span>  
  
### <a name="to-display-a-custom-format"></a><span data-ttu-id="4d834-106">Per visualizzare un formato personalizzato</span><span class="sxs-lookup"><span data-stu-id="4d834-106">To display a custom format</span></span>  
  
1.  <span data-ttu-id="4d834-107">Impostare la proprietà <xref:System.Windows.Forms.DateTimePicker.Format%2A> su `DateTimePickerFormat.Custom`.</span><span class="sxs-lookup"><span data-stu-id="4d834-107">Set the <xref:System.Windows.Forms.DateTimePicker.Format%2A> property to `DateTimePickerFormat.Custom`.</span></span>  
  
2.  <span data-ttu-id="4d834-108">Impostare il <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> proprietà in una stringa di formato.</span><span class="sxs-lookup"><span data-stu-id="4d834-108">Set the <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> property to a format string.</span></span>  
  
    ```vb  
    DateTimePicker1.Format = DateTimePickerFormat.Custom  
    ' Display the date as "Mon 27 Feb 2012".  
    DateTimePicker1.CustomFormat = "ddd dd MMM yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.Format = DateTimePickerFormat.Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1.CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->Format = DateTimePickerFormat::Custom;  
    // Display the date as "Mon 27 Feb 2012".  
    dateTimePicker1->CustomFormat = "ddd dd MMM yyyy";  
    ```  
  
### <a name="to-add-text-to-the-formatted-value"></a><span data-ttu-id="4d834-109">Per aggiungere testo del valore formattato</span><span class="sxs-lookup"><span data-stu-id="4d834-109">To add text to the formatted value</span></span>  
  
1.  <span data-ttu-id="4d834-110">Utilizzare virgolette per racchiudere i caratteri che non sono un carattere di formato come "M" o un delimitatore come ":".</span><span class="sxs-lookup"><span data-stu-id="4d834-110">Use single quotation marks to enclose any character that is not a format character like "M" or a delimiter like ":".</span></span> <span data-ttu-id="4d834-111">Ad esempio, la stringa di formato riportato di seguito visualizza la data corrente con il formato "oggi: 05:30:31 venerdì 02 marzo 2012" in inglese (Stati Uniti) delle impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="4d834-111">For example, the format string below displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span>  
  
    ```vb  
    DateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy"  
    ```  
  
    ```csharp  
    dateTimePicker1.CustomFormat = "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
    ```cpp  
    dateTimePicker1->CustomFormat =  
       "'Today is:' hh:mm:ss dddd MMMM dd, yyyy";  
    ```  
  
     <span data-ttu-id="4d834-112">A seconda delle impostazioni cultura, qualsiasi carattere non racchiusi tra virgolette può essere modificato.</span><span class="sxs-lookup"><span data-stu-id="4d834-112">Depending on the culture setting, any characters not enclosed in single quotation marks may be changed.</span></span> <span data-ttu-id="4d834-113">Ad esempio, la stringa di formato precedente consente di visualizzare la data corrente con il formato "oggi: 05:30:31 venerdì 02 marzo 2012" in inglese (Stati Uniti) delle impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="4d834-113">For example, the format string above displays the current date with the format "Today is: 05:30:31 Friday March 02, 2012" in the English (United States) culture.</span></span> <span data-ttu-id="4d834-114">Si noti che i primi due punti sono racchiuso tra virgolette singole, poiché non è progettato per essere un carattere di delimitazione, come in "hh".</span><span class="sxs-lookup"><span data-stu-id="4d834-114">Note that the first colon is enclosed in single quotation marks, because it is not intended to be a delimiting character as it is in "hh:mm:ss".</span></span> <span data-ttu-id="4d834-115">In un'altra lingua, il formato potrebbe essere visualizzato come "oggi: 05.30.31 venerdì 02 marzo 2012".</span><span class="sxs-lookup"><span data-stu-id="4d834-115">In another culture, the format might appear as "Today is: 05.30.31 Friday March 02, 2012".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4d834-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4d834-116">See Also</span></span>  
 [<span data-ttu-id="4d834-117">Controllo DateTimePicker</span><span class="sxs-lookup"><span data-stu-id="4d834-117">DateTimePicker Control</span></span>](../../../../docs/framework/winforms/controls/datetimepicker-control-windows-forms.md)  
 [<span data-ttu-id="4d834-118">Procedura: Impostare e restituire date con il controllo DateTimePicker di Windows Form</span><span class="sxs-lookup"><span data-stu-id="4d834-118">How to: Set and Return Dates with the Windows Forms DateTimePicker Control</span></span>](../../../../docs/framework/winforms/controls/how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
