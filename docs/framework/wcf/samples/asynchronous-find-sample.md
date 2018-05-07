---
title: Esempio di ricerca asincrona
ms.date: 03/30/2017
ms.assetid: 7a713a25-c1f4-42e1-8c4a-93d64ca45a3b
ms.openlocfilehash: ed900ba3cd1b55f4e35ec0d2b92ef6b7283b498e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
---
# <a name="asynchronous-find-sample"></a>Esempio di ricerca asincrona
In questo esempio viene illustrato come utilizzare l'operazione di ricerca asincrona da un'applicazione client.  
  
## <a name="sample-details"></a>Dettagli dell'esempio  
 Il vantaggio di attenersi a questo modello di progettazione è che il client riceve una notifica in modo asincrono relativa agli endpoint individuati come risultato della richiesta di ricerca. Per visualizzare il funzionamento dell'esempio, aprire il file Client.cs. Si noti che l'oggetto <xref:System.ServiceModel.Discovery.DiscoveryClient> dispone di due delegati allegati ai gestori eventi. Un delegato viene chiamato quando viene generato un evento <xref:System.ServiceModel.Discovery.DiscoveryClient.FindCompleted>, mentre l'altro viene chiamato ogni volta che viene generato un evento <xref:System.ServiceModel.Discovery.DiscoveryClient.FindProgressChanged>. L'esempio mostra come è possibile usare questo modello nell'applicazione.  
  
> [!NOTE]
>  L'esempio utilizza endpoint HTTP e, per eseguirlo, è necessario aggiungere ACL URL appropriati. Per altre informazioni, vedere [Configuring HTTP and HTTPS](../../../../docs/framework/wcf/feature-details/configuring-http-and-https.md). L'esecuzione del comando seguente con privilegi elevati consente di aggiungere gli elenchi di controllo di accesso appropriati. È possibile sostituire dominio e nome utente per gli argomenti seguenti se il comando non funziona in modo corretto. `netsh http add urlacl url=http://+:8000/ user=%DOMAIN%\%UserName%`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Per impostare, compilare ed eseguire l'esempio  
  
1.  Utilizzando [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)], aprire AsyncFind.sln.  
  
2.  Per compilare la soluzione, premere CTRL+MAIUSC+B.  
  
3.  Aprire il prompt dei comandi di [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] e passare alla directory \WCF\Basic\Discovery\AsyncFind\CS\service\bin\Debug o alla directory \WCF\Basic\Discovery\AsyncFind\VB\service\bin\Debug ed eseguire Service.exe.  
  
4.  Una volta avviato il servizio, passare alla directory \WCF\Basic\Discovery\AsyncFind\CS\client\bin\Debug o alla directory WCF\Basic\Discovery\AsyncFind\VB\client\bin\Debug ed eseguire Client.exe.  
  
5.  Si noti che il client è in grado di individuare e chiamare il servizio.  
  
> [!IMPORTANT]
>  È possibile che gli esempi siano già installati nel computer. Verificare la directory seguente (impostazione predefinita) prima di continuare.  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  Se questa directory non esiste, andare al [Windows Communication Foundation (WCF) e gli esempi di Windows Workflow Foundation (WF) per .NET Framework 4](http://go.microsoft.com/fwlink/?LinkId=150780) per scaricare tutti i Windows Communication Foundation (WCF) e [!INCLUDE[wf1](../../../../includes/wf1-md.md)] esempi. Questo esempio si trova nella directory seguente.  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Discovery\AsyncFind`  
  
## <a name="see-also"></a>Vedere anche
