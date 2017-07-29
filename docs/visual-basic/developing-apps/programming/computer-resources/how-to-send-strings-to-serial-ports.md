---
title: 'Procedura: inviare stringhe a porte seriali in Visual Basic'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- ports, sending strings to
- strings [Visual Basic], sending to serial ports
- My.Computer.Ports object
- serial ports, sending strings to
ms.assetid: 6ebf46cd-b2d0-4b2c-9a1f-be177b22ad52
caps.latest.revision: 13
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 306c608dc7f97594ef6f72ae0f5aaba596c936e1
ms.openlocfilehash: 602b249d01252bbb1853ed02d9af86697d54b0a5
ms.contentlocale: it-it
ms.lasthandoff: 07/28/2017

---
# <a name="how-to-send-strings-to-serial-ports-in-visual-basic"></a>Procedura: inviare stringhe a porte seriali in Visual Basic
Questo argomento descrive come usare `My.Computer.Ports` per inviare stringhe alle porte seriali del computer in [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)].  
  
## <a name="example"></a>Esempio  
 In questo esempio si invia una stringa alla porta seriale COM1. Potrebbe essere necessario usare un'altra porta seriale nel computer in uso.  
  
 Usare il metodo `My.Computer.Ports.OpenSerialPort` per ottenere un riferimento alla porta. Per altre informazioni, vedere <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>.  
  
 Il blocco `Using` consente all'applicazione di chiudere la porta seriale anche se viene generata un'eccezione. Tutto il codice relativo alla porta seriale deve essere all'interno di questo blocco o di un blocco `Try...Catch...Finally`.  
  
 Il metodo <xref:System.IO.Ports.SerialPort.WriteLine%2A> invia i dati alla porta seriale.  
  
 [!code-vb[VbVbalrMyComputer#33](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-send-strings-to-serial-ports_1.vb)]  
  
## <a name="compiling-the-code"></a>Compilazione del codice  
  
-   Questo esempio presuppone l'uso della porta `COM1`.  
  
## <a name="robust-programming"></a>Programmazione efficiente  
 Questo esempio presuppone che il computer usi la porta `COM1`; per una maggiore flessibilità, il codice deve consentire all'utente di selezionare la porta seriale desiderata da un elenco di porte disponibili. Per altre informazioni, vedere [Procedura: Mostrare le porte seriali disponibili](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md).  
  
 Questo esempio usa un blocco `Using` per verificare che l'applicazione chiuda la porta anche se viene generata un'eccezione. Per altre informazioni, vedere [Istruzione using](../../../../visual-basic/language-reference/statements/using-statement.md).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:Microsoft.VisualBasic.Devices.Ports>   
 <xref:System.IO.Ports.SerialPort?displayProperty=fullName>   
 [Procedura: Comporre numeri con modem collegati a porte seriali](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-dial-modems-attached-to-serial-ports.md)   
 [Procedura: Mostrare le porte seriali disponibili](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)

