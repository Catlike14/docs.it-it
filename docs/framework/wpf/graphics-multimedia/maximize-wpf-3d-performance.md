---
title: "Ottimizzazione delle prestazioni tridimensionali di WPF | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-wpf"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "3D (grafica) [WPF]"
ms.assetid: 4bcf949d-d92f-4d8d-8a9b-1e4c61b25bf6
caps.latest.revision: 9
author: "dotnet-bot"
ms.author: "dotnetcontent"
manager: "wpickett"
caps.handback.revision: 9
---
# Ottimizzazione delle prestazioni tridimensionali di WPF
Quando si utilizza [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] per compilare controlli 3D e includere scene 3D nelle applicazioni, è importante tenere in considerazione l'ottimizzazione delle prestazioni. In questo argomento viene fornito un elenco di classi e proprietà 3D che influenzano le prestazioni dell'applicazione, oltre a consigli per l'ottimizzazione delle prestazioni al momento del loro utilizzo.  
  
 In questo argomento si presuppone una conoscenza avanzata delle funzionalità tridimensionali di [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)].  I suggerimenti presenti in questo documento si applicano al livello di rendering 2, generalmente definito hardware, che supporta il pixel shader versione 2.0 e il vertex shader versione 2.0.  Per informazioni dettagliate, vedere [Livelli di rendering della grafica](../../../../docs/framework/wpf/advanced/graphics-rendering-tiers.md).  
  
## Impatto sulle prestazioni: elevato  
  
