---
title: 'Procedura: definire un ambito del nome'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- name scope [WPF], defining
- Storyboards [WPF], animating in procedural code
- animation [WPF], Storyboards [WPF], in procedural code
ms.assetid: 4f361925-6a08-40dc-8231-a61111c6b28b
caps.latest.revision: "6"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: 3007088f849f40e4e9b4f1846c19c98c33e95c17
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-define-a-name-scope"></a><span data-ttu-id="599dd-102">Procedura: definire un ambito del nome</span><span class="sxs-lookup"><span data-stu-id="599dd-102">How to: Define a Name Scope</span></span>
<span data-ttu-id="599dd-103">Per aggiungere un'animazione con <xref:System.Windows.Media.Animation.Storyboard> nel codice, è necessario creare un <xref:System.Windows.NameScope> e registrare i nomi degli oggetti di destinazione con l'elemento che possiede tale ambito dei nomi.</span><span class="sxs-lookup"><span data-stu-id="599dd-103">To animate with <xref:System.Windows.Media.Animation.Storyboard> in code, you must create a <xref:System.Windows.NameScope> and register the target objects' names with the element that owns that name scope.</span></span> <span data-ttu-id="599dd-104">Nell'esempio seguente, un <xref:System.Windows.NameScope> viene creato per `myMainPanel`.</span><span class="sxs-lookup"><span data-stu-id="599dd-104">In the following example, a <xref:System.Windows.NameScope> is created for `myMainPanel`.</span></span> <span data-ttu-id="599dd-105">Due pulsanti, `button1` e `button2`, vengono aggiunti al pannello e i relativi nomi registrati.</span><span class="sxs-lookup"><span data-stu-id="599dd-105">Two buttons, `button1` and `button2`, are added to the panel, and their names registered.</span></span> <span data-ttu-id="599dd-106">Numerose animazioni e <xref:System.Windows.Media.Animation.Storyboard> vengono creati.</span><span class="sxs-lookup"><span data-stu-id="599dd-106">Several animations and a <xref:System.Windows.Media.Animation.Storyboard> are created.</span></span> <span data-ttu-id="599dd-107">Lo storyboard <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> metodo viene utilizzato per avviare le animazioni.</span><span class="sxs-lookup"><span data-stu-id="599dd-107">The storyboard's <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method is used to start the animations.</span></span>  
  
 <span data-ttu-id="599dd-108">Poiché `button1`, `button2`, e `myMainPanel` condividono lo stesso ambito del nome, uno di essi può essere utilizzato con il <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> metodo per avviare le animazioni.</span><span class="sxs-lookup"><span data-stu-id="599dd-108">Because `button1`, `button2`, and `myMainPanel` all share the same name scope, any one of them can be used with the <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method to start the animations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="599dd-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="599dd-109">Example</span></span>  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="599dd-110">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="599dd-110">See Also</span></span>  
 [<span data-ttu-id="599dd-111">Animare una proprietà utilizzando uno storyboard</span><span class="sxs-lookup"><span data-stu-id="599dd-111">Animate a Property by Using a Storyboard</span></span>](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-property-by-using-a-storyboard.md)  
 [<span data-ttu-id="599dd-112">Cenni preliminari sull'animazione</span><span class="sxs-lookup"><span data-stu-id="599dd-112">Animation Overview</span></span>](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
