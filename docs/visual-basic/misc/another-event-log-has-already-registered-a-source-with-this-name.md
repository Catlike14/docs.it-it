---
title: "Un altro log eventi ha già registrato un'origine con questo nome"
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
ms.assetid: e6f5cd95-bb3f-4845-84fb-ae623a9bd44e
caps.latest.revision: "13"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 8beea344d233794ddc36d7fc53db1c01be84399f
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="another-event-log-has-already-registered-a-source-with-this-name"></a>Un altro log eventi ha già registrato un'origine con questo nome
Si è provato a scrivere una voce in un log eventi ma l'origine specificata è stata registrata in un altro log eventi.  
  
 Per consentire al componente <xref:System.Diagnostics.EventLog.Source%2A> di scrivere voci in un log, è necessario impostare la proprietà <xref:System.Diagnostics.EventLog> sull'istanza del componente. Quando si esegue questa operazione, viene controllato che l'origine specificata sia registrata nel log eventi in cui viene scritto il componente e, se necessario, viene chiamata la proprietà <xref:System.Diagnostics.EventLog.CreateEventSource%2A> .  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Rimuovere l'associazione tra l'origine e il primo log usando il metodo <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> o <xref:System.Diagnostics.EventLog.DeleteEventSource%2A> .  
  
2.  Registrare l'origine nel nuovo log.  
  
## <a name="see-also"></a>Vedere anche  
 [Oggetto My.Application.Log](../../visual-basic/language-reference/objects/my-application-log-object.md)  
 [Procedura: rimuovere un'origine evento](http://msdn.microsoft.com/en-us/bc66c900-4b8a-426a-b8e2-17031a20167e)  
 [Procedura: aggiungere l'applicazione come origine delle voci del registro eventi](http://msdn.microsoft.com/en-us/948ff920-a739-4e66-a191-ee951512d42c)