|||  
|-|-|  
|Proprietà|Consigli|  
|<xref:System.Windows.Media.Brush>|Velocità del pennello \(dalla più veloce alla più lenta\):<br /><br /> <xref:System.Windows.Media.SolidColorBrush><br /><br /> <xref:System.Windows.Media.LinearGradientBrush><br /><br /> <xref:System.Windows.Media.ImageBrush><br /><br /> <xref:System.Windows.Media.DrawingBrush> \(memorizzato nella cache\)<br /><br /> <xref:System.Windows.Media.VisualBrush> \(memorizzato nella cache\)<br /><br /> <xref:System.Windows.Media.RadialGradientBrush><br /><br /> <xref:System.Windows.Media.DrawingBrush> \(non memorizzato nella cache\)<br /><br /> <xref:System.Windows.Media.VisualBrush> \(non memorizzato nella cache\)|  
|<xref:System.Windows.UIElement.ClipToBoundsProperty>|Impostare `Viewport3D.ClipToBounds` su false quando non è necessario ritagliare in modo esplicito in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] il contenuto di un oggetto <xref:System.Windows.Controls.Viewport3D> in base al rettangolo di Viewport3D. Le operazioni nell'area di visualizzazione con antialias di [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] possono risultare molto lente e `ClipToBounds` è abilitato \(lento\) per impostazione predefinita su <xref:System.Windows.Controls.Viewport3D>.|  
|<xref:System.Windows.UIElement.IsHitTestVisible%2A>|Impostare `Viewport3D.IsHitTestVisible` su false quando non è necessario tenere in considerazione in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] l contenuto di un oggetto <xref:System.Windows.Controls.Viewport3D> quando si esegue l'hit test del mouse. L'hit test del contenuto 3D viene eseguito nel software e può risultare lento con mesh di grandi dimensioni. <xref:System.Windows.UIElement.IsHitTestVisible%2A> è abilitata \(lenta\) per impostazione predefinita su <xref:System.Windows.Controls.Viewport3D>.|  
|<xref:System.Windows.Media.Media3D.GeometryModel3D>|Creare modelli diversi solo quando sono necessari materiali o trasformazioni diverse.  In caso contrario, tentare di riunire più istanze di <xref:System.Windows.Media.Media3D.GeometryModel3D> con gli stessi materiali e trasformazioni in alcune istanze più grandi di <xref:System.Windows.Media.Media3D.GeometryModel3D> e <xref:System.Windows.Media.Media3D.MeshGeometry3D>.|  
|<xref:System.Windows.Media.Media3D.MeshGeometry3D>|L'animazione mesh, con la modifica dei singoli vertici di una mesh per singolo fotogramma, non è sempre efficace in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]. Per ridurre al minimo l'impatto sulle prestazioni delle notifiche delle modifiche nel caso di modifica di ogni vertice, disconnettere la mesh dalla struttura ad albero visuale prima di eseguire la modifica per singolo vertice. Dopo aver modificato la mesh, riconnetterla alla struttura ad albero visuale. Tentare inoltre di ridurre al minimo la dimensione delle mesh che verranno animate in questo modo.|  
|Anti\-aliasing 3D|Per aumentare la velocità del rendering, disabilitare il campionamento multiplo su un oggetto <xref:System.Windows.Controls.Viewport3D> impostando la proprietà associata <xref:System.Windows.Media.RenderOptions.EdgeMode%2A> su `Aliased`.  Per impostazione predefinita, l'anti\-aliasing 3D è disabilitato in [!INCLUDE[TLA#tla_winxp](../../../../includes/tlasharptla-winxp-md.md)] e abilitato in [!INCLUDE[TLA#tla_longhorn](../../../../includes/tlasharptla-longhorn-md.md)] con 4 campioni per pixel.|  
|Text|Il testo attivo in una scena 3D \(attivo perché si trova in <xref:System.Windows.Media.DrawingBrush> o <xref:System.Windows.Media.VisualBrush>\) può risultare lento.  In alternativa, provare a utilizzare immagini di testo \(tramite <xref:System.Windows.Media.Imaging.RenderTargetBitmap>\) a meno che non si intenda modificare il testo.|  
|<xref:System.Windows.Media.TileBrush>|Se è necessario utilizzare <xref:System.Windows.Media.VisualBrush> o <xref:System.Windows.Media.DrawingBrush> in una scena 3D poiché il contenuto del pennello non è statico, provare a memorizzare il pennello nella cache, impostando la proprietà associata <xref:System.Windows.Media.RenderOptions.CachingHint%2A> su `Cache`.  Impostare le soglie minima e massima di annullamento della convalida della scala \(con le proprietà associate <xref:System.Windows.Media.RenderOptions.CacheInvalidationThresholdMinimum%2A> e <xref:System.Windows.Media.RenderOptions.CacheInvalidationThresholdMaximum%2A>\) in modo che i pennelli memorizzati nella cache non vengano rigenerati con troppa frequenza, mantenendo così il livello di qualità desiderato.  Per impostazione predefinita, <xref:System.Windows.Media.DrawingBrush> e <xref:System.Windows.Media.VisualBrush> non vengono memorizzati nella cache, di conseguenza ogni volta che è necessario sottoporre nuovamente a rendering un elemento disegnato con il pennello, occorrerà prima eseguire un nuovo rendering dell'intero contenuto del pennello su una superficie intermedia.|  
|<xref:System.Windows.Media.Effects.BitmapEffect>|<xref:System.Windows.Media.Effects.BitmapEffect> impone l'esecuzione del rendering di tutto il contenuto interessato senza accelerazione hardware.  Per prestazioni ottimali, non utilizzare <xref:System.Windows.Media.Effects.BitmapEffect>.|  
  
## Impatto sulle prestazioni: medio  
  
