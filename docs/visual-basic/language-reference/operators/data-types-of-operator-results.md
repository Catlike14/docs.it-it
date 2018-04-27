---
title: Tipi di dati dei risultati degli operatori (Visual Basic)
ms.date: 07/20/2015
ms.prod: .net
ms.reviewer: ''
ms.suite: ''
ms.technology:
- devlang-visual-basic
ms.topic: article
helpviewer_keywords:
- data types [Visual Basic], operator result data types
- result data types [Visual Basic]
- operator result data types [Visual Basic]
- operators [Visual Basic], data types
- data types [Visual Basic], ranges
- operators [Visual Basic], result data types
ms.assetid: 9d524533-e1a1-4aa8-b1b8-622068173d06
caps.latest.revision: 27
author: dotnet-bot
ms.author: dotnetcontent
ms.openlocfilehash: 508329894758436158970760ba0d13a7780f83db
ms.sourcegitcommit: 86adcc06e35390f13c1e372c36d2e044f1fc31ef
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2018
---
# <a name="data-types-of-operator-results-visual-basic"></a>Tipi di dati dei risultati degli operatori (Visual Basic)
Visual Basic determina il tipo di dati del risultato di un'operazione in base ai tipi di dati degli operandi. In alcuni casi potrebbe trattarsi di un tipo di dati con un intervallo maggiore rispetto a quello degli operandi.  
  
## <a name="data-type-ranges"></a>Intervalli dei tipi di dati  
 Gli intervalli dei tipi di dati rilevanti, in ordine dal più piccolo al più grande, sono i seguenti:  
  
-   [Booleano](../../../visual-basic/language-reference/data-types/boolean-data-type.md) , ovvero due valori possibili  
  
-   [SByte](../../../visual-basic/language-reference/data-types/sbyte-data-type.md), [Byte](../../../visual-basic/language-reference/data-types/byte-data-type.md) : 256 valori integrali possibili  
  
-   [Short](../../../visual-basic/language-reference/data-types/short-data-type.md), [UShort](../../../visual-basic/language-reference/data-types/ushort-data-type.md) : 65.536 (6,5... E + 4) valori integrali possibili  
  
-   [Numero intero](../../../visual-basic/language-reference/data-types/integer-data-type.md), [UInteger](../../../visual-basic/language-reference/data-types/uinteger-data-type.md) : 4.294.967.296 (4,2... E + 9) valori integrali possibili  
  
-   [Long](../../../visual-basic/language-reference/data-types/long-data-type.md), [ULong](../../../visual-basic/language-reference/data-types/ulong-data-type.md) : 18.446.744.073.709.551.615 (1,8... E + 19) valori integrali possibili  
  
-   [Decimale](../../../visual-basic/language-reference/data-types/decimal-data-type.md) -1,5... E + 29 possibili valori integrali intervallo 7,9... E + 28 (valore assoluto)  
  
-   [Singolo](../../../visual-basic/language-reference/data-types/single-data-type.md) : intervallo massimo 3.4... E + 38 (valore assoluto)  
  
-   [Double](../../../visual-basic/language-reference/data-types/double-data-type.md) : intervallo massimo 1.7... E + 308 (valore assoluto)  
  
 Per ulteriori informazioni sui tipi di dati Visual Basic, vedere [tipi di dati](../../../visual-basic/language-reference/data-types/data-type-summary.md).  
  
 Se restituisce un operando [Nothing](../../../visual-basic/language-reference/nothing.md), gli operatori aritmetici di Visual Basic considerano come zero.  
  
## <a name="decimal-arithmetic"></a>Operazioni aritmetiche decimali  
 Si noti che il [decimale](../../../visual-basic/language-reference/data-types/decimal-data-type.md) non è il tipo di dati a virgola mobile né integer.  
  
 Se degli operandi di un `+`, `–`, `*`, `/`, o `Mod` operazione `Decimal` e l'altro non lo è `Single` o `Double`, Visual Basic viene ampliato l'altro operando a `Decimal`. L'operazione viene eseguita in `Decimal`, e il tipo di dati del risultato è `Decimal`.  
  
