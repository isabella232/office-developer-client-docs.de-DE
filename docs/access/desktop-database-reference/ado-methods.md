---
title: ActiveX Data Objects (ADO)-Methoden
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 94d7fcdbbbe442bfd7218d70e20b7d306f3f2e01
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559290"
---
# <a name="ado-methods"></a>ADO-Methoden

**Gilt für**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Methode</th>
<th>Beschreibung</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Ein neuer Datensatz für ein aktualisierbares <strong>Recordset</strong>-Objekt wird erstellt.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Ein Objekt wird einer Auflistung angefügt. Bei einer <strong>Fields</strong>-Auflistung wird möglicherweise ein neues <strong>Field</strong>-Objekt erstellt, bevor es der Auflistung angefügt wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Daten werden einem großen <strong>Field</strong>-Text- oder -Binärdatenobjekt oder einem <strong>Parameter</strong>-Objekt angefügt.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">"BeginTrans", "CommitTrans" und "RollbackTrans"</a></p></td>
<td><p>Die Transaktionsverarbeitung in einem <strong>Connection</strong>-Objekt wird wie folgt verwaltet:<br/><br/><strong>BeginTrans</strong> - Eine neue Transaktion wird begonnen.<br/><br/>
<strong>CommitTrans</strong> - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.<br/><br/>
<strong>RollbackTrans</strong> - Bricht alle Änderungen ab und beendet die aktuelle Transaktion. Möglicherweise wird auch eine neue Transaktion gestartet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Eine ausstehende Batchaktualisierung wird abgebrochen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Alle an der aktuellen oder neuen Zeile eines <strong>Recordset</strong>-Objekts oder der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vorgenommenen Änderungen werden abgebrochen, bevor die <strong>Update</strong>-Methode aufgerufen wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Alle <strong>Error</strong>-Objekte werden aus der <strong>Errors</strong>-Auflistung entfernt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objektduplikat wird aus einem vorhandenen <strong>Recordset</strong> -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Schließen</a></p></td>
<td><p>Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Zwei Textmarken werden verglichen, und die relativen Werte werden zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Die angegebene Anzahl von Zeichen oder Bytes (abhängig vom <strong>Typ</strong>) im <strong>Datenstrom</strong> wird in ein anderes <strong>Stream</strong>-Objekt kopiert.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">Createparameter</a></p></td>
<td><p>Ein neues <strong>Parameter</strong>-Objekt mit den angegebenen Eigenschaften wird erstellt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (Parameters-Auflistung in ADO)</a></p></td>
<td><p>Ein Objekt wird aus der <strong>Parameters</strong>-Auflistung gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Delete (Fields-Auflistung in ADO)</a></p></td>
<td><p>Ein Objekt wird aus der <strong>Fields</strong>-Auflistung gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (ADO-Recordset)</a></p></td>
<td><p>Der aktuelle Datensatz oder eine Gruppe von Datensätzen wird gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO-Befehl)</a></p></td>
<td><p>Es wird die Abfrage, SQL-Anweisung oder gespeicherte Prozedur ausgeführt, die in der <strong>CommandText</strong>-Eigenschaft angegeben ist.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO-Verbindung)</a></p></td>
<td><p>Die angegebene Abfrage, SQL-Anweisung, gespeicherte Prozedur oder der angegebene anbieterspezifische Text wird ausgeführt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Suchen</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objekt wird nach der Zeile durchsucht, die den angegebenen Kriterien entspricht.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Flush</a></p></td>
<td><p>Es wird erzwungen, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts in das zugrunde liegende Objekt übernommen wird, das dem <strong>Stream</strong>-Objekt zugeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objekt wird zurückgegeben, dessen Zeilen die Daten und Unterverzeichnisse in dem durch dieses <strong>Record</strong>-Objekt dargestellten Verzeichnis darstellen.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Der gesamte Inhalt oder ein Teil des Inhalts eines großen <strong>Field</strong>-Text- oder -Binärdatenobjekts wird zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Mehrere Datensätze eines <strong>Recordset</strong>-Objekts werden in ein Array abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">Getstring</a></p></td>
<td><p>Das <strong>Recordset</strong>-Objekt wird als Zeichenfolge zurückgegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Der Inhalt einer vorhandenen Datei wird in ein <strong>Stream</strong>-Objekt geladen.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Die Position des aktuellen Datensatzes in einem <strong>Recordset</strong>-Objekt wird verschoben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">"MoveFirst", "MoveLast", "MoveNext" und "MovePrevious"</a></p></td>
<td><p>Es wird zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt gewechselt, und dieser Datensatz wird zum aktuellen Datensatz gemacht.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Der Inhalt des aktuellen <strong>Recordset</strong>-Objekts wird gelöscht, und das nächste <strong>Recordset</strong>-Objekt wird durch eine Reihe von Befehlen zurückgegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (ADO-Verbindung)</a></p></td>
<td><p>Eine Verbindung mit einer Datenquelle wird geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (ADO-Record)</a></p></td>
<td><p>Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (ADO-Recordset)</a></p></td>
<td><p>Ein Cursor wird geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (ADO-Stream)</a></p></td>
<td><p>Ein <strong>Stream</strong>-Objekt zum Ändern von Datenströmen von Binär- oder Textdaten wird geöffnet.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Datenbank-Schemainformationen werden vom Anbieter abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Lesen</a></p></td>
<td><p>Eine angegebene Anzahl von Bytes aus einem <strong>Stream</strong>-Objekt wird abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">Readtext</a></p></td>
<td><p>Eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt wird abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Die Objekte in einer Auflistung werden aktualisiert, um Objekte widerzuspiegeln, die vom Anbieter verfügbar sind und spezifisch für diesen sind.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Die Daten in einem <strong>Recordset</strong>-Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Die Daten im aktuellen <strong>Recordset</strong>-Objekt oder in der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts werden anhand der zugrunde liegenden Datenbank aktualisiert.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Das <strong>Recordset</strong>-Objekt wird in einer Datei oder in einem <strong>Stream</strong>-Objekt gespeichert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Der Binärinhalt eines <strong>Stream</strong>-Objekts wird in einer Datei gespeichert.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Der Index eines <strong>Recordset</strong>-Objekts wird durchsucht, um schnell die Zeile zu finden, die mit den angegebenen Werten übereinstimmt, und die aktuelle Zeilenposition wird in diese Zeile geändert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Die Position, die das Ende des Datenstroms darstellt, wird festgelegt.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Beim Lesen eines Textdatenstroms wird eine gesamte Zeile übersprungen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Statistische Informationen zu einem geöffneten Datenstrom werden abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Unterstützt</a></p></td>
<td><p>Es wird bestimmt, ob ein bestimmter Funktionalitätstyp von einem angegebenen <strong>Recordset</strong>-Objekt unterstützt wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Alle Änderungen, die Sie an der aktuellen Zeile eines <strong>Recordset</strong>-Objekts oder an der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vornehmen, werden gespeichert.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Alle ausstehenden Batchaktualisierungen werden auf den Datenträger geschrieben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Binärdaten werden in ein <strong>Stream</strong>-Objekt geschrieben.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">Writetext</a></p></td>
<td><p>Eine angegebene Textzeichenfolge wird in ein <strong>Stream</strong>-Objekt geschrieben.</p></td>
</tr>
</tbody>
</table>

<br/>
