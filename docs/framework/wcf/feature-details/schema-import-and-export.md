---
title: Importazione ed esportazione degli schemi
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WCF, schema import and export
- XsdDataContractExporter class
- XsdDataContractImporter class
ms.assetid: 0da32b50-ccd9-463a-844c-7fe803d3bf44
ms.openlocfilehash: c9bb0d6df362380a37ae3079694ab91e9577741d
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33497282"
---
# <a name="schema-import-and-export"></a>Importazione ed esportazione degli schemi
Windows Communication Foundation (WCF) include un nuovo motore di serializzazione, la <xref:System.Runtime.Serialization.DataContractSerializer>. `DataContractSerializer` esegue la conversione tra oggetti [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] e XML in entrambe direzioni. Oltre al serializzatore, WCF include meccanismi esportazione ed importazione dello schema associato. *Schema* è una descrizione formale, precisa e leggibile dal computer della forma del codice XML che il serializzatore produce o che il deserializzatore può accedere. WCF utilizza il linguaggio di World Wide Web Consortium (W3C) XML Schema definition (XSD) come rappresentazione dello schema, che è ampiamente interoperabile con numerose piattaforme di terze parti.  
  
 Il componente per l'importazione dello schema, <xref:System.Runtime.Serialization.XsdDataContractImporter>, considera un documento dello schema XSD e genera classi [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] (generalmente classi del contratto dati) in modo che i formati serializzati corrispondano al determinato schema.  
  
 Si consideri ad esempio il frammento di schema seguente:  
  
 [!code-csharp[c_SchemaImportExport#8](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/cs/source.cs#8)]
 [!code-vb[c_SchemaImportExport#8](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_schemaimportexport/vb/source.vb#8)]  
  
 genera il tipo seguente (leggermente semplificato per una migliore leggibilità)  
  
 [!code-csharp[c_SchemaImportExport#1](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/cs/source.cs#1)]
 [!code-vb[c_SchemaImportExport#1](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_schemaimportexport/vb/source.vb#1)]  
  
 Si noti che il tipo generato segue diverse procedure consigliate del contratto dati (vedere [le procedure consigliate: controllo delle versioni del contratto dati](../../../../docs/framework/wcf/best-practices-data-contract-versioning.md)):  
  
-   Il tipo implementa l'interfaccia <xref:System.Runtime.Serialization.IExtensibleDataObject>. Per altre informazioni, vedere [Contratti di dati compatibili con versioni successive](../../../../docs/framework/wcf/feature-details/forward-compatible-data-contracts.md).  
  
-   I membri dati vengono implementati come proprietà pubbliche che incapsulano campi privati.  
  
-   La classe è una classe parziale e le aggiunte possono essere eseguite senza modificare il codice generato.  
  
 La classe <xref:System.Runtime.Serialization.XsdDataContractExporter> consente di eseguire l'inverso, ovvero considera i tipi serializzabili con `DataContractSerializer` e genera un documento dello schema XSD.  
  
## <a name="fidelity-is-not-guaranteed"></a>Fedeltà non garantita   
 Non è garantito che lo schema o i tipi eseguano un round trip con fedeltà assoluta (A *round trip* significa che importare uno schema per creare un set di classi e l'esportazione del risultato per creare nuovamente uno schema.) È possibile che non venga restituito lo stesso schema. Anche per l'inversione del processo non è garantito il mantenimento della fedeltà (quando si esporta un tipo per generare lo schema e quindi si importa di nuovo il tipo, è improbabile che venga restituito lo stesso tipo).  
  
## <a name="supported-types"></a>Tipi supportati  
 Il modello del contratto dati supporta solo un sottoinsieme limitato dello schema WC3. Qualsiasi schema che non è conforme a tale sottoinsieme genererà un'eccezione durante il processo di importazione. Ad esempio, non esiste alcun sistema per specificare che un membro dati di un contratto dati debba essere serializzato come attributo XML. Di conseguenza, gli schemi che richiedono l'utilizzo di attributi XML non sono supportati e verranno generate eccezioni durante l'importazione, poiché è impossibile generare un contratto dati con la proiezione XML corretta.  
  
 Ad esempio, non è possibile importare il frammento di schema seguente utilizzando le impostazioni di importazione predefinite.  
  
 [!code-xml[c_SchemaImportExport#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_schemaimportexport/common/source.config#9)]  
  
 Per altre informazioni, vedere [riferimento dello Schema del contratto dati](../../../../docs/framework/wcf/feature-details/data-contract-schema-reference.md). Se un schema non è conforme alle regole del contratto dati, utilizzare un motore di serializzazione diverso. Ad esempio, la classe <xref:System.Xml.Serialization.XmlSerializer> utilizza un proprio meccanismo separato di importazione dello schema. È inoltre disponibile una modalità di importazione speciale in cui l'intervallo dello schema supportato viene espanso. Per altre informazioni, vedere la sezione sulla generazione <xref:System.Xml.Serialization.IXmlSerializable> digita [importazione dello Schema per generare classi](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md).  
  
 La classe `XsdDataContractExporter` supporta tutti i tipi [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] che possono essere serializzati con `DataContractSerializer`. Per altre informazioni, vedere [i tipi supportati dal serializzatore dei contratti dati](../../../../docs/framework/wcf/feature-details/types-supported-by-the-data-contract-serializer.md). Si noti che lo schema generato utilizzando `XsdDataContractExporter` consiste solitamente di dati validi che possono essere utilizzati da `XsdDataContractImporter`, a meno che non si utilizzi la classe <xref:System.Xml.Serialization.XmlSchemaProviderAttribute> per personalizzare lo schema.  
  
 Per ulteriori informazioni sull'utilizzo di <xref:System.Runtime.Serialization.XsdDataContractImporter>, vedere [importazione dello Schema per generare classi](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md).  
  
 Per ulteriori informazioni sull'utilizzo di <xref:System.Runtime.Serialization.XsdDataContractExporter>, vedere [esportazione di schemi dalle classi](../../../../docs/framework/wcf/feature-details/exporting-schemas-from-classes.md).  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Runtime.Serialization.DataContractSerializer>  
 <xref:System.Runtime.Serialization.XsdDataContractImporter>  
 <xref:System.Runtime.Serialization.XsdDataContractExporter>  
 [Importazione dello schema per generare classi](../../../../docs/framework/wcf/feature-details/importing-schema-to-generate-classes.md)  
 [Esportazione di schemi da classi](../../../../docs/framework/wcf/feature-details/exporting-schemas-from-classes.md)