## <a name="floating-point-arithmetic"></a>Aritmetica a virgola mobile  
 Visual Basic esegue la maggior parte delle operazioni aritmetiche a virgola mobile in [doppie](../../../visual-basic/language-reference/data-types/double-data-type.md), ovvero i dati più efficienti digitare per tali operazioni. Tuttavia, se uno degli operandi è [singolo](../../../visual-basic/language-reference/data-types/single-data-type.md) e l'altro non lo è `Double`, Visual Basic esegue l'operazione in `Single`. Amplia ogni operando in base alle esigenze per il tipo di dati appropriato prima dell'operazione e il risultato con il tipo di dati.  
  
### <a name="-and--operators"></a>/ e ^ operatori  
 Il `/` è definito solo per il [decimale](../../../visual-basic/language-reference/data-types/decimal-data-type.md), [singolo](../../../visual-basic/language-reference/data-types/single-data-type.md), e [doppie](../../../visual-basic/language-reference/data-types/double-data-type.md) tipi di dati. Visual Basic converte ogni operando se necessario, per il tipo di dati appropriato prima dell'operazione e il risultato con il tipo di dati.  
  
 La tabella seguente illustra il risultato di tipi di dati per il `/` operatore. Si noti che questa tabella è simmetrica. per una determinata combinazione di tipi di dati di operando, il tipo di dati del risultato è lo stesso indipendentemente dall'ordine degli operandi.  
  
||||||  
|---|---|---|---|---|  
||`Decimal`|`Single`|`Double`|Qualsiasi tipo integer|  
|`Decimal`|Decimale|Single|Double|Decimale|  
|`Single`|Single|Single|Double|Single|  
|`Double`|Double|Double|Double|Double|  
|Qualsiasi tipo integer|Decimale|Single|Double|Double|  
  
 Il `^` è definito solo per il `Double` tipo di dati. Visual Basic converte, se necessario, per ciascun operando `Double` prima dell'operazione e il risultato di tipo di dati è sempre `Double`.  
  
## <a name="integer-arithmetic"></a>Calcoli di interi  
 Il tipo di dati del risultato di un'operazione di tipo integer dipende dai tipi di dati degli operandi. In generale, Visual Basic utilizza i seguenti criteri per determinare il tipo di dati del risultato:  
  
-   Se entrambi gli operandi dell'operatore binario con lo stesso tipo di dati, il risultato con il tipo di dati. Un'eccezione è `Boolean`, che è obbligato a `Short`.  
  
-   Se fa parte di un operando non firmato con un operando con segno, il risultato è un tipo con segno con almeno un più ampio un intervallo come degli operandi.  
  
-   In caso contrario, il risultato ha in genere il maggiore dei due tipi di dati di operando.  
  
 Notare che il tipo di dati del risultato potrebbe non essere identico a qualsiasi tipo di dati di operando.  
  
> [!NOTE]
>  Il tipo di dati del risultato non è sempre sufficientemente grande da contenere tutti i valori possibili risultante dall'operazione. Un <xref:System.OverflowException> eccezione può verificarsi se il valore è troppo grande per il tipo di dati del risultato.  
  
### <a name="unary--and--operators"></a>Unari + e -operatori  
 Nella tabella seguente viene illustrato il risultato tipi di dati per i due operatori unari, `+` e `–`.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|Unario `+`|Short|SByte|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
|Unario `–`|Short|SByte|Short|Short|Integer|Integer|Long|Long|Decimale|  
  
### <a name="-and--operators"></a><\< e >> operatori  
 Nella tabella seguente viene illustrato il risultato tipi di dati per i due operatori di spostamento di bit, `<<` e `>>`. Visual Basic ogni operatore di spostamento di bit viene considerato come un operatore unario sull'operando sinistro (lo schema di bit da spostare).  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`<<`, `>>`|Short|SByte|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
  
 Se l'operando sinistro è `Decimal`, `Single`, `Double`, oppure `String`, tenta di convertirlo in Visual Basic `Long` prima dell'operazione e il risultato è di tipo di dati `Long`. L'operando di destra (il numero di posizioni di bit da spostare) deve essere `Integer` o un tipo convertibile in `Integer`.  
  
