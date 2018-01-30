---
title: 'Procedura: creare associazioni semplici'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- simple binding [WPF], creating
- data binding [WPF], creating simple bindings
- binding data [WPF], creating
ms.assetid: 69b80f72-6259-44cb-8294-5bdcebca1e08
caps.latest.revision: 
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: 73ed25406aa398aa35c275b20da1deee48b119ab
ms.sourcegitcommit: f28752eab00d2bd97e971542c0f49ce63cfbc239
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2018
---
# <a name="how-to-create-a-simple-binding"></a>Procedura: creare associazioni semplici
In questo esempio viene illustrato come creare un semplice <xref:System.Windows.Data.Binding>.  
  
## <a name="example"></a>Esempio  
 In questo esempio, è necessario un `Person` oggetto con una proprietà stringa denominata `PersonName`. Il `Person` oggetto viene definito nello spazio dei nomi denominato `SDKSample`.  
  
 Nell'esempio seguente viene creata un'istanza di `Person` dell'oggetto con un `PersonName` valore della proprietà `Joe`. Questa operazione viene eseguita `Resources` sezione e assegnare un `x:Key`.  
  
 [!code-xaml[SimpleBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml)]  
  
 Per associare il `PersonName` è necessario effettuare le seguenti proprietà:  
  
 [!code-xaml[SimpleBinding#BDO1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml#bdo1)]  
  
 Di conseguenza, il <xref:System.Windows.Controls.TextBlock> viene visualizzato con il valore "Joe".  
  
## <a name="see-also"></a>Vedere anche  
 [Panoramica sul data binding](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [Procedure relative alle proprietà](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
