---
title: Methoden ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5d5b08478b714a9b70e5cb08daff6e04b8883071
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026379"
---
# <a name="ado-methods"></a>ADO-Methoden

**Betrifft**: Access 2013, Office 2013

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
<td><p>Es wird ein neuer Datensatz für ein aktualisierbares <strong>Recordset</strong>-Objekt erstellt.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Append</a></p></td>
<td><p>Ein Objekt wird einer Auflistung angefügt. Bei einer <strong>Fields</strong>-Auflistung wird möglicherweise ein neues <strong>Field</strong>-Objekt erstellt, bevor es der Auflistung angefügt wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">Methoden "AppendChunk"</a></p></td>
<td><p>Daten werden einem großen <strong>Field</strong>-Text- oder -Binärdatenobjekt oder einem <strong>Parameter</strong>-Objekt angefügt.</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans und RollbackTrans</a></p></td>
<td><p>Die Transaktionsverarbeitung in einem <strong>Connection</strong>-Objekt wird wie folgt verwaltet:
<br/><br/><strong>BeginTrans</strong> - Eine neue Transaktion wird begonnen.<br/><br/>
<strong>CommitTrans</strong> - Alle Änderungen werden gespeichert, und die aktuelle Transaktion wird beendet. Möglicherweise wird auch eine neue Transaktion gestartet.<br/><br/>
<strong>RollbackTrans</strong> – alle Änderungen werden abgebrochen und beendet die aktuelle Transaktion. Möglicherweise wird auch eine neue Transaktion gestartet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Bricht die Ausführung eines ausstehenden asynchronen Methodenaufrufs ab.</p></td>
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
<td><p><a href="clear-method-ado.md">Löschen</a></p></td>
<td><p>Alle <strong>Error</strong> -Objekte werden aus der <strong>Errors</strong> -Auflistung entfernt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objektduplikat wird aus einem vorhandenen <strong>Recordset</strong> -Objekt erstellt. Optional wird angegeben, dass der Klon schreibgeschützt ist.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Ein geöffnetes Objekt und alle abhängigen Objekte werden geschlossen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Vergleicht zwei Textmarken und gibt einen Hinweis zu ihren relativen Werten zurück.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Kopiert die angegebene Anzahl von Zeichen oder Bytes (in Abhängigkeit vom <strong>Type</strong>) von einem <strong>Stream</strong>-Objekt in ein anderes <strong>Stream</strong> -Objekt.</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Erstellt ein neues <strong>Parameter</strong>-Objekt mit den angegebenen Eigenschaften.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (ADO-Parameters-Auflistung)</a></p></td>
<td><p>Ein Objekt wird aus der <strong>Parameters</strong>-Auflistung gelöscht.</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Löschen Sie (ADO-Fields-Auflistung)</a></p></td>
<td><p>Ein Objekt wird aus der <strong>Fields</strong>-Auflistung gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (ADO-Recordset)</a></p></td>
<td><p>Löscht den aktuellen Datensatz oder eine Gruppe von Datensätzen.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Führen Sie aus (ADO-Befehl)</a></p></td>
<td><p>Es wird die Abfrage, SQL-Anweisung oder gespeicherte Prozedur ausgeführt, die in der <strong>CommandText</strong>-Eigenschaft angegeben ist.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Führen Sie aus (ADO-Verbindung)</a></p></td>
<td><p>Die angegebene Abfrage, SQL-Anweisung, gespeicherte Prozedur oder der angegebene anbieterspezifische Text wird ausgeführt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Ein <strong>Recordset</strong>-Objekt wird nach der Zeile durchsucht, die den angegebenen Kriterien entspricht.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Leeren</a></p></td>
<td><p>Erzwingt, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts an das zugrundeliegende Objekt, dem das <strong>Stream</strong> -Objekt zugeordnet ist, übergeben wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Gibt ein <strong>Recordset-Objekt</strong> , dessen Zeilen die Dateien und Unterverzeichnisse in dem durch dieses <strong>Record</strong>dargestellten Verzeichnis darstellen.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Gibt den gesamten oder einen Teil des Inhalts eines umfangreichem Text oder Binärdaten <strong>Field</strong> -Objekts.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Ruft mehrere Datensätze eines <strong>Recordset</strong>-Objekts in ein Array ab.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Gibt das <strong>Recordset</strong>-Objekt als eine Zeichenfolge zurück.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Lädt den Inhalt einer vorhandenen Datei in ein <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Verschiebt die Position des aktuellen Datensatzes in einem <strong>Recordset</strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst-, MoveLast-, MoveNext- und MovePrevious</a></p></td>
<td><p>Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt. Mithilfe dieser Funktionen wird dieser Datensatz zum aktuellen Datensatz.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Löscht das aktuelle <strong>Recordset</strong>-Objekt, und gibt das nächste <strong>Recordset</strong> -Objekt zurück, indem sie durch eine Reihe von Befehlen wechselt.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Öffnen Sie (ADO-Verbindung)</a></p></td>
<td><p>Eine Verbindung mit einer Datenquelle wird geöffnet.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Öffnen Sie (ADO-Datensatz)</a></p></td>
<td><p>Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Öffnen Sie (ADO-Recordset)</a></p></td>
<td><p>Öffnet einen Cursor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Öffnen Sie (ADO-Datenstrom)</a></p></td>
<td><p>Öffnet ein <strong>Stream</strong>-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Datenbank-Schemainformationen werden vom Anbieter abgerufen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Eine angegebene Anzahl von Bytes aus einem <strong>Stream</strong>-Objekt wird abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
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
<td><p>Speichert das <strong>Recordset</strong>-Objekt in einer Datei oder in einem <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Speichert den binären Inhalt eines <strong>Stream</strong>-Objekts in eine Datei.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Durchsucht den Index eines <strong>Recordset</strong>-Objekt, um auf schnelle Weise die Zeile zu finden, die den angegebenen Werten entspricht, und ändert die aktuelle Zeilenposition auf diese Zeile.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Überspringt beim Lesen eine Textdatenstroms eine gesamte Zeile.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Statistische Informationen zu einem geöffneten Datenstrom werden abgerufen.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Unterstützt</a></p></td>
<td><p>Bestimmt, ob ein angegebenes <strong>Recordset</strong>-Objekt einen bestimmten Funktionalitätstyp unterstützt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Speichert alle Änderungen, die Sie an der aktuellen Zeile eines <strong>Recordset</strong>-Objekts oder der <strong>Fields</strong>-Auflistung eines <strong>Record</strong>-Objekts vornehmen.</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Schreibt alle ausstehenden Batchaktualisierungen auf einen Datenträger.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a>-Ereignis</p></td>
<td><p>Schreibt Binärdaten in ein <strong>Stream</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Schreibt eine angegebene Textzeichenfolge in ein <strong>Stream</strong>-Objekt.</p></td>
</tr>
</tbody>
</table>

<br/>