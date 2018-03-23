---
title: -nowin32manifest (Visual Basic)
ms.date: 03/13/2018
ms.prod: .net
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- /nowin32manifest compiler option [Visual Basic]
- nowin32manifest compiler option [Visual Basic]
- -nowin32manifest compiler option [Visual Basic]
ms.assetid: c0528aae-83b3-4425-99f0-19448e9843e3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c539f7833c86215a1b0f8102f9fc46419636bc7
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2018
---
# <a name="-nowin32manifest-visual-basic"></a><span data-ttu-id="f5111-102">-nowin32manifest (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f5111-102">-nowin32manifest (Visual Basic)</span></span>
<span data-ttu-id="f5111-103">Indica al compilatore di non incorporare un manifesto dell'applicazione nel file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="f5111-103">Instructs the compiler not to embed any application manifest into the executable file.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f5111-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5111-104">Syntax</span></span>  
  
```  
-nowin32manifest  
```  
  
## <a name="remarks"></a><span data-ttu-id="f5111-105">Note</span><span class="sxs-lookup"><span data-stu-id="f5111-105">Remarks</span></span>  
 <span data-ttu-id="f5111-106">Quando viene usata questa opzione, l'applicazione è soggetta a virtualizzazione in Windows Vista a meno che non venga specificato un manifesto dell'applicazione in un file di risorsa Win32 file o durante una istruzione di compilazione successiva.</span><span class="sxs-lookup"><span data-stu-id="f5111-106">When this option is used, the application will be subject to virtualization on Windows Vista unless you provide an application manifest in a Win32 Resource file or during a later build step.</span></span> <span data-ttu-id="f5111-107">Per ulteriori informazioni sulla virtualizzazione, vedere [distribuzione ClickOnce in Windows Vista](/visualstudio/deployment/clickonce-deployment-on-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="f5111-107">For more information about virtualization, see [ClickOnce Deployment on Windows Vista](/visualstudio/deployment/clickonce-deployment-on-windows-vista).</span></span>  
  
 <span data-ttu-id="f5111-108">Per ulteriori informazioni sulla creazione di manifesti, vedere [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md).</span><span class="sxs-lookup"><span data-stu-id="f5111-108">For more information about manifest creation, see [-win32manifest (Visual Basic)](../../../visual-basic/reference/command-line-compiler/win32manifest.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f5111-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f5111-109">See Also</span></span>  
 [<span data-ttu-id="f5111-110">Compilatore della riga di comando di Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f5111-110">Visual Basic Command-Line Compiler</span></span>](../../../visual-basic/reference/command-line-compiler/index.md)  
 [<span data-ttu-id="f5111-111">Pagina Applicazione, Creazione progetti (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="f5111-111">Application Page, Project Designer (Visual Basic)</span></span>](/visualstudio/ide/reference/application-page-project-designer-visual-basic)