### <a name="binary----and-mod-operators"></a>Binario +, -, * e gli operatori Mod  
 Nella tabella seguente viene illustrato il risultato dei tipi di dati per il file binario `+` e `–` operatori e `*` e `Mod` operatori. Si noti che questa tabella è simmetrica. per una determinata combinazione di tipi di dati di operando, il tipo di dati del risultato è lo stesso indipendentemente dall'ordine degli operandi.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Short|SByte|Short|Short|Integer|Integer|Long|Long|Decimale|  
|`SByte`|SByte|SByte|Short|Short|Integer|Integer|Long|Long|Decimale|  
|`Byte`|Short|Short|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
|`Short`|Short|Short|Short|Short|Integer|Integer|Long|Long|Decimale|  
|`UShort`|Integer|Integer|UShort|Integer|UShort|Integer|UInteger|Long|ULong|  
|`Integer`|Integer|Integer|Integer|Integer|Integer|Integer|Long|Long|Decimale|  
|`UInteger`|Long|Long|UInteger|Long|UInteger|Long|UInteger|Long|ULong|  
|`Long`|Long|Long|Long|Long|Long|Long|Long|Long|Decimale|  
|`ULong`|Decimal|Decimale|ULong|Decimale|ULong|Decimale|ULong|Decimale|ULong|  
  
### <a name="-operator"></a>Operatore \  
 La tabella seguente illustra il risultato di tipi di dati per il `\` operatore. Si noti che questa tabella è simmetrica. per una determinata combinazione di tipi di dati di operando, il tipo di dati del risultato è lo stesso indipendentemente dall'ordine degli operandi.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Short|SByte|Short|Short|Integer|Integer|Long|Long|Long|  
|`SByte`|SByte|SByte|Short|Short|Integer|Integer|Long|Long|Long|  
|`Byte`|Short|Short|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
|`Short`|Short|Short|Short|Short|Integer|Integer|Long|Long|Long|  
|`UShort`|Integer|Integer|UShort|Integer|UShort|Integer|UInteger|Long|ULong|  
|`Integer`|Integer|Integer|Integer|Integer|Integer|Integer|Long|Long|Long|  
|`UInteger`|Long|Long|UInteger|Long|UInteger|Long|UInteger|Long|ULong|  
|`Long`|Long|Long|Long|Long|Long|Long|Long|Long|Long|  
|`ULong`|Long|Long|ULong|Long|ULong|Long|ULong|Long|ULong|  
  
 Se degli operandi del `\` operatore [decimale](../../../visual-basic/language-reference/data-types/decimal-data-type.md), [singolo](../../../visual-basic/language-reference/data-types/single-data-type.md), o [doppie](../../../visual-basic/language-reference/data-types/double-data-type.md), Visual Basic tenta di convertirlo in [prolungata](../../../visual-basic/language-reference/data-types/long-data-type.md)prima dell'operazione e il risultato è di tipo di dati `Long`.  
  
## <a name="relational-and-bitwise-comparisons"></a>Confronti relazionali e bit per bit  
 Il tipo di dati del risultato di un'operazione relazionale (`=`, `<>`, `<`, `>`, `<=`, `>=`) è sempre `Boolean` [tipo di dati Boolean](../../../visual-basic/language-reference/data-types/boolean-data-type.md). Lo stesso vale per le operazioni logiche (`And`, `AndAlso`, `Not`, `Or`, `OrElse`, `Xor`) su `Boolean` operandi.  
  
 Il tipo di dati del risultato di un'operazione con OR logico dipende dai tipi di dati degli operandi. Si noti che `AndAlso` e `OrElse` sono definiti solo per `Boolean`, e Visual Basic converte ogni operando in base alle esigenze per `Boolean` prima di eseguire l'operazione.  
  
### <a name="-----and--operators"></a>=, <>, \<, >, \<= e > = operatori  
 Se entrambi gli operandi sono `Boolean`, Visual Basic considera `True` sia inferiore a `False`. Se un tipo numerico viene confrontato con un `String`, Visual Basic tenta di convertire il `String` a `Double` prima dell'operazione. Oggetto `Char` o `Date` solo con un altro operando dello stesso tipo di dati, è possibile confrontare l'operando. Il tipo di dati del risultato è sempre `Boolean`.  
  
### <a name="bitwise-not-operator"></a>Bit per bit Not (operatore)  
 La tabella seguente illustra il risultato di tipi di dati per il bit per bit `Not` operatore.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Not`|Booleano|SByte|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
  
 Se l'operando viene `Decimal`, `Single`, `Double`, oppure `String`, tenta di convertirlo in Visual Basic `Long` prima dell'operazione e il risultato è di tipo di dati `Long`.  
  
