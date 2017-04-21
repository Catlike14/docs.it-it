---
title: "Strutture ad albero in WPF | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-wpf"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "struttura ad albero dell'elemento"
  - "albero logico"
  - "struttura ad albero visuale"
ms.assetid: e83f25e5-d66b-4fc7-92d2-50130c9a6649
caps.latest.revision: 20
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 19
---
# Strutture ad albero in WPF
In molte tecnologie, gli elementi e i componenti sono organizzati in una struttura ad albero in cui gli sviluppatori modificano direttamente la struttura ad albero per influire sul rendering o sul comportamento di un'applicazione.  In [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] vengono utilizzate anche molte metafore della struttura ad albero per definire le relazioni tra gli elementi del programma.  In genere gli sviluppatori di WPF possono creare un'applicazione nel codice o definire parti dell'applicazione in XAML utilizzando come riferimento concettuale la metafora di struttura ad albero di oggetti, ma chiameranno un'API specifica o utilizzeranno un markup specifico a tale scopo anziché un'API di modifica della struttura ad albero di oggetti generica simile a quella utilizzata in DOM XML.  WPF espone due classi di supporto che forniscono una visualizzazione della metafora di struttura ad albero, ovvero <xref:System.Windows.LogicalTreeHelper> e <xref:System.Windows.Media.VisualTreeHelper>.  Nella documentazione di WPF vengono inoltre utilizzati i termini struttura ad albero visuale e struttura ad albero logica, in quanto tali strutture ad albero sono utili per la comprensione di alcune funzionalità principali di WPF.  In questo argomento viene definito ciò che una struttura ad albero visuale e una struttura ad albero logica rappresentano e viene descritta la relazione tra tali strutture ad albero e un concetto di struttura ad albero di oggetti complessivo. Vengono inoltre introdotte le classi <xref:System.Windows.LogicalTreeHelper> e <xref:System.Windows.Media.VisualTreeHelper>.  
  
 [!INCLUDE[autoOutline](../Token/autoOutline_md.md)]  
  
