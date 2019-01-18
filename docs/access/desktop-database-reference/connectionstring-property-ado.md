---
title: ConnectionString-Eigenschaft (ADO)
TOCTitle: ConnectionString property (ADO)
ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15)
ms:contentKeyID: 48547627
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3612652f3473c0794dbfe9be60f84ea2e3fee252
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712729"
---
# <a name="connectionstring-property-ado"></a><span data-ttu-id="a94b6-102">ConnectionString-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="a94b6-102">ConnectionString property (ADO)</span></span>


<span data-ttu-id="a94b6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a94b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a94b6-104">Gibt die Informationen an, mit denen eine Verbindung mit einer Datenquelle hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a94b6-104">Indicates the information used to establish a connection to a data source.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="a94b6-105">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a94b6-105">Settings and return values</span></span>

<span data-ttu-id="a94b6-106">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a94b6-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a94b6-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a94b6-107">Remarks</span></span>

<span data-ttu-id="a94b6-108">Verwenden Sie die **ConnectionString** -Eigenschaft, um eine Datenquelle anzugeben, indem Sie eine mit einer Reihe von durch Semikolons getrennte *Argument* *= Wert* Anweisungen detaillierte Verbindungszeichenfolge übergeben.</span><span class="sxs-lookup"><span data-stu-id="a94b6-108">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="a94b6-p101">ADO unterstützt fünf Argumente für die **ConnectionString** -Eigenschaft. Alle anderen Argumente werden ohne weitere Verarbeitung durch ADO direkt an den Anbieter übergeben. ADO unterstützt die im Folgenden aufgeführten Argumente.</span><span class="sxs-lookup"><span data-stu-id="a94b6-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a94b6-111">Argument</span><span class="sxs-lookup"><span data-stu-id="a94b6-111">Argument</span></span></p></th>
<th><p><span data-ttu-id="a94b6-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a94b6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a94b6-113"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="a94b6-113"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="a94b6-114">Gibt den Namen eines Anbieters an, der für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a94b6-114">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a94b6-115"><em>Dateiname =</em></span><span class="sxs-lookup"><span data-stu-id="a94b6-115"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="a94b6-116">Gibt den Namen einer anbieterspezifischen Datei an (z. B. ein gespeichertes Datenquellenobjekt), die voreingestellte Verbindungsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a94b6-116">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a94b6-117"><em>Remote Provider =</em></span><span class="sxs-lookup"><span data-stu-id="a94b6-117"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="a94b6-p102">Gibt den Namen eines Anbieters an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="a94b6-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a94b6-120"><em>Remoteserver =</em></span><span class="sxs-lookup"><span data-stu-id="a94b6-120"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="a94b6-p103">Gibt den Pfadnamen des Servers an, der beim Öffnen einer clientseitigen Verbindung verwendet werden soll (nur Remote Data Service).</span><span class="sxs-lookup"><span data-stu-id="a94b6-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a94b6-123"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="a94b6-123"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="a94b6-124">Gibt die Verbindungszeichenfolge als absolute URL an, die eine Ressource wie z. B. eine Datei oder ein Verzeichnis identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a94b6-124">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a94b6-125">Nachdem Sie die **ConnectionString** -Eigenschaft festgelegt und das [Connection](connection-object-ado.md)-Objekt geöffnet haben, kann der Anbieter den Inhalt der Eigenschaft ändern, indem er z. B. die in ADO definierten Argumentnamen den entsprechenden Anbieternamen zuordnet.</span><span class="sxs-lookup"><span data-stu-id="a94b6-125">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="a94b6-126">Die **ConnectionString** -Eigenschaft erbt automatisch den Wert für das Argument *ConnectionString* der [Open](open-method-ado-connection.md) -Methode verwendet, damit Sie die aktuelle **ConnectionString** -Eigenschaft beim Aufruf **Open** -Methode außer Kraft setzen können.</span><span class="sxs-lookup"><span data-stu-id="a94b6-126">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="a94b6-127">Da das Argument *Dateiname* ADO zugeordneten Anbieter geladen wird, kann nicht den *Anbieter* und den *Dateinamen* Argumente übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="a94b6-127">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="a94b6-128">Die **ConnectionString** -Eigenschaft hat Lese-/Schreibzugriff, wenn die Verbindung geschlossen ist. Wenn die Verbindung geöffnet ist, ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a94b6-128">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="a94b6-p104">Duplikate eines Arguments in der **ConnectionString** -Eigenschaft werden ignoriert. Die letzte Instanz eines Arguments wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="a94b6-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="a94b6-131">**Remote Data Service-Verwendung** Wenn für ein clientseitiges **Connection** -Objekt verwendet wird, kann die **ConnectionString** -Eigenschaft nur die Parameter *Remote Provider* und *Remote Server* enthalten.</span><span class="sxs-lookup"><span data-stu-id="a94b6-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