### <a name="bitwise-and-or-and-xor-operators"></a>Bit per bit e, in alternativa e gli operatori Xor  
 La tabella seguente illustra il risultato di tipi di dati per il bit per bit `And`, `Or`, e `Xor` operatori. Si noti che questa tabella è simmetrica. per una determinata combinazione di tipi di dati di operando, il tipo di dati del risultato è lo stesso indipendentemente dall'ordine degli operandi.  
  
|||||||||||  
|---|---|---|---|---|---|---|---|---|---|  
||`Boolean`|`SByte`|`Byte`|`Short`|`UShort`|`Integer`|`UInteger`|`Long`|`ULong`|  
|`Boolean`|Booleano|SByte|Short|Short|Integer|Integer|Long|Long|Long|  
|`SByte`|SByte|SByte|Short|Short|Integer|Integer|Long|Long|Long|  
|`Byte`|Short|Short|Byte|Short|UShort|Integer|UInteger|Long|ULong|  
|`Short`|Short|Short|Short|Short|Integer|Integer|Long|Long|Long|  
|`UShort`|Integer|Integer|UShort|Integer|UShort|Integer|UInteger|Long|ULong|  
|`Integer`|Integer|Integer|Integer|Integer|Integer|Integer|Long|Long|Long|  
|`UInteger`|Long|Long|UInteger|Long|UInteger|Long|UInteger|Long|ULong|  
|`Long`|Long|Long|Long|Long|Long|Long|Long|Long|Long|  
|`ULong`|Long|Long|ULong|Long|ULong|Long|ULong|Long|ULong|  
  
 Se un operando `Decimal`, `Single`, `Double`, oppure `String`, tenta di convertirlo in Visual Basic `Long` prima dell'operazione e i dati del risultato è lo stesso come se fosse già stata operando `Long`.  
  
## <a name="miscellaneous-operators"></a>Operatori vari  
 Il `&` è definito solo per la concatenazione di `String` operandi. Visual Basic converte ogni operando se necessario, per `String` prima dell'operazione e il risultato di tipo di dati è sempre `String`. Per quanto riguarda la `&` operatore, tutte le conversioni in `String` sono considerate di ampliamento, anche se `Option Strict` è `On`.  
  
 Il `Is` e `IsNot` operatori richiedono entrambi gli operandi di un tipo di riferimento. Il `TypeOf`... `Is` espressione richiede il primo operando di un tipo di riferimento e il secondo operando per corrispondere al nome di un tipo di dati. In tutti questi casi, i dati del risultato, il tipo è `Boolean`.  
  
 Il `Like` è definito solo per i criteri di ricerca di `String` operandi. Visual Basic tenta di convertire ogni operando in base alle esigenze per `String` prima dell'operazione. Il tipo di dati del risultato è sempre `Boolean`.  
  
## <a name="see-also"></a>Vedere anche  
 [Tipi di dati](../../../visual-basic/language-reference/data-types/data-type-summary.md)  
 [Operatori ed espressioni](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)  
 [Operatori aritmetici in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/arithmetic-operators.md)  
 [Operatori di confronto in Visual Basic](../../../visual-basic/programming-guide/language-features/operators-and-expressions/comparison-operators.md)  
 [Operatori](../../../visual-basic/language-reference/operators/index.md)  
 [Precedenza tra gli operatori in Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)  
 [Elenco degli operatori per funzionalità](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)  
 [Operatori aritmetici](../../../visual-basic/language-reference/operators/arithmetic-operators.md)  
 [Operatori di confronto](../../../visual-basic/language-reference/operators/comparison-operators.md)  
 [Istruzione Option Strict](../../../visual-basic/language-reference/statements/option-strict-statement.md)
