---
title: Per quanto riguarda le applicazioni Native Cloud?
description: Modernizzare le applicazioni .NET esistenti con i contenitori di Windows e Cloud di Azure | Per quanto riguarda le applicazioni Native Cloud?
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 04/28/2018
ms.openlocfilehash: 0e880689001ece2b770811cfbe3fea43aa425b32
ms.sourcegitcommit: 88f251b08bf0718ce119f3d7302f514b74895038
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/10/2018
---
# <a name="what-about-cloud-native-applications"></a><span data-ttu-id="97a3c-103">Per quanto riguarda le applicazioni Native Cloud?</span><span class="sxs-lookup"><span data-stu-id="97a3c-103">What about Cloud-Native applications?</span></span>

<span data-ttu-id="97a3c-104">Sebbene [Cloud nativo](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applicazioni non sono l'obiettivo principale di questa Guida, è utile per avere una conoscenza di questo livello di maturità modernizzazione e per distinguerlo dalle applicazioni ottimizzato su Cloud.</span><span class="sxs-lookup"><span data-stu-id="97a3c-104">Although [Cloud-Native](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applications are not the main focus of this guide, it's helpful to have an understanding of this modernization maturity level, and to distinguish it from Cloud-Optimized applications.</span></span>

<span data-ttu-id="97a3c-105">Figura 4-3 posiziona le app Cloud nativo nei livelli di maturità modernizzazione applicazione:</span><span class="sxs-lookup"><span data-stu-id="97a3c-105">Figure 4-3 positions Cloud-Native apps in the application modernization maturity levels:</span></span>

![Posizionamento delle applicazioni Cloud-nativo](./media/image3.png)

> <span data-ttu-id="97a3c-107">**Figura 4-3.**</span><span class="sxs-lookup"><span data-stu-id="97a3c-107">**Figure 4-3.**</span></span> <span data-ttu-id="97a3c-108">Posizionamento delle applicazioni Cloud-nativo</span><span class="sxs-lookup"><span data-stu-id="97a3c-108">Positioning Cloud-Native applications</span></span>

<span data-ttu-id="97a3c-109">Il livello di maturità modernizzazione nativo Cloud richiede in genere nuovi investimenti di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-109">The Cloud-Native modernization maturity level usually requires new development investments.</span></span> <span data-ttu-id="97a3c-110">Spostamento a livello di Cloud nativo in genere è dovuto a esigenze aziendali per modernizzare le applicazioni quanto più possibile migliorare drasticamente scala in applicazioni di grandi dimensioni mediante la creazione di sottosistemi autonomi (microservizi) che possono essere distribuiti e la scala in modo indipendente da altre aree dell'applicazione riducendo i costi nella flessibilità di evoluzione di lungo termine e l'aumento delle parti dell'app tali autonomi che forniscono significativi competere vantaggi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-110">Moving to the Cloud- Native level typically is driven by business need to modernize applications as much as possible to drastically improve scale in large applications by creating autonomous subsystems (microservices) that can be deployed and scale independently from other areas of the application while lowering costs in the long term and increase evolution agility of those autonomous app’s parts that provide significant compete advantages.</span></span> 

<span data-ttu-id="97a3c-111">I concetti di base di [Cloud nativo](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) applicazioni si basano gli approcci di architettura microservizi, che possono evolvere con una maggiore flessibilità e scalabilità entro i limiti che sarebbe difficile da eseguire in un'architettura monolitica distribuita a uno in locale o un ambiente cloud.</span><span class="sxs-lookup"><span data-stu-id="97a3c-111">The main pillars of [Cloud-Native](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) applications are based on microservices architecture approaches, which can evolve with agility and scale to limits that would be difficult to achieve in a monolithic architecture deployed to either on-premises or cloud environment.</span></span>

<span data-ttu-id="97a3c-112">Figura 4-4 mostra le principali caratteristiche del modello di Cloud nativo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-112">Figure 4-4 shows the main characteristics of the Cloud-Native model.</span></span>  

> ![Caratteristiche di cloud nativo sono Microservizi, contenitori, cloud resilienti, orchestrators e serverles](./media/image4.png)
>
> <span data-ttu-id="97a3c-114">**Figura 4-4.**</span><span class="sxs-lookup"><span data-stu-id="97a3c-114">**Figure 4-4.**</span></span> <span data-ttu-id="97a3c-115">Caratteristiche di cloud-nativo</span><span class="sxs-lookup"><span data-stu-id="97a3c-115">Cloud-Native characteristics</span></span>

<span data-ttu-id="97a3c-116">Inoltre, è possibile estendere le app web moderna base e le app cloud nativo mediante l'aggiunta di altri servizi, quali intelligence artificiale (AI), l'apprendimento automatico (ML) e IoT.</span><span class="sxs-lookup"><span data-stu-id="97a3c-116">In addition, you can extend basic modern web apps and cloud-native apps by adding other services, like artificial intelligence (AI), machine learning (ML), and IoT.</span></span> <span data-ttu-id="97a3c-117">È possibile utilizzare uno di questi servizi per estendere uno degli approcci possibili ottimizzato su Cloud.</span><span class="sxs-lookup"><span data-stu-id="97a3c-117">You might use any of these services to extend any of the possible Cloud-Optimized approaches.</span></span>

<span data-ttu-id="97a3c-118">La differenza fondamentale nelle applicazioni a livello di codice nativo Cloud è nell'architettura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97a3c-118">The fundamental difference in applications at the Cloud-Native level is in the application architecture.</span></span> <span data-ttu-id="97a3c-119">[Cloud nativo](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applicazioni sono per definizione, le applicazioni basate su microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-119">[Cloud-native](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) applications are, by definition, apps that are based on microservices.</span></span> <span data-ttu-id="97a3c-120">App cloud nativo richiedono speciali architetture, tecnologie e piattaforme, rispetto a un'applicazione web monolitico o a più livelli tradizionale.</span><span class="sxs-lookup"><span data-stu-id="97a3c-120">Cloud-native apps require special architectures, technologies, and platforms, compared to a monolithic web application or traditional N-Tier application.</span></span>

## <a name="cloud-native-applications-details"></a><span data-ttu-id="97a3c-121">Dettagli di applicazioni cloud-nativo</span><span class="sxs-lookup"><span data-stu-id="97a3c-121">Cloud-native applications details</span></span>

<span data-ttu-id="97a3c-122">[Cloud nativo](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) è uno stato più avanzato o avanzato per le applicazioni di grandi dimensioni e mission-critical.</span><span class="sxs-lookup"><span data-stu-id="97a3c-122">[Cloud-Native](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications) is a more advanced or mature state for large and mission-critical applications.</span></span> <span data-ttu-id="97a3c-123">Le applicazioni cloud nativo richiedono in genere architettura e progettazione vengono creati da zero anziché modernizzazione le applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="97a3c-123">Cloud-Native applications usually require architecture and design that are created from scratch instead of by modernizing existing applications.</span></span> <span data-ttu-id="97a3c-124">La differenza principale tra un'applicazione Cloud nativa e un'app web ottimizzato su Cloud più semplice è le raccomandazioni per usare le architetture di microservizi in un approccio cloud nativo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-124">The key difference between a Cloud-Native application and a simpler Cloud-Optimized web app is the recommendation to use microservices architectures in a cloud-native approach.</span></span> <span data-ttu-id="97a3c-125">Le app ottimizzato su cloud possono essere anche le app web monolitico o a più livelli.</span><span class="sxs-lookup"><span data-stu-id="97a3c-125">Cloud-Optimized apps can also be monolithic web apps or N-Tier apps.</span></span>

<span data-ttu-id="97a3c-126">Il [App dodici Factor](https://12factor.net/) (una raccolta di modelli che sono strettamente correlate agli approcci di microservizi) anche viene considerata un requisito per [cloud nativo](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) architetture di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="97a3c-126">The [Twelve-Factor App](https://12factor.net/) (a collection of patterns that are closely related to microservices approaches) is also considered a requirement for [cloud-native](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) application architectures.</span></span>

<span data-ttu-id="97a3c-127">Il [Foundation elaborazione nativa Cloud (CNCF)](https://www.cncf.io/) è un promotore principale dei principi cloud nativo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-127">The [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/) is a primary promoter of cloud-native principles.</span></span> <span data-ttu-id="97a3c-128">Microsoft è un [appartenente il CNCF](https://azure.microsoft.com/blog/announcing-cncf/).</span><span class="sxs-lookup"><span data-stu-id="97a3c-128">Microsoft is a [member of the CNCF](https://azure.microsoft.com/blog/announcing-cncf/).</span></span>

<span data-ttu-id="97a3c-129">Per una definizione di esempio e per ulteriori informazioni sulle caratteristiche di applicazioni cloud nativo, vedere l'articolo Gartner [come a progettare le applicazioni cloud nativo](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications).</span><span class="sxs-lookup"><span data-stu-id="97a3c-129">For a sample definition and for more information about the characteristics of cloud-native applications, see the Gartner article [How to architect and design cloud-native applications](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications).</span></span> <span data-ttu-id="97a3c-130">Per indicazioni specifiche su come implementare un'applicazione cloud nativo di Microsoft, vedere [microservizi .NET: architettura per applicazioni .NET nei contenitori](https://aka.ms/microservicesebook).</span><span class="sxs-lookup"><span data-stu-id="97a3c-130">For specific guidance from Microsoft about how to implement a cloud-native application, see [.NET microservices: Architecture for containerized .NET applications](https://aka.ms/microservicesebook).</span></span>

<span data-ttu-id="97a3c-131">Il fattore più importante da considerare se si esegue la migrazione di un'applicazione completa per la [cloud nativo](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) modello è che è necessario ridefinizione dell'architettura per un'architettura basata su microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-131">The most important factor to consider if you migrate a full application to the [cloud-native](https://www.gartner.com/doc/3738117/comparing-leading-cloudnative-application-platforms) model is that you must rearchitect to a microservices-based architecture.</span></span> <span data-ttu-id="97a3c-132">Chiaramente, ciò richiede un investimento significativo in fase di sviluppo a causa di grandi dimensioni refactoring processo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-132">This clearly requires a significant investment in development because of the large refactoring process involved.</span></span> <span data-ttu-id="97a3c-133">In genere si sceglie questa opzione per le applicazioni mission-critical che richiedono nuovi livelli di scalabilità e flessibilità a lungo termine.</span><span class="sxs-lookup"><span data-stu-id="97a3c-133">This option usually is chosen for mission-critical applications that need new levels of scalability and long-term agility.</span></span> <span data-ttu-id="97a3c-134">Tuttavia, è possibile avviare lo spostamento verso il cloud nativo mediante l'aggiunta di microservizi per pochi nuovi scenari e infine effettuare il refactoring dell'applicazione completamente in microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-134">But, you could start moving toward cloud-native by adding microservices for just a few new scenarios, and eventually refactor the application fully as microservices.</span></span> <span data-ttu-id="97a3c-135">Questo è un approccio incrementale è l'opzione migliore per alcuni scenari.</span><span class="sxs-lookup"><span data-stu-id="97a3c-135">This is an incremental approach that is the best option for some scenarios.</span></span>

## <a name="what-about-microservices"></a><span data-ttu-id="97a3c-136">Per quanto riguarda microservizi?</span><span class="sxs-lookup"><span data-stu-id="97a3c-136">What about microservices?</span></span> 

<span data-ttu-id="97a3c-137">È importante comprendere microservizi e come funzionano se si siano valutando le applicazioni cloud nativo per l'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="97a3c-137">Understanding microservices and how they work is important when you are considering cloud-native applications for your organization.</span></span>

<span data-ttu-id="97a3c-138">L'architettura di microservizi è un approccio avanzato che è possibile utilizzare per le applicazioni che vengono create da zero o quando è sviluppare le applicazioni esistenti per le applicazioni cloud nativo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-138">The microservices architecture is an advanced approach that you can use for applications that are created from scratch or when you evolve existing applications toward cloud-native applications.</span></span> <span data-ttu-id="97a3c-139">È possibile avviare aggiungendo alcuni microservizi alle applicazioni esistenti per apprendere i paradigmi di microservizi nuovo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-139">You can start by adding a few microservices to existing applications to learn about the new microservices paradigms.</span></span> <span data-ttu-id="97a3c-140">Ma ovviamente, è necessario architetto e codice, in particolare per questo tipo di approccio architetturale.</span><span class="sxs-lookup"><span data-stu-id="97a3c-140">But clearly, you need to architect and code, especially for this type of architectural approach.</span></span>

<span data-ttu-id="97a3c-141">Tuttavia, microservizi non sono obbligatori per tutte le applicazioni moderne o nuovo.</span><span class="sxs-lookup"><span data-stu-id="97a3c-141">However, microservices are not mandatory for any new or modern application.</span></span> <span data-ttu-id="97a3c-142">Microservizi non sono un "punto elenco magic" e non sono il modo migliore per creare ogni applicazione.</span><span class="sxs-lookup"><span data-stu-id="97a3c-142">Microservices are not a "magic bullet," and they aren't the single, best way to create every application.</span></span> <span data-ttu-id="97a3c-143">Come e quando si usano microservizi dipende dal tipo di applicazione che si desidera compilare.</span><span class="sxs-lookup"><span data-stu-id="97a3c-143">How and when you use microservices depends on the type of application that you need to build.</span></span>

<span data-ttu-id="97a3c-144">L'architettura di microservizi è sempre la scelta migliore per le applicazioni cruciali distribuite e grandi dimensioni o complesse basati su più sottosistemi indipendenti sotto forma di servizi autonomi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-144">The microservices architecture is becoming the preferred approach for distributed and large or complex mission-critical applications that are based on multiple, independent subsystems in the form of autonomous services.</span></span> <span data-ttu-id="97a3c-145">In un'architettura basata su microservizi, un'applicazione basata su una raccolta di servizi che possono essere sviluppate in modo indipendente, testati, con controllo delle versioni, distribuiti e ridimensionata.</span><span class="sxs-lookup"><span data-stu-id="97a3c-145">In a microservices-based architecture, an application is built as a collection of services that can be independently developed, tested, versioned, deployed, and scaled.</span></span> <span data-ttu-id="97a3c-146">Può trattarsi di qualsiasi database autonomo, correlati per microservizio.</span><span class="sxs-lookup"><span data-stu-id="97a3c-146">This can include any related, autonomous database per microservice.</span></span>

<span data-ttu-id="97a3c-147">Per informazioni dettagliate in un'architettura di microservizi che è possibile implementare con .NET Core, vedere l'e-book a PDF scaricabile [microservizi .NET: architettura per applicazioni .NET nei contenitori](https://aka.ms/microservicesebook).</span><span class="sxs-lookup"><span data-stu-id="97a3c-147">For a detailed look at a microservices architecture that you can implement by using .NET Core, see the downloadable PDF e-book [.NET microservices: Architecture for containerized .NET applications](https://aka.ms/microservicesebook).</span></span> <span data-ttu-id="97a3c-148">La Guida è disponibile anche [online](../../microservices-architecture/index.md).</span><span class="sxs-lookup"><span data-stu-id="97a3c-148">The guide also is available [online](../../microservices-architecture/index.md).</span></span>

<span data-ttu-id="97a3c-149">Ma anche negli scenari in cui microservizi offrono potente funzionalità indipendenti dalla distribuzione, i limiti del sottosistema sicuro e diversità di tecnologia-generano anche molte nuove sfide.</span><span class="sxs-lookup"><span data-stu-id="97a3c-149">But even in scenarios in which microservices offer powerful capabilities-independent deployment, strong subsystem boundaries, and technology diversity-they also raise many new challenges.</span></span> <span data-ttu-id="97a3c-150">I problemi sono correlati allo sviluppo di applicazioni distribuite, ad esempio i modelli di dati frammentati e indipendente; ottenere resiliente comunicazione tra microservizi; la necessità di coerenza finale; e la complessità operativa.</span><span class="sxs-lookup"><span data-stu-id="97a3c-150">The challenges are related to distributed application development, such as fragmented and independent data models; achieving resilient communication between microservices; the need for eventual consistency; and operational complexity.</span></span> <span data-ttu-id="97a3c-151">Microservizi introducono un livello superiore rispetto alle tradizionali applicazioni monolitiche di complessità.</span><span class="sxs-lookup"><span data-stu-id="97a3c-151">Microservices introduce a higher level of complexity compared to traditional monolithic applications.</span></span>

<span data-ttu-id="97a3c-152">A causa della complessità di un'architettura di microservizi, solo a scenari specifici e a determinati tipi di applicazioni sono adatti per le applicazioni basate su microservizio.</span><span class="sxs-lookup"><span data-stu-id="97a3c-152">Because of the complexity of a microservices architecture, only specific scenarios and certain application types are suitable for microservice-based applications.</span></span> <span data-ttu-id="97a3c-153">Sono incluse le applicazioni di grandi e complesse con più evoluzione sottosistemi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-153">These include large and complex applications that have multiple, evolving subsystems.</span></span> <span data-ttu-id="97a3c-154">In questi casi, è opportuno investire in un'architettura più complessa di software, per una maggiore flessibilità a lungo termine e la manutenzione dell'applicazione più efficiente.</span><span class="sxs-lookup"><span data-stu-id="97a3c-154">In these cases, it's worth investing in a more complex software architecture, for increased long-term agility and more efficient application maintenance.</span></span> <span data-ttu-id="97a3c-155">Ma per scenari meno complessi, potrebbe essere meglio continuare con un approccio monolitico applicazione o si avvicina di più semplice a più livelli.</span><span class="sxs-lookup"><span data-stu-id="97a3c-155">But for less complex scenarios, it might be better to continue with a monolithic application approach or simpler N-Tier approaches.</span></span>

<span data-ttu-id="97a3c-156">Come nota finale, anche a rischio being ricorrenti su questo concetto, non dovrebbero esaminare tramite microservizi nelle applicazioni come "secondo o nulla."</span><span class="sxs-lookup"><span data-stu-id="97a3c-156">As a final note, even at the risk of being repetitive about this concept, you shouldn't look at using microservices in your applications as "all-in or nothing at all."</span></span> <span data-ttu-id="97a3c-157">È possibile estendere e sviluppare applicazioni monolitiche esistente aggiungendo nuovi scenari di piccole dimensioni basati su microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-157">You can extend and evolve existing monolithic applications by adding new, small scenarios based on microservices.</span></span> <span data-ttu-id="97a3c-158">Non è necessario iniziare da zero per iniziare a lavorare con un approccio architetturale microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-158">You don't need to start from scratch to start working with a microservices architecture approach.</span></span> <span data-ttu-id="97a3c-159">In effetti, è consigliabile che evolvono dall'utilizzo di un'applicazione monolitica o a più livelli esistente aggiungendo nuovi scenari.</span><span class="sxs-lookup"><span data-stu-id="97a3c-159">In fact, we recommend that you evolve from using an existing monolithic or N-Tier application by adding new scenarios.</span></span> <span data-ttu-id="97a3c-160">Infine, è possibile suddividere l'applicazione in componenti autonomi o microservizi.</span><span class="sxs-lookup"><span data-stu-id="97a3c-160">Eventually, you can break down the application into autonomous components or microservices.</span></span> <span data-ttu-id="97a3c-161">È possibile avviare l'evoluzione monolitiche applicazioni in una direzione di microservizi dettagliate.</span><span class="sxs-lookup"><span data-stu-id="97a3c-161">You can start evolving your monolithic applications in a microservices direction, step by step.</span></span>

<span data-ttu-id="97a3c-162">In ogni caso, il resto della presenta Guida è incentrata la maggior parte di tutti i su "Nessuna App basate su microservizi" poiché questa guida è destinato principalmente a moderna del App esistenti che hanno in genere architetture monolitiche o a più livelli.</span><span class="sxs-lookup"><span data-stu-id="97a3c-162">In any case, the rest of this present guidance focuses most of all on "no microservices-based apps" because this guidance is mainly targeting the modernization of existing apps that usually have monolithic or N-Tier architectures.</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="97a3c-163">[Precedente](microsoft-technologies-in-cloud-optimized-applications.md)
[Successivo](deploy-existing-net-apps-as-windows-containers.md)</span><span class="sxs-lookup"><span data-stu-id="97a3c-163">[Previous](microsoft-technologies-in-cloud-optimized-applications.md)
[Next](deploy-existing-net-apps-as-windows-containers.md)</span></span>