<a name="element_tree"></a>   
## Strutture ad albero in WPF  
 La struttura ad albero più completa in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] è la struttura ad albero di oggetti.  Se si definisce la pagina di un'applicazione in [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] e quindi si carica il file [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)], la struttura ad albero viene creata in base alle relazioni di annidamento degli elementi nel markup.  Se si definisce un'applicazione o una parte dell'applicazione nel codice, la struttura ad albero verrà creata in base alla modalità utilizzata per assegnare valori di proprietà per le proprietà che implementano il modello di contenuto per un oggetto specifico.  In [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] la struttura ad albero di oggetti completa viene concettualizzata e può essere segnalata alla relativa API pubblica in due modi diversi: come struttura ad albero logica e come struttura ad albero visuale.  Le distinzioni tra albero logico e struttura ad albero visuale non sono sempre necessariamente importanti, tuttavia possono talvolta causare problemi ad alcuni sottosistemi [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] e influire sulle scelte fatte nel markup o nel codice.  
  
 Sebbene la struttura ad albero logica o la struttura ad albero visuale non venga sempre modificata direttamente, la corretta comprensione dei concetti correlati all'interazione delle strutture ad albero è utile per comprendere WPF in quanto tecnologia.  Il concetto di WPF come metafora di struttura ad albero di un certo tipo è anche essenziale per la comprensione del funzionamento dell'ereditarietà delle proprietà e del routing degli eventi in [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
> [!NOTE]
>  Poiché la struttura ad albero di oggetti è più un concetto che un'API effettiva, è possibile considerare tale concetto anche un oggetto grafico.  In pratica, in fase di esecuzione sussistono relazioni tra oggetti per cui la metafora di struttura ad albero non è valida.  Ciononostante, in particolare con un'interfaccia utente definita in XAML, la metafora di struttura ad albero è sufficientemente pertinente da far sì che nella maggior parte della documentazione di WPF venga utilizzato il termine struttura ad albero di oggetti per fare riferimento a tale concetto generale.  
  
<a name="logical_tree"></a>   
## Albero logico  
 In [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] è possibile aggiungere contenuto a elementi di interfaccia utente impostando proprietà degli oggetti di supporto per tali elementi.  È possibile, ad esempio, aggiungere elementi a un controllo <xref:System.Windows.Controls.ListBox> modificandone la proprietà <xref:System.Windows.Controls.ItemsControl.Items%2A>.  In questo modo, vengono aggiunti elementi nell'oggetto <xref:System.Windows.Controls.ItemCollection>, che rappresenta il valore della proprietà <xref:System.Windows.Controls.ItemsControl.Items%2A>.  Analogamente, per aggiungere oggetti a un controllo <xref:System.Windows.Controls.DockPanel>, è necessario modificare il valore della relativa proprietà <xref:System.Windows.Controls.Panel.Children%2A>.  In questo caso, vengono aggiunti oggetti a <xref:System.Windows.Controls.UIElementCollection>.  Per un esempio di codice, vedere [Add an Element Dynamically](http://msdn.microsoft.com/it-it/d00f258a-7973-4de7-bc54-a3fc1f638419).  
  
 In [!INCLUDE[TLA#tla_xaml](../../../../includes/tlasharptla-xaml-md.md)], quando si aggiungono voci di elenco in un oggetto <xref:System.Windows.Controls.ListBox> o controlli o altri elementi di interfaccia utente in un oggetto <xref:System.Windows.Controls.DockPanel>, è anche possibile utilizzare le proprietà <xref:System.Windows.Controls.ItemsControl.Items%2A> e <xref:System.Windows.Controls.Panel.Children%2A> in modo esplicito o implicito, come nell'esempio seguente.  
  
 [!code-xml[TreeOvwsSupport#AllCode](../../../../samples/snippets/csharp/VS_Snippets_Wpf/TreeOvwsSupport/CS/page1.xaml#allcode)]  
  
 Se si elabora questo file XAML come XML in un modello DOM \(Document Object Model\) e sono stati inclusi i tag impostati come commenti impliciti \(operazione consentita\), la struttura ad albero DOM XML risultante includerà elementi per `<ListBox.Items>` e gli altri elementi impliciti.  Poiché tuttavia XAML non viene elaborato in questo modo durante la lettura del markup e la scrittura negli oggetti, l'oggetto grafico risultante non includerà letteralmente `ListBox.Items`.  Includerà tuttavia una proprietà <xref:System.Windows.Controls.ListBox> denominata `Items` contenente una classe <xref:System.Windows.Controls.ItemCollection> e tale classe <xref:System.Windows.Controls.ItemCollection> sarà inizializzata ma vuota durante l'elaborazione del markup XAML di <xref:System.Windows.Controls.ListBox>.  Ogni elemento oggetto figlio presente come contenuto per <xref:System.Windows.Controls.ListBox> verrà quindi aggiunto alla classe <xref:System.Windows.Controls.ItemCollection> da chiamate del parser a `ItemCollection.Add`.  Fino a questo punto, in questo esempio di elaborazione del markup XAML in una struttura ad albero di oggetti la struttura ad albero di oggetti creata sembra fondamentalmente essere la struttura ad albero logica.  
  
 La struttura ad albero logica, tuttavia, non è l'intero oggetto grafico presente per l'interfaccia utente dell'applicazione in fase di esecuzione, anche se si considerano gli elementi della sintassi implicita XAML.  Ciò è dovuto principalmente agli elementi visivi e ai modelli.  Si consideri, ad esempio, <xref:System.Windows.Controls.Button>.  La struttura ad albero logica indica l'oggetto <xref:System.Windows.Controls.Button> e anche la relativa stringa `Content`.  Nella struttura ad albero di oggetti di runtime, tuttavia, questo pulsante è molto più complesso.  In particolare, la limitata visualizzazione del pulsante sullo schermo è dovuta all'applicazione di un modello di controllo <xref:System.Windows.Controls.Button> specifico.  Gli elementi visivi derivati da un modello applicato, ad esempio il controllo <xref:System.Windows.Controls.Border> definito dal modello che prevede un bordo grigio scuro intorno al pulsante visivo, non sono specificati nella struttura ad albero logica, neanche se si osserva tale struttura in fase di esecuzione, ad esempio durante la gestione di un evento di input dall'interfaccia utente visibile e la successiva lettura della struttura ad albero logica.  Per trovare gli elementi visivi del modello, è invece necessario esaminare la struttura ad albero visuale.  
  
 Per ulteriori informazioni sul mapping all'oggetto grafico creato da parte della sintassi [!INCLUDE[TLA2#tla_xaml](../../../../includes/tla2sharptla-xaml-md.md)] e sulla sintassi implicita in XAML, vedere [Descrizione dettagliata della sintassi XAML](../../../../docs/framework/wpf/advanced/xaml-syntax-in-detail.md) o [Cenni preliminari su XAML \(WPF\)](../../../../docs/framework/wpf/advanced/xaml-overview-wpf.md).  
  
<a name="tree_property_inheritance_event_routing"></a>   
### Scopo dell'albero logico  
 La struttura ad albero logica consente ai modelli di contenuto di scorrere rapidamente i relativi oggetti figlio e rende i modelli di contenuto estendibili.  La struttura ad albero logica, inoltre, fornisce un framework per determinate notifiche, ad esempio relative al caricamento di tutti gli oggetti nella struttura ad albero logica stessa.  Fondamentalmente la struttura ad albero logica è un'approssimazione di un oggetto grafico di runtime a livello di framework, che esclude elementi visivi, ma è efficace per molte operazioni di esecuzione di query sulla composizione dell'applicazione di runtime.  
  
 I riferimenti a risorse sia statiche che dinamiche, inoltre, vengono risolti cercando verso l'alto nella struttura ad albero logica raccolte <xref:System.Windows.FrameworkElement.Resources%2A> nell'oggetto richiedente iniziale, quindi continuando verso l'alto nella struttura ad albero logica e verificando ogni oggetto <xref:System.Windows.FrameworkElement> \(o <xref:System.Windows.FrameworkContentElement>\) per un altro valore `Resources` che contiene una classe <xref:System.Windows.ResourceDictionary>, possibilmente contenente tale chiave.  L'albero logico viene utilizzato per la ricerca delle risorse, quando sono presenti sia l'albero logico, sia la struttura ad albero visuale.  Per ulteriori informazioni sui dizionari risorse e la ricerca, vedere [Risorse XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
<a name="composition"></a>   
### Composizione della struttura ad albero logica  
 La struttura ad albero logica è definita a [livello di framework WPF](GTMT), a indicare che l'elemento di base WPF più pertinente per le operazioni della struttura ad albero logica è <xref:System.Windows.FrameworkElement> o <xref:System.Windows.FrameworkContentElement>.  Come è possibile osservare se si utilizza effettivamente l'API <xref:System.Windows.LogicalTreeHelper>, tuttavia, la struttura ad albero logica contiene talvolta nodi che non sono <xref:System.Windows.FrameworkElement> o <xref:System.Windows.FrameworkContentElement>.  La struttura ad albero logica, ad esempio, specifica il valore <xref:System.Windows.Controls.TextBlock.Text%2A> di un oggetto <xref:System.Windows.Controls.TextBlock>, che è una stringa.  
  
<a name="override_logical_tree"></a>   
### Override dell'albero logico  
 Gli autori di controlli avanzati possono eseguire l'override della struttura ad albero logica tramite l'override di diverse [!INCLUDE[TLA2#tla_api#plural](../../../../includes/tla2sharptla-apisharpplural-md.md)] che definiscono le modalità di aggiunta o rimozione di oggetti nella struttura ad albero logica utilizzate da un oggetto o un modello di contenuto generale.  Per un esempio relativo all'override dell'albero logico, vedere [Eseguire l'override dell'albero logico](../../../../docs/framework/wpf/advanced/how-to-override-the-logical-tree.md).  
  
<a name="pvi"></a>   
### Ereditarietà del valore della proprietà  
 L'ereditarietà del valore della proprietà opera tramite una struttura ad albero ibrida.  I metadati effettivi che contengono la proprietà <xref:System.Windows.FrameworkPropertyMetadata.Inherits%2A> che consente l'ereditarietà della proprietà sono presenti nella classe <xref:System.Windows.FrameworkPropertyMetadata>a livello di framework WPF[](GTMT).  L'oggetto padre che contiene il valore originale e l'oggetto figlio che eredita tale valore, pertanto, devono entrambi essere <xref:System.Windows.FrameworkElement> o <xref:System.Windows.FrameworkContentElement> e devono entrambi far parte della stessa struttura ad albero logica.  Per le proprietà WPF esistenti che supportano l'ereditarietà delle proprietà, tuttavia, l'ereditarietà dei valori di proprietà può essere mantenuta tramite un nuovo oggetto non incluso nella struttura ad albero logica.  Questa caratteristica è pertinente per lo più se si desidera fare in modo che gli elementi del modello utilizzino valori di proprietà ereditati impostati sull'istanza basata sul modello o a livelli ancora superiori di composizione a livello di pagina e pertanto superiori nella struttura ad albero logica.  Per garantire un funzionamento coerente dell'ereditarietà dei valori di proprietà in un limite di questo tipo, la proprietà che eredita deve essere registrata come proprietà associata. È inoltre consigliabile utilizzare questo modello se si desidera definire una proprietà di dipendenza personalizzata con un comportamento di ereditarietà della proprietà.  La struttura ad albero esatta utilizzata per l'ereditarietà della proprietà non può essere completamente prevista da un metodo di utilità di una classe di supporto, persino in fase di esecuzione.  Per ulteriori informazioni, vedere [Ereditarietà del valore della proprietà](../../../../docs/framework/wpf/advanced/property-value-inheritance.md).  
  
<a name="two_trees"></a>   
## Struttura ad albero visuale  
 In [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)], oltre al concetto di albero logico esiste anche il concetto di [struttura ad albero visuale](GTMT).  Nella struttura ad albero visuale viene descritta la struttura degli oggetti visivi rappresentati dalla classe di base <xref:System.Windows.Media.Visual>.  Quando si scrive un modello per un controllo, si definisce o ridefinisce la struttura ad albero visuale relativa a quel controllo.  La struttura ad albero visuale è di interesse anche per gli sviluppatori che desiderano un controllo di livello inferiore sui disegni per ragioni di prestazioni e ottimizzazione.  Un'esposizione della struttura ad albero visuale come parte della programmazione di applicazioni [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] convenzionale è rappresentata dal fatto che le route degli eventi per un [evento indirizzato](GTMT) percorrono per la maggior parte la struttura ad albero visuale e non la struttura ad albero logica.  Questa sottigliezza del comportamento dell'evento indirizzato potrebbe non essere immediatamente visibile, a meno che l'utente non sia un autore di controlli.  Il routing di eventi nella struttura ad albero visuale consente ai controlli che implementano la composizione a livello visivo di gestire eventi o creare metodi di impostazione degli eventi.  
  
<a name="trees_content"></a>   
## Strutture ad albero, elementi e host di contenuto  
 Gli elementi di contenuto \(classi che derivano da <xref:System.Windows.ContentElement>\) non fanno parte della struttura ad albero visuale, non ereditano da <xref:System.Windows.Media.Visual> e non dispongono di una rappresentazione visiva.  Per essere visualizzato in un'interfaccia utente, un oggetto <xref:System.Windows.ContentElement> deve essere ospitato in un host di contenuto che consista sia in un oggetto <xref:System.Windows.Media.Visual> sia in un partecipante della struttura ad albero logica.  In genere, si tratta di un oggetto <xref:System.Windows.FrameworkElement>.  È possibile partire dal concetto che l'host di contenuto è come un "browser" per il contenuto e sceglie come visualizzare tale contenuto all'interno dell'area dello schermo controllata dall'host.  Quando ospitato, il contenuto può partecipare ad alcuni processi della struttura ad albero che normalmente sono associati alla struttura ad albero visuale.  Generalmente, la classe host <xref:System.Windows.FrameworkElement> include il codice di implementazione che aggiunge tutti gli oggetti <xref:System.Windows.ContentElement> ospitati alla route dell'evento tramite nodi secondari dell'albero logico del contenuto, anche se il contenuto ospitato non fa parte della vera struttura ad albero visuale.  Questa operazione è necessaria affinché <xref:System.Windows.ContentElement> possa originare un evento indirizzato che indirizzi a qualsiasi elemento diverso da sé stesso.  
  
<a name="tree_traversal"></a>   
## Attraversamento della struttura ad albero  
 La classe <xref:System.Windows.LogicalTreeHelper> fornisce i metodi <xref:System.Windows.LogicalTreeHelper.GetChildren%2A>, <xref:System.Windows.LogicalTreeHelper.GetParent%2A> e <xref:System.Windows.LogicalTreeHelper.FindLogicalNode%2A> per l'attraversamento dell'albero logico.  Nella maggior parte dei casi, non è necessario attraversare la struttura ad albero logica dei controlli esistenti, in quanto tali controlli espongono quasi sempre i relativi elementi figlio logici come proprietà di raccolta dedicata che supporta accesso alla raccolta, ad esempio `Add`, un indicizzatore e così via.  L'attraversamento della struttura ad albero è principalmente uno scenario utilizzato dagli autori di controlli che scelgono di non derivare da pattern di controllo previsti per questo scopo, ad esempio <xref:System.Windows.Controls.ItemsControl> o <xref:System.Windows.Controls.Panel> in cui le proprietà della raccolta sono già definite e che intendono fornire il proprio supporto della proprietà della raccolta.  
  
 La struttura ad albero visuale supporta anche una classe di supporto per l'attraversamento della struttura ad albero visuale, <xref:System.Windows.Media.VisualTreeHelper>.  La struttura ad albero visuale non viene esposta in modo appropriato tramite le proprietà specifiche del controllo, pertanto la classe <xref:System.Windows.Media.VisualTreeHelper> rappresenta il modo migliore per attraversare la struttura ad albero visuale, se necessario per lo scenario di programmazione.  Per ulteriori informazioni, vedere [Cenni preliminari sul rendering della grafica WPF](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md).  
  
> [!NOTE]
>  È talvolta necessario esaminare la struttura ad albero visuale di un modello applicato.  Quando si utilizza questa tecnica, è consigliabile procedere con attenzione.  Anche quando si attraversa una struttura ad albero visuale per un controllo in cui viene definito il modello, i consumer del controllo possono sempre modificare il modello impostando la proprietà <xref:System.Windows.Controls.Control.Template%2A> nelle istanze. Anche l'utente finale può influire sul modello applicato modificando il tema di sistema.  
  
<a name="routes"></a>   
## Route per eventi indirizzati come "struttura ad albero"  
 Come indicato in precedenza, la route di qualsiasi evento indirizzato specificato percorre un singolo percorso predeterminato di una struttura ad albero che consiste in una forma ibrida delle rappresentazioni di struttura ad albero visuale e logica.  La route di eventi può percorrere la struttura ad albero verso l'alto o verso il basso, a seconda che si tratti di un evento indirizzato di tunneling o di bubbling.  Il concetto di route dell'evento non prevede una classe di supporto diretto che potrebbe essere utilizzata per "percorrere" la route dell'evento indipendentemente dalla generazione di un evento che effettivamente esegue l'indirizzamento.  È disponibile una classe che rappresenta la route, <xref:System.Windows.EventRoute>, tuttavia i metodi di tale classe sono generalmente riservati all'utilizzo interno.  
  
<a name="resourcesandtrees"></a>   
## Dizionari risorse e strutture ad albero  
 La ricerca nei dizionari risorse di tutte le proprietà `Resources` definite in una pagina attraversa fondamentalmente la struttura ad albero logica.  Gli oggetti non inclusi nella struttura ad albero logica possono fare riferimento a risorse con chiave, ma la sequenza di ricerca delle risorse inizia nel punto in cui l'oggetto è connesso alla struttura ad albero logica.  Poiché in WPF solo i nodi della struttura ad albero logica possono includere una proprietà `Resources` contenente un oggetto <xref:System.Windows.ResourceDictionary>, l'attraversamento della struttura ad albero visuale alla ricerca di risorse con chiave da un oggetto <xref:System.Windows.ResourceDictionary> non offre alcun vantaggio.  
  
 Tuttavia, la ricerca delle risorse può anche essere estesa oltre l'albero logico diretto.  Per il markup dell'applicazione, la ricerca di risorse può quindi proseguire verso dizionari risorse a livello di applicazione e quindi verso il supporto dei temi e i valori di sistema cui viene fatto riferimento come proprietà o chiavi statiche.  Se i riferimenti di risorsa sono dinamici, i temi stessi possono fare riferimento anche ai valori di sistema esterni all'albero logico del tema.  Per ulteriori informazioni sui dizionari risorse e la logica di ricerca, vedere [Risorse XAML](../../../../docs/framework/wpf/advanced/xaml-resources.md).  
  
## Vedere anche  
 [Cenni preliminari sull’input](../../../../docs/framework/wpf/advanced/input-overview.md)   
 [Cenni preliminari sul rendering della grafica WPF](../../../../docs/framework/wpf/graphics-multimedia/wpf-graphics-rendering-overview.md)   
 [Cenni preliminari sugli eventi indirizzati](../../../../docs/framework/wpf/advanced/routed-events-overview.md)   
 [Inizializzazione di elementi oggetto non presenti in una struttura ad albero di oggetti](../../../../docs/framework/wpf/advanced/initialization-for-object-elements-not-in-an-object-tree.md)   
 [Architettura WPF](../../../../docs/framework/wpf/advanced/wpf-architecture.md)