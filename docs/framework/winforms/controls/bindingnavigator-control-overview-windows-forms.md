---
title: Cenni preliminari sul controllo BindingNavigator (Windows Form)
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: DataNavigator
helpviewer_keywords:
- BindingNavigator control [Windows Forms], about BindingNavigator control
- records [Windows Forms], navigating on a form
- data [Windows Forms], navigating
- data navigation
ms.assetid: 4423eede-f8d1-4d02-822f-5bf8432680d0
caps.latest.revision: "26"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 932223a48500d8a0df5be6ae1ca08e1f333fc711
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="bindingnavigator-control-overview-windows-forms"></a>Cenni preliminari sul controllo BindingNavigator (Windows Form)
È possibile usare il controllo <xref:System.Windows.Forms.BindingNavigator> per fornire agli utenti un metodo standard per la ricerca e la modifica dei dati in un Windows Form. <xref:System.Windows.Forms.BindingNavigator> viene spesso usato con il componente <xref:System.Windows.Forms.BindingSource> per consentire agli utenti di spostarsi tra i vari record di dati in un form e apportare modifiche ai record.  
  
## <a name="how-the-bindingnavigator-works"></a>Funzionamento di BindingNavigator  
 Il controllo <xref:System.Windows.Forms.BindingNavigator> è composto da un <xref:System.Windows.Forms.ToolStrip> con una serie di oggetti <xref:System.Windows.Forms.ToolStripItem> per la maggior parte delle azioni correlate ai dati: aggiunta, eliminazione ed esplorazione. Per impostazione predefinita, il controllo <xref:System.Windows.Forms.BindingNavigator> contiene questi pulsanti standard. Nell'immagine riportata di seguito è illustrato il controllo <xref:System.Windows.Forms.BindingNavigator> in un form.  
  
 ![Controllo BindingNavigator](../../../../docs/framework/winforms/controls/media/cpdatacontainerctrl.gif "cpDataContainerCtrl")  
  
 La tabella seguente elenca i vari controlli con le relative funzioni.  
  
|Controllo|Funzione|  
|-------------|--------------|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.AddNewItem%2A>|Inserisce una nuova riga nell'origine dati sottostante.|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.DeleteItem%2A>|Elimina la riga corrente dall'origine dati sottostante.|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.MoveFirstItem%2A>|Passa al primo elemento nell'origine dati sottostante.|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.MoveLastItem%2A>|Passa all'ultimo elemento nell'origine dati sottostante.|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.MoveNextItem%2A>|Passa all'elemento successivo nell'origine dati sottostante.|  
|Pulsante <xref:System.Windows.Forms.BindingNavigator.MovePreviousItem%2A>|Passa all'elemento precedente nell'origine dati sottostante.|  
|Casella di testo <xref:System.Windows.Forms.BindingNavigator.PositionItem%2A>|Restituisce la posizione corrente nell'origine dati sottostante.|  
|Casella di testo <xref:System.Windows.Forms.BindingNavigator.CountItem%2A>|Restituisce il numero totale di elementi nell'origine dati sottostante.|  
  
 A ogni controllo contenuto nell'insieme corrisponde un membro del componente <xref:System.Windows.Forms.BindingSource> che fornisce la stessa funzionalità a livello di codice. Il pulsante <xref:System.Windows.Forms.BindingNavigator.MoveFirstItem%2A>, ad esempio, corrisponde al metodo <xref:System.Windows.Forms.BindingSource.MoveFirst%2A> del componente <xref:System.Windows.Forms.BindingSource>, il pulsante <xref:System.Windows.Forms.BindingNavigator.DeleteItem%2A> corrisponde al metodo <xref:System.Windows.Forms.BindingSource.RemoveCurrent%2A> e così via.  
  
 Se i pulsanti predefiniti non sono adatti per l'applicazione in fase di sviluppo oppure se sono necessari altri pulsanti per supportare altri tipi di funzionalità, è possibile fornire pulsanti <xref:System.Windows.Forms.ToolStrip> personalizzati. Vedere anche [Procedura: Aggiungere i pulsanti Carica, Salva e Annulla al controllo BindingNavigator Windows Forms](../../../../docs/framework/winforms/controls/load-save-and-cancel-bindingnavigator.md).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Forms.BindingNavigator>  
 <xref:System.Windows.Forms.BindingSource>  
 [Controllo BindingNavigator](../../../../docs/framework/winforms/controls/bindingnavigator-control-windows-forms.md)
