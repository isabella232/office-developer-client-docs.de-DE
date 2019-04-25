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
# <a name="recordset-members-dao"></a>Recordset-Elemente (DAO)


**Gilt für**: Access 2013, Office 2013

Ein Recordset-Objekt stellt die Datensätze in einer Basistabelle oder die Datensätze dar, die aus einer Abfrageausführung resultieren.

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
<td><p>Erstellt einen neuen Datensatz für ein aktualisierbares <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Die Ausführung eines ausstehenden asynchronen Methodenaufrufs wird abgebrochen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Bricht alle ausstehenden Updates für ein <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt ab.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Erstellt ein dupliziertes <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt, das auf das ursprüngliche <strong>Recordset</strong>-Objekt verweist.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Close</a></strong></p></td>
<td><p>Schließt ein geöffnetes <strong>Recordset</strong>-Objekt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Gibt ein <strong><a href="querydef-object-dao.md">QueryDef</a></strong>-Objekt zurück, das eine Kopie des <strong>QueryDef</strong>-Objekts darstellt, welches zum Erstellen des <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekts verwendet wurde, das durch den recordset-Platzhalter dargestellt wird (gilt nur für Microsoft Access-Arbeitsbereiche). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>Für dieses Objekt nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Kopiert den aktuellen Datensatz zur weiteren Bearbeitung aus einem aktualisierbaren <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt in den Kopierpuffer.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Füllt den lokalen Cache für ein <strong>Recordset</strong>-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen), teilweise oder vollständig auf.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Sucht den ersten Datensatz in einem <strong>Recordset</strong>-Objekt vom "dynaset"- oder "snapshot"-Typ, der die angegebenen Kriterien erfüllt, und macht den Datensatz zum aktuellen Datensatz (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Ruft mehrere Zeilen aus einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt ab.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Move</a></strong></p></td>
<td><p>Verschiebt die Position des aktuellen Datensatzes in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</p></td>
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
<td><p>Wechselt zum nächsten Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen Datensatz zum aktuellen Datensatz.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Wechselt zum vorherigen Datensatz in einem angegebenen <strong>Recordset</strong>-Objekt und macht diesen Datensatz zum aktuellen Datensatz.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Ruft die nächste Datensatzgruppe ab (falls vorhanden), die von einer mehrteiligen Auswahlabfrage in einem <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> -Aufruf zurückgegeben wurde. Daraufhin wird ein <strong>Boolean</strong>-Wert ausgegeben, der angibt, ob weitere Datensätze ausstehen (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Erstellt ein neues <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt und fügt es an die <strong>Recordsets</strong>-Auflistung an.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Aktualisiert die Daten in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt, indem die Abfrage erneut ausgeführt wird, auf der das Objekt basiert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Sucht den Datensatz in einem indizierten <strong>Recordset</strong>-Objekt vom Typ Tabelle, das den angegebenen Kriterien für den aktuellen Index entspricht, und macht diesen Datensatz zum aktuellen Datensatz (gilt nur für Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Update</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
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
<td><p>Legt die relative Datensatznummer des aktuellen Datensatzes eines <strong>Recordset</strong>-Objekts fest oder gibt den betreffenden Wert zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt die Anzahl der Datensätze zurück, die die letzte Batchaktualisierung nicht ausgeführt haben (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt ein Textmarkenarray zurück, das die Zeilen angibt, die bei der letzten Batchaktualisierung Konflikte verursacht haben (gilt nur für ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Legt die Anzahl der Anweisungen fest, die in jedem Batch an den Server zurückgesendet wurden, oder gibt die betreffende Anzahl zurück (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition in einem <strong>Recordset</strong>-Objekt vor dem ersten Datensatz liegt. Schreibgeschützter <strong>boolescher</strong> Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></p></td>
<td><p>Legt eine Textmarke fest oder gibt sie zurück. Sie identifiziert den aktuellen Datensatz eindeutig in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong>Recordset</strong>-Objekt Textmarken unterstützt, die Sie unter Verwendung der <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>-Eigenschaft festlegen können.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Mit dieser Eigenschaft wird die Anzahl von Datensätzen, die aus einer ODBC-Datenquelle abgerufen und lokal gespeichert werden, festgelegt oder zurückgegeben. <strong>Long</strong> mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>Gibt das <strong><a href="connection-object-dao.md">Connection</a></strong>-Objekt zurück, das der Datenbank entspricht.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der Erstellung einer Basistabelle zurück (nur Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der den Bearbeitungsstatus für den aktuellen Datensatz angibt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob die aktuelle Datensatzposition hinter dem letzten Datensatz in einem <strong>Recordset</strong>-Objekt liegt. Schreibgeschützter <strong>boolescher</strong> Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Gibt eine <strong>Fields</strong> -Auflistung zurück, die alle gespeicherten <strong>Field</strong> -Objekte für das angegebene Objekt enthält. Schreibgeschützt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>Legt einen Wert fest, der feststellt, welche Datensätze in einem nachfolgend geöffneten <strong>Recordset</strong>-Objekt einbezogen werden, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>Zeichenfolge</strong> mit Lese-/Schreibzugriff.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Index</a></strong></p></td>
<td><p>Legt einen Wert fest, der den Namen des aktuellen <strong><a href="index-object-dao.md">Index</a></strong>-Objekts in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt vom Typ "Tabelle" angibt, oder gibt einen solchen Wert zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Gibt eine Textmarke zurück, die den zuletzt hinzugefügten oder geänderten Datensatz angibt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Gibt das Datum und die Uhrzeit der letzten Änderung einer Basistabelle zurück. Schreibgeschützter <strong>Variant</strong>-Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Legt einen Wert fest, der die Art der Sperrung angibt, die beim Bearbeiten wirksam ist, oder gibt diesen zurück.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>Gibt den Namen des angegebenen Objekts zurück. Schreibgeschützte <strong>Zeichenfolge</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Gibt an, ob ein bestimmter Datensatz mithilfe der <strong><a href="recordset-seek-method-dao.md">Seek</a></strong>-Methode oder einer der <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong>-Methoden gefunden wurde (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Legt einen Wert fest, der die ungefähre Position des aktuellen Datensatzes (aktueller Datensatz) im <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt basierend auf einem Prozentwert der Datensätze im <strong>Recordset</strong> angibt, oder gibt diesen Wert zurück.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object. or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object. Read-only <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt einen Wert zurück, der den Aktualisierungsstatus des aktuellen Datensatzes angibt, wenn dieser Teil einer Batchktualisierung ist (nur ODBCDirect-Arbeitsbereiche). Schreibgeschützter <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong> -Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekt die <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> -Methode unterstützt, die die Abfrage, auf der das <strong>Recordset</strong>-Objekt basiert, erneut ausführt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Legt die Sortierreihenfolge von Datensätzen in einem <strong><a href="recordset-object-dao.md">Recordset</a></strong>-Objekt fest oder gibt sie zurück (nur Microsoft Access-Arbeitsbereiche).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
<p>Gibt an, ob ein asynchroner Vorgang (d. h. eine Methode, die mit der <strong>dbRunAsync</strong>-Option aufgerufen wurde) abgeschlossen wurde (nur ODBCDirect-Arbeitsbereiche).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der angibt, ob ein Objekt Transaktionen unterstützt. Schreibgeschützter <strong>boolescher</strong> Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Type</strong></p></td>
<td><p>Die Beschreibung für dieses Element wird in der endgültigen Version von Office 14 angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter <strong>boolescher</strong> Wert.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p><strong>HINWEIS</strong>: ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</p>
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

