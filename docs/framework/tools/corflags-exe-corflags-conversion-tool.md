---
title: CorFlags.exe (strumento di conversione CorFlags) | Microsoft Docs
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-clr
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- CorFlags conversion tool
- CorFlags.exe
- portable executable files, CorFlags section
ms.assetid: ef900f8f-71ca-4dde-9b8c-95ddb0d7d89c
caps.latest.revision: 17
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 49906f2e9416f1e6cccda5de7f657f10acaaab5a
ms.contentlocale: it-it
ms.lasthandoff: 06/02/2017

---
# <a name="corflagsexe-corflags-conversion-tool"></a>CorFlags.exe (strumento di conversione CorFlags)
Lo strumento di conversione CorFlags consente di configurare la sezione CorFlags dell'intestazione di un'immagine eseguibile di tipo PE.  
  
 Viene installato automaticamente con Visual Studio. Per eseguire lo strumento, usare il prompt dei comandi per sviluppatori o il prompt dei comandi di Visual Studio in Windows 7. Per altre informazioni, vedere [Prompt dei comandi](../../../docs/framework/tools/developer-command-prompt-for-vs.md).  
  
 Al prompt dei comandi digitare quanto segue:  
  
## <a name="syntax"></a>Sintassi  
  
```  
CorFlags.exe assembly [options]  
```  
  
#### <a name="parameters"></a>Parametri  
  
|Parametro obbligatorio.|Descrizione|  
|------------------------|-----------------|  
|`assembly`|Nome dell'assembly per il quale configurare CorFlags.|  
  
|Opzione|Descrizione|  
|------------|-----------------|  
|**/32BIT[REQ]+**|Imposta il flag 32BITREQUIRED.|  
|**/32BIT[REQ]-**|Cancella il flag 32BITREQUIRED.|  
|**/32BITPREF+**|Imposta il flag 32BITPREFERRED. L'applicazione viene eseguita come processo a 32 bit anche sulle piattaforme a 64 bit. Impostare questo flag solo su file EXE. Se il flag viene impostato su una DLL, la DLL non viene caricata nei processi a 64 bit e viene generata un'eccezione <xref:System.BadImageFormatException>. Un file EXE con questo flag può essere caricato in un processo a 64 bit.<br /><br /> Nuovo in [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].|  
|**/32BITPREF-**|Cancella il flag 32BITPREFERRED.<br /><br /> Nuovo in [!INCLUDE[net_v45](../../../includes/net-v45-md.md)].|  
|**/?**|Visualizza la sintassi e le opzioni di comando dello strumento.|  
|**/Force**|Forza un aggiornamento anche se l'assembly ha un nome sicuro. **Importante:** se si aggiorna un assembly con nome sicuro è necessario firmarlo nuovamente prima di eseguirne il codice.|  
|**/help**|Visualizza la sintassi e le opzioni di comando dello strumento.|  
|**/ILONLY+**|Imposta il flag ILONLY.|  
|**/ILONLY-**|Cancella il flag ILONLY.|  
|**/nologo**|Evita la visualizzazione del messaggio di avvio Microsoft.|  
|**/RevertCLRHeader**|Ripristina la versione 2.0 dell'intestazione CLR.|  
|**/UpgradeCLRHeader**|Esegue l'aggiornamento dell'intestazione CLR alla versione 2.5. **Nota:** per essere eseguiti a livello nativo, gli assembly devono disporre di un'intestazione CLR versione 2.5 o successiva.|  
  
## <a name="remarks"></a>Note  
 Se non viene specificata alcuna opzione, lo strumento di conversione CorFlags visualizza i flag relativi all'assembly specificato.  
  
## <a name="see-also"></a>Vedere anche  
 [Strumenti](../../../docs/framework/tools/index.md)   
 [Applicazioni a 64 bit](../../../docs/framework/64-bit-apps.md)   
 [Prompt dei comandi](../../../docs/framework/tools/developer-command-prompt-for-vs.md)
