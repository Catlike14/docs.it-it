---
title: 'Procedura: Enumerare gli archivi per lo spazio di memorizzazione isolato'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- enumerating stores
- data storage using isolated storage, enumerating stores
- storing data using isolated storage, enumerating stores
- stores, enumerating
- isolated storage, enumerating stores
- data stores, enumerating
ms.assetid: 0fcf279a-f241-48f0-8034-2e3d331f1fcb
caps.latest.revision: "13"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8f8863f1d8b3c7f4ed8f65f8f8eb3e8af51b0405
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-enumerate-stores-for-isolated-storage"></a><span data-ttu-id="52a9d-102">Procedura: Enumerare gli archivi per lo spazio di memorizzazione isolato</span><span class="sxs-lookup"><span data-stu-id="52a9d-102">How to: Enumerate Stores for Isolated Storage</span></span>
<span data-ttu-id="52a9d-103">È possibile enumerare tutti gli archivi isolati dell'utente corrente utilizzando il metodo statico <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="52a9d-103">You can enumerate all isolated stores for the current user by using the  <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A?displayProperty=nameWithType> static method.</span></span> <span data-ttu-id="52a9d-104">Questo metodo accetta un valore <xref:System.IO.IsolatedStorage.IsolatedStorageScope> e restituisce un enumeratore <xref:System.IO.IsolatedStorage.IsolatedStorageFile>.</span><span class="sxs-lookup"><span data-stu-id="52a9d-104">This  method takes an <xref:System.IO.IsolatedStorage.IsolatedStorageScope> value and returns an <xref:System.IO.IsolatedStorage.IsolatedStorageFile> enumerator.</span></span> <span data-ttu-id="52a9d-105">Per enumerare gli archivi, è necessario disporre di <xref:System.Security.Permissions.IsolatedStorageFilePermission> autorizzazione che specifica il <xref:System.Security.Permissions.IsolatedStorageContainment.AdministerIsolatedStorageByUser> valore.</span><span class="sxs-lookup"><span data-stu-id="52a9d-105">To enumerate stores, you must have the <xref:System.Security.Permissions.IsolatedStorageFilePermission> permission that specifies the <xref:System.Security.Permissions.IsolatedStorageContainment.AdministerIsolatedStorageByUser> value.</span></span> <span data-ttu-id="52a9d-106">Se si chiama il <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A> metodo con il <xref:System.IO.IsolatedStorage.IsolatedStorageScope.User> valore, viene restituita una matrice di <xref:System.IO.IsolatedStorage.IsolatedStorageFile> gli oggetti definiti per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="52a9d-106">If you call the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A> method with the <xref:System.IO.IsolatedStorage.IsolatedStorageScope.User> value, it returns an array of <xref:System.IO.IsolatedStorage.IsolatedStorageFile> objects that are defined for the current user.</span></span>  
  
## <a name="example"></a><span data-ttu-id="52a9d-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="52a9d-107">Example</span></span>  
 <span data-ttu-id="52a9d-108">L'esempio di codice seguente viene ottenuto un archivio che è isolato dall'utente e all'assembly, vengono creati alcuni file e recupera i file utilizzando il <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="52a9d-108">The following code example obtains a store that is isolated by user and assembly, creates a few files, and retrieves those files by using the <xref:System.IO.IsolatedStorage.IsolatedStorageFile.GetEnumerator%2A> method.</span></span>  
  
 [!code-csharp[Conceptual.IsolatedStorage#2](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.isolatedstorage/cs/source2.cs#2)]
 [!code-vb[Conceptual.IsolatedStorage#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.isolatedstorage/vb/source2.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="52a9d-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="52a9d-109">See Also</span></span>  
 <xref:System.IO.IsolatedStorage.IsolatedStorageFile>  
 [<span data-ttu-id="52a9d-110">Spazio di memorizzazione isolato</span><span class="sxs-lookup"><span data-stu-id="52a9d-110">Isolated Storage</span></span>](../../../docs/standard/io/isolated-storage.md)
