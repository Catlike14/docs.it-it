### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a><span data-ttu-id="05e28-101">I nomi di eventi ETW non possono essere diversi solo per il suffisso "Start" o "Stop"</span><span class="sxs-lookup"><span data-stu-id="05e28-101">ETW event names cannot differ only by a "Start" or "Stop" suffix</span></span>

|   |   |
|---|---|
|<span data-ttu-id="05e28-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="05e28-102">Details</span></span>|<span data-ttu-id="05e28-103">In .NET Framework 4.6 e 4.6.1 il runtime genera una <xref:System.ArgumentException> quando due nomi di eventi ETW (Event Tracing for Windows) sono diversi solo per il suffisso &quot;Start&quot; o &quot;Stop&quot;, ad esempio quando un evento è denominato <code>LogUser</code> e un altro <code>LogUserStart</code>.</span><span class="sxs-lookup"><span data-stu-id="05e28-103">In the .NET Framework 4.6 and 4.6.1, the runtime throws an <xref:System.ArgumentException> when two Event Tracing for Windows (ETW) event names differ only by a &quot;Start&quot; or &quot;Stop&quot; suffix (as when one event is named <code>LogUser</code> and another is named <code>LogUserStart</code>).</span></span> <span data-ttu-id="05e28-104">In questo caso, il runtime non può creare l'origine dell'evento, quindi non viene generata alcuna registrazione.</span><span class="sxs-lookup"><span data-stu-id="05e28-104">In this case, the runtime cannot construct the event source, which cannot emit any logging.</span></span><ul><li><span data-ttu-id="05e28-105">[X] Anomalo // Usa un meccanismo per attivare o disattivare la funzionalità, in genere usando una destinazione di runtime, AppContext o i file di configurazione.</span><span class="sxs-lookup"><span data-stu-id="05e28-105">[X] Quirked // Uses some mechanism to turn the feature on or off, usually using runtime targeting, AppContext or config files.</span></span> <span data-ttu-id="05e28-106">Deve essere attivato automaticamente per alcune situazioni.</span><span class="sxs-lookup"><span data-stu-id="05e28-106">Needs to be turned on automatically for some situations.</span></span></li><li><span data-ttu-id="05e28-107">[ ] Interruzione in fase di compilazione // Causa un'interruzione se si tenta di rieseguire la compilazione</span><span class="sxs-lookup"><span data-stu-id="05e28-107">[ ] Build-time break // Causes a break if attempted to recompile</span></span></li></ul>|
|<span data-ttu-id="05e28-108">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="05e28-108">Suggestion</span></span>|<span data-ttu-id="05e28-109">Per evitare l'eccezione, assicurarsi che non siano presenti nomi di evento che differiscono solo per il suffisso &quot;Start&quot; oppure &quot;Stop&quot;. Questo requisito è stato rimosso a rimosso a partire da .NET Framework 4.6.2 e il runtime può risolvere l'ambiguità di nomi di evento che differiscono solo per il suffisso &quot;Start&quot; e &quot;Stop&quot;.</span><span class="sxs-lookup"><span data-stu-id="05e28-109">To prevent the exception, ensure that no two event names differ only by a &quot;Start&quot; or &quot;Stop&quot; suffix.This requirement is removed starting with the .NET Framework 4.6.2; the runtime can disambiguate event names that differ only by the &quot;Start&quot; and &quot;Stop&quot; suffix.</span></span>|
|<span data-ttu-id="05e28-110">Ambito</span><span class="sxs-lookup"><span data-stu-id="05e28-110">Scope</span></span>|<span data-ttu-id="05e28-111">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="05e28-111">Edge</span></span>|
|<span data-ttu-id="05e28-112">Versione</span><span class="sxs-lookup"><span data-stu-id="05e28-112">Version</span></span>|<span data-ttu-id="05e28-113">4.6</span><span class="sxs-lookup"><span data-stu-id="05e28-113">4.6</span></span>|
|<span data-ttu-id="05e28-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="05e28-114">Type</span></span>|<span data-ttu-id="05e28-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="05e28-115">Runtime</span></span>|
