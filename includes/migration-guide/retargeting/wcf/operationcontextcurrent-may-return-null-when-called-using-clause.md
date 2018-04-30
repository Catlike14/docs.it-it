### <a name="operationcontextcurrent-may-return-null-when-called-in-a-using-clause"></a><span data-ttu-id="31886-101">OperationContext.Current può restituire Null in caso di chiamata in una clausola using</span><span class="sxs-lookup"><span data-stu-id="31886-101">OperationContext.Current may return null when called in a using clause</span></span>

|   |   |
|---|---|
|<span data-ttu-id="31886-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="31886-102">Details</span></span>|<span data-ttu-id="31886-103"><xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> può restituire <code>null</code> e può essere generata un'eccezione <xref:System.NullReferenceException> se vengono soddisfatte tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="31886-103"><xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> may return <code>null</code> and a <xref:System.NullReferenceException> may result if all of the following conditions are true:</span></span><ul><li><span data-ttu-id="31886-104">Si recupera il valore della proprietà <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> in un metodo che restituisce <xref:System.Threading.Tasks.Task> o <xref:System.Threading.Tasks.Task%601>.</span><span class="sxs-lookup"><span data-stu-id="31886-104">You retrieve the value of the <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> property in a method that returns a <xref:System.Threading.Tasks.Task> or <xref:System.Threading.Tasks.Task%601>.</span></span></li><li><span data-ttu-id="31886-105">Si crea un'istanza dell'oggetto <xref:System.ServiceModel.OperationContextScope> in una clausola <code>using</code>.</span><span class="sxs-lookup"><span data-stu-id="31886-105">You instantiate the <xref:System.ServiceModel.OperationContextScope> object in a <code>using</code> clause.</span></span></li><li><span data-ttu-id="31886-106">Si recupera il valore della proprietà <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> all'interno di <code>using statement</code>.</span><span class="sxs-lookup"><span data-stu-id="31886-106">You retrieve the value of the <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> property within the <code>using statement</code>.</span></span> <span data-ttu-id="31886-107">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="31886-107">For example:</span></span></li></ul><pre><code class="language-csharp">using (new OperationContextScope(OperationContext.Current))&#13;&#10;{&#13;&#10;OperationContext context = OperationContext.Current;      // OperationContext.Current is null.&#13;&#10;// ...&#13;&#10;}&#13;&#10;</code></pre>|
|<span data-ttu-id="31886-108">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="31886-108">Suggestion</span></span>|<span data-ttu-id="31886-109">Per risolvere questo problema, è possibile eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="31886-109">To address this issue, you can do the following:</span></span><ul><li><span data-ttu-id="31886-110">Modificare il codice come indicato di seguito per creare un'istanza di un nuovo oggetto <xref:System.ServiceModel.OperationContext.Current%2A> non <code>null</code>:</span><span class="sxs-lookup"><span data-stu-id="31886-110">Modify your code as follows to instantiate a new non-<code>null</code> <xref:System.ServiceModel.OperationContext.Current%2A> object:</span></span></li></ul><pre><code class="language-csharp">OperationContext ocx = OperationContext.Current;&#13;&#10;using (new OperationContextScope(OperationContext.Current))&#13;&#10;{&#13;&#10;OperationContext.Current = new OperationContext(ocx.Channel);&#13;&#10;// ...&#13;&#10;}&#13;&#10;</code></pre><ul><li><span data-ttu-id="31886-111">Installare l'aggiornamento più recente di .NET Framework 4.6.2 oppure eseguire l'aggiornamento a una versione successiva di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="31886-111">Install the latest update to the .NET Framework 4.6.2, or upgrade to a later version of the .NET Framework.</span></span> <span data-ttu-id="31886-112">Viene così disabilitato il flusso di <xref:System.Threading.ExecutionContext> in <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> e ripristinato il comportamento delle applicazioni WCF in .NET Framework 4.6.1 e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="31886-112">This disables the flow of the <xref:System.Threading.ExecutionContext> in <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType> and restores the behavior of WCF applications in the .NET Framework 4.6.1 and earlier versions.</span></span> <span data-ttu-id="31886-113">Questo comportamento è configurabile ed è equivalente all'aggiunta dell'impostazione dell'app seguente nel file di configurazione:</span><span class="sxs-lookup"><span data-stu-id="31886-113">This behavior is configurable; it is equivalent to adding the following app setting to your configuration file:</span></span></li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre><span data-ttu-id="31886-114">Se questa modifica non è opportuna e l'applicazione dipende dal flusso del contesto di esecuzione tra i contesti operativi, è possibile abilitare il flusso come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="31886-114">If this change is undesirable and your application depends on execution context flowing between operation contexts, you can enable its flow as follows:</span></span><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;false&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="31886-115">Ambito</span><span class="sxs-lookup"><span data-stu-id="31886-115">Scope</span></span>|<span data-ttu-id="31886-116">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="31886-116">Edge</span></span>|
|<span data-ttu-id="31886-117">Versione</span><span class="sxs-lookup"><span data-stu-id="31886-117">Version</span></span>|<span data-ttu-id="31886-118">4.6.2</span><span class="sxs-lookup"><span data-stu-id="31886-118">4.6.2</span></span>|
|<span data-ttu-id="31886-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="31886-119">Type</span></span>|<span data-ttu-id="31886-120">Ridestinazione</span><span class="sxs-lookup"><span data-stu-id="31886-120">Retargeting</span></span>|
|<span data-ttu-id="31886-121">API interessate</span><span class="sxs-lookup"><span data-stu-id="31886-121">Affected APIs</span></span>|<ul><li><xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType></li></ul>|
