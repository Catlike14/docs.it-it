---
title: '&#39;Modulo&#39; le istruzioni possono trovarsi solo a livello di file o spazio dei nomi'
ms.date: 07/20/2015
f1_keywords:
- bc30617
- vbc30617
helpviewer_keywords:
- BC30617
ms.assetid: 5e9de8e5-d26b-4fb2-9e28-814413fe9cef
ms.openlocfilehash: 53199c2d7081445dc5490d5c54c98f93ee7522eb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
ms.locfileid: "33593165"
---
# <a name="39module39-statements-can-occur-only-at-file-or-namespace-level"></a>&#39;Modulo&#39; le istruzioni possono trovarsi solo a livello di file o spazio dei nomi
`Module` le istruzioni devono essere visualizzati nella parte superiore del file di origine immediatamente dopo `Option` e `Imports` istruzioni, gli attributi globali e le dichiarazioni dello spazio dei nomi, ma prima di tutte le altre dichiarazioni.  
  
 **ID errore:** BC30617  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Spostare il `Module` all'inizio del file di origine o di dichiarazione dello spazio dei nomi.  
  
## <a name="see-also"></a>Vedere anche  
 [Istruzione Module](../../../visual-basic/language-reference/statements/module-statement.md)
