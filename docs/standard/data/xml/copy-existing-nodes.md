---
title: Copia di nodi esistenti
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 2aa8f65c-cc62-4638-9c46-129dc15be786
caps.latest.revision: 
author: mairaw
ms.author: mairaw
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: c026d9f825375d74d53d5cc46969ff0f713bab1c
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/23/2017
---
# <a name="copy-existing-nodes"></a>Copia di nodi esistenti
Nel DOM (Document Object Model) XML sono disponibili molti metodi e proprietà che è possibile usare per selezionare un nodo, ad esempio **SelectSingleNode**, **ChildNodes[int i]** e **Attributes[int i]**. Una volta selezionato il nodo, è possibile inserirlo nell'albero mediante uno dei metodi di inserimento applicabili a quel determinato tipo di nodo. L'unica restrizione all'inserimento di un nodo nell'albero è che il documento deve conservare un formato corretto dopo l'inserimento del nodo. Quando un nodo esistente viene inserito nell'albero DOM, viene rimosso dalla posizione originale e aggiunto alla posizione di destinazione.  
  
## <a name="see-also"></a>Vedere anche  
 [Modello DOM (Document Object Mode) XML](../../../../docs/standard/data/xml/xml-document-object-model-dom.md)
