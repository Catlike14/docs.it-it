---
title: Strumento con priorità al contratto ("contract-first")
ms.date: 03/30/2017
ms.assetid: 0a880690-f460-4475-a5f4-9f91ce08fcc6
ms.openlocfilehash: 86ef109425a75e46e056447f4f40df36aa332293
ms.sourcegitcommit: 700b9003ea6bdd83a53458bbc436c9b5778344f1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/03/2018
ms.locfileid: "48261615"
---
# <a name="contract-first-tool"></a>Strumento con priorità al contratto ("contract-first")
I contratti di servizio devono spesso essere creati a partire da servizi esistenti. In [!INCLUDE[net_v45](../../../includes/net-v45-md.md)] le classi dei contratti dati possono essere create automaticamente dai servizi esistenti utilizzando lo strumento con priorità al contratto ("contract-first"). Per utilizzare lo strumento con priorità al contratto ("contract-first") è necessario che il file di definizione di XML Schema (XSD) sia scaricato localmente; lo strumento non può importare i contratti dati remoti tramite HTTP.

 Lo strumento contratto-first è integrato in Visual Studio 2012 come un'attività di compilazione. I file di codice generati dall'attività di compilazione vengono creati ogni volta che il progetto viene compilato, in modo che nel progetto possano essere facilmente adottate le modifiche nel contratto di servizio sottostante.

 Di seguito sono riportati i tipi di schema che lo strumento con priorità al contratto ("contract-first") può importare:

```xml
<xsd:complexType>
<xsd:simpleType>
```

 I tipi semplici non vengono generati se sono primitivi come `Int16` o `String`; i tipi complessi non vengono generati se sono di tipo `Collection`. Inoltre i tipi non vengono generati se fanno parte di un altro oggetto `xsd:complexType`. In tutti questi casi, per un riferimento ai tipi vengono invece utilizzati i tipi esistenti nel progetto.

## <a name="adding-a-data-contract-to-a-project"></a>Aggiunta di un contratto dati a un progetto
 Prima di poter utilizzare lo strumento con priorità al contratto ("contract-first") è necessario aggiungere il contratto di servizio (XSD) al progetto. Ai fini di questa panoramica, per illustrare le funzioni con priorità al contratto ("contract-first") verrà utilizzato il contratto seguente. Questa definizione del servizio è un subset di piccole dimensioni del contratto di servizio utilizzato dall'API di ricerca di Bing.

```xml
<?xml version="1.0" encoding="utf-8"?>
<xs:schema id="ServiceSchema"
    targetNamespace="http://tempuri.org/ServiceSchema.xsd"
    elementFormDefault="qualified"
    xmlns="http://tempuri.org/ServiceSchema.xsd"
    xmlns:mstns="http://tempuri.org/ServiceSchema.xsd"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
>
  <xs:complexType name="SearchRequest">
    <xs:sequence>
      <xs:element minOccurs="0" maxOccurs="1" name="Version" type="xs:string" default="2.2" />
      <xs:element minOccurs="0" maxOccurs="1" name="Market" type="xs:string" />
      <xs:element minOccurs="0" maxOccurs="1" name="UILanguage" type="xs:string" />
      <xs:element minOccurs="1" maxOccurs="1" name="Query" type="xs:string" />
      <xs:element minOccurs="1" maxOccurs="1" name="AppId" type="xs:string" />
      <xs:element minOccurs="0" maxOccurs="1" name="Latitude" type="xs:double" />
      <xs:element minOccurs="0" maxOccurs="1" name="Longitude" type="xs:double" />
      <xs:element minOccurs="0" maxOccurs="1" name="Radius" type="xs:double" />
    </xs:sequence>
  </xs:complexType>
  <xs:simpleType name="WebSearchOption">
    <xs:restriction base="xs:string">
      <xs:enumeration value="DisableHostCollapsing" />
      <xs:enumeration value="DisableQueryAlterations" />
    </xs:restriction>
  </xs:simpleType>
</xs:schema>
```

 Per aggiungere il contratto di servizio precedente al progetto, fare clic sul progetto e selezionare **Aggiungi nuovo...** . Selezionare Definizione schema nel riquadro WCF della finestra di dialogo Modelli e denominare il nuovo file SampleContract.xsd. Copiare e incollare il codice illustrato in precedenza nella visualizzazione codice del nuovo file.

