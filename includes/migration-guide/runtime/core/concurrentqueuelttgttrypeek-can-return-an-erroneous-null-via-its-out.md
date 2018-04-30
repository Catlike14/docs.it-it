### <a name="concurrentqueuelttgttrypeek-can-return-an-erroneous-null-via-its-out-parameter"></a><span data-ttu-id="cc97a-101">ConcurrentQueue&lt;T&gt;.TryPeek può restituire erroneamente un valore Null tramite il parametro di output</span><span class="sxs-lookup"><span data-stu-id="cc97a-101">ConcurrentQueue&lt;T&gt;.TryPeek can return an erroneous null via its out parameter</span></span>

|   |   |
|---|---|
|<span data-ttu-id="cc97a-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="cc97a-102">Details</span></span>|<span data-ttu-id="cc97a-103">In alcuni scenari multithread, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> può restituire true, ma popolare il parametro di output con un valore null, anziché il valore corretto, restituito.</span><span class="sxs-lookup"><span data-stu-id="cc97a-103">In some multi-threaded scenarios, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> can return true, but populate the out parameter with a null value (instead of the correct, peeked value).</span></span>|
|<span data-ttu-id="cc97a-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="cc97a-104">Suggestion</span></span>|<span data-ttu-id="cc97a-105">Questo problema è risolto in .NET Framework 4.5.1.</span><span class="sxs-lookup"><span data-stu-id="cc97a-105">This issue is fixed in the .NET Framework 4.5.1.</span></span> <span data-ttu-id="cc97a-106">L'aggiornamento a questa versione di .NET Framework consentirà di risolvere il problema.</span><span class="sxs-lookup"><span data-stu-id="cc97a-106">Upgrading to that Framework will solve the issue.</span></span>|
|<span data-ttu-id="cc97a-107">Ambito</span><span class="sxs-lookup"><span data-stu-id="cc97a-107">Scope</span></span>|<span data-ttu-id="cc97a-108">Principale</span><span class="sxs-lookup"><span data-stu-id="cc97a-108">Major</span></span>|
|<span data-ttu-id="cc97a-109">Versione</span><span class="sxs-lookup"><span data-stu-id="cc97a-109">Version</span></span>|<span data-ttu-id="cc97a-110">4.5</span><span class="sxs-lookup"><span data-stu-id="cc97a-110">4.5</span></span>|
|<span data-ttu-id="cc97a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc97a-111">Type</span></span>|<span data-ttu-id="cc97a-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="cc97a-112">Runtime</span></span>|
|<span data-ttu-id="cc97a-113">API interessate</span><span class="sxs-lookup"><span data-stu-id="cc97a-113">Affected APIs</span></span>|<ul><li><xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=nameWithType></li></ul>|
