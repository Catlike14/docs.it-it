---
title: Elemento &lt;xmlSerializer&gt;
ms.date: 03/30/2017
helpviewer_keywords:
- <xmlSerializer> element
- XML serialization, configuration
- xmlSerializer element
ms.assetid: d129d10c-3eb7-45d9-8098-5fa853825e47
ms.openlocfilehash: 2770b82f71f3c4b43df4c44f75248e5392c528c2
ms.sourcegitcommit: ad99773e5e45068ce03b99518008397e1299e0d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/22/2018
ms.locfileid: "46585254"
---
# <a name="ltxmlserializergt-element"></a>Elemento &lt;xmlSerializer&gt;
Specifica se effettuare un controllo aggiuntivo dello stato di avanzamento di <xref:System.Xml.Serialization.XmlSerializer>.  
  
 \<configuration>  
\<system.xml.serialization>  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<xmlSerializer checkDeserializerAdvance = "true"|"false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### <a name="attributes"></a>Attributi  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|**checkDeserializeAdvances**|Specifica se controllare lo stato di avanzamento di <xref:System.Xml.Serialization.XmlSerializer>. Impostare l'attributo su "true" o "false". Il valore predefinito è "true".|  
|**useLegacySerializationGeneration**|Specifica se <xref:System.Xml.Serialization.XmlSerializer> usa la generazione legacy di serializzazione che genera assembly scrivendo un codice C# in un file e quindi compilandola in un assembly. Il valore predefinito è **false**.|  
  
### <a name="child-elements"></a>Elementi figlio  
 Nessuno.  
  
### <a name="parent-elements"></a>Elementi padre  
  
|Elemento|Descrizione|  
|-------------|-----------------|  
|[Elemento \<system.xml.serialization>](../../../docs/standard/serialization/system-xml-serialization-element.md)|Contiene le impostazioni di configurazione per le classi <xref:System.Xml.Serialization.XmlSerializer> e <xref:System.Xml.Serialization.XmlSchemaImporter>.|  
  
## <a name="remarks"></a>Note  
 Per impostazione predefinita, <xref:System.Xml.Serialization.XmlSerializer> fornisce un livello aggiuntivo di sicurezza contro potenziali attacchi di tipo Denial of Service durante la deserializzazione di dati non attendibili. Per ottenere questo risultato, tenta di rilevare cicli infiniti durante la deserializzazione. Se tale condizione viene rilevata, viene generata un'eccezione con un messaggio che comunica che a causa di un errore interno la deserializzazione non può passare al flusso sottostante.  
  
 Se si riceve questo messaggio, non significa che è necessariamente in corso un attacco di tipo Denial of Service. In rare circostanze, il meccanismo di rilevamento di ciclo infinito produce un falso positivo e l'eccezione viene generata pur trattandosi di un messaggio in arrivo valido. Nel caso in cui i messaggi validi della propria applicazione vengano rifiutati da tale livello aggiuntivo di protezione, impostare l'attributo **checkDeserializeAdvances** su "false".  
  
## <a name="example"></a>Esempio  
 L'esempio seguente imposta l'attributo **checkDeserializeAdvances** su "false".  
  
```xml  
<configuration>  
  <system.xml.serialization>  
    <xmlSerializer checkDeserializeAdvances="false" />  
  </system.xml.serialization>  
</configuration>  
```  
  
## <a name="see-also"></a>Vedere anche

- <xref:System.Xml.Serialization.XmlSerializer>  
- [Elemento \<system.xml.serialization>](../../../docs/standard/serialization/system-xml-serialization-element.md)  
- [Serializzazione SOAP e XML](../../../docs/standard/serialization/xml-and-soap-serialization.md)
