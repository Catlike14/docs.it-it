---
title: /debug (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- debug compiler switches
- /debug compiler option [Visual Basic]
- -debug compiler option [Visual Basic]
- debug compiler option [Visual Basic]
ms.assetid: c2b0bea5-1d5e-499f-9bd5-4f6c6b715ea2
caps.latest.revision: "18"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: f1c90b28f1df18e7e0a4f9e22730e1c3476fa650
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="debug-visual-basic"></a>/debug (Visual Basic)
Indica al compilatore di generare informazioni di debug e di inserirlo nei file di output.  
  
## <a name="syntax"></a>Sintassi  
  
```  
/debug[+ | -]  
' -or-  
/debug:[full | pdbonly]  
```  
  
## <a name="arguments"></a>Argomenti  
  
|Termine|Definizione|  
|---|---|  
|`+` &#124; `-`|Parametro facoltativo. Specifica di `+` o `/debug` indica al compilatore di generare informazioni di debug e inserirle in un file con estensione pdb. Specifica di `-` ha lo stesso effetto della mancata specifica `/debug`.|  
|`full` &#124; `pdbonly`|Parametro facoltativo. Specifica il tipo di informazioni di debug generate dal compilatore. Se non si specifica `/debug:pdbonly`, il valore predefinito è `full`, che consente di collegare un debugger al programma in esecuzione. Il `pdbonly` argomento consente il debug del codice sorgente quando il programma viene avviato nel debugger, ma in linguaggio assembly viene visualizzato solo quando il programma in esecuzione è collegato il debugger.|  
  
## <a name="remarks"></a>Note  
 Usare questa opzione per creare build di debug. Se non si specifica `/debug`, `/debug+`, o `/debug:full`, non sarà possibile eseguire il debug di file di output del programma.  
  
 Per impostazione predefinita, le informazioni di debug non viene generata (`/debug-`). Per generare informazioni di debug, specificare `/debug` o `/debug+`.  
  
 Per informazioni su come configurare le prestazioni di debug di un'applicazione, vedere [Semplificazione del debug di un'immagine](../../../framework/debug-trace-profile/making-an-image-easier-to-debug.md).  
  
|Per impostare l'opzione /debug nella compilazione di Visual Studio ambiente di sviluppo integrato.|  
|---|  
|1.  Con un progetto selezionato in **Esplora soluzioni**, scegliere **Proprietà** dal menu **Progetto**. Per altre informazioni, vedere [Introduzione a Creazione progetti](http://msdn.microsoft.com/en-us/898dd854-c98d-430c-ba1b-a913ce3c73d7).<br />2.  Fare clic sulla scheda **Compila**.<br />3.  Fare clic su **opzioni di compilazione avanzate**.<br />4.  Modificare il valore di **genera informazioni di Debug** casella.|  
  
## <a name="example"></a>Esempio  
 Nell'esempio seguente inserisce informazioni di debug nel file di output `App.exe`.  
  
```  
vbc /debug /out:app.exe test.vb  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Compilatore della riga di comando di Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md)  
 [Esempi di righe di comando di compilazione](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
