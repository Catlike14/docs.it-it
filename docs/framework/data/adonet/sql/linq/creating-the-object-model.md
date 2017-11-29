---
title: Creazione del modello a oggetti
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 27afce86-9b1d-45fb-8e0b-636bf671a236
caps.latest.revision: "3"
author: JennieHubbard
ms.author: jhubbard
manager: jhubbard
ms.openlocfilehash: c933e7e2871d0a72e8e10a25d94e9d458cdd1d43
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="creating-the-object-model"></a><span data-ttu-id="c1f18-102">Creazione del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="c1f18-102">Creating the Object Model</span></span>
<span data-ttu-id="c1f18-103">È possibile creare un modello a oggetti da un database esistente e usare il modello nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="c1f18-103">You can create your object model from an existing database and use the model in its default state.</span></span> <span data-ttu-id="c1f18-104">È anche possibile personalizzare molti aspetti del modello e il relativo comportamento.</span><span class="sxs-lookup"><span data-stu-id="c1f18-104">You can also customize many aspects of the model and its behavior.</span></span>  
  
 <span data-ttu-id="c1f18-105">Se si utilizza [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)], è possibile utilizzare il [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] per creare il modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="c1f18-105">If you are using [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)], you can use the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] to create your object model.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c1f18-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="c1f18-106">In This Section</span></span>  
 [<span data-ttu-id="c1f18-107">Procedura: generare il modello a oggetti in Visual Basic o c#</span><span class="sxs-lookup"><span data-stu-id="c1f18-107">How to: Generate the Object Model in Visual Basic or C#</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-generate-the-object-model-in-visual-basic-or-csharp.md)  
 <span data-ttu-id="c1f18-108">Viene descritto come usare lo strumento SQLMetal dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="c1f18-108">Describes how to use the SQLMetal command-line tool.</span></span> <span data-ttu-id="c1f18-109">Viene inoltre fornito un collegamento a [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] per gli utenti di [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1f18-109">Also provides a link to the [!INCLUDE[vs_ordesigner_long](../../../../../../includes/vs-ordesigner-long-md.md)] for [!INCLUDE[vs_current_short](../../../../../../includes/vs-current-short-md.md)] users</span></span>  
  
 [<span data-ttu-id="c1f18-110">Procedura: generare il modello a oggetti come File esterno</span><span class="sxs-lookup"><span data-stu-id="c1f18-110">How to: Generate the Object Model as an External File</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-generate-the-object-model-as-an-external-file.md)  
 <span data-ttu-id="c1f18-111">Viene descritto come generare un file di mapping esterno anziché usare il mapping basato su attributi.</span><span class="sxs-lookup"><span data-stu-id="c1f18-111">Describes how to generate an external mapping file instead of using attribute-based mapping.</span></span>  
  
 [<span data-ttu-id="c1f18-112">Procedura: generare codice personalizzato modificando un File DBML</span><span class="sxs-lookup"><span data-stu-id="c1f18-112">How to: Generate Customized Code by Modifying a DBML File</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-generate-customized-code-by-modifying-a-dbml-file.md)  
 <span data-ttu-id="c1f18-113">Viene descritto come generare codice [!INCLUDE[vbprvb](../../../../../../includes/vbprvb-md.md)] o C# da un file di metadati DBML.</span><span class="sxs-lookup"><span data-stu-id="c1f18-113">Describes how to generate [!INCLUDE[vbprvb](../../../../../../includes/vbprvb-md.md)] or C# code from a DBML metadata file.</span></span>  
  
 [<span data-ttu-id="c1f18-114">Procedura: convalidare file di Mapping esterni e DBML</span><span class="sxs-lookup"><span data-stu-id="c1f18-114">How to: Validate DBML and External Mapping Files</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-validate-dbml-and-external-mapping-files.md)  
 <span data-ttu-id="c1f18-115">Viene descritto come convalidare file di mapping modificati (funzionalità avanzate).</span><span class="sxs-lookup"><span data-stu-id="c1f18-115">Describes how to validate mapping files that you have modified (advanced).</span></span>  
  
 [<span data-ttu-id="c1f18-116">Procedura: rendere serializzabili le entità</span><span class="sxs-lookup"><span data-stu-id="c1f18-116">How to: Make Entities Serializable</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-make-entities-serializable.md)  
 <span data-ttu-id="c1f18-117">Viene descritto come aggiungere attributi appropriati per creare entità serializzabili.</span><span class="sxs-lookup"><span data-stu-id="c1f18-117">Describes how to add appropriate attributes to make entities serializable.</span></span>  
  
 [<span data-ttu-id="c1f18-118">Procedura: personalizzare classi di entità utilizzando l'Editor di codice</span><span class="sxs-lookup"><span data-stu-id="c1f18-118">How to: Customize Entity Classes by Using the Code Editor</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)  
 <span data-ttu-id="c1f18-119">Viene descritto come usare l'editor di codice per scrivere codice di mapping o per personalizzare il codice generato.</span><span class="sxs-lookup"><span data-stu-id="c1f18-119">Describes how to use the code editor to write your own mapping code, or customize code that has been autogenerated.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c1f18-120">Sezioni correlate</span><span class="sxs-lookup"><span data-stu-id="c1f18-120">Related Sections</span></span>  
 [<span data-ttu-id="c1f18-121">LINQ to SQL modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="c1f18-121">The LINQ to SQL Object Model</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)  
 <span data-ttu-id="c1f18-122">Vengono fornite informazioni dettagliate sul [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="c1f18-122">Provides details about the [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] object model.</span></span>  
  
 [<span data-ttu-id="c1f18-123">Passaggi tipici per l'utilizzo di LINQ to SQL</span><span class="sxs-lookup"><span data-stu-id="c1f18-123">Typical Steps for Using LINQ to SQL</span></span>](../../../../../../docs/framework/data/adonet/sql/linq/typical-steps-for-using-linq-to-sql.md)  
 <span data-ttu-id="c1f18-124">Vengono illustrati i passaggi tipici che è necessario seguire per implementare un'applicazione [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c1f18-124">Explains the typical steps that you follow to implement a [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] application.</span></span>
