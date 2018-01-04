---
title: 'Procedura: convertire un''immagine BMP in un''immagine PNG'
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
- BMP images [Windows Forms], converting to PNG
- image formats [Windows Forms], converting between
ms.assetid: 9d4a692d-73ac-4ce3-9e05-9ec321e8fbd6
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 2ee2669c41f4ee558d9457cee7df0ae8425cf065
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-convert-a-bmp-image-to-a-png-image"></a><span data-ttu-id="ffcbc-102">Procedura: convertire un'immagine BMP in un'immagine PNG</span><span class="sxs-lookup"><span data-stu-id="ffcbc-102">How to: Convert a BMP image to a PNG image</span></span>
<span data-ttu-id="ffcbc-103">Spesso può essere opportuno convertire un formato di file immagine in un altro.</span><span class="sxs-lookup"><span data-stu-id="ffcbc-103">Oftentimes, you will want to convert from one image file format to another.</span></span> <span data-ttu-id="ffcbc-104">È possibile eseguire questa conversione chiamando il metodo <xref:System.Drawing.Image.Save%2A> della classe <xref:System.Drawing.Image> e specificando l'oggetto <xref:System.Drawing.Imaging.ImageFormat> per il formato di file immagine desiderato.</span><span class="sxs-lookup"><span data-stu-id="ffcbc-104">You can do this conversion easily by calling the <xref:System.Drawing.Image.Save%2A> method of the <xref:System.Drawing.Image> class and specifying the <xref:System.Drawing.Imaging.ImageFormat> for the desired image file format.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ffcbc-105">Esempio</span><span class="sxs-lookup"><span data-stu-id="ffcbc-105">Example</span></span>  
 <span data-ttu-id="ffcbc-106">Nell'esempio seguente viene caricata un'immagine BMP da un tipo e quindi salvata nel formato PNG.</span><span class="sxs-lookup"><span data-stu-id="ffcbc-106">The following example loads a BMP image from a type, and saves the image in the PNG format.</span></span>  
  
 [!code-csharp[UsingImageEncodersDecoders#4](../../../../samples/snippets/csharp/VS_Snippets_Winforms/UsingImageEncodersDecoders/CS/Form1.cs#4)]
 [!code-vb[UsingImageEncodersDecoders#4](../../../../samples/snippets/visualbasic/VS_Snippets_Winforms/UsingImageEncodersDecoders/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="ffcbc-107">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="ffcbc-107">Compiling the Code</span></span>  
 <span data-ttu-id="ffcbc-108">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffcbc-108">This example requires:</span></span>  
  
-   <span data-ttu-id="ffcbc-109">Applicazione Windows Form.</span><span class="sxs-lookup"><span data-stu-id="ffcbc-109">A Windows Forms application.</span></span>  
  
-   <span data-ttu-id="ffcbc-110">Un riferimento allo spazio dei nomi `System.Drawing.Imaging`.</span><span class="sxs-lookup"><span data-stu-id="ffcbc-110">A reference to the `System.Drawing.Imaging` namespace.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ffcbc-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ffcbc-111">See Also</span></span>  
 [<span data-ttu-id="ffcbc-112">Procedura: Elencare i codificatori installati</span><span class="sxs-lookup"><span data-stu-id="ffcbc-112">How to: List Installed Encoders</span></span>](../../../../docs/framework/winforms/advanced/how-to-list-installed-encoders.md)  
 [<span data-ttu-id="ffcbc-113">Uso di codificatori e decodificatori di immagini nel codice gestito GDI+</span><span class="sxs-lookup"><span data-stu-id="ffcbc-113">Using Image Encoders and Decoders in Managed GDI+</span></span>](../../../../docs/framework/winforms/advanced/using-image-encoders-and-decoders-in-managed-gdi.md)  
 [<span data-ttu-id="ffcbc-114">Tipi di bitmap</span><span class="sxs-lookup"><span data-stu-id="ffcbc-114">Types of Bitmaps</span></span>](../../../../docs/framework/winforms/advanced/types-of-bitmaps.md)
