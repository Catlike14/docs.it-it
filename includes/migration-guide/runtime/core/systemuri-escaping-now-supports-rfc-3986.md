### <a name="systemuri-escaping-now-supports-rfc-3986"></a><span data-ttu-id="c8dde-101">La funzionalità di escape System.Uri ora supporta RFC 3986</span><span class="sxs-lookup"><span data-stu-id="c8dde-101">System.Uri escaping now supports RFC 3986</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c8dde-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c8dde-102">Details</span></span>|<span data-ttu-id="c8dde-103">La funzionalità di escape URI è stata modificata in .NET 4.5 per supportare la specifica [RFC 3986](http://tools.ietf.org/html/rfc3986).</span><span class="sxs-lookup"><span data-stu-id="c8dde-103">URI escaping has changed in .NET 4.5 to support [RFC 3986](http://tools.ietf.org/html/rfc3986).</span></span> <span data-ttu-id="c8dde-104">Le modifiche specifiche includono:</span><span class="sxs-lookup"><span data-stu-id="c8dde-104">Specific changes include:</span></span><ul><li><span data-ttu-id="c8dde-105">Tramite il metodo <xref:System.Uri.EscapeDataString(System.String)?displayProperty=name> viene effettuato l'escape dei caratteri riservati basati su RFC 3986.</span><span class="sxs-lookup"><span data-stu-id="c8dde-105"><xref:System.Uri.EscapeDataString(System.String)?displayProperty=name> escapes reserved characters based on RFC 3986.</span></span></li><li><span data-ttu-id="c8dde-106">Tramite il metodo <xref:System.Uri.EscapeUriString(System.String)?displayProperty=name> non viene effettuato l'escape dei caratteri riservati.</span><span class="sxs-lookup"><span data-stu-id="c8dde-106"><xref:System.Uri.EscapeUriString(System.String)?displayProperty=name> does not escape reserved characters.</span></span></li><li><span data-ttu-id="c8dde-107"><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> non genera un'eccezione se rileva una sequenza di escape non valida.</span><span class="sxs-lookup"><span data-stu-id="c8dde-107"><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> does not throw an exception if it encounters an invalid escape sequence.</span></span></li><li><span data-ttu-id="c8dde-108">I caratteri di escape non riservati non sono sottoposti a escape.</span><span class="sxs-lookup"><span data-stu-id="c8dde-108">Unreserved escaped characters are un-escaped.</span></span></li></ul>|
|<span data-ttu-id="c8dde-109">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="c8dde-109">Suggestion</span></span>|<ul><li><span data-ttu-id="c8dde-110">Aggiornare le applicazioni in modo che non si basino sul fatto che <xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> generi un'eccezione in presenza di una sequenza di escape non valida.</span><span class="sxs-lookup"><span data-stu-id="c8dde-110">Update applications to not rely on <xref:System.Uri.UnescapeDataString(System.String)?displayProperty=name> to throw in the case of an invalid escape sequence.</span></span> <span data-ttu-id="c8dde-111">Queste sequenze devono ora essere rilevate direttamente.</span><span class="sxs-lookup"><span data-stu-id="c8dde-111">Such sequences must be detected directly now.</span></span></li><li><span data-ttu-id="c8dde-112">Allo stesso modo, prevedere che gli URI e le stringhe di dati con e senza codice di escape possano variare da .NET 4.0 a .NET 4.5 ed evitare confronti diretti tra versioni diverse di .NET.</span><span class="sxs-lookup"><span data-stu-id="c8dde-112">Similarly, expect that Escaped and Unescaped URI and Data strings may vary from .NET 4.0 and .NET 4.5 and should not be compared across .NET versions directly.</span></span> <span data-ttu-id="c8dde-113">Questi elementi devono essere invece analizzati e normalizzati in una singola versione di .NET prima di eseguire eventuali confronti.</span><span class="sxs-lookup"><span data-stu-id="c8dde-113">Instead, they should be parsed and normalized in a single .NET version before any comparisons are made.</span></span></li></ul>|
|<span data-ttu-id="c8dde-114">Ambito</span><span class="sxs-lookup"><span data-stu-id="c8dde-114">Scope</span></span>|<span data-ttu-id="c8dde-115">Secondario</span><span class="sxs-lookup"><span data-stu-id="c8dde-115">Minor</span></span>|
|<span data-ttu-id="c8dde-116">Versione</span><span class="sxs-lookup"><span data-stu-id="c8dde-116">Version</span></span>|<span data-ttu-id="c8dde-117">4.5</span><span class="sxs-lookup"><span data-stu-id="c8dde-117">4.5</span></span>|
|<span data-ttu-id="c8dde-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="c8dde-118">Type</span></span>|<span data-ttu-id="c8dde-119">Runtime</span><span class="sxs-lookup"><span data-stu-id="c8dde-119">Runtime</span></span>|
|<span data-ttu-id="c8dde-120">API interessate</span><span class="sxs-lookup"><span data-stu-id="c8dde-120">Affected APIs</span></span>|<ul><li><xref:System.Uri.EscapeDataString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.EscapeUriString(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.UnescapeDataString(System.String)?displayProperty=nameWithType></li></ul>|
