---
title: 'Procedura: copiare ToolStripMenuItems'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- menu items [Windows Forms], copying and pasting
- MenuStrip control [Windows Forms], arranging items
- ToolStripMenuItems [Windows Forms], copying and pasting
ms.assetid: 17ef4207-e92e-4db2-b648-27246e6517ad
caps.latest.revision: "9"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 77f48d7af76cc65092e9045ab76654c96a1a7c02
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-copy-toolstripmenuitems"></a><span data-ttu-id="3c599-102">Procedura: copiare ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="3c599-102">How to: Copy ToolStripMenuItems</span></span>
<span data-ttu-id="3c599-103">In fase di progettazione è possibile copiare interi menu di primo livello e le voci dei relativi sottomenu in un'altra posizione in <xref:System.Windows.Forms.MenuStrip>.</span><span class="sxs-lookup"><span data-stu-id="3c599-103">At design time, you can copy entire top-level menus and their submenu items to a different place on the <xref:System.Windows.Forms.MenuStrip>.</span></span> <span data-ttu-id="3c599-104">È anche possibile copiare singole voci di menu tra i menu di primo livello o modificare la posizione delle voci di menu all'interno di un menu.</span><span class="sxs-lookup"><span data-stu-id="3c599-104">You can also copy individual menu items between top-level menus or change the position of menu items within a menu.</span></span>  
  
### <a name="to-copy-a-top-level-menu-and-its-submenu-items-to-another-top-level-location"></a><span data-ttu-id="3c599-105">Per copiare un menu di primo livello e le voci dei relativi sottomenu in un'altra posizione di primo livello</span><span class="sxs-lookup"><span data-stu-id="3c599-105">To copy a top-level menu and its submenu items to another top-level location</span></span>  
  
1.  <span data-ttu-id="3c599-106">Fare clic sul menu da copiare, premere CTRL+C o fare clic con il pulsante destro del mouse sul menu e selezionare **Copia** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-106">Left-click the menu that you want to copy and press CTRL+C, or right-click the menu and select **Copy** from the shortcut menu.</span></span>  
  
2.  <span data-ttu-id="3c599-107">Fare clic sul menu di primo livello dopo la nuova posizione individuata e premere CTRL+V oppure fare clic con il pulsante destro del mouse sulla voce di menu di primo livello che precede la nuova posizione e selezionare **Incolla** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-107">Left-click the top-level menu that is after the intended new location and press CTRL+V, or right-click the top-level menu item that is before the intended new location and select **Paste** from the shortcut menu.</span></span>  
  
     <span data-ttu-id="3c599-108">Il menu copiato viene inserito prima del menu di primo livello selezionato.</span><span class="sxs-lookup"><span data-stu-id="3c599-108">The menu that you copied is inserted before the selected top-level menu.</span></span>  
  
### <a name="to-copy-a-top-level-menu-and-its-submenu-items-to-a-drop-down-location"></a><span data-ttu-id="3c599-109">Per copiare un menu di primo livello e le voci dei relativi sottomenu in una posizione a discesa</span><span class="sxs-lookup"><span data-stu-id="3c599-109">To copy a top-level menu and its submenu items to a drop-down location</span></span>  
  
1.  <span data-ttu-id="3c599-110">Fare clic sul menu da spostare, premere CTRL+C o fare clic con il pulsante destro del mouse sul menu e selezionare **Copia** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-110">Left-click the menu that you want to move and press CTRL+C, or right-click the menu and select **Copy** from the shortcut menu.</span></span>  
  
2.  <span data-ttu-id="3c599-111">Nel menu di primo livello di destinazione, fare clic sulla voce del sottomenu che precede la nuova posizione individuata e premere CTRL+V oppure fare clic con il pulsante destro del mouse sulla voce di sottomenu che precede la nuova posizione e selezionare **Incolla** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-111">In the destination top-level menu, left-click the submenu item that is above the intended new location and press CTRL+V, or right-click the submenu item that is above the intended new location and select **Paste** from the shortcut menu.</span></span>  
  
     <span data-ttu-id="3c599-112">Il menu copiato viene inserito prima della voce di sottomenu selezionata.</span><span class="sxs-lookup"><span data-stu-id="3c599-112">The menu that you copied is inserted before the selected submenu item.</span></span>  
  
### <a name="to-copy-a-submenu-item-to-another-menu"></a><span data-ttu-id="3c599-113">Per copiare una voce di sottomenu in un altro menu</span><span class="sxs-lookup"><span data-stu-id="3c599-113">To copy a submenu item to another menu</span></span>  
  
1.  <span data-ttu-id="3c599-114">Fare clic sulla voce di sottomenu da copiare, premere CTRL+C o fare clic con il pulsante destro del mouse sulla voce di sottomenu e selezionare **Copia** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-114">Left-click the submenu item that you want to copy and press CTRL+C, or right-click the submenu item and choose **Copy** from the shortcut menu.</span></span>  
  
2.  <span data-ttu-id="3c599-115">Fare clic sul menu che conterrà la voce di sottomenu tagliata.</span><span class="sxs-lookup"><span data-stu-id="3c599-115">Left-click the menu that will contain the submenu item that you cut.</span></span>  
  
3.  <span data-ttu-id="3c599-116">Fare clic sulla voce di sottomenu che precede la nuova posizione individuata e premere CTRL+V oppure fare clic con il pulsante destro del mouse sulla voce di sottomenu che precede la nuova posizione e selezionare **Incolla** dal menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="3c599-116">Left-click the submenu item that is before the intended new location and press CTRL+V, or right-click the submenu item that is before the intended new location and select **Paste** from the shortcut menu.</span></span>  
  
     <span data-ttu-id="3c599-117">La voce di sottomenu copiata viene inserita prima della voce di sottomenu selezionata.</span><span class="sxs-lookup"><span data-stu-id="3c599-117">The submenu item that you copied is inserted before the selected submenu item.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3c599-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="3c599-118">See Also</span></span>  
 <xref:System.Windows.Forms.MenuStrip>  
 <xref:System.Windows.Forms.ToolStripMenuItem>  
 [<span data-ttu-id="3c599-119">Panoramica sul controllo MenuStrip</span><span class="sxs-lookup"><span data-stu-id="3c599-119">MenuStrip Control Overview</span></span>](../../../../docs/framework/winforms/controls/menustrip-control-overview-windows-forms.md)
