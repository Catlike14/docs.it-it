---
title: '&lt;exception&gt; (Guida per programmatori C#)'
ms.date: 07/20/2015
f1_keywords:
- exception
- <exception>
helpviewer_keywords:
- <exception> C# XML tag
- exception C# XML tag
ms.assetid: dd73aac5-3c74-4fcf-9498-f11bff3a2f3c
ms.openlocfilehash: eca61416077896c9fa7d5828bbab79b399ad69d3
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33332660"
---
# <a name="ltexceptiongt-c-programming-guide"></a><span data-ttu-id="a61f6-102">&lt;exception&gt; (Guida per programmatori C#)</span><span class="sxs-lookup"><span data-stu-id="a61f6-102">&lt;exception&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="a61f6-103">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a61f6-103">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="a61f6-104">Parametri</span><span class="sxs-lookup"><span data-stu-id="a61f6-104">Parameters</span></span>  
 <span data-ttu-id="a61f6-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="a61f6-105">cref = " `member`"</span></span>  
 <span data-ttu-id="a61f6-106">Riferimento ad un'eccezione disponibile dall'ambiente di compilazione corrente.</span><span class="sxs-lookup"><span data-stu-id="a61f6-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="a61f6-107">Il compilatore controlla che l'eccezione specificata esista e converte `member` nel nome canonico dell'elemento nel file XML di output.</span><span class="sxs-lookup"><span data-stu-id="a61f6-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="a61f6-108">`member` deve essere racchiuso tra virgolette doppie (" ").</span><span class="sxs-lookup"><span data-stu-id="a61f6-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="a61f6-109">Per altre informazioni su come creare un riferimento cref a un tipo generico, vedere [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span><span class="sxs-lookup"><span data-stu-id="a61f6-109">For more information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
 `description`  
 <span data-ttu-id="a61f6-110">Descrizione dell'eccezione.</span><span class="sxs-lookup"><span data-stu-id="a61f6-110">A description of the exception.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="a61f6-111">Note</span><span class="sxs-lookup"><span data-stu-id="a61f6-111">Remarks</span></span>  
 <span data-ttu-id="a61f6-112">Il tag \<exception> consente di specificare le eccezioni che possono essere generate.</span><span class="sxs-lookup"><span data-stu-id="a61f6-112">The \<exception> tag lets you specify which exceptions can be thrown.</span></span> <span data-ttu-id="a61f6-113">Questo tag può essere applicato alle definizioni di metodi, proprietà, eventi e indicizzatori.</span><span class="sxs-lookup"><span data-stu-id="a61f6-113">This tag can be applied to definitions for methods, properties, events, and indexers.</span></span>  
  
 <span data-ttu-id="a61f6-114">Compilare con [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) per elaborare i commenti relativi alla documentazione in un file.</span><span class="sxs-lookup"><span data-stu-id="a61f6-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
 <span data-ttu-id="a61f6-115">Per altre informazioni sulla gestione delle eccezioni, vedere [Eccezioni e gestione delle eccezioni](../../../csharp/programming-guide/exceptions/index.md).</span><span class="sxs-lookup"><span data-stu-id="a61f6-115">For more information about exception handling, see [Exceptions and Exception Handling](../../../csharp/programming-guide/exceptions/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="a61f6-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="a61f6-116">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#4](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/exception_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="a61f6-117">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="a61f6-117">See Also</span></span>  
 [<span data-ttu-id="a61f6-118">Guida per programmatori C#</span><span class="sxs-lookup"><span data-stu-id="a61f6-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="a61f6-119">Tag consigliati per i commenti relativi alla documentazione</span><span class="sxs-lookup"><span data-stu-id="a61f6-119">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
