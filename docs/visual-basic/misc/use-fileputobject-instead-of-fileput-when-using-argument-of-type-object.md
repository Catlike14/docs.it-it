---
title: Usa &#39; FilePutObject &#39; invece di &#39; FilePut &#39; Quando si usano argomenti di tipo &#39; oggetto &#39;
ms.date: 07/20/2015
ms.prod: .net
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vbrUseFilePutObject
ms.assetid: d207b9b7-5898-4c13-8b03-9feefac5f726
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 8cba4af206e2dbf767fdb883ec81229a67842c57
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="use-39fileputobject39-instead-of-39fileput39-when-using-argument-of-type-39object39"></a>Usa &#39; FilePutObject &#39; invece di &#39; FilePut &#39; Quando si usano argomenti di tipo &#39; oggetto &#39;
Il `FilePut` metodo include un argomento di tipo `Object`. Per evitare ambiguità, è opportuno usare`FilePutObject` invece di `FilePut` .  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Sostituire `FilePut` con `FilePutObject`.  
  
-   Eseguire il cast dell'argomento `Object` su un tipo più specifico.  
  
-   Usare la funzionalità disponibile nell'oggetto `My.Computer.FileSystem` .  
  
## <a name="see-also"></a>Vedere anche  
 [NOT IN BUILD: FilePutObject (funzione)](http://msdn.microsoft.com/en-us/a0f52a1c-5ecc-4945-b18c-03147af61d6b)  
 [Oggetto My.Computer.FileSystem](../../visual-basic/language-reference/objects/my-computer-filesystem-object.md)  
 [WriteAllBytes (metodo)](http://msdn.microsoft.com/en-us/b1a24dc1-eac8-4e22-8ffa-cc3bacbaf826)
