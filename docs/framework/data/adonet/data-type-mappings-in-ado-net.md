---
title: Mapping dei tipi di dati in ADO.NET
ms.date: 03/30/2017
ms.assetid: d4afab94-ada6-4c77-a73c-41f17bae6b5a
ms.openlocfilehash: aba1eb4fdaaf43d66337ca764fe01b7d3f4624bd
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43516927"
---
# <a name="data-type-mappings-in-adonet"></a>Mapping dei tipi di dati in ADO.NET
.NET Framework è basato su Common Type System, che definisce come vengono dichiarati, usati e gestiti i tipi nel runtime. È costituito sia da tipi di valore che da tipi di riferimento, che derivano tutti dal tipo di base <xref:System.Object>. Quando si usa un'origine dati, il tipo di dati viene dedotto dal provider di dati, se non è specificato in modo esplicito. Un oggetto <xref:System.Data.DataSet> è ad esempio indipendente da qualsiasi origine dati specifica. I dati in un oggetto `DataSet` vengono recuperati da un'origine dati e le modifiche vengono applicate nell'origine dati usando un oggetto `DataAdapter`. Questo significa che quando un `DataAdapter` compila un oggetto <xref:System.Data.DataTable> in un `DataSet` con valori provenienti da un'origine dati, i tipi di dati che si ottengono nelle colonne dell'oggetto `DataTable` sono tipi [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] anziché tipi specifici del provider di dati [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] usato per la connessione all'origine dati.  
  
 Analogamente, quando un `DataReader` restituisce un valore da un'origine dati, il valore ottenuto viene archiviato in una variabile locale con un tipo [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)]. Per le operazioni `Fill` di `DataAdapter` e i metodi `Get` di `DataReader`, il tipo [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] viene dedotto dal valore restituito dal provider di dati [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)].  
  
 Anziché basarsi sul tipo di dati dedotto, quando si conosce il tipo specifico del valore che viene restituito è consigliabile usare i metodi delle funzioni di accesso tipizzate di `DataReader` . I metodi delle funzioni di accesso tipizzate garantiscono prestazioni migliori restituendo un valore come tipo [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] specifico ed eliminando quindi la necessità di un'ulteriore conversione del tipo.  
  
> [!NOTE]
>  I valori null per i tipi di dati dei provider di dati [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] sono rappresentati da `DBNull.Value`.  
  
## <a name="in-this-section"></a>In questa sezione  
 [Mapping dei tipi di dati SQL Server](../../../../docs/framework/data/adonet/sql-server-data-type-mappings.md)  
 Vengono elencati i mapping dei tipi di dati dedotti e i metodi delle funzioni di accesso ai dati per <xref:System.Data.SqlClient>.  
  
 [Mapping dei tipi di dati OLE DB](../../../../docs/framework/data/adonet/ole-db-data-type-mappings.md)  
 Vengono elencati i mapping dei tipi di dati dedotti e i metodi delle funzioni di accesso ai dati per <xref:System.Data.OleDb>.  
  
 [Mapping dei tipi di dati ODBC](../../../../docs/framework/data/adonet/odbc-data-type-mappings.md)  
 Vengono elencati i mapping dei tipi di dati dedotti e i metodi delle funzioni di accesso ai dati per <xref:System.Data.Odbc>.  
  
 [Mapping dei tipi di dati Oracle](../../../../docs/framework/data/adonet/oracle-data-type-mappings.md)  
 Vengono elencati i mapping dei tipi di dati dedotti e i metodi delle funzioni di accesso ai dati per <xref:System.Data.OracleClient>.  
  
 [Numeri a virgola mobile](../../../../docs/framework/data/adonet/floating-point-numbers.md)  
 Vengono descritti i problemi rilevati di frequente dagli sviluppatori con l'uso di numeri a virgola mobile.  
  
## <a name="see-also"></a>Vedere anche  
 [Tipi di dati SQL Server e ADO.NET](../../../../docs/framework/data/adonet/sql/sql-server-data-types.md)  
 [Configurazione di parametri e tipi di dati dei parametri](../../../../docs/framework/data/adonet/configuring-parameters-and-parameter-data-types.md)  
 [Recupero di informazioni sullo schema del database](../../../../docs/framework/data/adonet/retrieving-database-schema-information.md)  
 [Common Type System](../../../../docs/standard/base-types/common-type-system.md)  
 [La conversione dei tipi](https://msdn.microsoft.com/library/6038316e-bdaf-4f55-8006-407f591ce156)  
 [Provider gestiti ADO.NET e Centro per sviluppatori di set di dati](https://go.microsoft.com/fwlink/?LinkId=217917)
