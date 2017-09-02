---
title: Creare un modello personalizzato per dotnet new
description: Informazioni su come creare un modello personalizzato per il comando dotnet new in questa gradevole esercitazione.
keywords: .NET, .NET Core, modello, creazione di modelli, esercitazione, dotnet new
author: guardrex
ms.author: mairaw
ms.date: 08/12/2017
ms.topic: article
ms.prod: .net-core
ms.devlang: dotnet
ms.assetid: 519b910a-6efe-4394-9b81-0546aa3e7462
ms.translationtype: HT
ms.sourcegitcommit: c58ed1b3c09f1e358d0b66f6cf7186821601fd69
ms.openlocfilehash: e31977c511f18737aef673c78a3e295d7c24782f
ms.contentlocale: it-it
ms.lasthandoff: 08/12/2017

---

# <a name="create-a-custom-template-for-dotnet-new"></a>Creare un modello personalizzato per dotnet new

In questa esercitazione verrà illustrato come:

- Creare un modello di base da un progetto esistente o un nuovo progetto app console.
- Comprimere il modello per la distribuzione su nuget.org o da l file di una variabile locale *nupkg*.
- Installare il modello da nuget.org, un file locale *nupkg* o nel file system locale.
- Disinstallare il modello.

Se si preferisce continuare l'esercitazione con un esempio completo, scaricare la [il modello del progetto di esempio](https://github.com/dotnet/dotnet-template-samples/tree/master/16-nuget-package). Il modello di esempio è configurato per la distribuzione di NuGet.

Se si desidera utilizzare l'esempio scaricato con la distribuzione di file system, eseguire le operazioni seguenti:

- Spostare il contenuto della cartella *content* dell'esempio di un livello verso l’alto nella cartella *GarciaSoftware.ConsoleTemplate.CSharp*.
- Eliminare la cartella *content* vuota.
- Eliminare il file *.nuspec*.

## <a name="prerequisites"></a>Prerequisiti

