---
title: Recordset2-Member (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29d1472e8cd02d8968ba84dbc1c1cf99be7ee858
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726281"
---
# <a name="recordset2-members-dao"></a><span data-ttu-id="89731-102">Recordset2-Member (DAO)</span><span class="sxs-lookup"><span data-stu-id="89731-102">Recordset2 members (DAO)</span></span>


<span data-ttu-id="89731-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89731-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89731-104">Ein Recordset2 -Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrage stammen.</span><span class="sxs-lookup"><span data-stu-id="89731-104">A Recordset2 object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="89731-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="89731-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89731-106">Name</span><span class="sxs-lookup"><span data-stu-id="89731-106">Name</span></span></p></th>
<th><p><span data-ttu-id="89731-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89731-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89731-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-109">Erstellt einen neuen Datensatz für ein aktualisierbares <strong>Recordset2</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="89731-109">Creates a new record for an updatable <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-110"><strong><a href="recordset2-cancel-method-dao.md">Abbrechen</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-111"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-111"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-112">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-113">Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-115">Alle ausstehenden Aktualisierungen für ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="89731-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-117">Erstellt ein doppeltes <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt, das auf das ursprüngliche <strong>Recordset2</strong>-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="89731-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-118"><strong><a href="recordset2-close-method-dao.md">Schließen Sie</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-119">Schließt ein geöffnetes <strong>Recordset</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89731-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-121">Gibt ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt, das eine Kopie des <strong>QueryDef-Objekt</strong> ist verwendeten zum Erstellen des <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts, dargestellt durch das Recordset-Objekt-Platzhalter (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="89731-122">.</span><span class="sxs-lookup"><span data-stu-id="89731-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-123"><strong><a href="recordset2-delete-method-dao.md">Löschen</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-124">Wird für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-125"><strong><a href="recordset2-edit-method-dao.md">Bearbeiten</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-126">Kopiert den aktuellen Datensatz aus einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt zur nachfolgenden Bearbeitung in den Kopierpuffer.</span><span class="sxs-lookup"><span data-stu-id="89731-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-128">Füllt den lokalen Cache für ein <strong>Recordset</strong>-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält, teilweise oder vollständig auf (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen).</span><span class="sxs-lookup"><span data-stu-id="89731-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-130">Sucht den ersten Datensatz in einem <strong>Recordset</strong> -Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-132">Sucht den letzten Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> vom Typ Dynaset oder Snapshot-Objekt, die den angegebenen Kriterien entspricht, und macht, die den Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-134">Sucht den nächsten Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ Dynaset oder Snapshot, der den angegebenen Kriterien entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-134">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="89731-135">.</span><span class="sxs-lookup"><span data-stu-id="89731-135"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p104">Sucht den vorherigen Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ "Dynaset" oder "Snapshot", der die angegebenen Kriterien erfüllt, und macht diesen Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-140">Ruft mehrere Zeilen aus einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="89731-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-142">Verschiebt die Position des aktuellen Datensatzes in ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89731-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-144">Wechselt zum ersten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89731-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-146">Wechselt zum letzten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89731-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-148">Wechselt zum nächsten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89731-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-150">Wechselt zum vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="89731-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-152"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-152"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-153">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-154">Ruft die nächste Datensatzgruppe ab (falls vorhanden), die von einer mehrteiligen Auswahlabfrage in einem <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> -Aufruf zurückgegeben wurde. Daraufhin wird ein <strong>Boolean</strong>-Wert ausgegeben, der angibt, ob weitere Datensätze ausstehen (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-156">Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="89731-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-158">Die Daten in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="89731-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-160">Sucht den Datensatz in einem indizierten <strong>Recordset</strong> -Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-162"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-162"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-163">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-164">Speichert den Inhalt des Kopierpuffers in einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89731-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="89731-165">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="89731-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89731-166">Name</span><span class="sxs-lookup"><span data-stu-id="89731-166">Name</span></span></p></th>
<th><p><span data-ttu-id="89731-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89731-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89731-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-169">Legt die relative Datensatznummer des aktuellen Datensatzes eines <strong>Recordset2</strong>-Objekts fest oder gibt die Nummer zurück.</span><span class="sxs-lookup"><span data-stu-id="89731-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-171"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-171"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-172">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-173">Gibt die Anzahl von Datensätzen zurück, bei denen die letzte Batchaktualisierung nicht abgeschlossen wurde (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-175"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-176">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-177">Gibt ein Textmarkenarray zurück, das die Zeilen angibt, die bei der letzten Batchaktualisierung Konflikte verursacht haben (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-179"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-179"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-180">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-181">Mit dieser Eigenschaft wird die Anzahl von Anweisungen festgelegt oder zurückgegeben, die in jedem Batch an den Server zurückgesendet werden (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p110">Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem <strong>Recordset</strong> -Objekt vor dem ersten Datensatz liegt. Schreibgeschützter <strong>Boolean</strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p110">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-185"><strong><a href="recordset2-bookmark-property-dao.md">Lesezeichen</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-186">Legt ein Lesezeichen fest, das den aktuellen Datensatz in einem <strong>Recordset</strong>-Objekt eindeutig identifiziert, oder gibt das Lesezeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="89731-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-188">Gibt einen Wert zurück, der angibt, ob ein <strong>Recordset</strong>-Objekt Textmarken unterstützt, die Sie mithilfe der <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> -Eigenschaft festlegen können.</span><span class="sxs-lookup"><span data-stu-id="89731-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p111">Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="89731-p111">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-193">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Textmarke des ersten Datensatzes in einem Recordset -Objekt vom Typ Dynaset angibt, das lokal zwischenzuspeichernde Daten aus einer ODBC-Datenquelle enthält (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-194"><strong><a href="recordset2-connection-property-dao.md">Verbindung</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-195">Gibt das <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt zurück, das sich auf die Datenbank bezieht.</span><span class="sxs-lookup"><span data-stu-id="89731-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p112">Gibt das Datum und die Uhrzeit der Erstellung einer Basistabelle zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p112">Returns the date and time a base table was created (Microsoft Access workspaces only). Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-200">Gibt einen Wert zurück, der den Status der Bearbeitung für den aktuellen Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="89731-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p113">Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem <strong>Recordset</strong>-Objekt liegt. Schreibgeschützter <strong>Boolean</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p113">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-204"><strong><a href="recordset2-fields-property-dao.md">Felder</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p114">Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="89731-p114">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p115">Legt einen Wert fest, der die in einem nachfolgend geöffneten <strong>Recordset</strong> -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="89731-p115">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-211">Legt einen Wert fest, der den Namen des aktuellen <strong><a href="index-object-dao.md">Index</a></strong> -Objekts in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-213">Gibt ein Lesezeichen zurück, das den zuletzt hinzugefügten oder geänderten Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="89731-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p116">Gibt das Datum und die Uhrzeit der letzten Änderung einer Basistabelle zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p116">Returns the date and time of the most recent change made to a base table. Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-218">Legt einen Wert fest, der den Typ der Sperreangibt, die während der Bearbeitung wirksam ist, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89731-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p117">Gibt den Namen des angegebenen Objekts zurück. Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p117">Returns the name of the specified object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-223">Gibt an, ob ein bestimmter Datensatz mithilfe der <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> -Methode oder einer der <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> -Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-223">Indicates whether a particular record was found by using the <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p118">Gibt das übergeordnete <strong>Recordset</strong>-Objekt des angegebenen Datensatzes zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="89731-p118">Returns the parent <strong>Recordset</strong> of the specified recordset. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-228">Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt basierend auf einem Prozentwert der Datensätze im <strong>Recordset</strong> angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="89731-228">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-229"><strong><a href="recordset2-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p119">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="89731-p119">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p120">Gibt die Anzahl der Datensätze zurück, auf die in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt zugegriffen wird, oder die Gesamtzahl der Datensätze in einem <strong>Recordset</strong> -Objekt vom "table"-Typ oder in einem <strong><a href="tabledef-object-dao.md">TableDef</a></strong> -Objekt zurück. Schreibgeschütztes <strong>Long</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="89731-p120">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-237"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-237"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-238">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-238">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-p122">Gibt einen Wert zurück, der den Aktualisierungsstatus des aktuellen Datensatzes angibt, wenn dieser Teil einer Batchktualisierung ist (nur ODBCDirect-Arbeitsbereiche). Schreibgeschützter <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p122">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-242">Gibt einen Wert zurück, der angibt, ob ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt die <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> -Methode unterstützt, die die Abfrage, auf der das <strong>Recordset</strong>-Objekt basiert, erneut ausführt.</span><span class="sxs-lookup"><span data-stu-id="89731-242">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-244">Legt die Sortierreihenfolge für Datensätze in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-244">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-246"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-246"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-247">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-247">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-248">Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <strong>dbRunAsync</strong>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="89731-248">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-249"><strong><a href="recordset2-transactions-property-dao.md">Transaktionen</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p124">Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter <strong>Boolean</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p124">Returns a value that indicates whether an object supports transactions. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-252"><strong><a href="recordset2-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p125">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Schreibgeschützter <strong>Integer</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p125">Sets or returns a value that indicates the operational type or data type of an object. Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p126">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p126">Returns a value that indicates whether you can change a DAO object. Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-259"><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="89731-259"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="89731-260">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="89731-260">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="89731-p128">Legt einen Wert fest, der angibt, wie die WHERE-Klausel für jeden Datensatz während einer Batchaktualisierung erstellt wird, und ob die Batchaktualisierung eine UPDATE- oder eine DELETE-Anweisung gefolgt von einer INSERT-Anweisung verwenden soll, oder gibt den betreffenden Wert zurück (nur ODBCDirect-Arbeitsbereiche). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="89731-p128">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89731-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-264">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="89731-264">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89731-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="89731-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="89731-p129">Legt einen Wert fest, der den Text der Meldung festlegt, der von Ihrer Anwendung angezeigt wird, wenn der Wert eines <strong>Field</strong>-Objekts nicht der von der <strong>ValidationRule</strong>-Eigenschaft festgelegten Gültigkeitsregel entspricht, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="89731-p129">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

