---
title: Lettura di un documento XML nel DOM
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: a4fb291f-5630-49ba-a49a-5b66c3b71e49
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9031f5df0d0f48dc2844cdfd0654ee4ab876cc22
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/29/2018
ms.locfileid: "47399047"
---
# <a name="reading-an-xml-document-into-the-dom"></a>Lettura di un documento XML nel DOM
Le informazioni relative a XML vengono lette in memoria da diversi formati. Possono essere lette da una stringa, un flusso, un URL, un lettore di testo o una classe derivata dal tipo <xref:System.Xml.XmlReader>.  
  
 Il metodo <xref:System.Xml.XmlDocument.Load%2A> consente di portare il documento in memoria e di usufruire dei metodi di overload disponibili per prelevare dati da ognuno dei diversi formati. È disponibile anche un metodo <xref:System.Xml.XmlDocument.LoadXml%2A>, con il quale è possibile leggere dati XML da una stringa.  
  
 I diversi metodi <xref:System.Xml.XmlDocument.Load%2A> determinano il tipo di nodi creati quando il DOM XML viene caricato. Nella tabella seguente vengono elencate le differenze tra alcuni dei metodi <xref:System.Xml.XmlDocument.Load%2A> e i relativi argomenti.  
  
|Oggetto|Argomento|  
|-------------|-----------|  
|Creazione di nodi con spazi vuoti|L'oggetto usato per caricare il DOM influisce sui nodi con spazi vuoti e spazi vuoti significativi generati nel DOM. Per altre informazioni, vedere [Gestione degli spazi vuoti e degli spazi vuoti significativi durante il caricamento del DOM](../../../../docs/standard/data/xml/white-space-and-significant-white-space-handling-when-loading-the-dom.md).|  
|Caricamento di XML da un nodo specifico o caricamento dell'intero documento XML|Tramite il metodo <xref:System.Xml.XmlDocument.Load%2A?displayProperty=nameWithType> è possibile caricare i dati da un nodo specifico nel DOM. Per altre informazioni, vedere [Caricare i dati da un lettore](../../../../docs/standard/data/xml/load-data-from-a-reader.md).|  
|Convalida di XML durante il caricamento|È possibile convalidare i dati XML quando vengono caricati nel DOM. Per eseguire l'operazione si usa un tipo <xref:System.Xml.XmlReader> per la convalida. Per altre informazioni sulla convalida di XML durante il caricamento, vedere [Convalida di un documento XML nel DOM](../../../../docs/standard/data/xml/validating-an-xml-document-in-the-dom.md).|  
  
 Nell'esempio seguente viene illustrato il caricamento di dati XML con il metodo <xref:System.Xml.XmlDocument.LoadXml%2A> e il successivo salvataggio dei dati in un file di testo denominato `data.xml`.  
  
```vb  
Imports System  
Imports System.IO  
Imports System.Xml  
  
Public Class Sample  
  
    Public Shared Sub Main()  
        ' Create the XmlDocument.  
        Dim doc As New XmlDocument()  
        doc.LoadXml(("<book genre='novel' ISBN='1-861001-57-5'>" & _  
                    "<title>Pride And Prejudice</title>" & _  
                    "</book>"))  
        ' Save the document to a file.  
        doc.Save("data.xml")  
    End Sub 'Main  
End Class 'Sample  
```  
  
```csharp  
using System;  
using System.IO;  
using System.Xml;  
  
public class Sample  
{  
    public static void Main()  
    {  
        // Create the XmlDocument.  
        XmlDocument doc = new XmlDocument();  
        doc.LoadXml("<book genre='novel' ISBN='1-861001-57-5'>" +  
                    "<title>Pride And Prejudice</title>" +  
                    "</book>");  
  
        // Save the document to a file.  
        doc.Save("data.xml");  
    }  
}  
```  
  
## <a name="see-also"></a>Vedere anche

- [Modello DOM (Document Object Mode) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
