### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a><span data-ttu-id="ea988-101">Generazione di codice non corretto per il passaggio e il confronto di valori UInt16</span><span class="sxs-lookup"><span data-stu-id="ea988-101">Incorrect code generation when passing and comparing UInt16 values</span></span>

|   |   |
|---|---|
|<span data-ttu-id="ea988-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="ea988-102">Details</span></span>|<span data-ttu-id="ea988-103">A causa di modifiche introdotte in .NET Framework 4.7, in alcuni casi il codice generato dal compilatore JIT nelle applicazioni in esecuzione in .NET Framework 4.7 confrontano in modo non corretto due valori <code>T:System.UInt16</code>.</span><span class="sxs-lookup"><span data-stu-id="ea988-103">Because of changes introduced in the .NET Framework 4.7, in some cases the code generated by the JIT compiler in applications running on the .NET Framework 4.7 incorrectly compares two <code>T:System.UInt16</code> values.</span></span> <span data-ttu-id="ea988-104">Per altre informazioni, vedere [Issue #11508: Silent bad codegen when passing and comparing ushort args](https://github.com/dotnet/coreclr/issues/11508) (Problema n. 11508: Generazione automatica di codice non valido quando si passano e confrontano argomenti ushort) su GitHub.com.</span><span class="sxs-lookup"><span data-stu-id="ea988-104">For more information, see [Issue #11508: Silent bad codegen when passing and comparing ushort args](https://github.com/dotnet/coreclr/issues/11508) on GitHub.com.</span></span>|
|<span data-ttu-id="ea988-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="ea988-105">Suggestion</span></span>|<span data-ttu-id="ea988-106">Se si verificano problemi nel confronto di valori senza segno a 16 bit in .NET Framework 4.7, eseguire l'aggiornamento a .NET Framework 4.7.1.</span><span class="sxs-lookup"><span data-stu-id="ea988-106">If you encounter issues in the comparison of 16-bit unsigned values in the .NET Framework 4.7, upgrade to the .NET Framework 4.7.1.</span></span>|
|<span data-ttu-id="ea988-107">Ambito</span><span class="sxs-lookup"><span data-stu-id="ea988-107">Scope</span></span>|<span data-ttu-id="ea988-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ea988-108">Edge</span></span>|
|<span data-ttu-id="ea988-109">Versione</span><span class="sxs-lookup"><span data-stu-id="ea988-109">Version</span></span>|<span data-ttu-id="ea988-110">4.7</span><span class="sxs-lookup"><span data-stu-id="ea988-110">4.7</span></span>|
|<span data-ttu-id="ea988-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea988-111">Type</span></span>|<span data-ttu-id="ea988-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="ea988-112">Runtime</span></span>|
