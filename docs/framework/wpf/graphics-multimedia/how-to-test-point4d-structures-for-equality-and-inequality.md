---
title: 'Procedura: verificare l''uguaglianza e la disuguaglianza di strutture Point4D'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- inequality [WPF], testing Point4D structures for
- equality [WPF], testing Point4D structures for
- testing [WPF], Point4D structures for equality
- Point4D structures [WPF], testing for inequality
- testing [WPF], Point4D structures for inequality
- Point4D structures [WPF], testing for equality
ms.assetid: e004a67e-db7f-4af8-a31f-e6b2a44ccf34
caps.latest.revision: "8"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: 849082fc1b933c4172c0d22ec3c9c2a1644a32fb
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-test-point4d-structures-for-equality-and-inequality"></a><span data-ttu-id="f6a4b-102">Procedura: verificare l'uguaglianza e la disuguaglianza di strutture Point4D</span><span class="sxs-lookup"><span data-stu-id="f6a4b-102">How to: Test Point4D structures for equality and inequality</span></span>
<span data-ttu-id="f6a4b-103">Questo esempio viene illustrato come testare <xref:System.Windows.Media.Media3D.Point4D> strutture di uguaglianza e disuguaglianza.</span><span class="sxs-lookup"><span data-stu-id="f6a4b-103">This example shows how to test <xref:System.Windows.Media.Media3D.Point4D> structures for equality and inequality.</span></span>  
  
 <span data-ttu-id="f6a4b-104">Il codice seguente viene illustrato come verificare <xref:System.Windows.Media.Media3D.Point4D> l'uguaglianza e disuguaglianza con strutture di <xref:System.Windows.Media.Media3D.Point4D> metodi di uguaglianza.</span><span class="sxs-lookup"><span data-stu-id="f6a4b-104">The following code illustrates how to test <xref:System.Windows.Media.Media3D.Point4D> structures for equality and inequality using the <xref:System.Windows.Media.Media3D.Point4D> equality methods.</span></span>  <span data-ttu-id="f6a4b-105">Il <xref:System.Windows.Media.Media3D.Point4D> strutture vengono testate per verificarne l'uguaglianza con l'overload di uguaglianza (`==`) (operatore), quindi per stabilirne la disuguaglianza utilizzando la disuguaglianza di overload (`!=`) (operatore) e infine un <xref:System.Windows.Media.Media3D.Point3D> struttura e un <xref:System.Windows.Media.Media3D.Point4D> verifica dell'uguaglianza utilizzando il metodo statico <xref:System.Windows.Media.Media3D.Point4D.Equals%2A> metodo.</span><span class="sxs-lookup"><span data-stu-id="f6a4b-105">The <xref:System.Windows.Media.Media3D.Point4D> structures are tested for equality using the overloaded equality (`==`) operator, then for inequality using the overloaded inequality (`!=`) operator, and finally a <xref:System.Windows.Media.Media3D.Point3D> structure and a <xref:System.Windows.Media.Media3D.Point4D> structure are checked for equality using the static <xref:System.Windows.Media.Media3D.Point4D.Equals%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f6a4b-106">Esempio</span><span class="sxs-lookup"><span data-stu-id="f6a4b-106">Example</span></span>  
 [!code-csharp[3DGallery_procedural_snip#Point4DEqualityExample_csharp](../../../../samples/snippets/csharp/VS_Snippets_Wpf/3DGallery_procedural_snip/CSharp/Misc3DOperationsExample.cs#point4dequalityexample_csharp)]  
  
## <a name="see-also"></a><span data-ttu-id="f6a4b-107">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f6a4b-107">See Also</span></span>  
 <xref:System.Windows.Media.Media3D.Point4D.op_Equality%2A>  
 <xref:System.Windows.Media.Media3D.Point4D.op_Inequality%2A>  
 <xref:System.Windows.Media.Media3D.Point4D.Equals%2A>
