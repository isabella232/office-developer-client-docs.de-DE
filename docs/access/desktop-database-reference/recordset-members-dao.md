---
title: Recordset-Elemente (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c36187eef0b55681b2ba426d979f42ee8a6efea8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284806"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="418e3-102">Recordset-Elemente (DAO)</span><span class="sxs-lookup"><span data-stu-id="418e3-102">Recordset Members (DAO)</span></span>


<span data-ttu-id="418e3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="418e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="418e3-104">Ein Recordset-Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrageausführung resultieren.</span><span class="sxs-lookup"><span data-stu-id="418e3-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="418e3-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="418e3-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="418e3-106">Name</span><span class="sxs-lookup"><span data-stu-id="418e3-106">Name</span></span></p></th>
<th><p><span data-ttu-id="418e3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="418e3-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="418e3-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-108"><a href="recordset-addnew-method-dao.md">expression</a>  . <strong>AddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-109">Erstellt einen neuen Datensatz für ein aktualisierbares <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="418e3-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-110"><a href="recordset-cancel-method-dao.md">Cancel</a>.</span></span></p></td>
<td><p><span data-ttu-id="418e3-111"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-112">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-113">Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-115">Bricht alle ausstehenden Updates für ein <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="418e3-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-117">Erstellt ein dupliziertes <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt, das auf das ursprüngliche <strong>Recordset</strong>-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="418e3-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-119">Schließt ein geöffnetes <strong>Recordset</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="418e3-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-120"><a href="recordset-copyquerydef-method-dao.md">expression</a>  . <strong>CopyQueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-121">Gibt ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong>-Objekt zurück, das eine Kopie des <strong>QueryDef</strong>-Objekts darstellt, welches zum Erstellen des <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekts verwendet wurde, das durch den recordset-Platzhalter dargestellt wird (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the  recordset placeholder (Microsoft Access workspaces only). .</span></span> <span data-ttu-id="418e3-122">.</span><span class="sxs-lookup"><span data-stu-id="418e3-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-124">Für dieses Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-126">Kopiert den aktuellen Datensatz zur weiteren Bearbeitung aus einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt in den Kopierpuffer.</span><span class="sxs-lookup"><span data-stu-id="418e3-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-128">Füllt den lokalen Cache für ein <strong>Recordset</strong>-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen), teilweise oder vollständig auf.</span><span class="sxs-lookup"><span data-stu-id="418e3-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-130">Sucht den ersten Datensatz in einem <strong>Recordset</strong>-Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span><span class="sxs-lookup"><span data-stu-id="418e3-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span><span class="sxs-lookup"><span data-stu-id="418e3-p103">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span><span class="sxs-lookup"><span data-stu-id="418e3-p104">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-140">Ruft mehrere Zeilen aus einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="418e3-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-142">Verschiebt die Position des aktuellen Datensatzes in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="418e3-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-143"><a href="recordset-movefirst-method-dao.md">expression</a>  . <strong>MoveFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-144">Wechselt zum ersten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="418e3-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-146">Wechselt zum letzten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="418e3-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-147"><a href="recordset-movenext-method-dao.md">expression</a>  . <strong>MoveNext</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-148">Wechselt zum nächsten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen Datensatz zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="418e3-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-149"><a href="recordset-moveprevious-method-dao.md">expression</a>  . <strong>MovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-150">Wechselt zum vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen Datensatz zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="418e3-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-151"><a href="recordset-nextrecordset-method-dao.md">expression</a>  . <strong>NextRecordset</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-152"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-153">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-154">Ruft die nächste Datensatzgruppe ab (falls vorhanden), die von einer mehrteiligen Auswahlabfrage in einem <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> -Aufruf zurückgegeben wurde. Daraufhin wird ein <strong>Boolean</strong>-Wert ausgegeben, der angibt, ob weitere Datensätze ausstehen (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-156">Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</span><span class="sxs-lookup"><span data-stu-id="418e3-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-158">Aktualisiert die Daten in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt, indem die Abfrage erneut ausgeführt wird, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="418e3-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-160">Sucht den Datensatz in einem indizierten <strong>Recordset</strong>-Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-162"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-163">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-164">Speichert den Inhalt des Kopierpuffers in einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="418e3-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="418e3-165">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="418e3-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="418e3-166">Name</span><span class="sxs-lookup"><span data-stu-id="418e3-166">Name</span></span></p></th>
<th><p><span data-ttu-id="418e3-167">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="418e3-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="418e3-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-168"><a href="recordset-absoluteposition-property-dao.md">expression</a>  . <strong>AbsolutePosition</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-169">Legt die relative Datensatznummer des aktuellen Datensatzes eines <strong>Recordset</strong>-Objekts fest oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-169">Sets or returns the relative record number of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-170"><a href="recordset-batchcollisioncount-property-dao.md">expression</a>  . <strong>BatchCollisionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-171"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-172">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-173">Gibt die Anzahl der Datensätze zurück, die die letzte Batchaktualisierung nicht ausgeführt haben (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-174"><a href="recordset-batchcollisions-property-dao.md">expression</a>  . <strong>BatchCollisions</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-175"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-176">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-177">Gibt ein Textmarkenarray zurück, das die Zeilen angibt, die bei der letzten Batchaktualisierung Konflikte verursacht haben (gilt nur für ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-178"><a href="recordset-batchsize-property-dao.md">expression</a>  . <strong>BatchSize</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-179"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-180">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-181">Legt die Anzahl der Anweisungen fest, die in jedem Batch an den Server zurückgesendet wurden, oder gibt die betreffende Anzahl zurück (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-183">Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem <strong>Recordset</strong>-Objekt vor dem ersten Datensatz liegt.</span><span class="sxs-lookup"><span data-stu-id="418e3-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="418e3-184">Schreibgeschützter <strong>boolescher</strong> Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-185"><strong><a href="recordset-bookmark-property-dao.md">BOOKMARK</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-186">Legt eine Textmarke fest oder gibt sie zurück. Sie identifiziert den aktuellen Datensatz eindeutig in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="418e3-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-188">Gibt einen Wert zurück, der angibt, ob ein <strong>Recordset</strong>-Objekt Textmarken unterstützt, die Sie unter Verwendung der <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>-Eigenschaft festlegen können.</span><span class="sxs-lookup"><span data-stu-id="418e3-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-189"><a href="recordset-cachesize-property-dao.md">expression</a>  . <strong>CacheSize</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-190">Mit dieser Eigenschaft wird die Anzahl von Datensätzen, die aus einer ODBC-Datenquelle abgerufen und lokal gespeichert werden, festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="418e3-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="418e3-191"><strong>Long</strong> mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="418e3-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-192">CacheStart Property</span></span></p></td>
<td><p><span data-ttu-id="418e3-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span><span class="sxs-lookup"><span data-stu-id="418e3-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-195">Gibt das <strong><a href="connection-object-dao.md">Connection</a></strong>-Objekt zurück, das der Datenbank entspricht.</span><span class="sxs-lookup"><span data-stu-id="418e3-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-197">Gibt das Datum und die Uhrzeit der Erstellung einer Basistabelle zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="418e3-198">Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-199"><a href="recordset-editmode-property-dao.md">expression</a>  . <strong>EditMode</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-200">Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="418e3-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-202">Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem <strong>Recordset</strong>-Objekt liegt.</span><span class="sxs-lookup"><span data-stu-id="418e3-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="418e3-203">Schreibgeschützter <strong>boolescher</strong> Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-205">Gibt eine <strong>Fields</strong> -Auflistung zurück, die alle gespeicherten <strong>Field</strong> -Objekte für das angegebene Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="418e3-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="418e3-206">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-207"><strong><a href="recordset-filter-property-dao.md">$filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-208">Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten <strong>Recordset</strong>-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="418e3-209"><strong>Zeichenfolge</strong> mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="418e3-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-211">Legt einen Wert fest, der den Namen des aktuellen <strong><a href="index-object-dao.md">Index</a></strong>-Objekts in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-212">LastModified Property</span></span></p></td>
<td><p><span data-ttu-id="418e3-213">Gibt eine Textmarke zurück, die den zuletzt hinzugefügten oder geänderten Datensatz angibt.</span><span class="sxs-lookup"><span data-stu-id="418e3-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-214">LastUpdated Property</span></span></p></td>
<td><p><span data-ttu-id="418e3-215">Gibt das Datum und die Uhrzeit der letzten Änderung einer Basistabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="418e3-216">Schreibgeschützter <strong>Variant</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-217"><a href="recordset-lockedits-property-dao.md">expression</a>  . <strong>LockEdits</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-218">Legt einen Wert fest, der die Art der Sperrung angibt, die beim Bearbeiten wirksam ist, oder gibt diesen zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-220">Gibt den Namen des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-220">Returns the name of the specified object.</span></span> <span data-ttu-id="418e3-221">Schreibgeschützte <strong>Zeichenfolge</strong>.</span><span class="sxs-lookup"><span data-stu-id="418e3-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-222"><a href="recordset-nomatch-property-dao.md">expression</a>  . <strong>NoMatch</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-223">Gibt an, ob ein bestimmter Datensatz mithilfe der <strong><a href="recordset-seek-method-dao.md">Seek</a></strong>-Methode oder einer der <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong>-Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-224">PercentPosition Property</span></span></p></td>
<td><p><span data-ttu-id="418e3-225">Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt basierend auf einem Prozentwert der Datensätze im <strong>Recordset</strong> angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-227">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="418e3-227">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="418e3-228">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-228">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="418e3-p119">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-233"><a href="recordset-recordstatus-property-dao.md">expression</a>  . <strong>RecordStatus</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-234"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-234">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-235">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-235">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-p121">Gibt einen Wert zurück, der den Aktualisierungsstatus des aktuellen Datensatzes angibt, wenn dieser Teil einer Batchktualisierung ist (nur ODBCDirect-Arbeitsbereiche). Schreibgeschützter <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> -Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-p121">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only). Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-239">Gibt einen Wert zurück, der angibt, ob ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt die <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> -Methode unterstützt, die die Abfrage, auf der das <strong>Recordset</strong>-Objekt basiert, erneut ausführt.</span><span class="sxs-lookup"><span data-stu-id="418e3-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-241">Legt die Sortierreihenfolge von Datensätzen in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-242"><a href="recordset-stillexecuting-property-dao.md">expression</a>  . <strong>StillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-243"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-243">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-244">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-244">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-245">Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <strong>dbRunAsync</strong>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="418e3-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-247">Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-247">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="418e3-248">Schreibgeschützter <strong>boolescher</strong> Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-248">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-249"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="418e3-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-250">Die Beschreibung für dieses Element wird in der endgültigen Version von Office 14 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="418e3-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-252">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="418e3-252">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="418e3-253">Schreibgeschützter <strong>boolescher</strong> Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-253">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-255"><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="418e3-255">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="418e3-256">Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="418e3-256">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="418e3-p126">Legt einen Wert fest, der angibt, wie die WHERE-Klausel für jeden Datensatz während einer Batchaktualisierung erstellt wird, und ob die Batchaktualisierung eine UPDATE- oder eine DELETE-Anweisung gefolgt von einer INSERT-Anweisung verwenden soll, oder gibt den betreffenden Wert zurück (nur ODBCDirect-Arbeitsbereiche). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> -Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="418e3-p126">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only). Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="418e3-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-260">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="418e3-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="418e3-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="418e3-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="418e3-p127">Legt einen Wert fest, der den Text der Meldung festlegt, der von Ihrer Anwendung angezeigt wird, wenn der Wert eines <strong>Field</strong>-Objekts nicht der von der <strong>ValidationRule</strong>-Eigenschaft festgelegten Gültigkeitsregel entspricht, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="418e3-p127">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

