---
title: 'Procedura: Serializzare tramite DataContractSerializer (C#)'
ms.date: 07/20/2015
ms.assetid: 3320ecbf-cdbe-480e-979c-2c14bbef9988
ms.openlocfilehash: 2c0324b1eeeab9f6cf9223e2a3e201771b188749
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/04/2018
ms.locfileid: "43510991"
---
# <a name="how-to-serialize-using-datacontractserializer-c"></a><span data-ttu-id="08497-102">Procedura: Serializzare tramite DataContractSerializer (C#)</span><span class="sxs-lookup"><span data-stu-id="08497-102">How to: Serialize Using DataContractSerializer (C#)</span></span>
<span data-ttu-id="08497-103">In questo argomento viene illustrato un esempio in cui viene usato <xref:System.Runtime.Serialization.DataContractSerializer> per eseguire la serializzazione e la deserializzazione.</span><span class="sxs-lookup"><span data-stu-id="08497-103">This topic shows an example that serializes and deserializes using <xref:System.Runtime.Serialization.DataContractSerializer>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="08497-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="08497-104">Example</span></span>  
 <span data-ttu-id="08497-105">Nell'esempio seguente vengono creati diversi oggetti contenenti oggetti <xref:System.Xml.Linq.XElement>.</span><span class="sxs-lookup"><span data-stu-id="08497-105">The following example creates a number of objects that contain <xref:System.Xml.Linq.XElement> objects.</span></span> <span data-ttu-id="08497-106">Tali oggetti vengono quindi serializzati in file di testo e successivamente deserializzati dagli stessi file di testo.</span><span class="sxs-lookup"><span data-stu-id="08497-106">It then serializes them to text files, and then deserializes them from the text files.</span></span>  
  
```csharp  
using System;  
using System.Xml;  
using System.Xml.Linq;  
using System.IO;  
using System.Runtime.Serialization;  
  
public class XLinqTest  
{  
    public static void Main()  
    {  
        Test<XElement>(CreateXElement());  
        Test<XElementContainer>(new XElementContainer());  
        Test<XElementNullContainer>(new XElementNullContainer());  
    }  
  
    public static void Test<T>(T obj)  
    {  
        DataContractSerializer s = new DataContractSerializer(typeof(T));  
        using (FileStream fs = File.Open("test" + typeof(T).Name + ".xml", FileMode.Create))  
        {  
            Console.WriteLine("Testing for type: {0}", typeof(T));   
            s.WriteObject(fs, obj);  
        }  
        using (FileStream fs = File.Open("test" + typeof(T).Name + ".xml", FileMode.Open))  
        {  
            object s2 = s.ReadObject(fs);  
            if (s2 == null)  
                Console.WriteLine("  Deserialized object is null (Nothing in VB)");  
            else  
                Console.WriteLine("  Deserialized type: {0}", s2.GetType());  
        }  
    }  
  
    public static XElement CreateXElement()  
    {  
        return new XElement(XName.Get("NameInNamespace", "http://www.adventure-works.org"));  
    }  
}  
  
[DataContract]  
public class XElementContainer  
{  
    [DataMember]  
    public XElement member;  
  
    public XElementContainer()  
    {  
        member = XLinqTest.CreateXElement();  
    }  
}  
  
[DataContract]  
public class XElementNullContainer  
{  
    [DataMember]  
    public XElement member;  
  
    public XElementNullContainer()  
    {  
        member = null;  
    }  
}  
```  
  
 <span data-ttu-id="08497-107">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="08497-107">This example produces the following output:</span></span>  
  
```  
Testing for type: System.Xml.Linq.XElement  
  Deserialized type: System.Xml.Linq.XElement  
Testing for type: XElementContainer  
  Deserialized type: XElementContainer  
Testing for type: XElementNullContainer  
  Deserialized type: XElementNullContainer  
```  
  
## <a name="see-also"></a><span data-ttu-id="08497-108">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="08497-108">See Also</span></span>

- [<span data-ttu-id="08497-109">Serializzazione di oggetti grafici contenenti oggetti XElement (C#)</span><span class="sxs-lookup"><span data-stu-id="08497-109">Serializing Object Graphs that Contain XElement Objects (C#)</span></span>](../../../../csharp/programming-guide/concepts/linq/serializing-object-graphs-that-contain-xelement-objects.md)
