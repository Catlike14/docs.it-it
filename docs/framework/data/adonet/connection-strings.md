---
title: Stringhe di connessione in ADO.NET
ms.date: 03/30/2017
ms.assetid: 745c5f95-2f02-4674-b378-6d51a7ec2490
ms.openlocfilehash: 1e6e2b6870195c99279639e1f4576a30b7126d4d
ms.sourcegitcommit: 69229651598b427c550223d3c58aba82e47b3f82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/04/2018
ms.locfileid: "48583694"
---
# <a name="connection-strings-in-adonet"></a>Stringhe di connessione in ADO.NET
In .NET Framework 2.0 sono state introdotte nuove funzionalità per l'uso delle stringhe di connessione, tra cui l'introduzione di nuove parole chiave nelle classi di generatori di stringhe di connessione che facilitano la creazione di stringhe di connessione valide in fase di esecuzione.  
  
Una stringa di connessione contiene informazioni di inizializzazione che vengono passate come parametro da un provider di dati a un'origine dati. La sintassi dipende dal provider di dati e la stringa di connessione viene analizzata durante il tentativo di aprire una connessione. Gli errori di sintassi generano un'eccezione in fase di esecuzione, ma altri errori si verificano solo dopo che l'origine dati riceve informazioni sulla connessione. Una volta convalidata, l'origine dati applica le opzioni specificate nella stringa di connessione e apre la connessione.
  
Il formato di una stringa di connessione è un elenco delimitato da punti e virgola composto da coppie di parametri chiave/valore:
  
    keyword1=value; keyword2=value;
  
Le parole chiave non sono tra maiuscole e minuscole. I valori, tuttavia, potrebbero essere tra maiuscole e minuscole, a seconda dell'origine dati. Entrambe le parole chiave e i valori possono contenere [spazi vuoti](https://en.wikipedia.org/wiki/Whitespace_character#Unicode), sebbene iniziali e finali di uno spazio vuoto viene ignorata nelle parole chiave e senza virgolette i valori.

Se il valore contiene il punto e virgola, [caratteri di controllo Unicode](https://en.wikipedia.org/wiki/Unicode_control_characters), iniziale o finale di uno spazio vuoto deve essere racchiuso tra virgolette singole o doppie, ad esempio:

    Keyword=" whitespace  ";
    Keyword='special;character';

Il carattere che lo contiene potrebbe non verificarsi all'interno del valore che racchiude. Pertanto, un valore che contiene virgolette singole può essere racchiusi solo tra virgolette doppie e viceversa:

    Keyword='double"quotation;mark';
    Keyword="single'quotation;mark";

Le virgolette se stessi, nonché il segno di uguale, non richiede l'escape, in modo che le stringhe di connessione seguenti sono valide:

    Keyword=no "escaping" 'required';
    Keyword=a=b=c

Poiché ogni valore viene letto fino alla fine della stringa o il successivo punto e virgola, il valore nell'esempio di quest'ultimo è `a=b=c`, e il punto e virgola finale è facoltativo.

La sintassi di una stringa di connessione valida varia a seconda del provider e, nel corso degli anni, si è evoluta dalle API iniziali quale ODBC. Il provider di dati .NET Framework per SQL Server (SqlClient)  incorpora numerosi elementi della sintassi precedente e, in genere, presenta una sintassi delle stringhe di connessione comuni più flessibile. Esistono spesso sinonimi ugualmente validi per gli elementi della sintassi delle stringhe di connessione, ma alcuni errori di sintassi e di ortografia possono causare problemi. Ad esempio "`Integrated Security=true`" è valido, mentre "`IntegratedSecurity=true`" genera un errore. Inoltre, le stringhe di connessione create in fase di esecuzione da input dell'utente non convalidato possono portare ad attacchi injection alle stringhe, compromettendo la sicurezza nell'origine dati.
  
Per risolvere questi problemi, in ADO.NET 2.0 sono stati introdotti nuovi generatori di stringhe di connessione per ogni provider di dati .NET Framework. Le parole chiave sono esposte come proprietà, consentendo la convalida della sintassi delle stringhe di connessione prima dell'invio all'origine dati.
  
## <a name="in-this-section"></a>In questa sezione  
 [Generatori di stringhe di connessione](../../../../docs/framework/data/adonet/connection-string-builders.md)  
 Viene illustrato come usare le classi `ConnectionStringBuilder` per creare stringhe di connessione valide in fase di esecuzione.
  
 [Stringhe di connessione e file di configurazione](../../../../docs/framework/data/adonet/connection-strings-and-configuration-files.md)  
 Viene illustrato come archiviare e recuperare le stringhe di connessione nei file di configurazione.
  
 [Sintassi di stringhe di connessione](../../../../docs/framework/data/adonet/connection-string-syntax.md)  
 Viene descritto come configurare stringhe di connessione specifiche del provider per `SqlClient`, `OracleClient`, `OleDb` e `Odbc`.
  
 [Protezione delle informazioni di connessione](../../../../docs/framework/data/adonet/protecting-connection-information.md)  
 Vengono illustrate tecniche per proteggere le informazioni usate per la connessione a un'origine dati.
  
## <a name="see-also"></a>Vedere anche  
 [Connessione a un'origine dati](/cpp/data/odbc/connecting-to-a-data-source)  
 [Provider gestiti ADO.NET e Centro per sviluppatori di set di dati](https://go.microsoft.com/fwlink/?LinkId=217917)
