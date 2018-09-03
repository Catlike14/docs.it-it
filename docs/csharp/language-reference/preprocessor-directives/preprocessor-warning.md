---
title: '#warning (Riferimenti per C#)'
ms.date: 07/20/2015
f1_keywords:
- '#warning'
helpviewer_keywords:
- '#warning directive [C#]'
ms.assetid: e6fb496d-bb8b-4018-baf6-5b60a0c8902b
ms.openlocfilehash: 59ca63d5089e377627a9116f24f9a0a1681bb4b2
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2018
ms.locfileid: "42932677"
---
# <a name="warning-c-reference"></a>#warning (Riferimenti per C#)
`#warning` consente di generare l'avviso [CS1030](../../misc/cs1030.md) di livello uno del compilatore da una posizione specifica del codice. Ad esempio:  
  
```csharp
#warning Deprecated code in this method.  
```  
  
## <a name="remarks"></a>Note
 La direttiva `#warning` viene generalmente usata nelle direttive condizionali. È possibile anche generare un errore definito dall'utente tramite [#error](../../../csharp/language-reference/preprocessor-directives/preprocessor-error.md).  
  
## <a name="example"></a>Esempio  

```csharp
// preprocessor_warning.cs  
// CS1030 expected  
#define DEBUG  
class MainClass
{  
    static void Main()
    {  
#if DEBUG  
#warning DEBUG is defined  
#endif  
    }  
}  
```  

## <a name="see-also"></a>Vedere anche

- [Riferimenti per C#](../../../csharp/language-reference/index.md)  
- [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
- [Direttive per il preprocessore C#](../../../csharp/language-reference/preprocessor-directives/index.md)
