---
title: Esempi di righe di comando di compilazione (Visual Basic)
ms.date: 03/13/2018
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- command line [Visual Basic], compilers
- compilation [Visual Basic], command-line
- command-line compilers
- compiling source code [Visual Basic], from command line
- Visual Basic compiler, sample command lines
ms.assetid: 5bfbb487-5f47-4267-969a-39dfb917beeb
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: a7c3fac318e05c5e3d6fb9dd7117cac70ead03dc
ms.sourcegitcommit: 498799639937c89de777361aab74261efe7b79ea
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2018
---
# <a name="sample-compilation-command-lines-visual-basic"></a>Esempi di righe di comando compilazione (Visual Basic)
In alternativa alla compilazione [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] programmi dall'interno [!INCLUDE[vsprvs](~/includes/vsprvs-md.md)], è possibile compilare dalla riga di comando per generare file di libreria a collegamento dinamico (DLL) o file eseguibile (.exe).  
  
 Il [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] compilatore da riga di comando supporta un set completo di opzioni che controllano il debug, assembly e i file di input e outpui e le opzioni per il preprocessore. Ogni opzione è disponibile in due formati intercambiabili: `-option` e `/option`. Questa documentazione viene visualizzato soltanto il `-option` form.  
  
 Nella tabella seguente sono elencati alcuni esempi di righe di comando che è possibile modificare le proprie esigenze.  
  
|A|Usa|  
|--------|---------|  
|Compilare i file. vb e creare File.exe|`vbc -reference:Microsoft.VisualBasic.dll File.vb`|  
|Compilare i file. vb e creare file. dll|`vbc -target:library File.vb`|  
|Compilare i file. vb e creare My.exe|`vbc -out:My.exe File.vb`|  
|Compilare tutti [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] dei file nella directory corrente, con le ottimizzazioni di in e `DEBUG` simbolo definito, generando File2.exe|`vbc -define:DEBUG=1 -optimize -out:File2.exe *.vb`|  
|Compilare tutti [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] file nella directory corrente, generando una versione di debug di File2. dll senza visualizzare il logo o avvisi|`vbc -target:library -out:File2.dll -nowarn -nologo -debug *.vb`|  
|Compilare tutti [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] file nella directory corrente in qualcosa. dll|`vbc -target:library -out:Something.dll *.vb`|  
  
 Durante la compilazione dalla riga di comando, è necessario fare riferimento esplicitamente Microsoft [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] libreria di runtime tramite il `-reference` l'opzione del compilatore.  
  
> [!TIP]
>  Quando si compila un progetto tramite l'IDE di Visual Studio, è possibile visualizzare informazioni su associato **vbc** comando con le opzioni del compilatore nella finestra di output. Per visualizzare queste informazioni, aprire il [la finestra di dialogo Opzioni, progetti e soluzioni, compila ed Esegui](/visualstudio/ide/reference/options-dialog-box-projects-and-solutions-build-and-run), quindi impostare il **dettaglio di output di compilazione progetto MSBuild** a **normale** o un livello di dettaglio. Per altre informazioni, vedere [Procedura: Visualizzare, salvare e configurare file di log di compilazione](http://msdn.microsoft.com/library/75d38b76-26d6-4f43-bbe7-cbacd7cc81e7).  
  
## <a name="see-also"></a>Vedere anche  
 [Compilatore della riga di comando di Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Compilazione condizionale](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