- Installare [.NET Core 2.0 SDK](https://www.microsoft.com/net/core) o versioni successive.
- Leggere l’argomento di riferimento [Modelli personalizzati per dotnet new](../tools/custom-templates.md).

## <a name="create-a-template-from-a-project"></a>Creare un modello da un progetto

Utilizzare un progetto esistente per cui è stata confermata la compilazione e l’esecuzione, o creare un nuovo progetto di app console in una cartella sul disco rigido. In questa esercitazione si presuppone che il nome della cartella del progetto sia *GarciaSoftware.ConsoleTemplate.CSharp* archiviato in *Documents/Templates* nel profilo dell'utente. Il nome del modello di progetto dell'esercitazione è nel formato  *\<nome società>.\< Tipo di modello>. \<Linguaggio di programmazione>*, tuttavia è possibile attribuire al progetto e al modello il nome desiderato.

1. Aggiungere una cartella radice del progetto denominato *.template.config*.
1. All'interno della cartella *.template.config*, creare un file di configurazione del modello *template.json*. Per altre informazioni e la definizione del membro per il file *template.json*, vedere l’argomento [Modelli personalizzati per dotnet new](../tools/custom-templates.md#templatejson) e lo schema [ *template.json* nell'archivio di Schema JSON](http://json.schemastore.org/template).

```json
{
    "$schema": "http://json.schemastore.org/template",
    "author": "Catalina Garcia",
    "classifications": [ "Common", "Console" ],
    "identity": "GarciaSoftware.ConsoleTemplate.CSharp",
    "name": "Garcia Software Console Application",
    "shortName": "garciaconsole"
}
```

Il modello è finito. A questo punto, sono disponibili due opzioni per la distribuzione del modello. Per continuare questa esercitazione, scegliere uno dei due percorsi:

1. [Distribuzione NuGet](#use-nuget-distribution): installare il modello da NuGet o dal file locale *nupkg* utilizzare il modello installato.
2. [Distribuzione file system](#use-file-system-distribution).

## <a name="use-nuget-distribution"></a>Utilizzare distribuuzione NuGet

### <a name="pack-the-template-into-a-nuget-package"></a>Comprimere il modello in un pacchetto NuGet

1. Creare una cartella per il pacchetto NuGet. Per l'esercitazione, viene utilizzato il nome della cartella *GarciaSoftware.ConsoleTemplate.CSharp* e la cartella viene creata all'interno della cartella *Documents/NuGetTemplate* nel profilo dell'utente. Creare una cartella denominata *content* all'interno della cartella del nuovo modello per contenere i file di progetto.
1. Copiare il contenuto della cartella del progetto, insieme al relativo file *.template.config/template.json*nella cartella *content* creata.
1. Accanto alla cartella *content*, aggiungere un file [*nuspec*](/nuget/create-packages/creating-a-package). Il file nuspec un file manifesto XML che descrive il contenuto di un pacchetto e guida il processo di creazione del pacchetto NuGet.
   
   ![Struttura della directory contenente il layout del pacchetto NuGet](./media/create-custom-template/nugetdirectorylayout.png)

1. All'interno di un elemento  **\<packageTypes>** nel file *nuspec*, includere un elemento  **\<packageType>** con un valore dell'attributo `name` di `Template`. La cartella *content* e il file *nuspec* devono trovarsi nella stessa directory. La tabella mostra gli elementi del file *nuspec* minimi necessari per produrre un modello come pacchetto NuGet.

   | Elemento            | Tipo   | Descrizione |
   | ------------------ | ------ | ----------- |
   | **\<authors>**     | string | Elenco con valori delimitati da virgola di autori di pacchetti, corrispondenti ai nomi di profilo in nuget.org. Gli autori, visualizzati nella raccolta NuGet in nuget.org, vengono usati per creare riferimenti incrociati ai pacchetti dello stesso autore. |
   | **\<description>** | string | Descrizione lunga del pacchetto per la visualizzazione dell'interfaccia utente. |
   | **\<id>**          | string | L'identificatore del pacchetto senza distinzione tra maiuscole e minuscole, che deve essere univoco in nuget.org o qualsiasi raccolta in cui risiederà il pacchetto. L'ID non può contenere spazi o caratteri che non sono validi per un URL e in genere seguono le regole dello spazio dei nomi .NET. Vedere [Choosing a unique package identifier and setting the version number](/nuget/create-packages/creating-a-package#choosing-a-unique-package-identifier-and-setting-the-version-number) (Scelta di un identificatore univoco del pacchetto e impostazione del numero di versione) per il materiale sussidiario. |
   | **\<packageType>** | string | Inserire l'elemento all'interno di un elemento  **\<packageTypes >** tra elementi  **\<metadata >**. Impostare l'attributo `name` dell'elemento **\<packageType>** su `Template`. |
   | **\<version>**     | string | La versione del pacchetto, che segue il criterio major.minor.patch. I numeri di versione possono includere un suffisso di versione non definitiva, come descritto in [Versioni non definitive](/nuget/create-packages/prerelease-packages#semantic-versioning). |

   Vedere il [riferimento a .nuspec](/nuget/schema/nuspec) per lo schema completo del file *nuspec*.

   Il *nuspec* file per l'esercitazione è denominata *GarciaSoftware.ConsoleTemplate.CSharp.nuspec* e contiene il contenuto seguente:

   ```xml
   <?xml version="1.0" encoding="utf-8"?>
   <package xmlns="http://schemas.microsoft.com/packaging/2012/06/nuspec.xsd">
     <metadata>
       <id>GarciaSoftware.ConsoleTemplate.CSharp</id>
       <version>1.0.0</version>
       <description>
         Creates the Garcia Software console app.
       </description>
       <authors>Catalina Garcia</authors>
       <packageTypes>
         <packageType name="Template" />
       </packageTypes>
     </metadata>
   </package>
   ```

1. [Creare il pacchetto](/nuget/create-packages/creating-a-package#creating-the-package) usando il comando `nuget pack <PATH_TO_NUSPEC_FILE>`. Il comando seguente presuppone che la cartella che contiene gli asset di NuGet si trovi al percorso *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp/*. Tuttavia quando la cartella è collocata nel sistema, il comando `nuget pack` accetta il percorso del file *nuspec*:

   ```console
   nuget pack C:/Users/<USER>/Documents/NuGetTemplates/GarciaSoftware.ConsoleTemplate.CSharp/GarciaSoftware.ConsoleTemplate.CSharp.nuspec
   ```

### <a name="publishing-the-package-to-nugetorg"></a>Pubblicazione del pacchetto su nuget.org

Per pubblicare un pacchetto NuGet, seguire le istruzioni dell’argomento [Creazione e pubblicazione di un pacchetto](/nuget/quickstart/create-and-publish-a-package#publish-the-package). Tuttavia, si consiglia di non pubblicare il modello dell'esercitazione su NuGet poiché non è mai possibile eliminarlo una volta pubblicato, ma solo rimuoverlo dall'elenco. Dopo aver creato il pacchetto NuGet sotto forma di file *nupkg*, è consigliabile seguire le istruzioni seguenti per installare il modello direttamente dal file locale *nupkg*.

### <a name="install-the-template-from-a-nuget-package"></a>Installare il modello da un pacchetto NuGet

#### <a name="install-the-template-from-the-local-nupkg-file"></a>Installare il modello da un file locale *nupkg*

Per installare il modello dal file *nupkg* che è stato creato, utilizzare il comando `dotnet new` con l’opzione `-i|--install` e specificare il percorso del file *nupkg*:

```console
dotnet new -i C:/Users/<USER>/GarciaSoftware.ConsoleTemplate.CSharp.1.0.0.nupkg
```

#### <a name="install-the-template-from-a-nuget-package-stored-at-nugetorg"></a>Installare il modello da un pacchetto NuGet archiviato in nuget.org

Se si desidera installare un modello da un pacchetto NuGet archiviato su nuget.org, utilizzare il comando `dotnet new` con l’opzione `-i|--install` e specificare il nome del pacchetto NuGet:

```console
dotnet new -i GarciaSoftware.ConsoleTemplate.CSharp
```

> [!NOTE]
> L'esempio ha solo scopo dimostrativo. Non è presente un `GarciaSoftware.ConsoleTemplate.CSharp` pacchetto NuGet su nuget.org, e non è consigliabile di pubblicare e utilizzare modelli di test da NuGet. Se si esegue il comando, non viene installato alcun modello. Tuttavia, è possibile installare un modello che non è stato pubblicato su nuget.org facendo riferimento al file *nupkg* direttamente nel file system locale, come illustrato nella sezione precedente [Installare il modello dal file nupkg locale](#install-the-template-from-the-local-nupkg-file).

Se si desidera un esempio della procedura di installazione di un modello da un pacchetto in nuget.org in tempo reale, è possibile utilizzare il [modello NUnit 3 per dotnet-new](https://www.nuget.org/packages/NUnit3.DotNetNew.Template/). Questo modello configura un progetto per utilizzare il testing unità NUnit. Usare il comando seguente per installarlo:

```console
dotnet new -i NUnit3.DotNetNew.Template
```

Quando si elencano i modelli con `dotnet new -l`, viene visualizzato il *progetto di test NUnit 3* con un nome breve di *nunit* nell'elenco dei modelli. Si è pronti a utilizzare il modello nella sezione successiva.

![Finestra della console che mostra il modello NUnit elencato con altri modelli installati](./media/create-custom-template/nunit1.png)

### <a name="create-a-project-from-the-template"></a>Creare un progetto da un modello

Dopo aver installato il modello da NuGet, utilizzare il modello eseguendo il comando `dotnet new <TEMPLATE>` dalla directory in cui si desidera collocare il motore del modello di output (a meno che non si utilizzi l’opzione `-o|--output` per specificare una directory specifica). Per altre informazioni, vedere [`dotnet new` Opzioni](~/docs/core/tools/dotnet-new.md#options). Specificare il nome breve del modello direttamente nel comando `dotnet new`. Per creare un progetto dal modello NUnit, eseguire il comando seguente:

```console
dotnet new nunit
```

La console mostra che il progetto viene creato e che vengono ripristinati i pacchetti del progetto. Dopo l’esecuzione del comando, il progetto è pronto per l'utilizzo.

![Finestra della console che mostra l'output del comando dotnet new mentre crea il progetto NUnit e ripristina le dipendenze di progetto](./media/create-custom-template/nunit2.png)

### <a name="to-uninstall-a-template-from-a-nuget-package-stored-at-nugetorg"></a>Per disinstallare un modello da un pacchetto NuGet archiviato in nuget.org

```console
dotnet new -u GarciaSoftware.ConsoleTemplate.CSharp
```

> [!NOTE]
> L'esempio ha solo scopo dimostrativo. Non è presente un `GarciaSoftware.ConsoleTemplate.CSharp` pacchetto NuGet in nuget.org o installato con .NET Core SDK. Se si esegue il comando, nessun pacchetto o modello viene disinstallato e si riceve l'eccezione seguente:
> 
> > Impossibile trovare un elemento da disinstallare denominato 'GarciaSoftware.ConsoleTemplate.CSharp'.

Se è stato installato il modello [NUnit 3 per dotnet new](https://www.nuget.org/packages/NUnit3.DotNetNew.Template/) e si desidera disinstallare l'estensione, usare il comando seguente:

```console
dotnet new -u NUnit3.DotNetNew.Template
```

### <a name="uninstall-the-template-from-a-local-nupkg-file"></a>Disnstallare il modello dal file locale nupkg

Quando si desidera disinstallare il modello, non tentare di usare il percorso al file *nupkg*. *Il tentativo di disinstallare un modello usando `dotnet new -u <PATH_TO_NUPKG_FILE>` ha esito negativo.* Fare riferimento al pacchetto in base al relativo `id`:

```console
dotnet new -u GarciaSoftware.ConsoleTemplate.CSharp.1.0.0
```

## <a name="use-file-system-distribution"></a>Utilizzare la distribuzione file system

Per distribuire il modello, collocare la cartella del modello di progetto in una posizione accessibile agli utenti della rete. Utilizzare il comando `dotnet new` con l’opzione `-i|--install` e specificare il percorso alla cartella del modello (la cartella di progetto contenente il progetto e la cartella *.template.config*).

L'esercitazione presuppone che il modello di progetto sia archiviato nella cartella *Documents/Templates* del profilo dell'utente. Da quel percorso, è necessario installare il modello con il comando seguente sostituendo \<USER > con il nome del profilo dell'utente:

```console
dotnet new -i C:/Users/<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp
```

### <a name="create-a-project-from-the-template"></a>Creare un progetto da un modello

Dopo aver installato il modello dal file system, utilizzare il modello eseguendo il comando `dotnet new <TEMPLATE>` dalla directory in cui si desidera collocare il motore del modello di output (a meno che non si utilizzi l’opzione `-o|--output` per specificare una directory specifica). Per altre informazioni, vedere [`dotnet new` Opzioni](~/docs/core/tools/dotnet-new.md#options). Specificare il nome breve del modello direttamente nel comando `dotnet new`.

Da una nuova cartella di progetto creata in *C:/Users/\<USER>/Documents/Projects/MyConsoleApp*, creare un progetto dal modello `garciaconsole`:

```console
dotnet new garciaconsole
```

### <a name="uninstall-the-template"></a>Disinstallare il modello

Se è stato creato il modello nel file system locale in *C:/Users/\<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp*, disinstallarlo con lo switch `-u|--uninstall` e il percorso della cartella di modello:

```console
dotnet new -u C:/Users/<USER>/Documents/Templates/GarciaSoftware.ConsoleTemplate.CSharp
```

## <a name="see-also"></a>Vedere anche

[Wiki del repository GitHub dotnet/templating](https://github.com/dotnet/templating/wiki)  
[Repository GitHub dotnet/dotnet-template-samples](https://github.com/dotnet/dotnet-template-samples)  
[Come creare modelli personalizzati per dotnet new](https://blogs.msdn.microsoft.com/dotnet/2017/04/02/how-to-create-your-own-templates-for-dotnet-new/)  
Lo schema [*template.JSON* nell'archivio di schemi JSON](http://json.schemastore.org/template)  
