---
title: Convalida XDR con XmlSchemaCollection
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
ms.assetid: 00833027-1428-4586-83c1-42f5de3323d1
author: mairaw
ms.author: mairaw
ms.openlocfilehash: 72bb3c2badef5262907e2e4fa8b461b576e8867d
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2018
ms.locfileid: "42934167"
---
# <a name="xdr-validation-with-xmlschemacollection"></a><span data-ttu-id="ec2ef-102">Convalida XDR con XmlSchemaCollection</span><span class="sxs-lookup"><span data-stu-id="ec2ef-102">XDR Validation with XmlSchemaCollection</span></span>

<span data-ttu-id="ec2ef-103">Se lo schema XDR (XML-Data Reduced) rispetto al quale si esegue la convalida è archiviato in **XmlSchemaCollection**, sarà associato all'URI dello spazio dei nomi specificato quando lo schema è stato aggiunto alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="ec2ef-103">If the XML-Data Reduced (XDR) schema you are validating against is stored in the **XmlSchemaCollection**, it is associated with the namespace URI specified when the schema was added to the collection.</span></span> <span data-ttu-id="ec2ef-104">**XmlValidatingReader** associa l'URI dello spazio dei nomi nel documento XML allo schema che corrisponde a quell'URI nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ec2ef-104">**XmlValidatingReader** maps the namespace URI in the XML document to the schema that corresponds to that URI in the collection.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ec2ef-105">La classe <xref:System.Xml.Schema.XmlSchemaCollection> è obsoleta ed è stata sostituita dalla classe <xref:System.Xml.Schema.XmlSchemaSet>.</span><span class="sxs-lookup"><span data-stu-id="ec2ef-105">The <xref:System.Xml.Schema.XmlSchemaCollection> class is now obsolete and has been replaced with the <xref:System.Xml.Schema.XmlSchemaSet> class.</span></span> <span data-ttu-id="ec2ef-106">Per altre informazioni sulla classe <xref:System.Xml.Schema.XmlSchemaSet>, vedere [XmlSchemaSet per la compilazione di schemi](xmlschemaset-for-schema-compilation.md).</span><span class="sxs-lookup"><span data-stu-id="ec2ef-106">For more information about the <xref:System.Xml.Schema.XmlSchemaSet> class see, [XmlSchemaSet for Schema Compilation](xmlschemaset-for-schema-compilation.md).</span></span>

<span data-ttu-id="ec2ef-107">Se ad esempio l'elemento radice del documento XML è `<bookstore xmlns="urn:newbooks-schema">`, quando lo schema viene aggiunto a **XmlSchemaCollection**, fa riferimento allo stesso spazio dei nomi, nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="ec2ef-107">For example, if the root element of the XML document is `<bookstore xmlns="urn:newbooks-schema">`, when the schema is added to the **XmlSchemaCollection** it references the same namespace, as follows:</span></span>

```
xsc.Add("urn:newbooks-schema", "newbooks.xdr")
```

<span data-ttu-id="ec2ef-108">Nell'esempio di codice seguente viene creato un **XmlValidatingReader** che accetta un **XmlTextReader** e aggiunge uno schema XDR, HeadCount.xdr, a **XmlSchemaCollection**.</span><span class="sxs-lookup"><span data-stu-id="ec2ef-108">The following code example creates an **XmlValidatingReader** that takes an **XmlTextReader** and adds an XDR schema, HeadCount.xdr, to the **XmlSchemaCollection**.</span></span>

