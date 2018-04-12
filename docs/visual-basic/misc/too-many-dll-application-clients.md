---
title: Troppe applicazioni client DLL
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-visual-basic
ms.topic: article
f1_keywords:
- vbrID47
ms.assetid: 4b87780b-67ad-4c96-9253-db954a751dad
caps.latest.revision: 8
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: d4b9278134e937ac8bf4626237954432d727ac0d
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2017
---
# <a name="too-many-dll-application-clients"></a>Troppe applicazioni client DLL
La libreria di collegamento dinamico (DLL) per [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] supporta solo l'accesso a un numero limitato di applicazioni host. L'applicazione e altre applicazioni che sono host di [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] (alcune delle quali sono accessibili dall'applicazione) stanno tentando di accedere contemporaneamente alla DLL [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)] .  
  
## <a name="to-correct-this-error"></a>Per correggere l'errore  
  
-   Ridurre il numero di applicazioni aperte che accedono a [!INCLUDE[vbprvb](~/includes/vbprvb-md.md)].  
  
## <a name="see-also"></a>Vedere anche  
 [Tipi di errore](../../visual-basic/programming-guide/language-features/error-types.md)
