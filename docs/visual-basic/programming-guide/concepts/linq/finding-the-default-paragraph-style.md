---
title: Ricerca dello stile di paragrafo predefinito (Visual Basic) | Documenti di Microsoft
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
ms.assetid: 9d094a4a-ec8c-41b0-b7ab-a3deb2a01d45
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 22d97c95a1dec52c0290555daeedce51c5a567e3
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017


---
# <a name="finding-the-default-paragraph-style-visual-basic"></a><span data-ttu-id="ff425-102">Ricerca dello stile di paragrafo predefinito (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ff425-102">Finding the Default Paragraph Style (Visual Basic)</span></span>
<span data-ttu-id="ff425-103">La prima attività per la modifica di informazioni in un'esercitazione documento WordprocessingML consiste nel trovare lo stile predefinito dei paragrafi del documento.</span><span class="sxs-lookup"><span data-stu-id="ff425-103">The first task in the Manipulating Information in a WordprocessingML Document tutorial is to find the default style of paragraphs in the document.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ff425-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="ff425-104">Example</span></span>  
  
### <a name="description"></a><span data-ttu-id="ff425-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff425-105">Description</span></span>  
 <span data-ttu-id="ff425-106">Nell'esempio seguente viene aperto un documento WordprocessingML di Office Open XML, vengono individuate le parti del package relative a documento e stile, quindi viene eseguita una query che trova il nome dello stile predefinito.</span><span class="sxs-lookup"><span data-stu-id="ff425-106">The following example opens an Office Open XML WordprocessingML document, finds the document and style parts of the package, and then executes a query that finds the default style name.</span></span> <span data-ttu-id="ff425-107">Per informazioni sui pacchetti di documento Office Open XML e le parti sono costituiti, vedere [i dettagli di Office Open XML documenti WordprocessingML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/details-of-office-open-xml-wordprocessingml-documents.md).</span><span class="sxs-lookup"><span data-stu-id="ff425-107">For information about Office Open XML document packages, and the parts they consist of, see [Details of Office Open XML WordprocessingML Documents (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/details-of-office-open-xml-wordprocessingml-documents.md).</span></span>  
  
 <span data-ttu-id="ff425-108">La query cerca un nodo denominato `w:style` che ha un attributo denominato `w:type` con il valore "paragraph" e un attributo denominato `w:default` con il valore "1".</span><span class="sxs-lookup"><span data-stu-id="ff425-108">The query finds a node named `w:style` that has an attribute named `w:type` with a value of "paragraph", and also has an attribute named `w:default` with a value of "1".</span></span> <span data-ttu-id="ff425-109">Poiché non esiste un solo nodo XML con questi attributi, la query utilizza il <xref:System.Linq.Enumerable.First%2A?displayProperty=fullName>per convertire una raccolta in un singleton.</xref:System.Linq.Enumerable.First%2A?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="ff425-109">Because there will be only one XML node with these attributes, the query uses the <xref:System.Linq.Enumerable.First%2A?displayProperty=fullName> operator to convert a collection to a singleton.</span></span> <span data-ttu-id="ff425-110">Ottiene quindi il valore dell'attributo con il nome `w:styleId`.</span><span class="sxs-lookup"><span data-stu-id="ff425-110">It then gets the value of the attribute with the name `w:styleId`.</span></span>  
  
 <span data-ttu-id="ff425-111">In questo esempio vengono usate classi dell'assembly WindowsBase</span><span class="sxs-lookup"><span data-stu-id="ff425-111">This example uses classes from the WindowsBase assembly.</span></span> <span data-ttu-id="ff425-112">Utilizza i tipi di <xref:System.IO.Packaging?displayProperty=fullName>dello spazio dei nomi.</xref:System.IO.Packaging?displayProperty=fullName></span><span class="sxs-lookup"><span data-stu-id="ff425-112">It uses types in the <xref:System.IO.Packaging?displayProperty=fullName> namespace.</span></span>  
  
