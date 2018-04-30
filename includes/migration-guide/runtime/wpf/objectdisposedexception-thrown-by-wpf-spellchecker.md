### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a><span data-ttu-id="c4188-101">ObjectDisposedException generata dal controllo ortografico WPF</span><span class="sxs-lookup"><span data-stu-id="c4188-101">ObjectDisposedException thrown by WPF spellchecker</span></span>

|   |   |
|---|---|
|<span data-ttu-id="c4188-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="c4188-102">Details</span></span>|<span data-ttu-id="c4188-103">Può verificarsi l'arresto anomalo di applicazioni WPF con un <xref:System.ObjectDisposedException?displayProperty=name> generato dal controllo ortografico.</span><span class="sxs-lookup"><span data-stu-id="c4188-103">WPF applications occasionally crash during application shutdown with an <xref:System.ObjectDisposedException?displayProperty=name> thrown by the spellchecker.</span></span> <span data-ttu-id="c4188-104">Questo problema è risolto in .NET 4.7 WPF, dove l'eccezione viene gestita in modo normale e pertanto si evitano effetti avversi sulle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c4188-104">This is fixed in .NET 4.7 WPF by handling the exception gracefully, and thus ensuring that applications are no longer adversely affected.</span></span> <span data-ttu-id="c4188-105">Si noti che potranno essere rilevate eccezioni first-chance occasionali nelle applicazioni in esecuzione in un debugger.</span><span class="sxs-lookup"><span data-stu-id="c4188-105">It should be noted that occasional first-chance exceptions would continue to be observed in applications running under a debugger.</span></span>|
|<span data-ttu-id="c4188-106">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="c4188-106">Suggestion</span></span>|<span data-ttu-id="c4188-107">Eseguire l'aggiornamento a .NET 4.7</span><span class="sxs-lookup"><span data-stu-id="c4188-107">Upgrade to .NET 4.7</span></span>|
|<span data-ttu-id="c4188-108">Ambito</span><span class="sxs-lookup"><span data-stu-id="c4188-108">Scope</span></span>|<span data-ttu-id="c4188-109">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c4188-109">Edge</span></span>|
|<span data-ttu-id="c4188-110">Versione</span><span class="sxs-lookup"><span data-stu-id="c4188-110">Version</span></span>|<span data-ttu-id="c4188-111">4.6.1</span><span class="sxs-lookup"><span data-stu-id="c4188-111">4.6.1</span></span>|
|<span data-ttu-id="c4188-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4188-112">Type</span></span>|<span data-ttu-id="c4188-113">Runtime</span><span class="sxs-lookup"><span data-stu-id="c4188-113">Runtime</span></span>|
