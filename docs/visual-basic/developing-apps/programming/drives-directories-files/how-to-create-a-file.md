---
title: 'Procedura: creare un file in Visual Basic'
ms.custom: 
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- text files [Visual Basic], creating
- files [Visual Basic], creating
ms.assetid: 0253bb6d-5519-4a50-b882-b93ef5cca0d9
caps.latest.revision: "15"
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: c1ce74601136c870097d6d558e1f3ff12ba1c212
ms.sourcegitcommit: 34ec7753acf76f90a0fa845235ef06663dc9e36e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2017
---
# <a name="how-to-create-a-file-in-visual-basic"></a><span data-ttu-id="11bd2-102">Procedura: creare un file in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="11bd2-102">How to: Create a File in Visual Basic</span></span>
<span data-ttu-id="11bd2-103">In questo esempio viene creato un file di testo vuoto nel percorso specificato usando il metodo <xref:System.IO.File.Create%2A> nella classe <xref:System.IO.File>.</span><span class="sxs-lookup"><span data-stu-id="11bd2-103">This example creates an empty text file at the specified path using the <xref:System.IO.File.Create%2A> method in the <xref:System.IO.File> class.</span></span>  
  
## <a name="example"></a><span data-ttu-id="11bd2-104">Esempio</span><span class="sxs-lookup"><span data-stu-id="11bd2-104">Example</span></span>  
 [!code-vb[VbFileIOMisc#1](../../../../visual-basic/developing-apps/programming/drives-directories-files/codesnippet/VisualBasic/how-to-create-a-file_1.vb)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="11bd2-105">Compilazione del codice</span><span class="sxs-lookup"><span data-stu-id="11bd2-105">Compiling the Code</span></span>  
 <span data-ttu-id="11bd2-106">Usare la variabile `file` per scrivere il file.</span><span class="sxs-lookup"><span data-stu-id="11bd2-106">Use the `file` variable to write to the file.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="11bd2-107">Programmazione efficiente</span><span class="sxs-lookup"><span data-stu-id="11bd2-107">Robust Programming</span></span>  
 <span data-ttu-id="11bd2-108">Se il file esiste già, viene sostituito.</span><span class="sxs-lookup"><span data-stu-id="11bd2-108">If the file already exists, it is replaced.</span></span>  
  
 <span data-ttu-id="11bd2-109">Le seguenti condizioni possono generare un'eccezione:</span><span class="sxs-lookup"><span data-stu-id="11bd2-109">The following conditions may cause an exception:</span></span>  
  
-   <span data-ttu-id="11bd2-110">Il nome del percorso non è valido.</span><span class="sxs-lookup"><span data-stu-id="11bd2-110">The path name is malformed.</span></span> <span data-ttu-id="11bd2-111">Contiene ad esempio caratteri non validi o è costituito solo da uno spazio (<xref:System.ArgumentException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-111">For example, it contains illegal characters or is only white space (<xref:System.ArgumentException>).</span></span>  
  
-   <span data-ttu-id="11bd2-112">Il percorso è di sola lettura (<xref:System.IO.IOException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-112">The path is read-only (<xref:System.IO.IOException>).</span></span>  
  
-   <span data-ttu-id="11bd2-113">Il nome del percorso è `Nothing` (<xref:System.ArgumentNullException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-113">The path name is `Nothing` (<xref:System.ArgumentNullException>).</span></span>  
  
-   <span data-ttu-id="11bd2-114">Il nome del percorso è troppo lungo (<xref:System.IO.PathTooLongException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-114">The path name is too long (<xref:System.IO.PathTooLongException>).</span></span>  
  
-   <span data-ttu-id="11bd2-115">Il percorso non è valido (<xref:System.IO.DirectoryNotFoundException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-115">The path is invalid (<xref:System.IO.DirectoryNotFoundException>).</span></span>  
  
-   <span data-ttu-id="11bd2-116">Il percorso contiene solo due punti ":" (<xref:System.NotSupportedException>).</span><span class="sxs-lookup"><span data-stu-id="11bd2-116">The path is only a colon ":" (<xref:System.NotSupportedException>).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="11bd2-117">Sicurezza di .NET Framework</span><span class="sxs-lookup"><span data-stu-id="11bd2-117">.NET Framework Security</span></span>  
 <span data-ttu-id="11bd2-118">È possibile che venga generata un'eccezione <xref:System.Security.SecurityException> in ambienti ad attendibilità parziale.</span><span class="sxs-lookup"><span data-stu-id="11bd2-118">A <xref:System.Security.SecurityException> may be thrown in partial-trust environments.</span></span>  
  
 <span data-ttu-id="11bd2-119">La chiamata al metodo <xref:System.IO.File.Create%2A> richiede <xref:System.Security.Permissions.FileIOPermission>.</span><span class="sxs-lookup"><span data-stu-id="11bd2-119">The call to the <xref:System.IO.File.Create%2A> method requires <xref:System.Security.Permissions.FileIOPermission>.</span></span>  
  
 <span data-ttu-id="11bd2-120">Viene generata un'eccezione <xref:System.UnauthorizedAccessException> se l'utente non dispone dell'autorizzazione per creare il file.</span><span class="sxs-lookup"><span data-stu-id="11bd2-120">An <xref:System.UnauthorizedAccessException> is thrown if the user does not have permission to create the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="11bd2-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="11bd2-121">See Also</span></span>  
 <xref:System.IO>  
 <xref:System.IO.File.Create%2A>  
 [<span data-ttu-id="11bd2-122">Uso di librerie da codice parzialmente attendibile</span><span class="sxs-lookup"><span data-stu-id="11bd2-122">Using Libraries from Partially Trusted Code</span></span>](../../../../framework/misc/using-libraries-from-partially-trusted-code.md)  
 [<span data-ttu-id="11bd2-123">Nozioni fondamentali sulla sicurezza per l’accesso al codice</span><span class="sxs-lookup"><span data-stu-id="11bd2-123">Code Access Security Basics</span></span>](../../../../framework/misc/code-access-security-basics.md)
