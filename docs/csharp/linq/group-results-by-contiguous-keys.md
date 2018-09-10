---
title: Raggruppare i risultati per chiavi contigue (LINQ in C#)
description: Come raggruppare i risultati per chiavi contigue usando LINQ in C#.
ms.date: 08/14/2018
ms.assetid: cbda9c08-151b-4c9e-82f7-c3d7f3dac66b
ms.openlocfilehash: b5753c85bb07be4fc84b78a299eece961969ff9d
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2018
ms.locfileid: "44209342"
---
# <a name="group-results-by-contiguous-keys"></a>Raggruppare i risultati per chiavi contigue

Nell'esempio seguente viene illustrato come raggruppare elementi in blocchi che rappresentano sottosequenze di chiavi contigue. Si supponga di avere ad esempio la sequenza di coppie chiave-valore riportata di seguito:

|Chiave|Valore|
|---------|-----------|
|A|Me|
|A|think|
|A|that|
|B|Linq|
|C|is|
|A|really|
|B|cool|
|B|!|

Verranno creati i gruppi seguenti in questo ordine:

1. We, think, that

2. Linq

3. is

4. really

5. cool, !

La soluzione viene implementata come metodo di estensione thread-safe che restituisce i risultati in modalità di flusso. In altre parole, i gruppi vengono prodotti man mano che ci si sposta lungo la sequenza di origine. A differenza degli operatori `group` o `orderby`, questa soluzione può iniziare a restituire i gruppi al chiamante prima che sia stata letta tutta la sequenza.

La caratteristica thread-safe viene ottenuta effettuando una copia di ogni gruppo o blocco nel corso dell'iterazione della sequenza di origine, come spiegato nei commenti del codice sorgente. Se la sequenza di origine include una sequenza di grandi dimensioni di elementi contigui, Common Language Runtime potrebbe generare un'eccezione <xref:System.OutOfMemoryException>.

## <a name="example"></a>Esempio

L'esempio seguente illustra sia il metodo di estensione che il codice client usato:

[!code-csharp[cscsrefContiguousGroups#1](~/samples/snippets/csharp/concepts/linq/how-to-group-results-by-contiguous-keys_1.cs)]

Per usare il metodo di estensione nel progetto, copiare la classe statica `MyExtensions` in un file di codice sorgente nuovo o esistente e, se richiesto, aggiungere una direttiva `using` per lo spazio dei nomi in cui si trova.

## <a name="see-also"></a>Vedere anche

- [LINQ (Language-Integrated Query)](index.md)
