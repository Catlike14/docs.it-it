---
title: Introduzione a LINQ (Visual Basic) | Documenti di Microsoft
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
ms.assetid: c6339c12-9b2d-433e-961c-0d2b7f0091c2
caps.latest.revision: 3
author: dotnet-bot
ms.author: dotnetcontent
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: d2c02daacc2674da31715e5fda027b97e6b7bc97
ms.contentlocale: it-it
ms.lasthandoff: 04/12/2017

---
# <a name="introduction-to-linq-visual-basic"></a><span data-ttu-id="8b537-102">Introduzione a LINQ (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8b537-102">Introduction to LINQ (Visual Basic)</span></span>
<span data-ttu-id="8b537-103">Language-Integrated Query (LINQ) è che una novità introdotta in .NET Framework versione 3.5 che colma il divario tra il mondo degli oggetti e il mondo dei dati.</span><span class="sxs-lookup"><span data-stu-id="8b537-103">Language-Integrated Query (LINQ) is an innovation introduced in the .NET Framework version 3.5 that bridges the gap between the world of objects and the world of data.</span></span>  
  
 <span data-ttu-id="8b537-104">In genere, le query sui dati sono espressi come stringhe semplici senza controllo dei tipi in fase di compilazione o il supporto IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="8b537-104">Traditionally, queries against data are expressed as simple strings without type checking at compile time or IntelliSense support.</span></span> <span data-ttu-id="8b537-105">Inoltre, è necessario imparare un linguaggio di query diverso per ogni tipo di origine dati: SQL database, documenti XML, vari servizi Web e così via.</span><span class="sxs-lookup"><span data-stu-id="8b537-105">Furthermore, you have to learn a different query language for each type of data source: SQL databases, XML documents, various Web services, and so on.</span></span> <span data-ttu-id="8b537-106">LINQ consente una *query* un costrutto di costrutto di linguaggio in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8b537-106">LINQ makes a *query* a first-class language construct in Visual Basic.</span></span> <span data-ttu-id="8b537-107">Scrivere query su raccolte fortemente tipizzate di oggetti utilizzando parole chiave del linguaggio e gli operatori comuni.</span><span class="sxs-lookup"><span data-stu-id="8b537-107">You write queries against strongly typed collections of objects by using language keywords and familiar operators.</span></span>  
  
 <span data-ttu-id="8b537-108">È possibile scrivere query LINQ in Visual Basic per database SQL Server, documenti XML, DataSet ADO.NET e qualsiasi raccolta di oggetti che supporta <xref:System.Collections.IEnumerable>o generica <xref:System.Collections.Generic.IEnumerable%601>interfaccia.</xref:System.Collections.Generic.IEnumerable%601> </xref:System.Collections.IEnumerable></span><span class="sxs-lookup"><span data-stu-id="8b537-108">You can write LINQ queries in Visual Basic for SQL Server databases, XML documents, ADO.NET Datasets, and any collection of objects that supports <xref:System.Collections.IEnumerable> or the generic <xref:System.Collections.Generic.IEnumerable%601> interface.</span></span> <span data-ttu-id="8b537-109">Supporto per LINQ viene anche fornito da terze parti per molti servizi Web e altre implementazioni di database.</span><span class="sxs-lookup"><span data-stu-id="8b537-109">LINQ support is also provided by third parties for many Web services and other database implementations.</span></span>  
  
 <span data-ttu-id="8b537-110">È possibile utilizzare le query LINQ nei nuovi progetti o insieme alle query LINQ non nei progetti esistenti.</span><span class="sxs-lookup"><span data-stu-id="8b537-110">You can use LINQ queries in new projects, or alongside non-LINQ queries in existing projects.</span></span> <span data-ttu-id="8b537-111">L'unico requisito è che il progetto è destinato a .NET Framework 3.5 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="8b537-111">The only requirement is that the project target .NET Framework 3.5 or later.</span></span>  
  
 <span data-ttu-id="8b537-112">Da Visual Studio nella figura seguente mostra una query LINQ parzialmente completata per un database di SQL Server in c# e Visual Basic con controllo completo del tipo e il supporto IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="8b537-112">The following illustration from Visual Studio shows a partially-completed LINQ query against a SQL Server database in both C# and Visual Basic with full type checking and IntelliSense support.</span></span>  
  
 <span data-ttu-id="8b537-113">![Query LINQ con Intellisense](../../../../csharp/programming-guide/concepts/linq/media/query_intell.png "Query_Intell")</span><span class="sxs-lookup"><span data-stu-id="8b537-113">![LINQ query with Intellisense](../../../../csharp/programming-guide/concepts/linq/media/query_intell.png "Query_Intell")</span></span>  
  
## <a name="next-steps"></a><span data-ttu-id="8b537-114">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="8b537-114">Next Steps</span></span>  
 <span data-ttu-id="8b537-115">Per ulteriori informazioni su LINQ, iniziare ad acquisire dimestichezza con alcuni concetti di base nella sezione Introduzione [Introduzione a LINQ in Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/getting-started-with-linq.md), e quindi leggere la documentazione per la tecnologia LINQ in cui si è interessati:</span><span class="sxs-lookup"><span data-stu-id="8b537-115">To learn more details about LINQ, start by becoming familiar with some basic concepts in the Getting Started section [Getting Started with LINQ in Visual Basic](../../../../visual-basic/programming-guide/concepts/linq/getting-started-with-linq.md), and then read the documentation for the LINQ technology in which you are interested:</span></span>  
  
-   <span data-ttu-id="8b537-116">Database di SQL Server: [LINQ to SQL](https://msdn.microsoft.com/library/bb386976)</span><span class="sxs-lookup"><span data-stu-id="8b537-116">SQL Server databases: [LINQ to SQL](https://msdn.microsoft.com/library/bb386976)</span></span>  
  
-   <span data-ttu-id="8b537-117">Documenti XML: [LINQ to XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml.md)</span><span class="sxs-lookup"><span data-stu-id="8b537-117">XML documents: [LINQ to XML (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-xml.md)</span></span>  
  
-   <span data-ttu-id="8b537-118">Set di dati ADO.NET: [LINQ to DataSet](http://msdn.microsoft.com/library/743e3755-3ecb-45a2-8d9b-9ed41f0dcf17)</span><span class="sxs-lookup"><span data-stu-id="8b537-118">ADO.NET Datasets: [LINQ to DataSet](http://msdn.microsoft.com/library/743e3755-3ecb-45a2-8d9b-9ed41f0dcf17)</span></span>  
  
-   <span data-ttu-id="8b537-119">Insiemi .NET, file, stringhe e così via: [LINQ to Objects (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md)</span><span class="sxs-lookup"><span data-stu-id="8b537-119">.NET collections, files, strings and so on: [LINQ to Objects (Visual Basic)](../../../../visual-basic/programming-guide/concepts/linq/linq-to-objects.md)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8b537-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="8b537-120">See Also</span></span>  
 [<span data-ttu-id="8b537-121">Language-Integrated Query (LINQ) (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="8b537-121">Language-Integrated Query (LINQ) (Visual Basic)</span></span>](../../../../visual-basic/programming-guide/concepts/linq/index.md)
