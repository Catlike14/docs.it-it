---
title: 'Procedura: modificare il valore di un''impostazione tra le sessioni dell''applicazione'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-winforms
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- application settings [Windows Forms], changing
- application settings [Windows Forms], between application sessions
ms.assetid: 1a85911f-97b2-476c-930b-83379edd890c
caps.latest.revision: "7"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: c00e61001d9c8877b1fcaa0e938c92249c7915e8
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="5c187-102">Procedura: modificare il valore di un'impostazione tra le sessioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5c187-102">How To: Change the Value of a Setting Between Application Sessions</span></span>
<span data-ttu-id="5c187-103">In alcuni casi, si potrebbe voler modificare il valore di un'impostazione tra le sessioni dell'applicazione dopo aver compilato e distribuito l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c187-103">At times, you might want to change the value of a setting between application sessions after the application has been compiled and deployed.</span></span> <span data-ttu-id="5c187-104">Potrebbe ad esempio, si desidera modificare una stringa di connessione in modo che punti al percorso del database corretto.</span><span class="sxs-lookup"><span data-stu-id="5c187-104">For example, you might want to change a connection string to point to the correct database location.</span></span> <span data-ttu-id="5c187-105">Poiché gli strumenti di progettazione non sono disponibili dopo aver compilato e distribuito l'applicazione, è necessario modificare il valore dell'impostazione manualmente nel file.</span><span class="sxs-lookup"><span data-stu-id="5c187-105">Since design-time tools are not available after the application has been compiled and deployed, you must change the setting value manually in the file.</span></span>  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="5c187-106">Per modificare il valore di un'impostazione tra le sessioni dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="5c187-106">To Change the Value of a Setting Between Application Sessions</span></span>  
  
1.  <span data-ttu-id="5c187-107">Utilizzando Microsoft Notepad o alcuni altri editor di testo o XML, aprire il file config associato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5c187-107">Using Microsoft Notepad or some other text or XML editor, open the .config file associated with your application.</span></span>  
  
2.  <span data-ttu-id="5c187-108">Individuare la voce per l'impostazione che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="5c187-108">Locate the entry for the setting you want to change.</span></span> <span data-ttu-id="5c187-109">Sarà simile all'esempio riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5c187-109">It should look similar to the example presented below.</span></span>  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3.  <span data-ttu-id="5c187-110">Digitare un nuovo valore per l'impostazione e salvare il file.</span><span class="sxs-lookup"><span data-stu-id="5c187-110">Type a new value for your setting and save the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5c187-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5c187-111">See Also</span></span>  
 [<span data-ttu-id="5c187-112">Uso delle impostazioni applicazione e delle impostazioni utente</span><span class="sxs-lookup"><span data-stu-id="5c187-112">Using Application Settings and User Settings</span></span>](../../../../docs/framework/winforms/advanced/using-application-settings-and-user-settings.md)  
 [<span data-ttu-id="5c187-113">Cenni preliminari sulle impostazioni delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="5c187-113">Application Settings Overview</span></span>](../../../../docs/framework/winforms/advanced/application-settings-overview.md)
