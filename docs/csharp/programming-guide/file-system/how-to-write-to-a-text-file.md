---
title: 'Procedura: scrivere in un file di testo (Guida per programmatori C#)'
ms.date: 07/20/2015
f1_keywords:
- TextWriter.WriteLine
- StreamWriter.Close
helpviewer_keywords:
- files [C#], text files
- text, writing to files [C#]
ms.assetid: 2e99f184-d88b-4719-a7f1-d9ec482aa809
ms.openlocfilehash: ca08651bfce1a92f65a3e6fec7da3411a22bffb2
ms.sourcegitcommit: 3c1c3ba79895335ff3737934e39372555ca7d6d0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/06/2018
ms.locfileid: "43780075"
---
# <a name="how-to-write-to-a-text-file-c-programming-guide"></a>Procedura: scrivere in un file di testo (Guida per programmatori C#)
In questi esempi vengono mostrati vari modi per scrivere testo in un file. I primi due esempi usano metodi pratici statici nella classe <xref:System.IO.File?displayProperty=nameWithType> per scrivere ogni elemento di qualsiasi oggetto `IEnumerable<string>` e una stringa in un file di testo. Nell'esempio 3 viene illustrato come aggiungere testo a un file quando è necessario elaborare individualmente ogni riga mentre si scrive nel file. Gli esempi da 1 a 3 sovrascrivono tutto il contenuto esistente nel file, ma l'esempio 4 mostra come aggiungere il testo a un file esistente.  
  
 Tutti gli esempi scrivono valori letterali stringa nei file. Per formattare il testo scritto in un file, usare il metodo <xref:System.String.Format%2A> o la funzionalità di [interpolazione di stringhe](../../../csharp/language-reference/tokens/interpolated.md) di C#.  
  
## <a name="example"></a>Esempio  
 [!code-csharp[csFilesandFolders#3](../../../csharp/programming-guide/file-system/codesnippet/CSharp/how-to-write-to-a-text-file_1.cs)]  
  
## <a name="robust-programming"></a>Programmazione efficiente  
 Le seguenti condizioni possono generare un'eccezione:  
  
-   Il file esiste ed è di sola lettura.  
  
-   Il nome del percorso è troppo lungo.  
  
-   Il disco è pieno.  
  
## <a name="see-also"></a>Vedere anche

- [Guida per programmatori C#](../../../csharp/programming-guide/index.md)  
- [File system e Registro di sistema (Guida per programmatori C#)](../../../csharp/programming-guide/file-system/index.md)  
- [Come salvare una raccolta di oggetti personalizzati nella memoria locale](https://code.msdn.microsoft.com/CSWinStoreAppSaveCollection-bed5d6e6)
