---
title: -deterministic (opzioni del compilatore C#)
ms.date: 04/12/2018
f1_keywords:
- /deterministic
helpviewer_keywords:
- -deterministic compiler option [C#]
- deterministic compiler option [C#]
- /deterministic compiler option [C#]
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9f9aca20a3ff65d061c04a21e31db3fb5eab62ba
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/29/2018
ms.locfileid: "47193447"
---
# <a name="-deterministic"></a>-deterministic

Fa sì che il compilatore generi un assembly il cui output byte per byte è identico in tutte le compilazioni se si usano input identici. 

## <a name="syntax"></a>Sintassi

```
-deterministic
```

## <a name="remarks"></a>Note

Per impostazione predefinita, l'output del compilatore che deriva da un determinato set di input è univoco, poiché il compilatore aggiunge un timestamp e un GUID generato da numeri casuali. L'opzione `-deterministic` si usa per generare un *assembly deterministico* il cui contenuto binario è identico in tutte le compilazioni purché l'input rimanga lo stesso.

Il compilatore considera i seguenti input al fine del determinismo:

- La sequenza dei parametri della riga di comando.
- Il contenuto del file di risposta del file RSP del compilatore.
- La versione precisa del compilatore in uso e i relativi assembly di riferimento.
- Il percorso della directory corrente.
- Il contenuto binario di tutti i file passati in modo esplicito al compilatore direttamente o indirettamente, tra cui:
    - File di origine
    - Assembly a cui viene fatto riferimento
    - Moduli a cui viene fatto riferimento
    - Risorse
    - Il file di chiave con nome sicuro
    - @ file di risposta
    - Analizzatori
    - Set di regole
    - File aggiuntivi che possono essere usati dagli analizzatori
- Le impostazioni cultura correnti (per la lingua in cui vengono generati la diagnostica e i messaggi di eccezione).
- La codifica predefinita (o la tabella codici corrente) se non è specificata la codifica.
- L'esistenza, non esistenza e contenuto dei file nei percorsi di ricerca del compilatore (specificati, ad esempio, da `/lib` o `/recurse`).
- La piattaforma CLR in cui viene eseguito il compilatore.
- Il valore di `%LIBPATH%`, che può influenzare il caricamento delle dipendenze dell'analizzatore.

Quando le origini sono disponibili pubblicamente, la compilazione deterministica può essere usata per stabilire se un file binario viene compilato da un'origine attendibile. Può anche essere utile in un sistema di compilazione continua per determinare se è necessario eseguire le istruzioni di compilazione che dipendono dalle modifiche apportate a un file binario. 

## <a name="see-also"></a>Vedere anche  

- [Opzioni del compilatore C#](../../../csharp/language-reference/compiler-options/index.md)  
- [Gestione delle proprietà di progetti e soluzioni](/visualstudio/ide/managing-project-and-solution-properties)
