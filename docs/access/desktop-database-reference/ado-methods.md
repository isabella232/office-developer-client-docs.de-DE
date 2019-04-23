---
title: ActiveX Data Objects (ADO)-Methoden
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283282"
---
# <a name="ado-methods"></a><span data-ttu-id="9d678-102">ADO-Methoden</span><span class="sxs-lookup"><span data-stu-id="9d678-102">ADO methods</span></span>

<span data-ttu-id="9d678-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d678-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="9d678-104">Methode</span><span class="sxs-lookup"><span data-stu-id="9d678-104">Method</span></span></th>
<th><span data-ttu-id="9d678-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d678-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="9d678-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-107">Ein neuer Datensatz für ein aktualisierbares <strong>Recordset</strong>-Objekt wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d678-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="9d678-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-p101">Ein Objekt wird einer Auflistung angefügt. Bei einer <strong>Fields</strong>-Auflistung wird möglicherweise ein neues <strong>Field</strong>-Objekt erstellt, bevor es der Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9d678-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="9d678-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-112">Daten werden einem großen <strong>Field</strong>-Text- oder -Binärdatenobjekt oder einem <strong>Parameter</strong>-Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="9d678-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">"BeginTrans", "CommitTrans" und "RollbackTrans"</a></span><span class="sxs-lookup"><span data-stu-id="9d678-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-114">Die Transaktionsverarbeitung in einem <strong>Connection</strong>-Objekt wird wie folgt verwaltet:</span><span class="sxs-lookup"><span data-stu-id="9d678-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="9d678-115"><strong>BeginTrans</strong> - Eine neue Transaktion wird begonnen.</span><span class="sxs-lookup"><span data-stu-id="9d678-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="9d678-p102">
<strong>CommitTrans</strong> - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="9d678-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="9d678-118">
<strong>RollbackTrans</strong> -bricht alle Änderungen ab und beendet die aktuelle Transaktion.</span><span class="sxs-lookup"><span data-stu-id="9d678-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="9d678-119">Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="9d678-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-120"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="9d678-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-121">Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9d678-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="9d678-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-123">Eine ausstehende Batchaktualisierung wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="9d678-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="9d678-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-125">Alle an der aktuellen oder neuen Zeile eines <strong>Recordset</strong>-Objekts oder der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vorgenommenen Änderungen werden abgebrochen, bevor die <strong>Update</strong>-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9d678-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="9d678-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-127">Alle <strong>Error</strong>-Objekte werden aus der <strong>Errors</strong>-Auflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9d678-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="9d678-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-129">Ein <strong>Recordset</strong>-Objektduplikat wird aus einem vorhandenen <strong>Recordset</strong> -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d678-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="9d678-130">Optional wird angegeben, dass der Klon schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="9d678-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="9d678-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-132">Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.</span><span class="sxs-lookup"><span data-stu-id="9d678-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="9d678-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-134">Zwei Textmarken werden verglichen, und die relativen Werte werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d678-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="9d678-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-136">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="9d678-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="9d678-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-138">Die angegebene Anzahl von Zeichen oder Bytes (abhängig vom <strong>Typ</strong>) im <strong>Datenstrom</strong> wird in ein anderes <strong>Stream</strong>-Objekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="9d678-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="9d678-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-140">Ein neues <strong>Parameter</strong>-Objekt mit den angegebenen Eigenschaften wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d678-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-141"><a href="delete-method-ado-parameters-collection.md">Delete (Parameters-Auflistung in ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-142">Ein Objekt wird aus der <strong>Parameters</strong>-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9d678-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-143"><a href="delete-method-ado-fields-collection.md">Delete (Fields-Auflistung in ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-144">Ein Objekt wird aus der <strong>Fields</strong>-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9d678-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-145"><a href="delete-method-ado-recordset.md">Delete (ADO-Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-146">Der aktuelle Datensatz oder eine Gruppe von Datensätzen wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9d678-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="9d678-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-148">Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9d678-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO-Befehl)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-150">Es wird die Abfrage, SQL-Anweisung oder gespeicherte Prozedur ausgeführt, die in der <strong>CommandText</strong>-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9d678-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO-Verbindung)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-152">Die angegebene Abfrage, SQL-Anweisung, gespeicherte Prozedur oder der angegebene anbieterspezifische Text wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d678-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-153"><a href="find-method-ado.md">Suchen</a></span><span class="sxs-lookup"><span data-stu-id="9d678-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-154">Ein <strong>Recordset</strong>-Objekt wird nach der Zeile durchsucht, die den angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="9d678-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-155"><a href="flush-method-ado.md">Leeren</a></span><span class="sxs-lookup"><span data-stu-id="9d678-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-156">Es wird erzwungen, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts in das zugrunde liegende Objekt übernommen wird, das dem <strong>Stream</strong>-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9d678-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="9d678-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-158">Ein <strong>Recordset</strong>-Objekt wird zurückgegeben, dessen Zeilen die Daten und Unterverzeichnisse in dem durch dieses <strong>Record</strong>-Objekt dargestellten Verzeichnis darstellen.</span><span class="sxs-lookup"><span data-stu-id="9d678-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="9d678-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-160">Der gesamte Inhalt oder ein Teil des Inhalts eines großen <strong>Field</strong>-Text- oder -Binärdatenobjekts wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d678-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="9d678-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-162">Mehrere Datensätze eines <strong>Recordset</strong>-Objekts werden in ein Array abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d678-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="9d678-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-164">Das <strong>Recordset</strong>-Objekt wird als Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d678-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="9d678-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-166">Der Inhalt einer vorhandenen Datei wird in ein <strong>Stream</strong>-Objekt geladen.</span><span class="sxs-lookup"><span data-stu-id="9d678-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="9d678-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-168">Die Position des aktuellen Datensatzes in einem <strong>Recordset</strong>-Objekt wird verschoben.</span><span class="sxs-lookup"><span data-stu-id="9d678-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">"MoveFirst", "MoveLast", "MoveNext" und "MovePrevious"</a></span><span class="sxs-lookup"><span data-stu-id="9d678-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-170">Es wird zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt gewechselt, und dieser Datensatz wird zum aktuellen Datensatz gemacht.</span><span class="sxs-lookup"><span data-stu-id="9d678-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="9d678-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-172">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="9d678-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="9d678-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-174">Der Inhalt des aktuellen <strong>Recordset</strong>-Objekts wird gelöscht, und das nächste <strong>Recordset</strong>-Objekt wird durch eine Reihe von Befehlen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9d678-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-175"><a href="open-method-ado-connection.md">Open (ADO-Verbindung)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-176">Eine Verbindung mit einer Datenquelle wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9d678-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-177"><a href="open-method-ado-record.md">Open (ADO-Record)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-178">Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="9d678-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-179"><a href="open-method-ado-recordset.md">Open (ADO-Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-180">Ein Cursor wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9d678-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-181"><a href="open-method-ado-stream.md">Open (ADO-Stream)</a></span><span class="sxs-lookup"><span data-stu-id="9d678-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-182">Ein <strong>Stream</strong>-Objekt zum Ändern von Datenströmen von Binär- oder Textdaten wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9d678-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="9d678-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-184">Datenbank-Schemainformationen werden vom Anbieter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d678-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-185"><a href="read-method-ado.md">Lesen</a></span><span class="sxs-lookup"><span data-stu-id="9d678-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-186">Eine angegebene Anzahl von Bytes aus einem <strong>Stream</strong>-Objekt wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d678-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="9d678-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-188">Eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d678-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="9d678-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-190">Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.</span><span class="sxs-lookup"><span data-stu-id="9d678-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="9d678-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-192">Die Daten in einem <strong>Recordset</strong>-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="9d678-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="9d678-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-194">Die Daten im aktuellen <strong>Recordset</strong>-Objekt oder in der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts werden anhand der zugrunde liegenden Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9d678-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="9d678-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-196">Das <strong>Recordset</strong>-Objekt wird in einer Datei oder in einem <strong>Stream</strong>-Objekt gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d678-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="9d678-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-198">Der Binärinhalt eines <strong>Stream</strong>-Objekts wird in einer Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d678-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="9d678-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-200">Der Index eines <strong>Recordset</strong>-Objekts wird durchsucht, um schnell die Zeile zu finden, die mit den angegebenen Werten übereinstimmt, und die aktuelle Zeilenposition wird in diese Zeile geändert.</span><span class="sxs-lookup"><span data-stu-id="9d678-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="9d678-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-202">Die Position, die das Ende des Datenstroms darstellt, wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9d678-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="9d678-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-204">Beim Lesen eines Textdatenstroms wird eine gesamte Zeile übersprungen.</span><span class="sxs-lookup"><span data-stu-id="9d678-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="9d678-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-206">Statistische Informationen zu einem geöffneten Datenstrom werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9d678-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-207"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="9d678-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-208">Es wird bestimmt, ob ein bestimmter Funktionalitätstyp von einem angegebenen <strong>Recordset</strong>-Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="9d678-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-209"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="9d678-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-210">Alle Änderungen, die Sie an der aktuellen Zeile eines <strong>Recordset</strong>-Objekts oder an der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vornehmen, werden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9d678-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="9d678-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-212">Alle ausstehenden Batchaktualisierungen werden auf den Datenträger geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d678-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d678-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="9d678-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-214">Binärdaten werden in ein <strong>Stream</strong>-Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d678-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d678-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="9d678-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="9d678-216">Eine angegebene Textzeichenfolge wird in ein <strong>Stream</strong>-Objekt geschrieben.</span><span class="sxs-lookup"><span data-stu-id="9d678-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
