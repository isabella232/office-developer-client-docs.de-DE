---
title: Recordset-Member (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ab0a04fd7282c983bd200a16108babf5e40d240c
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026309"
---
# <a name="recordset-members-dao"></a>Recordset-Member (DAO)


**Betrifft**: Access 2013, Office 2013

Ein Recordset -Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrageausführung resultieren.

## <a name="methods"></a>Methoden

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>Erstellt einen neuen Datensatz für ein aktualisierbares <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Abbrechen</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Alle ausstehenden Aktualisierungen für ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt werden abgebrochen.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Erstellt ein dupliziertes <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt, das auf das ursprüngliche <strong>Recordset</strong> -Objekt verweist.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Schließen Sie</a></strong></p></td>
<td><p>Schließt ein geöffnetes <strong>Recordset</strong> -Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Gibt ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong> -Objekt, das eine Kopie des <strong>QueryDef-Objekt</strong> ist verwendeten zum Erstellen des <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts, dargestellt durch das Recordset-Objekt-Platzhalter (nur Microsoft Access-Arbeitsbereiche). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Löschen</a></strong></p></td>
<td><p>Wird für dieses Objekt nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Kopiert den aktuellen Datensatz aus einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt zur nachfolgenden Bearbeitung in den Kopierpuffer.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Füllt den lokalen Cache für ein <strong>Recordset</strong>-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält, teilweise oder vollständig auf (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Sucht den ersten Datensatz in einem <strong>Recordset</strong> -Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Sucht den letzten Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> vom Typ Dynaset oder Snapshot-Objekt, die den angegebenen Kriterien entspricht, und macht, die den Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Sucht den nächsten Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ Dynaset oder Snapshot, der den angegebenen Kriterien entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Sucht den vorherigen Datensatz in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ "Dynaset" oder "Snapshot", der die angegebenen Kriterien erfüllt, und macht diesen Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Ruft mehrere Zeilen aus einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt ab.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Move</a></strong></p></td>
<td><p>Verschiebt die Position des aktuellen Datensatzes in ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>Wechselt zum ersten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Wechselt zum letzten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Wechselt zum nächsten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Wechselt zum vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen zum aktuellen Datensatz.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Ruft die nächste Datensatzgruppe ab (falls vorhanden), die von einer mehrteiligen Auswahlabfrage in einem <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> -Aufruf zurückgegeben wurde. Daraufhin wird ein <strong>Boolean</strong>-Wert ausgegeben, der angibt, ob weitere Datensätze ausstehen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Die Daten in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt werden aktualisiert durch erneutes Ausführen der Abfrage, auf der das Objekt basiert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Sucht den Datensatz in einem indizierten <strong>Recordset</strong> -Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Aktualisieren</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Speichert den Inhalt des Kopierpuffers in einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Eigenschaften

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p>Legt die relative Datensatznummer des aktuellen Datensatzes eines <strong>Recordset</strong> -Objekts fest oder gibt den betreffenden Wert zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt die Anzahl von Datensätzen zurück, bei denen die letzte Batchaktualisierung nicht abgeschlossen wurde (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt ein Textmarkenarray zurück, das die Zeilen angibt, die bei der letzten Batchaktualisierung Konflikte verursacht haben (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Mit dieser Eigenschaft wird die Anzahl von Anweisungen festgelegt oder zurückgegeben, die in jedem Batch an den Server zurückgesendet werden (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem <strong>Recordset</strong> -Objekt vor dem ersten Datensatz liegt. Schreibgeschützter <strong>Boolean</strong> -Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Lesezeichen</a></strong></p></td>
<td><p>Legt eine Textmarke fest oder gibt sie zurück. Sie identifiziert den aktuellen Datensatz eindeutig in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong>Recordset</strong>-Objekt Textmarken unterstützt, die Sie mithilfe der <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> -Eigenschaft festlegen können.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Legt die Anzahl der von einer ODBC-Datenquelle abgefragten Datensätze fest, die lokal zwischengespeichert werden, oder gibt den betreffenden Wert zurück. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die Textmarke des ersten Datensatzes in einem Recordset -Objekt vom Typ Dynaset angibt, das lokal zwischenzuspeichernde Daten aus einer ODBC-Datenquelle enthält (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Verbindung</a></strong></p></td>
<td><p>Gibt das <strong><a href="connection-object-dao.md">Connection</a></strong> -Objekt zurück, das sich auf die Datenbank bezieht.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der Erstellung einer Basistabelle zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Status der Bearbeitung für den aktuellen Datensatz angibt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem <strong>Recordset</strong>-Objekt liegt. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Felder</a></strong></p></td>
<td><p>Gibt eine <strong>Fields</strong>-Auflistung zurück, die alle gespeicherten <strong>Field</strong>-Objekte für das angegebene Objekt enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>Legt einen Wert fest, der die in einem nachfolgend geöffneten <strong>Recordset</strong> -Objekt enthaltenen Datensätze bestimmt, oder gibt diesen Wert zurück (nur Microsoft Access-Arbeitsbereich). Lese-/Schreibzugriff <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Index</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Namen des aktuellen <strong><a href="index-object-dao.md">Index</a></strong> -Objekts in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Gibt ein Lesezeichen zurück, das den zuletzt hinzugefügten oder geänderten Datensatz angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der letzten Änderung einer Basistabelle zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Typ der Sperreangibt, die während der Bearbeitung wirksam ist, oder gibt diesen Wert zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück. Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Gibt an, ob ein bestimmter Datensatz mithilfe der <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> -Methode oder einer der <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> -Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt basierend auf einem Prozentwert der Datensätze im <strong>Recordset</strong> angibt, oder gibt diesen Wert zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Eigenschaften</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Gibt die Anzahl der Datensätze zurück, auf die in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt zugegriffen wird, oder die Gesamtzahl der Datensätze in einem <strong>Recordset</strong> -Objekt vom "table"-Typ oder in einem <strong><a href="tabledef-object-dao.md">TableDef</a></strong> -Objekt zurück. Schreibgeschütztes <strong>Long</strong> -Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt einen Wert zurück, der den Aktualisierungsstatus des aktuellen Datensatzes angibt, wenn dieser Teil einer Batchktualisierung ist (nur ODBCDirect-Arbeitsbereiche). Schreibgeschützter <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> -Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt die <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> -Methode unterstützt, die die Abfrage, auf der das <strong>Recordset</strong>-Objekt basiert, erneut ausführt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Legt die Sortierreihenfolge für Datensätze in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <strong>dbRunAsync</strong>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transaktionen</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Typ</strong></p></td>
<td><p>Die Beschreibung dieses Elements finden Sie in der endgültigen Version von Office 2010.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>Boolean</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p><strong>Hinweis</strong>: für ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Legt einen Wert fest, der angibt, wie die WHERE-Klausel für jeden Datensatz während einer Batchaktualisierung erstellt wird, und ob die Batchaktualisierung eine UPDATE- oder eine DELETE-Anweisung gefolgt von einer INSERT-Anweisung verwenden soll, oder gibt den betreffenden Wert zurück (nur ODBCDirect-Arbeitsbereiche). <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong> -Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Text der Meldung festlegt, der von Ihrer Anwendung angezeigt wird, wenn der Wert eines <strong>Field</strong>-Objekts nicht der von der <strong>ValidationRule</strong>-Eigenschaft festgelegten Gültigkeitsregel entspricht, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>String</strong>-Wert.</p></td>
</tr>
</tbody>
</table>

