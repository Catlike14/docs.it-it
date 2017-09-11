---
title: 'Procedura: caricare XML da un File, stringa o flusso (Visual Basic) | Documenti di Microsoft'
ms.custom: 
ms.date: 2015-07-20
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
helpviewer_keywords:
- XML [Visual Basic], loading
- LINQ to XML [Visual Basic], loading XML from files
ms.assetid: 2b02dcec-4cca-4575-b4ad-89ceb87b984c
caps.latest.revision: 13
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 31905a37f09db5f5192123f0118252fbe8b02eff
ms.openlocfilehash: 6361ef29b88b4a05b774cf67ca0f3832a8e214fa
ms.contentlocale: it-it
ms.lasthandoff: 05/26/2017

---
# <a name="how-to-load-xml-from-a-file-string-or-stream-visual-basic"></a><span data-ttu-id="b2acc-102">Procedura: caricare XML da un file, da una stringa o da un flusso (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="b2acc-102">How to: Load XML from a File, String, or Stream (Visual Basic)</span></span>
<span data-ttu-id="b2acc-103">È possibile creare [valori letterali XML](../../../../visual-basic/language-reference/xml-literals/index.md) e popolarli con i contenuti da un'origine esterna, ad esempio un file, una stringa o un flusso, utilizzando vari metodi.</span><span class="sxs-lookup"><span data-stu-id="b2acc-103">You can create [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md) and populate them with the contents from an external source such as a file, a string, or a stream by using several methods.</span></span> <span data-ttu-id="b2acc-104">Questi metodi sono illustrati negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="b2acc-104">These methods are shown in the following examples.</span></span>  
  
[!INCLUDE[note_settings_general](~/includes/note-settings-general-md.md)]  
  
### <a name="to-load-xml-from-a-file"></a><span data-ttu-id="b2acc-105">Per caricare XML da un file</span><span class="sxs-lookup"><span data-stu-id="b2acc-105">To load XML from a file</span></span>  
  