## <a name="configuring-contract-first-options"></a>Configurazione delle opzioni con priorità al contratto ("contract-first")
 Contratto-first opzioni possono essere configurate nel menu delle proprietà di un progetto WCF. Per abilitare lo sviluppo incentrato contratto, selezionare la **Abilita XSD come linguaggio di definizione del tipo** casella di controllo nella pagina WCF della finestra delle proprietà del progetto.

 ![Il contratto che mostra le opzioni del progetto WCF&#45;primo](../../../docs/framework/wcf/media/contractfirstoptions.png "ContractFirstOptions")

 Per configurare le proprietà avanzate, fare clic sul pulsante Avanzate.

 ![Advanced contratto&#45;proprietà First](../../../docs/framework/wcf/media/contractfirstadvanced.png "ContractFirstAdvanced")

 Per la generazione di codice dai contratti è possibile configurare le seguenti impostazioni avanzate. Attualmente, le impostazioni possono essere configurate solo per tutti i file del progetto e non per singoli file.

-   **Modalità serializzatore**: questa impostazione determina il serializzatore che viene utilizzato per la lettura dei file di contratto di servizio. Quando **XML Serializer** è selezionata, il **tipi di raccolta** e **Riutilizza tipi** opzioni vengono disabilitate. Queste opzioni si applicano solo per i **Data Contract Serializer**.

-   **Riutilizza tipi**: questa impostazione specifica che le librerie sono usate per riutilizzare il tipo. Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **Tipo di raccolta**: questa impostazione specifica il tipo completo o qualificato dall'assembly da utilizzare per il tipo di raccolta dati. Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **Tipo di dizionario**: questa impostazione specifica il tipo completo o qualificato dall'assembly da utilizzare per il tipo di dati del dizionario.

-   **EnableDataBinding**: questa impostazione specifica se implementare il <xref:System.ComponentModel.INotifyPropertyChanged> interfaccia su tutti i tipi di dati per implementare il data binding.

-   **ExcludedTypes**: questa impostazione specifica l'elenco di tipi completi o completi di assembly da escludere dagli assembly di riferimento. Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **GenerateInternalTypes**: questa impostazione specifica se generare classi contrassegnate come interne. Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **GenerateSerializableTypes**: questa impostazione specifica se generare classi con la <xref:System.SerializableAttribute> attributo. Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **/Importxmltypes**: questa impostazione specifica se è necessario configurare il serializzatore dei contratti dati per applicare la <xref:System.SerializableAttribute> attributo alle classi senza il <xref:System.Runtime.Serialization.DataContractAttribute> attributo.  Questa impostazione si applica solo se **modalità serializzatore** è impostata su **Data Contract Serializer**.

-   **SupportFx35TypedDataSets**: questa impostazione specifica se fornire funzionalità aggiuntive per i set di dati tipizzati creati per .net Framework 3.5. Quando **modalità serializzatore** è impostata su **XML Serializer**, il <xref:System.Data.Design.TypedDataSetSchemaImporterExtensionFx35> estensione verrà aggiunti nell'utilità di importazione di XML schema quando questo valore è impostato su True. Quando **modalità serializzatore** è impostata su **Data Contract Serializer**, il tipo <xref:System.DateTimeOffset> verranno esclusi dai riferimenti quando questo valore è impostato su False, in modo che un <xref:System.DateTimeOffset> viene sempre generato per versioni precedenti del framework.

-   **InputXsdFiles**: questa impostazione specifica l'elenco dei file di input. Ogni file deve contenere un XML Schema valido.

-   **Linguaggio**: questa impostazione specifica il linguaggio del codice contratto generato. L'impostazione deve essere riconoscibile da <xref:System.CodeDom.Compiler.CodeDomProvider>.

-   **NamespaceMappings**: questa impostazione specifica i mapping degli spazi dei nomi di destinazione XSD agli spazi dei nomi CLR. Ogni mapping deve utilizzare il formato seguente:

    ```xml
    "<Schema Namespace>, <CLR Namespace>"
    ```

     Il serializzatore XML accetta solo un mapping nel formato seguente:

    ```xml
    "*, <CLR Namespace>"
    ```

-   **OutputDirectory**: questa impostazione specifica la directory in cui verranno generati i file di codice.

 Le impostazioni verranno utilizzate per generare i tipi di contratti di servizio dai relativi file quando il progetto viene compilato.

## <a name="using-contract-first-development"></a>Utilizzo dello sviluppo con priorità al contratto ("contract-first")
 Dopo l'aggiunta di contratto di servizio al progetto e confermando le impostazioni di compilazione, compilare il progetto premendo **F6**. I tipi definiti nel contratto di servizio potranno quindi essere utilizzati nel progetto.

 Per utilizzare i tipi definiti nel contratto di servizio, aggiungere un riferimento a `ContractTypes` nello spazio dei nomi corrente:

```csharp
using MyProjectNamespace.ContractTypes;
```

 I tipi definiti nel contratto di servizio potranno quindi essere risolti nel progetto, come mostrato di seguito.

 ![Uso dei tipi derivati da un contratto di servizio](../../../docs/framework/wcf/media/contractfirsttypes.png "ContractFirstTypes")

 I tipi generati dallo strumento vengono creati nel file GeneratedXSDTypes.cs. Il file viene creato nel \<directory di progetto >/obj /\<configurazione compilazione >/xsdgeneratedcode / directory per impostazione predefinita. Lo schema di esempio all'inizio di questo argomento viene convertito come segue:

```csharp
//------------------------------------------------------------------------------
// <auto-generated>
//     This code was generated by a tool.
//     Runtime Version:4.0.30319.17330
//
//     Changes to this file may cause incorrect behavior and will be lost if
//     the code is regenerated.
// </auto-generated>
//------------------------------------------------------------------------------

namespace TestXSD3.ContractTypes
{
    using System.Xml.Serialization;

    /// <remarks/>
    [System.CodeDom.Compiler.GeneratedCodeAttribute("System.Xml", "4.0.30319.17330")]
    [System.SerializableAttribute()]
    [System.Diagnostics.DebuggerStepThroughAttribute()]
    [System.ComponentModel.DesignerCategoryAttribute("code")]
    [System.Xml.Serialization.XmlTypeAttribute(Namespace="http://tempuri.org/ServiceSchema.xsd")]
    [System.Xml.Serialization.XmlRootAttribute(Namespace="http://tempuri.org/ServiceSchema.xsd", IsNullable=true)]
    public partial class SearchRequest
    {

        private string versionField;

        private string marketField;

        private string uILanguageField;

        private string queryField;

        private string appIdField;

        private double latitudeField;

        private bool latitudeFieldSpecified;

        private double longitudeField;

        private bool longitudeFieldSpecified;

        private double radiusField;

        private bool radiusFieldSpecified;

        public SearchRequest()
        {
            this.versionField = "2.2";
        }

        /// <remarks/>
        [System.ComponentModel.DefaultValueAttribute("2.2")]
        public string Version
        {
            get
            {
                return this.versionField;
            }
            set
            {
                this.versionField = value;
            }
        }

        /// <remarks/>
        public string Market
        {
            get
            {
                return this.marketField;
            }
            set
            {
                this.marketField = value;
            }
        }

        /// <remarks/>
        public string UILanguage
        {
            get
            {
                return this.uILanguageField;
            }
            set
            {
                this.uILanguageField = value;
            }
        }

        /// <remarks/>
        public string Query
        {
            get
            {
                return this.queryField;
            }
            set
            {
                this.queryField = value;
            }
        }

        /// <remarks/>
        public string AppId
        {
            get
            {
                return this.appIdField;
            }
            set
            {
                this.appIdField = value;
            }
        }

        /// <remarks/>
        public double Latitude
        {
            get
            {
                return this.latitudeField;
            }
            set
            {
                this.latitudeField = value;
            }
        }

        /// <remarks/>
        [System.Xml.Serialization.XmlIgnoreAttribute()]
        public bool LatitudeSpecified
        {
            get
            {
                return this.latitudeFieldSpecified;
            }
            set
            {
                this.latitudeFieldSpecified = value;
            }
        }

        /// <remarks/>
        public double Longitude
        {
            get
            {
                return this.longitudeField;
            }
            set
            {
                this.longitudeField = value;
            }
        }

        /// <remarks/>
        [System.Xml.Serialization.XmlIgnoreAttribute()]
        public bool LongitudeSpecified
        {
            get
            {
                return this.longitudeFieldSpecified;
            }
            set
            {
                this.longitudeFieldSpecified = value;
            }
        }

        /// <remarks/>
        public double Radius
        {
            get
            {
                return this.radiusField;
            }
            set
            {
                this.radiusField = value;
            }
        }

        /// <remarks/>
        [System.Xml.Serialization.XmlIgnoreAttribute()]
        public bool RadiusSpecified
        {
            get
            {
                return this.radiusFieldSpecified;
            }
            set
            {
                this.radiusFieldSpecified = value;
            }
        }
    }

    /// <remarks/>
    [System.CodeDom.Compiler.GeneratedCodeAttribute("System.Xml", "4.0.30319.17330")]
    [System.SerializableAttribute()]
    [System.Xml.Serialization.XmlTypeAttribute(Namespace="http://tempuri.org/ServiceSchema.xsd")]
    [System.Xml.Serialization.XmlRootAttribute(Namespace="http://tempuri.org/ServiceSchema.xsd", IsNullable=false)]
    public enum WebSearchOption
    {

        /// <remarks/>
        DisableHostCollapsing,

        /// <remarks/>
        DisableQueryAlterations,
    }
}
```

## <a name="errors-and-warnings"></a>Errori e avvisi
 Gli errori e gli avvisi rilevati durante l'analisi dello schema XSD verranno visualizzati come errori e avvisi di compilazione.

## <a name="interface-inheritance"></a>Ereditarietà dell'interfaccia
 Non è possibile utilizzare l'ereditarietà dell'interfaccia con lo sviluppo con priorità al contratto ("contract-first"); ciò è coerente con la modalità con cui le interfacce si comportano in altre operazioni. Per utilizzare un'interfaccia che eredita da un'interfaccia di base, utilizzare due endpoint separati. Nel primo endpoint viene utilizzato il contratto ereditato e nel secondo endpoint viene implementata l'interfaccia di base.
