### <a name="a-concurrentdictionary-serialized-in-net-framework-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-framework-451-or-452"></a><span data-ttu-id="9f602-101">Un oggetto ConcurrentDictionary serializzato in .NET Framework 4.5 con NetDataContractSerializer non può essere deserializzato da .NET Framework 4.5.1 o 4.5.2</span><span class="sxs-lookup"><span data-stu-id="9f602-101">A ConcurrentDictionary serialized in .NET Framework 4.5 with NetDataContractSerializer cannot be deserialized by .NET Framework 4.5.1 or 4.5.2</span></span>

|   |   |
|---|---|
|<span data-ttu-id="9f602-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="9f602-102">Details</span></span>|<span data-ttu-id="9f602-103">A causa di modifiche interne al tipo, non è possibile deserializzare in .NET Framework 4.5.1 o in .NET Framework 4.5.2 gli oggetti <xref:System.Collections.Concurrent.ConcurrentDictionary%602> serializzati con .NET Framework 4.5 usando <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. L'operazione nella direzione opposta, ovvero la serializzazione con .NET Framework 4.5.x e la deserializzazione con .NET Framework 4.5, invece funziona.</span><span class="sxs-lookup"><span data-stu-id="9f602-103">Due to internal changes to the type, <xref:System.Collections.Concurrent.ConcurrentDictionary%602> objects that are serialized with the .NET Framework 4.5 using the <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> cannot be deserialized in the .NET Framework 4.5.1 or in the .NET Framework 4.5.2.Note that moving in the other direction (serializing with the .NET Framework 4.5.x and deserializing with the .NET Framework 4.5) works.</span></span> <span data-ttu-id="9f602-104">In modo analogo, tutte le operazioni di serializzazione tra le diverse versioni 4.x funziona con .NET Framework 4.6. La serializzazione e la deserializzazione con una singola versione di .NET Framework non è interessata.</span><span class="sxs-lookup"><span data-stu-id="9f602-104">Similarly, all 4.x cross-version serialization works with the .NET Framework 4.6.Serializing and deserializing with a single version of the .NET Framework is not affected.</span></span>|
|<span data-ttu-id="9f602-105">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="9f602-105">Suggestion</span></span>|<span data-ttu-id="9f602-106">Se è necessario serializzare e deserializzare un oggetto <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> tra .NET Framework 4.5 e .NET Framework 4.5.1/4.5.2, usare un serializzatore alternativo, ad esempio <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> o <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name>, invece di <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. In alternativa, poiché il problema è stato risolto in .NET Framework 4.6, eseguire l'aggiornamento a questa versione.</span><span class="sxs-lookup"><span data-stu-id="9f602-106">If it is necessary to serialize and deserialize a <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> between the .NET Framework 4.5 and .NET Framework 4.5.1/4.5.2, an alternate serializer like the <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> or <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializer should be used instead of the <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>.Alternatively, because this issue is addressed in the .NET Framework 4.6, it may be solved by upgrading to that version of the .NET Framework.</span></span>|
|<span data-ttu-id="9f602-107">Ambito</span><span class="sxs-lookup"><span data-stu-id="9f602-107">Scope</span></span>|<span data-ttu-id="9f602-108">Secondario</span><span class="sxs-lookup"><span data-stu-id="9f602-108">Minor</span></span>|
|<span data-ttu-id="9f602-109">Versione</span><span class="sxs-lookup"><span data-stu-id="9f602-109">Version</span></span>|<span data-ttu-id="9f602-110">4.5.1</span><span class="sxs-lookup"><span data-stu-id="9f602-110">4.5.1</span></span>|
|<span data-ttu-id="9f602-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f602-111">Type</span></span>|<span data-ttu-id="9f602-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="9f602-112">Runtime</span></span>|
