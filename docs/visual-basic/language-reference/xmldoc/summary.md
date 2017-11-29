---
title: '&lt;riepilogo&gt; (Visual Basic)'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 2a3008d1393c44aa0ec2398a2bd6afa079013e7e
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="ltsummarygt-visual-basic"></a><span data-ttu-id="dc4da-102">&lt;riepilogo&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="dc4da-102">&lt;summary&gt; (Visual Basic)</span></span>
<span data-ttu-id="dc4da-103">Specifica il riepilogo del membro.</span><span class="sxs-lookup"><span data-stu-id="dc4da-103">Specifies the summary of the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="dc4da-104">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc4da-104">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="dc4da-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc4da-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="dc4da-106">Un riepilogo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dc4da-106">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="dc4da-107">Note</span><span class="sxs-lookup"><span data-stu-id="dc4da-107">Remarks</span></span>  
 <span data-ttu-id="dc4da-108">Utilizzare il `<summary>` tag per descrivere un tipo o un membro del tipo.</span><span class="sxs-lookup"><span data-stu-id="dc4da-108">Use the `<summary>` tag to describe a type or a type member.</span></span> <span data-ttu-id="dc4da-109">Utilizzare [ \<osservazioni >](../../../visual-basic/language-reference/xmldoc/remarks.md) per aggiungere informazioni supplementari alla descrizione di un tipo.</span><span class="sxs-lookup"><span data-stu-id="dc4da-109">Use [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) to add supplemental information to a type description.</span></span>  
  
 <span data-ttu-id="dc4da-110">Il testo per il `<summary>` tag è l'unica fonte di informazioni sul tipo in IntelliSense e viene anche visualizzato nel Visualizzatore oggetti.</span><span class="sxs-lookup"><span data-stu-id="dc4da-110">The text for the `<summary>` tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser.</span></span> <span data-ttu-id="dc4da-111">Per informazioni sul Visualizzatore oggetti, vedere [visualizzazione della struttura del codice](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="dc4da-111">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="dc4da-112">Compilare con [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) per elaborare i commenti relativi alla documentazione in un file.</span><span class="sxs-lookup"><span data-stu-id="dc4da-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dc4da-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="dc4da-113">Example</span></span>  
 <span data-ttu-id="dc4da-114">Questo esempio viene utilizzato il `<summary>` tag per descrivere il `ResetCounter` (metodo) e `Counter` proprietà.</span><span class="sxs-lookup"><span data-stu-id="dc4da-114">This example uses the `<summary>` tag to describe the `ResetCounter` method and `Counter` property.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="dc4da-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dc4da-115">See Also</span></span>  
 [<span data-ttu-id="dc4da-116">Tag di commento XML</span><span class="sxs-lookup"><span data-stu-id="dc4da-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