```vb
Imports System
Imports System.IO
Imports System.Xml
Imports System.Xml.Schema

Namespace ValidationSample

   Class Sample

      Public Shared Sub Main()
         Dim tr As New XmlTextReader("HeadCount.xml")
         Dim vr As New XmlValidatingReader(tr)

         vr.Schemas.Add("xdrHeadCount", "HeadCount.xdr")
         vr.ValidationType = ValidationType.XDR
         AddHandler vr.ValidationEventHandler, AddressOf ValidationHandler

         While vr.Read()
            PrintTypeInfo(vr)
            If vr.NodeType = XmlNodeType.Element Then
               While vr.MoveToNextAttribute()
                  PrintTypeInfo(vr)
               End While
            End If
         End While
         Console.WriteLine("Validation finished")
      End Sub
      ' Main

      Public Shared Sub PrintTypeInfo(vr As XmlValidatingReader)
         If Not (vr.SchemaType Is Nothing) Then
            If TypeOf vr.SchemaType Is XmlSchemaDatatype Or TypeOf vr.SchemaType Is XmlSchemaSimpleType Then
               Dim value As Object = vr.ReadTypedValue()
               Console.WriteLine("{0}({1},{2}):{3}", vr.NodeType, vr.Name, value.GetType().Name, value)
            End If
         End If
      End Sub
      ' PrintTypeInfo

      Public Shared Sub ValidationHandler(sender As Object, args As ValidationEventArgs)
         Console.WriteLine("***Validation error")
         Console.WriteLine("Severity:{0}", args.Severity)
         Console.WriteLine("Message:{0}", args.Message)
      End Sub
      ' ValidationHandler
   End Class
   ' Sample
End Namespace
' ValidationSample
```

```csharp
using System;
using System.IO;
using System.Xml;
using System.Xml.Schema;

namespace ValidationSample
{
   class Sample
   {
      public static void Main()
      {
         XmlTextReader tr = new XmlTextReader("HeadCount.xml");
         XmlValidatingReader vr = new XmlValidatingReader(tr);

         vr.Schemas.Add("xdrHeadCount", "HeadCount.xdr");
         vr.ValidationType = ValidationType.XDR;
         vr.ValidationEventHandler += new ValidationEventHandler (ValidationHandler);

         while(vr.Read())
         {
            PrintTypeInfo(vr);
            if(vr.NodeType == XmlNodeType.Element)
            {
               while(vr.MoveToNextAttribute())
                  PrintTypeInfo(vr);
            }
         }
         Console.WriteLine("Validation finished");
      }

      public static void PrintTypeInfo(XmlValidatingReader vr)
      {
         if(vr.SchemaType != null)
         {
            if(vr.SchemaType is XmlSchemaDatatype || vr.SchemaType is XmlSchemaSimpleType)
            {
               object value = vr.ReadTypedValue();
               Console.WriteLine("{0}({1},{2}):{3}", vr.NodeType, vr.Name, value.GetType().Name, value);
            }
         }
      }

      public static void ValidationHandler(object sender, ValidationEventArgs args)
      {
         Console.WriteLine("***Validation error");
         Console.WriteLine("\tSeverity:{0}", args.Severity);
         Console.WriteLine("\tMessage:{0}", args.Message);
      }
   }
}
```

<span data-ttu-id="ec2ef-109">Di seguito viene indicato il contenuto del file di input, *HeadCount.xml*, da convalidare:</span><span class="sxs-lookup"><span data-stu-id="ec2ef-109">The following outlines the contents of the input file, *HeadCount.xml*, to be validated:</span></span>

```xml
<!--Load HeadCount.xdr in SchemaCollection for Validation-->
<HeadCount xmlns='xdrHeadCount'>
   <Name>Waldo Pepper</Name>
   <Name>Red Pepper</Name>
</HeadCount>
```

<span data-ttu-id="ec2ef-110">Di seguito viene indicato il contenuto del file dello schema XDR, *HeadCount.xdr*, rispetto al quale eseguire la convalida:</span><span class="sxs-lookup"><span data-stu-id="ec2ef-110">The following outlines the contents of the XDR schema file, *HeadCount.xdr*, to be validated against:</span></span>

```xml
<Schema xmlns="urn:schemas-microsoft-com:xml-data" xmlns:dt="urn:schemas-microsoft-com:datatypes">
   <ElementType name="Name" content="textOnly"/>
   <AttributeType name="Bldg" default="2"/>
   <ElementType name="HeadCount" content="eltOnly">
      <element type="Name"/>
      <attribute type="Bldg"/>
   </ElementType>
</Schema>
```

## <a name="see-also"></a><span data-ttu-id="ec2ef-111">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ec2ef-111">See Also</span></span>

<xref:System.Xml.XmlValidatingReader.ValidationType%2A>  
[<span data-ttu-id="ec2ef-112">Compilazione dello schema XmlSchemaCollection</span><span class="sxs-lookup"><span data-stu-id="ec2ef-112">XmlSchemaCollection Schema Compilation</span></span>](xmlschemacollection-schema-compilation.md)  