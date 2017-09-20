---
title: 'Procedura: determinare gli aggiornamenti di .NET Framework installati'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- updates, determining for .NET Framework
- .NET Framework, determining updates
ms.assetid: 53c7b5f7-d47a-402a-b194-7244a696a88b
caps.latest.revision: 6
author: mairaw
ms.author: mairaw
manager: wpickett
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: b29b402e859688dcced6bd4429b18298070fb5e4
ms.contentlocale: it-it
ms.lasthandoff: 09/19/2017

---
# <a name="how-to-determine-which-net-framework-updates-are-installed"></a>Procedura: determinare gli aggiornamenti di .NET Framework installati
Gli aggiornamenti installati per ogni versione di .NET Framework installata in un computer sono elencati nel Registro di sistema di Windows. Per visualizzare queste informazioni, è possibile usare l'Editor del Registro di sistema (regedit.exe).  
  
 Nell'Editor del Registro di sistema le versioni di .NET Framework e gli aggiornamenti installati per ogni versione sono archiviati in sottochiavi diverse. Per informazioni sul rilevamento dei numeri delle versioni installate, vedere [Procedura: determinare le versioni di .NET Framework installate](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md). Per informazioni sull'installazione di .NET Framework, vedere [Install the .NET Framework for developers](../../../docs/framework/install/guide-for-developers.md) (Installare .NET Framework per sviluppatori).  
  
### <a name="to-find-installed-updates"></a>Per individuare gli aggiornamenti installati  
  
1.  Aprire il programma **regedit.exe**. In Windows 8 e versioni successive aprire la schermata Start e digitare il nome. Nelle versioni precedenti di Windows, fare clic sul pulsante **Start** per aprire il relativo menu, scegliere **Esegui** e nella casella **Apri** immettere **regedit.exe**.  
  
     Per eseguire regedit.exe, è necessario disporre di privilegi amministrativi.  
  
2.  Nell'Editor del Registro di sistema aprire la seguente sottochiave:  
  
     HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Updates  
  
     Gli aggiornamenti installati sono elencati nelle sottochiavi che identificano la versione di .NET Framework a che si applicano. Ogni aggiornamento è identificato da un numero di Knowledge Base (KB).  
  
## <a name="example"></a>Esempio  
 Il codice seguente consente di determinare gli aggiornamenti di .NET Framework installati in un computer a livello di codice. Per eseguire questo esempio, è necessario disporre delle credenziali di amministratore.  
  
 [!code-csharp[ListUpdates#1](../../../samples/snippets/csharp/VS_Snippets_CLR/listupdates/cs/program.cs#1)]
 [!code-vb[ListUpdates#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/listupdates/vb/program.vb#1)]  
  
 In questo esempio viene generato un output simile al seguente:  
  
```  
Microsoft .NET Framework 3.5 SP1  
  KB953595  Hotfix for Microsoft .NET Framework 3.5 SP1 (KB953595)  
  SP1  
    KB2657424  Security Update for Microsoft .NET Framework 3.5 SP1 (KB2657424)  
    KB958484  Hotfix for Microsoft .NET Framework 3.5 SP1 (KB958484)  
    KB963707  Update for Microsoft .NET Framework 3.5 SP1 (KB963707)  
Microsoft .NET Framework 4 Client Profile  
  KB2160841  Security Update for Microsoft .NET Framework 4 Client Profile (KB2160841)  
  KB2446708  Security Update for Microsoft .NET Framework 4 Client Profile (KB2446708)  
  KB2468871  Update for Microsoft .NET Framework 4 Client Profile (KB2468871)  
  KB2478663  Security Update for Microsoft .NET Framework 4 Client Profile (KB2478663)  
  KB2518870  Security Update for Microsoft .NET Framework 4 Client Profile (KB2518870)  
  KB2533523  Update for Microsoft .NET Framework 4 Client Profile (KB2533523)  
  KB2539636  Security Update for Microsoft .NET Framework 4 Client Profile (KB2539636)  
  KB2572078  Security Update for Microsoft .NET Framework 4 Client Profile (KB2572078)  
  KB2633870  Security Update for Microsoft .NET Framework 4 Client Profile (KB2633870)  
  KB2656351  Security Update for Microsoft .NET Framework 4 Client Profile (KB2656351)  
Microsoft .NET Framework 4 Extended  
  KB2416472  Security Update for Microsoft .NET Framework 4 Extended (KB2416472)  
  KB2468871  Update for Microsoft .NET Framework 4 Extended (KB2468871)  
  KB2487367  Security Update for Microsoft .NET Framework 4 Extended (KB2487367)  
  KB2533523  Update for Microsoft .NET Framework 4 Extended (KB2533523)  
  KB2656351  Security Update for Microsoft .NET Framework 4 Extended (KB2656351)  
```  
  
## <a name="see-also"></a>Vedere anche

[Procedura: determinare le versioni di .NET Framework installate](../../../docs/framework/migration-guide/how-to-determine-which-versions-are-installed.md)   
[Installare .NET Framework](../../../docs/framework/install/guide-for-developers.md)   
[Versioni e dipendenze](../../../docs/framework/migration-guide/versions-and-dependencies.md)

