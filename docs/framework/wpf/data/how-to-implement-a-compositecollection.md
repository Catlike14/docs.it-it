---
title: 'Procedura: implementare un oggetto CompositeCollection'
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
caps.latest.revision: "10"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.openlocfilehash: d7d9610c6c507ebdebdb5690dcb7aec19599ee80
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/21/2017
---
# <a name="how-to-implement-a-compositecollection"></a>Procedura: implementare un oggetto CompositeCollection
## <a name="example"></a>Esempio  
 Nell'esempio seguente viene illustrato come visualizzare più connessioni ed elementi come un elenco utilizzando il <xref:System.Windows.Data.CompositeCollection> classe. In questo esempio, `GreekGods` è un <xref:System.Collections.ObjectModel.ObservableCollection%601> di `GreekGod` oggetti personalizzati. I modelli di dati sono definiti in modo che `GreekGod` oggetti e `GreekHero` gli oggetti vengono visualizzati rispettivamente con un oro e un colore ciano.  
  
 [!code-xaml[CompositeCollections#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a>Vedere anche  
 <xref:System.Windows.Data.CollectionContainer>  
 <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>  
 <xref:System.Windows.Data.XmlDataProvider>  
 <xref:System.Windows.DataTemplate>  
 [Cenni preliminari sull'associazione dati](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [Procedure relative](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
