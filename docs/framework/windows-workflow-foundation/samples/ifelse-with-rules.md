---
title: IfElse con regole
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: c4ad9bb2-9037-413a-8b14-59ed7b927a9e
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: bec818ca5492e9a49a602a4f7baef4b45cb073c1
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="ifelse-with-rules"></a><span data-ttu-id="8f66e-102">IfElse con regole</span><span class="sxs-lookup"><span data-stu-id="8f66e-102">IfElse With Rules</span></span>
<span data-ttu-id="8f66e-103">In questo esempio viene mostrato l'uso di una condizione della regola con un'attività <xref:System.Workflow.Activities.IfElseActivity>.</span><span class="sxs-lookup"><span data-stu-id="8f66e-103">This sample shows the use of a rule condition with an <xref:System.Workflow.Activities.IfElseActivity> activity.</span></span>  
  
 <span data-ttu-id="8f66e-104">L'esempio passa un parametro `OrderValue` dall'host.</span><span class="sxs-lookup"><span data-stu-id="8f66e-104">The sample passes in an `OrderValue` parameter from the host.</span></span> <span data-ttu-id="8f66e-105">Il valore del parametro viene usato in una condizione della regola sul primo ramo dell'attività <xref:System.Workflow.Activities.IfElseActivity>.</span><span class="sxs-lookup"><span data-stu-id="8f66e-105">The value of the parameter is used in a rule condition on the first branch of the <xref:System.Workflow.Activities.IfElseActivity> activity.</span></span> <span data-ttu-id="8f66e-106">Se il valore è minore di 10.000, viene eseguito il primo ramo e <xref:System.Workflow.Activities.CodeActivity> attività nel primo branch stampa **ottenere l'approvazione Manager** nella console.</span><span class="sxs-lookup"><span data-stu-id="8f66e-106">If the value is less than 10,000, the first branch executes, and the <xref:System.Workflow.Activities.CodeActivity> activity in the first branch prints **Get Manager Approval** to the console.</span></span> <span data-ttu-id="8f66e-107">Se il valore è maggiore di 10.000, il <xref:System.Workflow.Activities.CodeActivity> attività nel secondo branch esegue e stampa **ottenere approvazione VP**.</span><span class="sxs-lookup"><span data-stu-id="8f66e-107">If the value is greater than 10,000, the <xref:System.Workflow.Activities.CodeActivity> activity in the second branch executes and prints **Get VP Approval**.</span></span>  
  
### <a name="to-build-the-sample"></a><span data-ttu-id="8f66e-108">Per compilare l'esempio</span><span class="sxs-lookup"><span data-stu-id="8f66e-108">To build the sample</span></span>  
  
1.  <span data-ttu-id="8f66e-109">Aprire la soluzione in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span><span class="sxs-lookup"><span data-stu-id="8f66e-109">Open the solution in [!INCLUDE[vs2010](../../../../includes/vs2010-md.md)].</span></span>  
  
2.  <span data-ttu-id="8f66e-110">Premere CTRL+MAIUSC+B per compilare la soluzione,</span><span class="sxs-lookup"><span data-stu-id="8f66e-110">Build the solution by pressing CTRL+SHIFT+B.</span></span>  
  
3.  <span data-ttu-id="8f66e-111">Eseguire la soluzione senza debug premendo CTRL+F5.</span><span class="sxs-lookup"><span data-stu-id="8f66e-111">Run the solution without debugging by pressing CTRL+F5.</span></span>  
  
### <a name="to-run-the-sample"></a><span data-ttu-id="8f66e-112">Per eseguire l'esempio</span><span class="sxs-lookup"><span data-stu-id="8f66e-112">To run the sample</span></span>  
  
-   <span data-ttu-id="8f66e-113">Nella finestra del prompt dei comandi di SDK eseguire il file con estensione exe nella cartella IfElseWithRules\bin\debug (oppure nella cartella IfElseWithRules\bin per la versione Visual Basic dell'esempio), collocata sotto la cartella principale dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="8f66e-113">In the SDK Command Prompt window, run the .exe file in the IfElseWithRules\bin\debug folder (or the IfElseWithRules\bin folder for the Visual Basic version of the sample), which is located below the main folder for the sample.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="8f66e-114">È possibile che gli esempi siano già installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="8f66e-114">The samples may already be installed on your computer.</span></span> <span data-ttu-id="8f66e-115">Verificare la directory seguente (impostazione predefinita) prima di continuare.</span><span class="sxs-lookup"><span data-stu-id="8f66e-115">Check for the following (default) directory before continuing:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="8f66e-116">Se questa directory non esiste, andare alla sezione relativa agli [esempi di Windows Communication Foundation (WCF) e Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti gli esempi di [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="8f66e-116">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) to download all [!INCLUDE[indigo1](../../../../includes/indigo1-md.md)] and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="8f66e-117">Questo esempio si trova nella directory seguente.</span><span class="sxs-lookup"><span data-stu-id="8f66e-117">This sample is located in the following directory:</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WF\Basic\Rules\IfElseWithRules`  
  
## <a name="see-also"></a><span data-ttu-id="8f66e-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8f66e-118">See Also</span></span>  
 <xref:System.Workflow.Activities.Rules>  
 <xref:System.Workflow.Activities.IfElseActivity>  
 <xref:System.Workflow.Activities.CodeActivity>  
 <xref:System.Workflow.Activities.Rules.RuleDefinitions>