-   <span data-ttu-id="b2acc-106">Per popolare un valore letterale XML come un <xref:System.Xml.Linq.XElement>o <xref:System.Xml.Linq.XDocument>oggetto da un file, utilizzare il `Load` (metodo).</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement></span><span class="sxs-lookup"><span data-stu-id="b2acc-106">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a file, use the `Load` method.</span></span> <span data-ttu-id="b2acc-107">Questo metodo può richiedere un percorso del file, un flusso di testo o flusso XML come input.</span><span class="sxs-lookup"><span data-stu-id="b2acc-107">This method can take a file path, text stream, or XML stream as input.</span></span>  
  
     <span data-ttu-id="b2acc-108">Esempio di codice seguente viene illustrato l'utilizzo di <xref:System.Xml.Linq.XDocument.Load%28System.String%29>metodo per popolare un <xref:System.Xml.Linq.XDocument>oggetto con XML da un file di testo.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XDocument.Load%28System.String%29></span><span class="sxs-lookup"><span data-stu-id="b2acc-108">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Load%28System.String%29> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a text file.</span></span>  
  
     <span data-ttu-id="b2acc-109">[!code-vb[VbXMLSamples&#43;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_1.vb)]</span><span class="sxs-lookup"><span data-stu-id="b2acc-109">[!code-vb[VbXMLSamples#43](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_1.vb)]</span></span>  
  
### <a name="to-load-xml-from-a-string"></a><span data-ttu-id="b2acc-110">Per caricare XML da una stringa</span><span class="sxs-lookup"><span data-stu-id="b2acc-110">To load XML from a string</span></span>  
  
-   <span data-ttu-id="b2acc-111">Per popolare un valore letterale XML come un <xref:System.Xml.Linq.XElement>o <xref:System.Xml.Linq.XDocument>dell'oggetto da una stringa, è possibile utilizzare il `Parse` (metodo).</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement></span><span class="sxs-lookup"><span data-stu-id="b2acc-111">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a string, you can use the `Parse` method.</span></span>  
  
     <span data-ttu-id="b2acc-112">Esempio di codice seguente viene illustrato l'utilizzo di <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName>metodo per popolare un <xref:System.Xml.Linq.XDocument>oggetto con XML da una stringa.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-112">The following code example shows the use of the <xref:System.Xml.Linq.XDocument.Parse%28System.String%29?displayProperty=fullName> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from a string.</span></span>  
  
     <span data-ttu-id="b2acc-113">[!code-vb[VbXMLSamples&#47;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_2.vb)]</span><span class="sxs-lookup"><span data-stu-id="b2acc-113">[!code-vb[VbXMLSamples#47](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_2.vb)]</span></span>  
  
### <a name="to-load-xml-from-a-stream"></a><span data-ttu-id="b2acc-114">Per caricare XML da un flusso</span><span class="sxs-lookup"><span data-stu-id="b2acc-114">To load XML from a stream</span></span>  
  
-   <span data-ttu-id="b2acc-115">Per popolare un valore letterale XML come un <xref:System.Xml.Linq.XElement>o <xref:System.Xml.Linq.XDocument>dell'oggetto da un flusso, è possibile utilizzare il `Load` metodo o <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName>(metodo).</xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName> </xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XElement></span><span class="sxs-lookup"><span data-stu-id="b2acc-115">To populate an XML literal such as an <xref:System.Xml.Linq.XElement> or <xref:System.Xml.Linq.XDocument> object from a stream, you can use the `Load` method or the <xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName> method.</span></span>  
  
 <span data-ttu-id="b2acc-116">Esempio di codice seguente viene illustrato l'utilizzo di <xref:System.Xml.Linq.XNode.ReadFrom%2A>metodo per popolare un <xref:System.Xml.Linq.XDocument>oggetto con XML da un flusso XML.</xref:System.Xml.Linq.XDocument> </xref:System.Xml.Linq.XNode.ReadFrom%2A></span><span class="sxs-lookup"><span data-stu-id="b2acc-116">The following code example shows the use of the <xref:System.Xml.Linq.XNode.ReadFrom%2A> method to populate an <xref:System.Xml.Linq.XDocument> object with XML from an XML stream.</span></span>  
  
 <span data-ttu-id="b2acc-117">[!code-vb[VbXMLSamples n.&46;](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_3.vb)]</span><span class="sxs-lookup"><span data-stu-id="b2acc-117">[!code-vb[VbXMLSamples#46](../../../../visual-basic/language-reference/operators/codesnippet/VisualBasic/how-to-load-xml-from-a-file-string-or-stream_3.vb)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b2acc-118">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b2acc-118">See Also</span></span>  
 <span data-ttu-id="b2acc-119"><xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName></xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-119"><xref:System.Xml.Linq.XDocument.Load%2A?displayProperty=fullName></span></span>   
 <span data-ttu-id="b2acc-120"><xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName></xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-120"><xref:System.Xml.Linq.XElement.Load%2A?displayProperty=fullName></span></span>   
 <span data-ttu-id="b2acc-121"><xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName></xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-121"><xref:System.Xml.Linq.XElement.Parse%2A?displayProperty=fullName></span></span>   
 <span data-ttu-id="b2acc-122"><xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName></xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-122"><xref:System.Xml.Linq.XDocument.Parse%2A?displayProperty=fullName></span></span>   
 <span data-ttu-id="b2acc-123"><xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName></xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="b2acc-123"><xref:System.Xml.Linq.XNode.ReadFrom%2A?displayProperty=fullName></span></span>   
<span data-ttu-id="b2acc-124"> [Valori letterali XML](../../../../visual-basic/language-reference/xml-literals/index.md) </span><span class="sxs-lookup"><span data-stu-id="b2acc-124"> [XML Literals](../../../../visual-basic/language-reference/xml-literals/index.md) </span></span>  
<span data-ttu-id="b2acc-125"> [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md) </span><span class="sxs-lookup"><span data-stu-id="b2acc-125"> [XML](../../../../visual-basic/programming-guide/language-features/xml/index.md) </span></span>  
<span data-ttu-id="b2acc-126"> [Modifica di XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)</span><span class="sxs-lookup"><span data-stu-id="b2acc-126"> [Manipulating XML in Visual Basic](../../../../visual-basic/programming-guide/language-features/xml/manipulating-xml.md)</span></span>

