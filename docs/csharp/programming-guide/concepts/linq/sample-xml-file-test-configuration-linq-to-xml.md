---
title: 'File XML di esempio: configurazione di test (LINQ to XML)'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-csharp
ms.topic: article
ms.assetid: 45bfb509-c1d4-4b4f-9690-1cb0c9816516
caps.latest.revision: "3"
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: 5990690dd5bd7138eab9ef2bf1234d251e67c351
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="sample-xml-file-test-configuration-linq-to-xml"></a><span data-ttu-id="fdeb9-102">File XML di esempio: configurazione di test (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="fdeb9-102">Sample XML File: Test Configuration (LINQ to XML)</span></span>
<span data-ttu-id="fdeb9-103">Il file XML seguente viene usato in vari esempi nella documentazione di [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="fdeb9-103">The following XML file is used in various examples in the [!INCLUDE[sqltecxlinq](~/includes/sqltecxlinq-md.md)] documentation.</span></span> <span data-ttu-id="fdeb9-104">Si tratta di un file di configurazione di test.</span><span class="sxs-lookup"><span data-stu-id="fdeb9-104">This is a test configuration file.</span></span>  
  
## <a name="testconfigxml"></a><span data-ttu-id="fdeb9-105">TestConfig.xml</span><span class="sxs-lookup"><span data-stu-id="fdeb9-105">TestConfig.xml</span></span>  
  
```xml  
<?xml version="1.0"?>  
<Tests>  
  <Test TestId="0001" TestType="CMD">  
    <Name>Convert number to string</Name>  
    <CommandLine>Examp1.EXE</CommandLine>  
    <Input>1</Input>  
    <Output>One</Output>  
  </Test>  
  <Test TestId="0002" TestType="CMD">  
    <Name>Find succeeding characters</Name>  
    <CommandLine>Examp2.EXE</CommandLine>  
    <Input>abc</Input>  
    <Output>def</Output>  
  </Test>  
  <Test TestId="0003" TestType="GUI">  
    <Name>Convert multiple numbers to strings</Name>  
    <CommandLine>Examp2.EXE /Verbose</CommandLine>  
    <Input>123</Input>  
    <Output>One Two Three</Output>  
  </Test>  
  <Test TestId="0004" TestType="GUI">  
    <Name>Find correlated key</Name>  
    <CommandLine>Examp3.EXE</CommandLine>  
    <Input>a1</Input>  
    <Output>b1</Output>  
  </Test>  
  <Test TestId="0005" TestType="GUI">  
    <Name>Count characters</Name>  
    <CommandLine>FinalExamp.EXE</CommandLine>  
    <Input>This is a test</Input>  
    <Output>14</Output>  
  </Test>  
  <Test TestId="0006" TestType="GUI">  
    <Name>Another Test</Name>  
    <CommandLine>Examp2.EXE</CommandLine>  
    <Input>Test Input</Input>  
    <Output>10</Output>  
  </Test>  
</Tests>  
```  
  
## <a name="see-also"></a><span data-ttu-id="fdeb9-106">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fdeb9-106">See Also</span></span>  
 [<span data-ttu-id="fdeb9-107">Documenti XML di esempio (LINQ to XML)</span><span class="sxs-lookup"><span data-stu-id="fdeb9-107">Sample XML Documents (LINQ to XML)</span></span>](../../../../csharp/programming-guide/concepts/linq/sample-xml-documents-linq-to-xml.md)