|||  
|-|-|  
|Proprietà|Consigli|  
|<xref:System.Windows.Media.Media3D.MeshGeometry3D>|Quando una mesh viene definita da triangoli adiacenti con vertici condivisi i quali hanno le stesse coordinate di posizione, normale e trama, definire ogni vertice condiviso una sola volta, quindi definire i triangoli in base all'indice con la proprietà <xref:System.Windows.Media.Media3D.MeshGeometry3D.TriangleIndices%2A>.|  
|<xref:System.Windows.Media.ImageBrush>|Provare a ridurre al minimo le dimensioni della trama quando si dispone di controllo esplicito sulla dimensione \(quando si utilizza <xref:System.Windows.Media.Imaging.RenderTargetBitmap> e\/o <xref:System.Windows.Media.ImageBrush>\).  Si noti che le trame dalla risoluzione inferiore possono ridurre la qualità visiva, pertanto è opportuno trovare un compromesso adeguato tra qualità e prestazioni.|  
|Opacità|Quando si esegue il rendering di contenuto tridimensionale semitrasparente \(ad esempio reflection\), utilizzare le proprietà di opacità su pennelli o materiali, tramite la proprietà <xref:System.Windows.Media.Brush.Opacity%2A> o <xref:System.Windows.Media.Media3D.DiffuseMaterial.Color%2A>, anziché creare un oggetto <xref:System.Windows.Controls.Viewport3D> semitrasparente separato impostando `Viewport3D.Opacity` su un valore inferiore a 1.|  
|<xref:System.Windows.Controls.Viewport3D>|Ridurre al minimo il numero di oggetti <xref:System.Windows.Controls.Viewport3D> utilizzati in una scena.  Inserire più modelli 3D nello stesso oggetto Viewport3D, anziché creare istanze di Viewport3D separate per ogni modello.|  
|<xref:System.Windows.Freezable>|In genere, è opportuno riutilizzare <xref:System.Windows.Media.Media3D.MeshGeometry3D>, <xref:System.Windows.Media.Media3D.GeometryModel3D>, pennelli e materiali.  Tutti questi oggetti possono disporre di più elementi padre poiché sono derivati da `Freezable`.|  
|<xref:System.Windows.Freezable>|Chiamare il metodo <xref:System.Windows.Freezable.Freeze%2A> sugli oggetti Freezable quando le proprietà rimangono invariate nell'applicazione.  L'operazione di blocco può ridurre il working set e aumentare la velocità.|  
|<xref:System.Windows.Media.Brush>|Utilizzare <xref:System.Windows.Media.ImageBrush> anziché <xref:System.Windows.Media.VisualBrush> o <xref:System.Windows.Media.DrawingBrush> quando il contenuto del pennello non viene modificato.  Il contenuto 2D può essere convertito in un oggetto <xref:System.Windows.Controls.Image> tramite <xref:System.Windows.Media.Imaging.RenderTargetBitmap> e può quindi essere utilizzato in un oggetto <xref:System.Windows.Media.ImageBrush>.|  
|<xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A>|Non utilizzare <xref:System.Windows.Media.Media3D.GeometryModel3D.BackMaterial%2A> a meno che non sia effettivamente necessario visualizzare le facce posteriori dell'oggetto <xref:System.Windows.Media.Media3D.GeometryModel3D>.|  
|<xref:System.Windows.Media.Media3D.Light>|Velocità della luce \(dalla più veloce alla più lenta\):<br /><br /> <xref:System.Windows.Media.Media3D.AmbientLight><br /><br /> <xref:System.Windows.Media.Media3D.DirectionalLight><br /><br /> <xref:System.Windows.Media.Media3D.PointLight><br /><br /> <xref:System.Windows.Media.Media3D.SpotLight>|  
|<xref:System.Windows.Media.Media3D.MeshGeometry3D>|Provare a mantenere le dimensioni della mesh entro i seguenti limiti:<br /><br /> <xref:System.Windows.Media.Media3D.MeshGeometry3D.Positions%2A>: 20.001 istanze di <xref:System.Windows.Media.Media3D.Point3D><br /><br /> <xref:System.Windows.Media.Media3D.MeshGeometry3D.TriangleIndices%2A>: 60.003 istanze di <xref:System.Int32>|  
|<xref:System.Windows.Media.Media3D.Material>|Velocità del materiale \(dalla più veloce alla più lenta\):<br /><br /> <xref:System.Windows.Media.Media3D.EmissiveMaterial><br /><br /> <xref:System.Windows.Media.Media3D.DiffuseMaterial><br /><br /> <xref:System.Windows.Media.Media3D.SpecularMaterial>|  
|<xref:System.Windows.Media.Brush>|[!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)] 3D non rifiuta esplicitamente i pennelli invisibili \(pennelli per luce nera, pennelli di cancellazione e così via\) in modo coerente. Valutare se è opportuno ometterli dalla scena.|  
|<xref:System.Windows.Media.Media3D.MaterialGroup>|Ogni <xref:System.Windows.Media.Media3D.Material> in un oggetto <xref:System.Windows.Media.Media3D.MaterialGroup> provoca un altro passaggio di rendering, pertanto l'inclusione di numerosi materiali, anche semplici, può aumentare drasticamente le richieste di riempimento alla GPU.  Ridurre al minimo il numero di materiali in <xref:System.Windows.Media.Media3D.MaterialGroup>.|  
  
