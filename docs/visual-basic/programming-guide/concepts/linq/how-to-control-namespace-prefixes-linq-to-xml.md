---
title: 'Procedura: controllare i prefissi dello spazio dei nomi (Visual Basic) (LINQ to XML)'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2fcf28a5-31b6-409d-84ea-27c22f71fc9f
caps.latest.revision: "3"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: a48feeb25cc8d28d57edc7421f73b2829f8c19ef
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="how-to-control-namespace-prefixes-visual-basic-linq-to-xml"></a>Procedura: controllare i prefissi dello spazio dei nomi (Visual Basic) (LINQ to XML)
In questo argomento viene descritto come controllare i prefissi di spazio dei nomi.  
  
## <a name="example"></a>Esempio  
  
### <a name="description"></a>Descrizione  
 In questo esempio vengono dichiarati due spazi dei nomi. Specifica che il `http://www.adventure-works.com` dello spazio dei nomi ha il prefisso `aw`e che il `www.fourthcoffee.com` dello spazio dei nomi ha il prefisso `fc`.  
  
### <a name="code"></a>Codice  
  
```vb  
Imports <xmlns:aw="http://www.adventure-works.com">  
Imports <xmlns:fc="www.fourthcoffee.com">  
  
Module Module1  
  
    Sub Main()  
        Dim root As XElement = _  
            <aw:Root>  
                <fc:Child>  
                    <aw:DifferentChild>other content</aw:DifferentChild>  
                </fc:Child>  
                <aw:Child2>c2 content</aw:Child2>  
                <fc:Child3>c3 content</fc:Child3>  
            </aw:Root>  
        Console.WriteLine(root)  
    End Sub  
  
End Module  
```  
  
### <a name="comments"></a>Commenti  
 Questo esempio produce il seguente output:  
  
```xml  
<aw:Root xmlns:fc="www.fourthcoffee.com" xmlns:aw="http://www.adventure-works.com">  
  <fc:Child>  
    <aw:DifferentChild>other content</aw:DifferentChild>  
  </fc:Child>  
  <aw:Child2>c2 content</aw:Child2>  
  <fc:Child3>c3 content</fc:Child3>  
</aw:Root>  
```  
  
## <a name="see-also"></a>Vedere anche  
 [Utilizzo di spazi dei nomi XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/working-with-xml-namespaces.md)
