### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a><span data-ttu-id="b69d7-101">La chiamata di DataGrid.CommitEdit da un gestore CellEditEnding fa perdere lo stato attivo</span><span class="sxs-lookup"><span data-stu-id="b69d7-101">Calling DataGrid.CommitEdit from a CellEditEnding handler drops focus</span></span>

|   |   |
|---|---|
|<span data-ttu-id="b69d7-102">Dettagli</span><span class="sxs-lookup"><span data-stu-id="b69d7-102">Details</span></span>|<span data-ttu-id="b69d7-103">La chiamata di <xref:System.Windows.Controls.DataGrid.CommitEdit> da uno dei gestori eventi <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> di <xref:System.Windows.Controls.DataGrid?displayProperty=name> causa la perdita dello stato attivo per <xref:System.Windows.Controls.DataGrid?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b69d7-103">Calling <xref:System.Windows.Controls.DataGrid.CommitEdit> from one of the <xref:System.Windows.Controls.DataGrid?displayProperty=name>'s <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> event handlers causes the <xref:System.Windows.Controls.DataGrid?displayProperty=name> to lose focus.</span></span>|
|<span data-ttu-id="b69d7-104">Suggerimento</span><span class="sxs-lookup"><span data-stu-id="b69d7-104">Suggestion</span></span>|<span data-ttu-id="b69d7-105">Questo bug è stato risolto in .NET Framework 4.5.2, pertanto può essere evitato eseguendo l'aggiornamento di .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b69d7-105">This bug has been fixed in the .NET Framework 4.5.2, so it can be avoided by upgrading the .NET Framework.</span></span> <span data-ttu-id="b69d7-106">In alternativa, è possibile evitarlo selezionando di nuovo in modo esplicito <xref:System.Windows.Controls.DataGrid?displayProperty=name> dopo la chiamata di <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="b69d7-106">Alternatively, it can be avoided by explicitly re-selecting the <xref:System.Windows.Controls.DataGrid?displayProperty=name> after calling <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.</span></span>|
|<span data-ttu-id="b69d7-107">Ambito</span><span class="sxs-lookup"><span data-stu-id="b69d7-107">Scope</span></span>|<span data-ttu-id="b69d7-108">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b69d7-108">Edge</span></span>|
|<span data-ttu-id="b69d7-109">Versione</span><span class="sxs-lookup"><span data-stu-id="b69d7-109">Version</span></span>|<span data-ttu-id="b69d7-110">4.5</span><span class="sxs-lookup"><span data-stu-id="b69d7-110">4.5</span></span>|
|<span data-ttu-id="b69d7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="b69d7-111">Type</span></span>|<span data-ttu-id="b69d7-112">Runtime</span><span class="sxs-lookup"><span data-stu-id="b69d7-112">Runtime</span></span>|
|<span data-ttu-id="b69d7-113">API interessate</span><span class="sxs-lookup"><span data-stu-id="b69d7-113">Affected APIs</span></span>|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|
