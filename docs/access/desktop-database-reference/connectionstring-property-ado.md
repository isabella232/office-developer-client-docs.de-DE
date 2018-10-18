---
<span data-ttu-id="01ec8-101"><<<<<<< HEAD-Titel: ConnectionString-Eigenschaft (ADO) TOCTitle: ConnectionString-Eigenschaft (ADO) === Titel: ConnectionString-Eigenschaft (ADO) TOCTitle: ConnectionString-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="01ec8-101"><<<<<<< HEAD title: ConnectionString Property (ADO) TOCTitle: ConnectionString Property (ADO) ======= title: ConnectionString property (ADO) TOCTitle: ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="01ec8-102">Master Ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) Ms:contentKeyID: 48547627 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="01ec8-102">master ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) ms:contentKeyID: 48547627 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="01ec8-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="01ec8-103"><<<<<<< HEAD</span></span>
# <a name="connectionstring-property-ado"></a><span data-ttu-id="01ec8-104">ConnectionString-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="01ec8-104">ConnectionString Property (ADO)</span></span>
=======
# <a name="connectionstring-property-ado"></a><span data-ttu-id="01ec8-105">ConnectionString-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="01ec8-105">ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="01ec8-106">master</span><span class="sxs-lookup"><span data-stu-id="01ec8-106">master</span></span>


<span data-ttu-id="01ec8-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="01ec8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="01ec8-108">Gibt die Informationen an, mit denen eine Verbindung mit einer Datenquelle hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="01ec8-108">Indicates the information used to establish a connection to a data source.</span></span>

<span data-ttu-id="01ec8-109"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="01ec8-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="01ec8-110">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="01ec8-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="01ec8-111">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="01ec8-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="01ec8-112">master</span><span class="sxs-lookup"><span data-stu-id="01ec8-112">master</span></span>

<span data-ttu-id="01ec8-113">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="01ec8-113">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01ec8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="01ec8-114">Remarks</span></span>

<span data-ttu-id="01ec8-115">Verwenden Sie die **ConnectionString** -Eigenschaft, um eine Datenquelle anzugeben, indem Sie eine mit einer Reihe von durch Semikolons getrennte *Argument* *= Wert* Anweisungen detaillierte Verbindungszeichenfolge übergeben.</span><span class="sxs-lookup"><span data-stu-id="01ec8-115">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="01ec8-p101">ADO unterstützt fünf Argumente für die **ConnectionString** -Eigenschaft. Alle anderen Argumente werden ohne weitere Verarbeitung durch ADO direkt an den Anbieter übergeben. ADO unterstützt die im Folgenden aufgeführten Argumente.</span><span class="sxs-lookup"><span data-stu-id="01ec8-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="01ec8-118">Argument</span><span class="sxs-lookup"><span data-stu-id="01ec8-118">Argument</span></span></p></th>
<th><p><span data-ttu-id="01ec8-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01ec8-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="01ec8-120"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="01ec8-120"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="01ec8-121">Gibt den Namen eines Anbieters an, der für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="01ec8-121">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01ec8-122"><em>Dateiname =</em></span><span class="sxs-lookup"><span data-stu-id="01ec8-122"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="01ec8-123">Gibt den Namen einer anbieterspezifischen Datei an (z. B. ein gespeichertes Datenquellenobjekt), die voreingestellte Verbindungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="01ec8-123">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01ec8-124"><em>Remote Provider =</em></span><span class="sxs-lookup"><span data-stu-id="01ec8-124"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="01ec8-p102">Gibt den Namen eines Anbieters an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="01ec8-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="01ec8-127"><em>Remoteserver =</em></span><span class="sxs-lookup"><span data-stu-id="01ec8-127"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="01ec8-p103">Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="01ec8-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="01ec8-130"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="01ec8-130"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="01ec8-131">Gibt die Verbindungszeichenfolge als absolute URL an, die eine Ressource wie z. B. eine Datei oder ein Verzeichnis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="01ec8-131">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="01ec8-132">Nachdem Sie die **ConnectionString** -Eigenschaft festgelegt und das [Connection](connection-object-ado.md)-Objekt geöffnet haben, kann der Anbieter den Inhalt der Eigenschaft ändern, indem er z. B. die in ADO definierten Argumentnamen den entsprechenden Anbieternamen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="01ec8-132">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="01ec8-133">Die **ConnectionString** -Eigenschaft erbt automatisch den Wert für das Argument *ConnectionString* der [Open](open-method-ado-connection.md) -Methode verwendet, damit Sie die aktuelle **ConnectionString** -Eigenschaft beim Aufruf **Open** -Methode außer Kraft setzen können.</span><span class="sxs-lookup"><span data-stu-id="01ec8-133">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="01ec8-134">Da das Argument *Dateiname* ADO zugeordneten Anbieter geladen wird, kann nicht den *Anbieter* und den *Dateinamen* Argumente übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="01ec8-134">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="01ec8-135">Die **ConnectionString** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="01ec8-135">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="01ec8-p104">Duplikate eines Arguments in der **ConnectionString** -Eigenschaft werden ignoriert. Die letzte Instanz eines Arguments wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="01ec8-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="01ec8-138">**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Connection** -Objekt verwendet wird, kann die **ConnectionString** -Eigenschaft nur die Parameter *Remote Provider* und *Remote Server* enthalten.</span><span class="sxs-lookup"><span data-stu-id="01ec8-138">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

