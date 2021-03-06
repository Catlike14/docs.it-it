---
title: Blocchi in lettura/scrittura
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- ReaderWriterLock class, about ReaderWriterLock class
- threading [.NET Framework], ReaderWriterLock class
ms.assetid: 8c71acf2-2c18-4f4d-8cdb-0728639265fd
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 8be9b4eef30333fbbdc26915635d17157176d6fc
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2018
ms.locfileid: "45640933"
---
# <a name="reader-writer-locks"></a>Blocchi in lettura/scrittura
La classe <xref:System.Threading.ReaderWriterLockSlim> consente a più thread di leggere una risorsa contemporaneamente, ma richiede a un thread di rimanere in attesa di un blocco esclusivo per poter scrivere nella risorsa.  
  
 È possibile usare una classe <xref:System.Threading.ReaderWriterLockSlim> nell'applicazione per fornire la sincronizzazione cooperativa tra i thread che accedono a una risorsa condivisa. I blocchi vengono acquisiti nella classe <xref:System.Threading.ReaderWriterLockSlim> stessa.  
  
 Come per qualsiasi meccanismo di sincronizzazione di thread, è necessario assicurarsi che nessun thread ignori il blocco fornito da <xref:System.Threading.ReaderWriterLockSlim>. A garanzia di ciò, progettare una classe che incapsuli la risorsa condivisa. Questa classe fornisce membri che accedono alla risorsa condivisa privata e che usano una classe <xref:System.Threading.ReaderWriterLockSlim> privata per la sincronizzazione. Per un esempio, vedere gli esempi di codice per la classe <xref:System.Threading.ReaderWriterLockSlim>. <xref:System.Threading.ReaderWriterLockSlim> è abbastanza efficace da usare per sincronizzare i singoli oggetti.  
  
 Strutturare l'applicazione per ridurre al minimo la durata delle operazioni di lettura e scrittura. Le operazioni di scrittura lunghe influiscono direttamente sulla velocità effettiva perché il blocco di scrittura è esclusivo. Le operazioni di lettura lunghe bloccano i writer in attesa e se almeno un thread è in attesa dell'accesso in scrittura, verranno bloccati anche i thread che richiedono l'accesso in lettura.  
  
> [!NOTE]
>  [!INCLUDE[dnprdnshort](../../../includes/dnprdnshort-md.md)] include due blocchi in lettura/scrittura, ovvero <xref:System.Threading.ReaderWriterLockSlim> e <xref:System.Threading.ReaderWriterLock>. <xref:System.Threading.ReaderWriterLockSlim> è consigliato per tutte le nuove fasi di sviluppo. <xref:System.Threading.ReaderWriterLockSlim> è simile a <xref:System.Threading.ReaderWriterLock>, ma include regole semplificate per la ricorsione e per l'aggiornamento e il downgrade dello stato del blocco. <xref:System.Threading.ReaderWriterLockSlim> evita molti casi di deadlock potenziale. Inoltre, le prestazioni di <xref:System.Threading.ReaderWriterLockSlim> sono significativamente migliori di <xref:System.Threading.ReaderWriterLock>.  
  
## <a name="see-also"></a>Vedere anche

- <xref:System.Threading.ReaderWriterLockSlim>  
- <xref:System.Threading.ReaderWriterLock>  
- [Threading](../../../docs/standard/threading/index.md)  
- [Threading Objects and Features](../../../docs/standard/threading/threading-objects-and-features.md) (Oggetti e funzionalità del threading)
