---
title: Assemblaggio e distribuzione personalizzata delle estensioni My (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- My namespace [Visual Basic], customizing
- My namespace
- My namespace [Visual Basic], extending
ms.assetid: fd89c54b-0290-4c50-95a3-ff17d4487a21
ms.openlocfilehash: 901d0b80a18d2f4d262cc65eb485dcc628bc6a08
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/04/2018
---
# <a name="packaging-and-deploying-custom-my-extensions-visual-basic"></a>Assemblaggio e distribuzione personalizzata delle estensioni My (Visual Basic)
Visual Basic fornisce un modo semplice per la distribuzione personalizzata `My` estensioni spazio dei nomi utilizzando modelli di Visual Studio. Se si sta creando un modello di progetto per il quale il `My` le estensioni sono parte integrante del nuovo tipo di progetto, è possibile includere personalizzato `My` codice di estensione con il progetto quando si esporta il modello. Per ulteriori informazioni sull'esportazione di modelli di progetto, vedere [procedura: creare modelli di progetto](/visualstudio/ide/how-to-create-project-templates).  
  
 Se personalizzato `My` estensione è in un singolo file di codice, è possibile esportare il file come modello di elemento che possono essere aggiunte a qualsiasi tipo di progetto Visual Basic. È quindi possibile personalizzare il modello di elemento per abilitare funzionalità aggiuntive e il comportamento per personalizzato `My` estensione in un progetto di Visual Basic. Tali funzionalità includono:  
  
-   Consentire agli utenti di gestire personalizzato `My` estensione dal **estensioni My** pagina della finestra di progettazione di progetto Visual Basic.  
  
-   Aggiunta automatica personalizzati `My` estensione quando un riferimento a un assembly specificato viene aggiunto a un progetto.  
  
-   Nascondere il `My` modello di elemento di estensione nel **Aggiungi elemento** nella finestra di dialogo in modo che non è incluso nell'elenco di elementi di progetto.  
  
 In questo argomento viene illustrato come creare un pacchetto personalizzato `My` estensione come un modello di elemento nascosto che può essere gestito dal **estensioni My** pagina della finestra di progettazione di progetto Visual Basic. L'oggetto personalizzato `My` estensione può inoltre essere aggiunta automaticamente quando viene aggiunto un riferimento a un assembly specificato a un progetto.  
  
## <a name="create-a-my-namespace-extension"></a>Creare un'estensione dello spazio dei nomi My  
 Il primo passaggio nella creazione di un pacchetto di distribuzione per un oggetto personalizzato `My` estensione consiste nel creare l'estensione come un singolo file di codice. Per informazioni dettagliate e istruzioni su come creare una classe personalizzata `My` estensione, vedere [estendendo il Namespace My in Visual Basic](../../../visual-basic/developing-apps/customizing-extending-my/extending-the-my-namespace.md).  
  
## <a name="export-a-my-namespace-extension-as-an-item-template"></a>Esportare un estensione My dello spazio dei nomi come modello di elemento  
 Dopo aver creato un file di codice che include il `My` estensione spazio dei nomi, è possibile esportare il file di codice come un modello di elemento di Visual Studio. Per istruzioni su come esportare un file di un modello di elemento di Visual Studio, vedere [procedura: creare modelli di elementi](/visualstudio/ide/how-to-create-item-templates).  
  
> [!NOTE]
>  Se il `My` estensione spazio dei nomi ha una dipendenza su un particolare assembly, è possibile personalizzare il modello di elemento per installare automaticamente il `My` estensione spazio dei nomi quando viene aggiunto un riferimento all'assembly. Verrà di conseguenza, si desidera escludere tale riferimento all'assembly quando si esporta il file di codice come un modello di elemento di Visual Studio.  
  
## <a name="customize-the-item-template"></a>Personalizzare il modello di elemento  
 È possibile attivare il modello di elemento deve essere gestito dal **estensioni My** pagina della finestra di progettazione di progetto Visual Basic. È inoltre possibile abilitare il modello di elemento che verrà aggiunta automaticamente quando viene aggiunto un riferimento a un assembly specificato a un progetto. Per abilitare queste personalizzazioni, si verrà aggiungere un nuovo file, chiamato CustomData, per il modello e quindi aggiungere un nuovo elemento al codice XML nel file. vstemplate.  
  
### <a name="add-the-customdata-file"></a>Aggiungere il file CustomData  
 Il file CustomData è un file di testo con un'estensione di file. CustomData (il nome del file può essere impostato su un valore significativo al modello) e che contiene XML. Il codice XML nel file CustomData indica di includere il `My` estensione quando gli utenti utilizzeranno il **estensioni My** pagina della finestra di progettazione di progetto Visual Basic. È possibile aggiungere facoltativamente il <`AssemblyFullName>` attributo XML del file CustomData. Ciò indica a Visual Basic per installare automaticamente personalizzato `My` estensione quando un riferimento a un particolare assembly viene aggiunto al progetto. È possibile usare qualsiasi editor di testo o editor XML per creare il file CustomData e aggiungerlo quindi cartella compressa del modello di elemento (file con estensione zip).  
  
 Ad esempio, il codice XML seguente viene illustrato il contenuto di un file CustomData che aggiungerà l'elemento del modello nella cartella delle estensioni My di un progetto di Visual Basic quando un riferimento all'assembly Microsoft.VisualBasic.PowerPacks.Vs.dll viene aggiunto al progetto.  
  
```xml  
<VBMyExtensionTemplate   
    ID="Microsoft.VisualBasic.Samples.MyExtensions.MyPrinterInfo"   
    Version="1.0.0.0"  
    AssemblyFullName="Microsoft.VisualBasic.PowerPacks.vs"  
/>  
```  
  
 Il file CustomData contiene un <`VBMyExtensionTemplate>` elemento con attributi, come indicato nella tabella seguente.  
  
|Attributo|Descrizione|  
|---|---|  
|`ID`|Obbligatorio. Identificatore univoco per l'estensione. Se l'estensione con questo ID è già stato aggiunto al progetto, l'utente non necessario aggiungerlo di nuovo.|  
|`Version`|Obbligatorio. Numero di versione per il modello di elemento.|  
|`AssemblyFullName`|Facoltativo. Nome dell'assembly. Quando viene aggiunto un riferimento all'assembly al progetto, l'utente viene chiesto di aggiungere il `My` estensione da questo modello di elemento.|  
  
### <a name="add-the-customdatasignature-element-to-the-vstemplate-file"></a>Aggiungere il \<CustomDataSignature > dell'elemento del file. vstemplate  
 Per identificare il modello di elemento di Visual Studio come un `My` estensione spazio dei nomi, è inoltre necessario modificare il file con estensione vstemplate per il modello di elemento. È necessario aggiungere un `<CustomDataSignature>` elemento per il `<TemplateData>` elemento. Il `<CustomDataSignature>` elemento deve contenere il testo `Microsoft.VisualBasic.MyExtension`, come illustrato nell'esempio seguente.  
  
```xml  
<CustomDataSignature>Microsoft.VisualBasic.MyExtension</CustomDataSignature>  
```  
  
 È possibile modificare direttamente i file in una cartella compressa (zip). È necessario copiare il file con estensione vstemplate dalla cartella compressa, modificarlo e quindi sostituire il file con estensione vstemplate nella cartella compressa con la copia aggiornata.  
  
 Nell'esempio seguente viene illustrato il contenuto di un file con estensione vstemplate con il `<CustomDataSignature>` elemento aggiunto.  
  
```xml  
<VSTemplate Version="2.0.0" xmlns="http://schemas.microsoft.com/developer/vstemplate/2005" Type="Item">  
  <TemplateData>  
    <DefaultName>MyCustomExtensionModule.vb</DefaultName>  
    <Name>MyPrinterInfo</Name>  
    <Description>Custom My Extensions Item Template</Description>  
    <ProjectType>VisualBasic</ProjectType>  
    <SortOrder>10</SortOrder>  
    <Icon>__TemplateIcon.ico</Icon>  
    <CustomDataSignature      >Microsoft.VisualBasic.MyExtension</CustomDataSignature>  
  </TemplateData>  
  <TemplateContent>  
    <References />  
    <ProjectItem SubType="Code"   
                 TargetFileName="$fileinputname$.vb"  
                 ReplaceParameters="true"  
     >MyCustomExtensionModule.vb</ProjectItem>  
  </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="install-the-template"></a>Installare il modello  
 Per installare il modello, è possibile copiare la cartella compressa (zip) nella cartella dei modelli di elemento Visual Basic (ad esempio, Documenti\Visual Studio 2008\Templates\Item Templates\Visual Basic). In alternativa, è possibile pubblicare il modello come un file di programma di installazione Visual Studio (vsi).  
  
## <a name="see-also"></a>Vedere anche  
 [Estensione dello spazio dei nomi My in Visual Basic](../../../visual-basic/developing-apps/customizing-extending-my/extending-the-my-namespace.md)  
 [Estensione del modello di applicazione Visual Basic](../../../visual-basic/developing-apps/customizing-extending-my/extending-the-visual-basic-application-model.md)  
 [Personalizzazione degli oggetti disponibili in My](../../../visual-basic/developing-apps/customizing-extending-my/customizing-which-objects-are-available-in-my.md)  
 [Pagina Estensioni My, Progettazione progetti](/visualstudio/ide/reference/my-extensions-page-project-designer-visual-basic)