## Impatto sulle prestazioni: basso  
  
|||  
|-|-|  
|Proprietà|Consigli|  
|<xref:System.Windows.Media.Media3D.Transform3DGroup>|Quando non è necessaria l'animazione o l'associazione dati, anziché utilizzare un gruppo di trasformazione che contiene più trasformazioni, utilizzare un solo oggetto <xref:System.Windows.Media.Media3D.MatrixTransform3D>, impostandolo come prodotto di tutte le trasformazioni che, in caso contrario, esisterebbero in modo indipendente nel gruppo di trasformazione.|  
|<xref:System.Windows.Media.Media3D.Light>|Ridurre al minimo il numero di luci sulla scena.  Un numero eccessivo di luci in una scena impone l'esecuzione del fallback al rendering software in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)]. I limiti sono di circa 110 oggetti <xref:System.Windows.Media.Media3D.DirectionalLight>, 70 oggetti <xref:System.Windows.Media.Media3D.PointLight> o 40 oggetti <xref:System.Windows.Media.Media3D.SpotLight>.|  
|<xref:System.Windows.Media.Media3D.ModelVisual3D>|Separare gli oggetti in movimento da quelli statici inserendoli in istanze separate di <xref:System.Windows.Media.Media3D.ModelVisual3D>.  ModelVisual3D è più pesante di <xref:System.Windows.Media.Media3D.GeometryModel3D>, poiché memorizza nella cache i limiti trasformati.  GeometryModel3D è ottimizzato come modello, mentre ModelVisual3D è ottimizzato come nodo della scena.  Utilizzare ModelVisual3D per inserire le istanze condivise di GeometryModel3D nella scena.|  
|<xref:System.Windows.Media.Media3D.Light>|Ridurre al minimo il numero di modifiche apportate al numero di luci nella scena.  Ogni modifica del conteggio delle luci impone la rigenerazione e la ricompilazione dello shader, a meno che tale configurazione non fosse già presente in precedenza con la conseguente memorizzazione nella cache del relativo shader.|  
|Luce|Le luci nere non sono visibili, ma vengono aggiunte in fase di rendering. Valutare se è opportuno ometterle.|  
|<xref:System.Windows.Media.Media3D.MeshGeometry3D>|Per ridurre al minimo il tempo di creazione di raccolte di grandi dimensioni in [!INCLUDE[TLA#tla_winclient](../../../../includes/tlasharptla-winclient-md.md)], ad esempio <xref:System.Windows.Media.Media3D.MeshGeometry3D.Positions%2A>, <xref:System.Windows.Media.Media3D.MeshGeometry3D.Normals%2A>, <xref:System.Windows.Media.Media3D.MeshGeometry3D.TextureCoordinates%2A> e <xref:System.Windows.Media.Media3D.MeshGeometry3D.TriangleIndices%2A> di MeshGeometry3D, preimpostare le dimensioni delle raccolte prima della compilazione dei valori.  Se possibile, passare ai costruttori delle raccolte strutture di dati precompilate, ad esempio matrici o elenchi.|  
  
## Vedere anche  
 [Cenni preliminari sulla grafica tridimensionale](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)