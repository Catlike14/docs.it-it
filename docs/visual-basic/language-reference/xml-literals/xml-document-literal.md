---
title: Valore letterale di documento XML (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
f1_keywords: vb.XmlLiteralDocument
helpviewer_keywords:
- XML document literal [Visual Basic]
- XML literals [Visual Basic], document
- XML documents [Visual Basic], creating
- document literal [Visual Basic]
ms.assetid: f7bbee56-0911-41de-b907-96f20450137b
caps.latest.revision: "20"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 008b5857418a572046797bf061a05f265669d427
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="xml-document-literal-visual-basic"></a>Valore letterale di documento XML (Visual Basic)
Un valore letterale che rappresenta un <xref:System.Xml.Linq.XDocument> oggetto.  
  
## <a name="syntax"></a>Sintassi  
  
```xml  
<?xml version="1.0" [encoding="encoding"] [standalone="standalone"] ?>  
[ piCommentList ]  
rootElement  
[ piCommentList ]  
```  
  
## <a name="parts"></a>Parti  
  
|Termine|Definizione|  
|---|---|  
|`encoding`|Parametro facoltativo. Usa testo letterale che dichiara la codifica del documento.|  
|`standalone`|Parametro facoltativo. Testo letterale. Deve essere "yes" o "no".|  
|`piCommentList`|Parametro facoltativo. Elenco di istruzioni di elaborazione XML e commenti XML. Assume il formato seguente:<br /><br /> `piComment [` `piComment` `... ]`<br /><br /> Ogni `piComment` può essere uno dei seguenti:<br /><br /> -   [Valore letterale istruzione di elaborazione XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md).<br />-   [Valore letterale di commento XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md).|  
|`rootElement`|Obbligatorio. Elemento radice del documento. Il formato è uno dei valori seguenti:<br /><br /> <ul><li>[Valore letterale elemento XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md).</li><li>Espressione incorporata del formato `<%=` `elementExp` `%>`. Il `elementExp` restituisce uno dei seguenti:<br /><br /> <ul><li>Oggetto <xref:System.Xml.Linq.XElement>.</li><li>Una raccolta che contiene uno <xref:System.Xml.Linq.XElement> oggetto e un numero qualsiasi di <xref:System.Xml.Linq.XProcessingInstruction> e <xref:System.Xml.Linq.XComment> oggetti.</li></ul></li></ul><br /> Per ulteriori informazioni, vedere [espressioni incorporate in XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md).|  
  
## <a name="return-value"></a>Valore restituito  
 Oggetto <xref:System.Xml.Linq.XDocument>.  
  
## <a name="remarks"></a>Note  
 Un valore letterale documento XML è identificato dalla dichiarazione XML all'inizio del valore letterale. Sebbene ogni valore letterale documento XML deve avere esattamente un elemento XML radice, può contenere un numero qualsiasi di istruzioni di elaborazione e commenti XML.  
  
 Un valore letterale documento XML non può trovarsi in un elemento XML.  
  
> [!NOTE]
>  Un valore letterale XML può estendersi su più righe senza utilizzare caratteri di continuazione di riga. Ciò consente di copiare il contenuto da un documento XML e incollarlo direttamente in un [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] programma.  
  
 Il [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] compilatore converte il valore letterale documento XML in chiamate al <xref:System.Xml.Linq.XDocument.%23ctor%2A> e <xref:System.Xml.Linq.XDeclaration.%23ctor%2A> costruttori.  
  
## <a name="example"></a>Esempio  
 L'esempio seguente crea un documento XML con una dichiarazione XML, un'istruzione di elaborazione, un commento e un elemento che contiene un altro elemento.  
  
 [!code-vb[VbXMLSamples#30](../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/xml-document-literal_1.vb)]  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Xml.Linq.XElement>  
 <xref:System.Xml.Linq.XProcessingInstruction>  
 <xref:System.Xml.Linq.XComment>  
 <xref:System.Xml.Linq.XDocument>  
 [Valore letterale istruzione di elaborazione XML](../../../visual-basic/language-reference/xml-literals/xml-processing-instruction-literal.md)  
 [Valore letterale di commento XML](../../../visual-basic/language-reference/xml-literals/xml-comment-literal.md)  
 [Valore letterale elemento XML](../../../visual-basic/language-reference/xml-literals/xml-element-literal.md)  
 [Valori letterali XML](../../../visual-basic/language-reference/xml-literals/index.md)  
 [Creazione di XML in Visual Basic](../../../visual-basic/programming-guide/language-features/xml/creating-xml.md)  
 [Espressioni incorporate in XML](../../../visual-basic/programming-guide/language-features/xml/embedded-expressions-in-xml.md)
