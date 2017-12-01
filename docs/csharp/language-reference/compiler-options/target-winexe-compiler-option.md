---
title: -target:winexe (opzioni del compilatore C#)
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-csharp
ms.topic: article
f1_keywords: /target:winexe
helpviewer_keywords:
- /target compiler options [C#], /target:winexe
- -target compiler options [C#], /target:winexe
- target compiler options [C#], /target:winexe
ms.assetid: b5a0619c-8caa-46a5-a743-1cf68408ad7a
caps.latest.revision: "11"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e155c64689f34c89443c7ff0a3dee38d6c190fcc
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="targetwinexe-c-compiler-options"></a>/target:winexe (opzioni del compilatore C#)
L'opzione **/target: winexe** indica al compilatore di creare un file eseguibile (con estensione EXE), il programma di Windows.  
  
## <a name="syntax"></a>Sintassi  
  
```console  
/target:winexe  
```  
  
## <a name="remarks"></a>Note  
 Il file eseguibile verrà creato con estensione .exe. È un programma di Windows che fornisce un'interfaccia utente dalla libreria di .NET Framework o con le API Win32.  
  
 Usare [/target:exe](../../../csharp/language-reference/compiler-options/target-exe-compiler-option.md) per creare un'applicazione console.  
  
 A meno che diversamente specificato con l'opzione [/out](../../../csharp/language-reference/compiler-options/out-compiler-option.md), il nome del file di output corrisponderà al nome del file di input contenente il metodo [Main](../../../csharp/programming-guide/main-and-command-args/index.md).  
  
 Quando specificato nella riga di comando, tutti i file fino alla successiva opzione **/out** o [/target](../../../csharp/language-reference/compiler-options/target-compiler-option.md) vengono usati per creare il programma Windows.  
  
 Un solo metodo **Main** è necessario nei file del codice sorgente che vengono compilati in un file con estensione exe. L'opzione [/main](../../../csharp/language-reference/compiler-options/main-compiler-option.md) consente di specificare la classe che contiene il metodo **Main**, nei casi in cui il codice ha più di una classe con un metodo **Main**.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Per impostare l'opzione del compilatore nell'ambiente di sviluppo di Visual Studio  
  
1.  Aprire la pagina **Proprietà** del progetto.  
  
2.  Fare clic sulla pagina delle proprietà **Applicazione**.  
  
3.  Modificare la proprietà **Tipo di output**.  
  
 Per informazioni su come impostare questa opzione del compilatore a livello di codice, vedere <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Esempio  
 Compilare `in.cs` in un programma di Windows:  
  
```console  
csc /target:winexe in.cs  
```  
  
## <a name="see-also"></a>Vedere anche  
 [/target (opzioni del compilatore c#)](../../../csharp/language-reference/compiler-options/target-compiler-option.md)  
 [Opzioni del compilatore C#](../../../csharp/language-reference/compiler-options/index.md)
