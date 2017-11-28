---
title: 'Procedura: sospendere un servizio Windows (Visual Basic)'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: vb
f1_keywords: ServiceController.Pause
helpviewer_keywords:
- Windows Service applications, pausing
- pausing Windows Service applications
ms.assetid: eddb9409-942b-46b6-a2ce-fbd4c65f2790
caps.latest.revision: "17"
author: ghogen
ms.author: ghogen
manager: douge
ms.openlocfilehash: d44358d3f76f50a06ede5e7d720f4f48d80893de
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-pause-a-windows-service-visual-basic"></a><span data-ttu-id="e6eda-102">Procedura: sospendere un servizio Windows (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e6eda-102">How to: Pause a Windows Service (Visual Basic)</span></span>
<span data-ttu-id="e6eda-103">Questo esempio viene utilizzato il <xref:System.ServiceProcess.ServiceController> componente per sospendere il servizio di amministrazione di IIS nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="e6eda-103">This example uses the <xref:System.ServiceProcess.ServiceController> component to pause the IIS Admin service on the local computer.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e6eda-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="e6eda-104">Example</span></span>  
 [!code-vb[VbRadconService#11](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#11)]  
[!code-vb[VbRadconService#12](../../../samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbRadconService/VB/MyNewService.vb#12)]  
  
 <span data-ttu-id="e6eda-105">Questo esempio di codice è disponibile anche come frammento di codice IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="e6eda-105">This code example is also available as an IntelliSense code snippet.</span></span> <span data-ttu-id="e6eda-106">In selezione frammento di codice, si trova in **sistema operativo Windows > Windows Services**.</span><span class="sxs-lookup"><span data-stu-id="e6eda-106">In the code snippet picker, it is located in **Windows Operating System > Windows Services**.</span></span> <span data-ttu-id="e6eda-107">Per altre informazioni, vedere [Code Snippets](/visualstudio/ide/code-snippets) (Frammenti di codice).</span><span class="sxs-lookup"><span data-stu-id="e6eda-107">For more information, see [Code Snippets](/visualstudio/ide/code-snippets).</span></span>  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e6eda-108">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="e6eda-108">Compiling the Code</span></span>  
 <span data-ttu-id="e6eda-109">L'esempio presenta i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6eda-109">This example requires:</span></span>  
  
-   <span data-ttu-id="e6eda-110">Un riferimento progetto a System.serviceprocess.dll.</span><span class="sxs-lookup"><span data-stu-id="e6eda-110">A project reference to System.serviceprocess.dll.</span></span>  
  
-   <span data-ttu-id="e6eda-111">Accedere ai membri dello spazio dei nomi <xref:System.ServiceProcess>.</span><span class="sxs-lookup"><span data-stu-id="e6eda-111">Access to the members of the <xref:System.ServiceProcess> namespace.</span></span> <span data-ttu-id="e6eda-112">Aggiungere un'istruzione `Imports` se i nomi dei membri all'interno del codice non sono specificati in modo completo.</span><span class="sxs-lookup"><span data-stu-id="e6eda-112">Add an `Imports` statement if you are not fully qualifying member names in your code.</span></span> <span data-ttu-id="e6eda-113">Per altre informazioni, vedere [Istruzione Imports (tipo e spazio dei nomi .NET)](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span><span class="sxs-lookup"><span data-stu-id="e6eda-113">For more information, see [Imports Statement (.NET Namespace and Type)](~/docs/visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="e6eda-114">Programmazione efficiente</span><span class="sxs-lookup"><span data-stu-id="e6eda-114">Robust Programming</span></span>  
 <span data-ttu-id="e6eda-115">Il <xref:System.ServiceProcess.ServiceController.MachineName%2A> proprietà la <xref:System.ServiceProcess.ServiceController> classe è il computer locale per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e6eda-115">The <xref:System.ServiceProcess.ServiceController.MachineName%2A> property of the <xref:System.ServiceProcess.ServiceController> class is the local computer by default.</span></span> <span data-ttu-id="e6eda-116">Per fare riferimento a servizi di Windows in un altro computer, modificare il <xref:System.ServiceProcess.ServiceController.MachineName%2A> proprietà sul nome del computer.</span><span class="sxs-lookup"><span data-stu-id="e6eda-116">To reference Windows services on another computer, change the <xref:System.ServiceProcess.ServiceController.MachineName%2A> property to the name of that computer.</span></span>  
  
 <span data-ttu-id="e6eda-117">Le seguenti condizioni possono generare un'eccezione:</span><span class="sxs-lookup"><span data-stu-id="e6eda-117">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="e6eda-118">Il servizio non può essere sospeso.</span><span class="sxs-lookup"><span data-stu-id="e6eda-118">The service cannot be paused.</span></span> <span data-ttu-id="e6eda-119">(<xref:System.InvalidOperationException>)</span><span class="sxs-lookup"><span data-stu-id="e6eda-119">(<xref:System.InvalidOperationException>)</span></span>  
  
-   <span data-ttu-id="e6eda-120">Si è verificato un errore durante l'accesso a un'API di sistema.</span><span class="sxs-lookup"><span data-stu-id="e6eda-120">An error occurred when accessing a system API.</span></span> <span data-ttu-id="e6eda-121">(<xref:System.ComponentModel.Win32Exception>)</span><span class="sxs-lookup"><span data-stu-id="e6eda-121">(<xref:System.ComponentModel.Win32Exception>)</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="e6eda-122">Sicurezza di .NET Framework</span><span class="sxs-lookup"><span data-stu-id="e6eda-122">.NET Framework Security</span></span>  
 <span data-ttu-id="e6eda-123">Il controllo dei servizi del computer può essere limitato tramite la <xref:System.ServiceProcess.ServiceControllerPermissionAccess> come impostare le autorizzazioni di <xref:System.ServiceProcess.ServiceControllerPermission>.</span><span class="sxs-lookup"><span data-stu-id="e6eda-123">Control of services on the computer may be restricted by using the <xref:System.ServiceProcess.ServiceControllerPermissionAccess> to set permissions in the <xref:System.ServiceProcess.ServiceControllerPermission>.</span></span>  
  
 <span data-ttu-id="e6eda-124">Utilizzando, è possibile limitare l'accesso alle informazioni sul servizio di <xref:System.Security.Permissions.PermissionState> come impostare le autorizzazioni di <xref:System.Security.Permissions.SecurityPermission>.</span><span class="sxs-lookup"><span data-stu-id="e6eda-124">Access to service information may be restricted by using the <xref:System.Security.Permissions.PermissionState> to set permissions in the <xref:System.Security.Permissions.SecurityPermission>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6eda-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e6eda-125">See Also</span></span>  
 <xref:System.ServiceProcess.ServiceController>  
 <xref:System.ServiceProcess.ServiceControllerStatus>  
 <xref:System.ServiceProcess.ServiceController.WaitForStatus%2A>  
 [<span data-ttu-id="e6eda-126">Procedura: continuare un servizio di Windows (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="e6eda-126">How to: Continue a Windows Service (Visual Basic)</span></span>](../../../docs/framework/windows-services/how-to-continue-a-windows-service-visual-basic.md)