### <a name="code"></a><span data-ttu-id="ff425-113">Codice</span><span class="sxs-lookup"><span data-stu-id="ff425-113">Code</span></span>  
  
```vb  
Imports <xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">  
  
Module Module1  
  
    Sub Main()  
  
        Const fileName As String = "SampleDoc.docx"  
  
        Const documentRelationshipType As String = _  
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument"  
        Const stylesRelationshipType As String = _  
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/styles"  
  
        Dim xDoc As XDocument = Nothing  
        Dim styleDoc As XDocument = Nothing  
  
        Using wdPackage As Package = Package.Open(fileName, FileMode.Open, FileAccess.Read)  
            Dim docPackageRelationship As PackageRelationship = _  
              wdPackage.GetRelationshipsByType(documentRelationshipType).FirstOrDefault()  
            If docPackageRelationship IsNot Nothing Then  
                Dim documentUri As Uri = PackUriHelper.ResolvePartUri(New Uri("/", UriKind.Relative), _  
                  docPackageRelationship.TargetUri)  
                Dim documentPart As PackagePart = wdPackage.GetPart(documentUri)  
  
                ' Load the document XML in the part into an XDocument instance.  
                xDoc = XDocument.Load(XmlReader.Create(documentPart.GetStream()))  
  
                ' Find the styles part. There will only be one.  
                Dim styleRelation As PackageRelationship = _  
                  documentPart.GetRelationshipsByType(stylesRelationshipType).FirstOrDefault()  
                If styleRelation IsNot Nothing Then  
                    Dim styleUri As Uri = _  
                      PackUriHelper.ResolvePartUri(documentUri, styleRelation.TargetUri)  
                    Dim stylePart As PackagePart = wdPackage.GetPart(styleUri)  
  
                    ' Load the style XML in the part into an XDocument instance.  
                    styleDoc = XDocument.Load(XmlReader.Create(stylePart.GetStream()))  
                End If  
            End If  
        End Using  
  
        ' The following query finds all the paragraphs that have the default style.  
        Dim defParas As IEnumerable(Of XElement) = _  
            From style In styleDoc.Root.<w:style> _  
            Where style.@w:type.Equals("paragraph") And _  
                   style.@w:default.Equals("1") _  
            Select style  
        ' Then find the style of the first.  
        Dim defaultStyle As String = defParas.First().@w:styleId  
  
        Console.WriteLine("The default style is: " & defaultStyle)  
    End Sub  
End Module  
```  
  
### <a name="comments"></a><span data-ttu-id="ff425-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff425-114">Comments</span></span>  
 <span data-ttu-id="ff425-115">Questo esempio produce il seguente output:</span><span class="sxs-lookup"><span data-stu-id="ff425-115">This example produces the following output:</span></span>  
  
```  
The default style is: Normal  
```  
  
## <a name="next-steps"></a><span data-ttu-id="ff425-116">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="ff425-116">Next Steps</span></span>  
 <span data-ttu-id="ff425-117">Nell'esempio seguente, si creerà una query simile che trova tutti i paragrafi in un documento e i relativi stili:</span><span class="sxs-lookup"><span data-stu-id="ff425-117">In the next example, you'll create a similar query that finds all the paragraphs in a document and their styles:</span></span>  
  
-   [<span data-ttu-id="ff425-118">Recupero dei paragrafi e i relativi stili (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ff425-118">Retrieving the Paragraphs and Their Styles (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/retrieving-the-paragraphs-and-their-styles.md)  
  
## <a name="see-also"></a><span data-ttu-id="ff425-119">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ff425-119">See Also</span></span>  
 [<span data-ttu-id="ff425-120">Esercitazione: Manipolazione di contenuto in un documento WordprocessingML (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="ff425-120">Tutorial: Manipulating Content in a WordprocessingML Document (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/tutorial-manipulating-content-in-a-wordprocessingml-document.md)
