---
title: Spazio dello stack insufficiente (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID28
ms.assetid: bfcd792b-ac29-4158-81fc-ea0c13f4ffa2
ms.openlocfilehash: e39be5913fe877cf7b3396e4f13f4440288cb8f3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593285"
---
# <a name="out-of-stack-space-visual-basic"></a>Spazio dello stack insufficiente (Visual Basic)
Lo stack è un'area di lavoro di memoria aumenta e si ridotta dinamicamente con le richieste del programma in esecuzione. Sono stati superati i limiti.  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
1.  Verificare che le procedure non sono eccessivamente annidate.  
  
2.  Verificare che le routine ricorsive terminino correttamente.  
  
3.  Se le variabili locali richiedono uno spazio più a quello disponibile, provare a dichiarare alcune variabili a livello di modulo. È anche possibile dichiarare tutte le variabili nella procedura static facendo precedere il `Property`, `Sub`, o `Function` parola chiave with `Static`. Oppure è possibile utilizzare il `Static` istruzione per dichiarare le variabili statiche singoli all'interno delle procedure.  
  
4.  Ridefinire alcune stringhe a lunghezza fissa come stringhe a lunghezza variabile, come stringhe a lunghezza fissa richiedono più spazio di stack di stringhe a lunghezza variabile. È inoltre possibile definire la stringa a livello di modulo in cui è necessario nessuno spazio dello stack.  
  
5.  Controllare il numero di nidificata `DoEvents` chiamate di funzioni, utilizzando il `Calls` finestra di dialogo per visualizzare le routine attive nello stack.  
  
6.  Assicurarsi che non si determinava "cascata di eventi" generando un evento che chiama una routine evento già nello stack. Una catena di eventi è simile a una chiamata di routine ricorsiva non terminata, ma è meno ovvio, poiché la chiamata viene effettuata da Visual Basic, anziché una chiamata esplicita nel codice. Utilizzare il `Calls` finestra di dialogo per visualizzare le routine attive nello stack.  
  
## <a name="see-also"></a>Vedere anche  
 [Finestra Memoria](/visualstudio/debugger/memory-windows)
