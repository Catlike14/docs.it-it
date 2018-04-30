### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a><span data-ttu-id="93d78-101">Associazione WCF con la modalità di sicurezza TransportWithMessageCredential</span><span class="sxs-lookup"><span data-stu-id="93d78-101">WCF binding with the TransportWithMessageCredential security mode</span></span>

|   |   |
|---|---|
|<span data-ttu-id="93d78-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="93d78-102">Details</span></span>|<span data-ttu-id="93d78-103">A partire da .NET Framework 4.6.1 l'associazione WCF che usa la modalità di sicurezza TransportWithMessageCredential può essere impostata in modo da ricevere i messaggi con intestazioni &quot;a&quot; non firmate per le chiavi di sicurezza asimmetriche. Per impostazione predefinita, le intestazioni &quot;a&quot; non firmate continueranno a essere rifiutate in .NET 4.6.1.</span><span class="sxs-lookup"><span data-stu-id="93d78-103">Beginning in the .NET Framework 4.6.1, WCF binding that uses the TransportWithMessageCredential security mode can be set up to receive messages with unsigned &quot;to&quot; headers for asymmetric security keys.By default, unsigned &quot;to&quot; headers will continue to be rejected in .NET 4.6.1.</span></span> <span data-ttu-id="93d78-104">Verranno accettate solo se un'applicazione accetta in modo esplicito questa nuova modalità di funzionamento usando l'opzione di configurazione Switch.System.ServiceModel.AllowUnsignedToHeader. Poiché si tratta di una funzionalità che richiede il consenso, non dovrebbe influire sul comportamento delle app esistenti.</span><span class="sxs-lookup"><span data-stu-id="93d78-104">They will only be accepted if an application opts into this new mode of operation using the Switch.System.ServiceModel.AllowUnsignedToHeader configuration switch.Because this is an opt-in feature, it should not affect the behavior of existing apps.</span></span>|
|<span data-ttu-id="93d78-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="93d78-105">Suggestion</span></span>|<span data-ttu-id="93d78-106">Poiché è una funzionalità che prevede il consenso esplicito, non dovrebbe influire sul comportamento delle app esistenti.</span><span class="sxs-lookup"><span data-stu-id="93d78-106">Because this is an opt-in feature, it should not affect the behavior of existing apps.</span></span> <span data-ttu-id="93d78-107">Per stabilire se il nuovo comportamento deve essere usato o meno, usare l'impostazione di configurazione seguente:</span><span class="sxs-lookup"><span data-stu-id="93d78-107">To control whether the new behavior is used or not, use the following configuration setting:</span></span><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|<span data-ttu-id="93d78-108">Ambito</span><span class="sxs-lookup"><span data-stu-id="93d78-108">Scope</span></span>|<span data-ttu-id="93d78-109">Trasparente</span><span class="sxs-lookup"><span data-stu-id="93d78-109">Transparent</span></span>|
|<span data-ttu-id="93d78-110">Versione</span><span class="sxs-lookup"><span data-stu-id="93d78-110">Version</span></span>|<span data-ttu-id="93d78-111">4.6.1</span><span class="sxs-lookup"><span data-stu-id="93d78-111">4.6.1</span></span>|
|<span data-ttu-id="93d78-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="93d78-112">Type</span></span>|<span data-ttu-id="93d78-113">Ridestinazione</span><span class="sxs-lookup"><span data-stu-id="93d78-113">Retargeting</span></span>|
|<span data-ttu-id="93d78-114">API interessate</span><span class="sxs-lookup"><span data-stu-id="93d78-114">Affected APIs</span></span>|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|
