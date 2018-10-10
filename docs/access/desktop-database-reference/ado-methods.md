---
title: ActiveX Data Objects (ADO)-Methoden
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b7a685352063c3c1dd4c9bbd62e9c1fc4cdfe11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472892"
---
# <a name="ado-methods"></a><span data-ttu-id="e99d7-102">ADO-Methoden</span><span class="sxs-lookup"><span data-stu-id="e99d7-102">ADO Methods</span></span>


<span data-ttu-id="e99d7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e99d7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-104"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-104"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-105">Es wird ein neuer Datensatz für ein aktualisierbares <strong>Recordset</strong>-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-105">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-106"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-106"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-p101">Ein Objekt wird einer Auflistung angefügt. Bei einer <strong>Fields</strong>-Auflistung wird möglicherweise ein neues <strong>Field</strong>-Objekt erstellt, bevor es der Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="e99d7-p101">Appends an object to a collection. If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-109"><a href="appendchunk-method-ado.md">Methoden "AppendChunk"</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-110">Daten werden einem großen <strong>Field</strong>-Text- oder -Binärdatenobjekt oder einem <strong>Parameter</strong>-Objekt angefügt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-110">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans und RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-112">Transaktionsverarbeitung in einem <strong>Connection</strong> -Objekt wie folgt verwaltet: <strong>BeginTrans</strong> – beginnt eine neue Transaktion.</span><span class="sxs-lookup"><span data-stu-id="e99d7-112">Manages transaction processing within a <strong>Connection</strong> object as follows: <strong>BeginTrans</strong> — Begins a new transaction.</span></span><br /><span data-ttu-id="e99d7-p102">
<strong>CommitTrans</strong> - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="e99d7-p102">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span><br /><span data-ttu-id="e99d7-115">
<strong>RollbackTrans</strong> – alle Änderungen werden abgebrochen und beendet die aktuelle Transaktion.</span><span class="sxs-lookup"><span data-stu-id="e99d7-115">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="e99d7-116">Möglicherweise wird auch eine neue Transaktion gestartet.</span><span class="sxs-lookup"><span data-stu-id="e99d7-116">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-117"><a href="cancel-method-ado.md">Cancel</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-117"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-118">Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.</span><span class="sxs-lookup"><span data-stu-id="e99d7-118">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-120">Eine ausstehende Batchaktualisierung wird abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-120">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-122">Alle an der aktuellen oder neuen Zeile eines <strong>Recordset</strong>-Objekts oder der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vorgenommenen Änderungen werden abgebrochen, bevor die <strong>Update</strong>-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e99d7-122">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-123"><a href="clear-method-ado.md">Löschen</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-123"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-124">Alle <strong>Error</strong> -Objekte werden aus der <strong>Errors</strong> -Auflistung entfernt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-124">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-125"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-125"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-p104">Ein <strong>Recordset</strong>-Objektduplikat wird aus einem vorhandenen <strong>Recordset</strong> -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="e99d7-p104">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object. Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-128"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-128"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-129">Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-129">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-131">Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.</span><span class="sxs-lookup"><span data-stu-id="e99d7-131">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-133">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="e99d7-133">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-134"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-134"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-135">Kopiert die angegebene Anzahl von Zeichen oder Bytes (in Abhängigkeit vom <strong>Type</strong>) von einem <strong>Stream</strong>-Objekt in ein anderes <strong>Stream</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-135">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-136"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-136"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-137">Erstellt ein neues <strong>Parameter</strong>-Objekt mit den angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e99d7-137">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO-Parameters-Auflistung)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-139">Ein Objekt wird aus der <strong>Parameters</strong>-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e99d7-139">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-140"><a href="delete-method-ado-fields-collection.md">Löschen Sie (ADO-Fields-Auflistung)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-140"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-141">Ein Objekt wird aus der <strong>Fields</strong>-Auflistung gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e99d7-141">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-142"><a href="delete-method-ado-recordset.md">Delete (ADO-Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-142"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-143">Löscht den aktuellen Datensatz oder eine Gruppe von Datensätzen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-143">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-145">Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e99d7-145">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Führen Sie aus (ADO-Befehl)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-147">Es wird die Abfrage, SQL-Anweisung oder gespeicherte Prozedur ausgeführt, die in der <strong>CommandText</strong>-Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e99d7-147">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Führen Sie aus (ADO-Verbindung)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-149">Die angegebene Abfrage, SQL-Anweisung, gespeicherte Prozedur oder der angegebene anbieterspezifische Text wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-149">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-150"><a href="find-method-ado.md">Find</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-150"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-151">Ein <strong>Recordset</strong>-Objekt wird nach der Zeile durchsucht, die den angegebenen Kriterien entspricht.</span><span class="sxs-lookup"><span data-stu-id="e99d7-151">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-152"><a href="flush-method-ado.md">Leeren</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-152"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-153">Erzwingt, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts an das zugrundeliegende Objekt, dem das <strong>Stream</strong> -Objekt zugeordnet ist, übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e99d7-153">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-154"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-154"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-155">Gibt ein <strong>Recordset-Objekt</strong> , dessen Zeilen die Dateien und Unterverzeichnisse in dem durch dieses <strong>Record</strong>dargestellten Verzeichnis darstellen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-155">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-156"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-156"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-157">Gibt den gesamten oder einen Teil des Inhalts eines umfangreichem Text oder Binärdaten <strong>Field</strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e99d7-157">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-158"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-158"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-159">Ruft mehrere Datensätze eines <strong>Recordset</strong>-Objekts in ein Array ab.</span><span class="sxs-lookup"><span data-stu-id="e99d7-159">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-160"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-160"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-161">Gibt das <strong>Recordset</strong>-Objekt als eine Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="e99d7-161">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-163">Lädt den Inhalt einer vorhandenen Datei in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-163">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-164"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-164"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-165">Verschiebt die Position des aktuellen Datensatzes in einem <strong>Recordset</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-165">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst-, MoveLast-, MoveNext- und MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-167">Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt. Mithilfe dieser Funktionen wird dieser Datensatz zum aktuellen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="e99d7-167">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-168"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-168"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-169">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="e99d7-169">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-171">Löscht das aktuelle <strong>Recordset</strong>-Objekt, und gibt das nächste <strong>Recordset</strong> -Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-171">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-172"><a href="open-method-ado-connection.md">Öffnen Sie (ADO-Verbindung)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-172"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-173">Eine Verbindung mit einer Datenquelle wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e99d7-173">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-174"><a href="open-method-ado-record.md">Öffnen Sie (ADO-Datensatz)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-174"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-175">Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-175">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-176"><a href="open-method-ado-recordset.md">Öffnen Sie (ADO-Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-176"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-177">Öffnet einen Cursor.</span><span class="sxs-lookup"><span data-stu-id="e99d7-177">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-178"><a href="open-method-ado-stream.md">Öffnen Sie (ADO-Datenstrom)</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-178"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-179">Öffnet ein <strong>Stream</strong>-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e99d7-179">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-180"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-180"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-181">Datenbank-Schemainformationen werden vom Anbieter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-181">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-182"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-182"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-183">Eine angegebene Anzahl von Bytes aus einem <strong>Stream</strong>-Objekt wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-183">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-184"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-184"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-185">Eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-185">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-186"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-186"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-187">Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.</span><span class="sxs-lookup"><span data-stu-id="e99d7-187">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-188"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-188"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-189">Die Daten in einem <strong>Recordset</strong>-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</span><span class="sxs-lookup"><span data-stu-id="e99d7-189">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-190"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-190"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-191">Die Daten im aktuellen <strong>Recordset</strong>-Objekt oder in der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts werden anhand der zugrunde liegenden Datenbank aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e99d7-191">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-192"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-192"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-193">Speichert das <strong>Recordset</strong>-Objekt in einer Datei oder in einem <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-193">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-194"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-194"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-195">Speichert den binären Inhalt eines <strong>Stream</strong>-Objekts in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="e99d7-195">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-196"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-196"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-197">Durchsucht den Index eines <strong>Recordset</strong>-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.</span><span class="sxs-lookup"><span data-stu-id="e99d7-197">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-198"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-198"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-199">Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-199">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-200"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-200"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-201">Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.</span><span class="sxs-lookup"><span data-stu-id="e99d7-201">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-202"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-202"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-203">Statistische Informationen zu einem geöffneten Datenstrom werden abgerufen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-203">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-204"><a href="supports-method-ado.md">Unterstützt</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-204"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-205">Bestimmt, ob ein angegebenes <strong>Recordset</strong>-Objekt einen bestimmten Funktionalitätstyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-205">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-206"><a href="update-method-ado.md">Update</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-206"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-207">Speichert alle Änderungen, die Sie an der aktuellen Zeile eines <strong>Recordset</strong>-Objekts oder der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vornehmen.</span><span class="sxs-lookup"><span data-stu-id="e99d7-207">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-209">Schreibt alle ausstehenden Batchaktualisierungen auf einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e99d7-209">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e99d7-210"><a href="write-method-ado.md">Schreiben</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-210"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-211">Schreibt Binärdaten in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-211">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e99d7-212"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="e99d7-212"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="e99d7-213">Schreibt eine angegebene Textzeichenfolge in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e99d7-213">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

