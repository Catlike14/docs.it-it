---
title: 'Procedura: Riprodurre un segnale acustico da un Windows Form'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], beep
- Windows Forms, sounds
- sounds [Windows Forms], playing
- forms [Windows Forms], sounds
- examples [Windows Forms], sounds
ms.assetid: 7ea5cded-4888-4f35-8f28-5cab1a55c973
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c0c0c369756547231c0f8171bdfa940cb353544b
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-play-a-beep-from-a-windows-form"></a><span data-ttu-id="e5149-102">Procedura: Riprodurre un segnale acustico da un Windows Form</span><span class="sxs-lookup"><span data-stu-id="e5149-102">How to: Play a Beep from a Windows Form</span></span>
<span data-ttu-id="e5149-103">In questo esempio viene riprodotto un segnale acustico in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e5149-103">This example plays a beep at run time.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e5149-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="e5149-104">Example</span></span>  
  
```vb  
Public Sub OnePing()  
    Beep()  
End Sub  
```  
  
```csharp  
public void onePing()  
{  
    SystemSounds.Beep.Play();  
}  
```  
  
> [!NOTE]
>  <span data-ttu-id="e5149-105">Il suono riprodotto nell'esempio di codice c# è determinato dal <xref:System.Media.SystemSounds.Beep%2A> suoni di sistema.</span><span class="sxs-lookup"><span data-stu-id="e5149-105">The sound played in the C# code sample is determined by the <xref:System.Media.SystemSounds.Beep%2A> system sound setting.</span></span> <span data-ttu-id="e5149-106">Per altre informazioni, vedere <xref:System.Media.SystemSounds>.</span><span class="sxs-lookup"><span data-stu-id="e5149-106">For more information, see <xref:System.Media.SystemSounds>.</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e5149-107">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="e5149-107">Compiling the Code</span></span>  
 <span data-ttu-id="e5149-108">Per c#, in questo esempio richiede un riferimento al <xref:System.Media?displayProperty=nameWithType> dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e5149-108">For C#, this example requires  a reference to the <xref:System.Media?displayProperty=nameWithType> namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e5149-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e5149-109">See Also</span></span>  
 <xref:Microsoft.VisualBasic.Interaction.Beep%2A>  
 <xref:System.Media.SoundPlayer>  
 [<span data-ttu-id="e5149-110">Procedura: Riprodurre un suono del sistema da un Windows Form</span><span class="sxs-lookup"><span data-stu-id="e5149-110">How to: Play a System Sound from a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-play-a-system-sound-from-a-windows-form.md)  
 [<span data-ttu-id="e5149-111">Procedura: Riprodurre un suono da un Windows Form</span><span class="sxs-lookup"><span data-stu-id="e5149-111">How to: Play a Sound from a Windows Form</span></span>](../../../../docs/framework/winforms/controls/how-to-play-a-sound-from-a-windows-form.md)
