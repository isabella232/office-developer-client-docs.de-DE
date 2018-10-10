---
title: Microsoft OLE DB-Anbieter für ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 168799b517598211ca9de680730490a0a41d1dde
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476021"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB-Anbieter für ODBC

**Betrifft**: Access 2013 | Office 2013

Unter idealen Bedingungen für einen ADO- oder RDS-Programmierer wäre für jede Datenquelle eine OLE DB-Schnittstelle verfügbar, sodass ADO Aufrufe direkt in der Datenquelle ausführen könnte. Obwohl Datenbankanbieter zunehmend OLE DB-Schnittstellen implementieren, sind einige Datenquellen noch nicht auf diese Weise verfügbar. Dennoch kann auf praktisch alle heutigen DBMS-Systeme über ODBC zugegriffen werden.

ODBC-Treiber sind für alle größeren DBMS-Systeme von heute verfügbar, so auch für Microsoft SQL Server, Microsoft Access (Microsoft Jet-Datenbankmodul) und Microsoft FoxPro sowie für Datenbankprodukte, die nicht von Microsoft stammen, wie z. B. Oracle.

Mithilfe des Microsoft ODBC-Anbieters kann ADO jedoch eine Verbindung mit einer ODBC-Datenquelle herstellen. Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.

Der Anbieter unterstützt Transaktionen, wenngleich unterschiedliche DBMS-Module Transaktionen auf unterschiedliche Art unterstützen. So unterstützt Microsoft Access beispielsweise bis zu fünf Ebenen tief geschachtelte Transaktionen.

Hierbei handelt es sich um den Standardanbieter für ADO. Alle vom Anbieter abhängigen ADO-Eigenschaften und -Methoden werden unterstützt.

## <a name="connection-string-parameters"></a>Verbindungszeichenfolgen-Parameter

Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:

```sql 
 
MSDASQL 
```

Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.

## <a name="typical-connection-string"></a>Typische Verbindungszeichenfolge

Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Schlüsselwort</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>Gibt den OLE DB-Anbieter für ODBC an.</p></td>
</tr>
<tr class="even">
<td><p><strong>DSN</strong></p></td>
<td><p>Gibt den Namen der Datenquelle an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UID</strong></p></td>
<td><p>Gibt den Benutzernamen an.</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>Gibt das Benutzerkennwort an.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL</strong></p></td>
<td><p>Gibt die URL einer Datei oder eines Verzeichnisses an, die oder das in einem Webordner veröffentlicht ist.</p></td>
</tr>
</tbody>
</table>


Da es sich hierbei um den Standardanbieter für ADO handelt, versucht ADO eine Verbindung mit diesem Anbieter herzustellen, wenn Sie den **Provider=** -Parameter in der Verbindungsreihenfolge nicht angeben.

Der Anbieter unterstützt neben den von ADO definierten keine bestimmten Verbindungsparameter. Der Anbieter übergibt jedoch alle Verbindungsparameter, die nicht von ADO stammen, an den ODBC-Treibermanager.

Da Sie den **Provider**-Parameter nicht angeben müssen, können Sie eine ADO-Verbindungszeichenfolge erstellen, die mit einer ODBC-Verbindungszeichenfolge für dieselbe Datenquelle identisch ist. Verwenden Sie dieselben Parameternamen (**DRIVER=**, **DATABASE=**, **DSN=** usw.) und Werte und dieselbe Syntax wie beim Erstellen einer ODBC-Verbindungszeichenfolge. Sie können eine Verbindung mit oder ohne vordefinierten Datenquellennamen (DSN) oder Datei-DSN herstellen.

**Syntax mit einem DSN oder Datei-DSN:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Syntax ohne einen DSN (Verbindung ohne DSN):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Wenn Sie einen DSN oder Datei-DSN verwenden, muss dieser über den ODBC-Datenquellenadministrator in der Windows-Systemsteuerung definiert werden. Bei Microsoft Windows 2000 befindet sich ODBC Administrator unter Verwaltung. Bei früheren Versionen von Windows heißt das Symbol für ODBC Administrator 32-Bit-ODBC oder einfach ODBC.

Alternativ zum Festlegen eines **DSN** können Sie auch den ODBC-Treiber (**DRIVER=**), wie z. B. "SQL Server", den Servernamen (**SERVER=**) und den Datenbanknamen (**DATABASE=**) angeben.

Sie können auch den Namen (**UID=**) und das Kennwort für ein Benutzerkonto (**PWD=**) in den ODBC-spezifischen Parametern oder in den von ADO definierten Standardparametern *user* und *password* angeben.

Obwohl die Definition eines **DSN** bereits eine Datenbank angibt, können Sie * *ein* Datenbankparameter neben einen **DSN** -Verbindung mit einer anderen Datenbank* angeben. Es ist ratsam, immer *dem* Parameter *Database* einschließen aus, wenn Sie einen **DSN**verwenden. Dadurch wird sichergestellt, dass Sie auf die gewünschte Datenbank verbinden, wenn ein anderer Benutzer den Datenbank Standardparameter geändert, seit Sie zuletzt die **DSN** -Definition geprüft.

## <a name="provider-specific-connection-properties"></a>Anbieterspezifische Verbindungseigenschaften

Der OLE DB-Anbieter für ODBC fügt der [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts verschiedene Eigenschaften hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaftenname</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Zugänglich Prozeduren<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Gibt an, ob der Benutzer Zugriff auf gespeicherte Prozeduren hat.</p></td>
</tr>
<tr class="even">
<td><p>Zugänglich Tabellen<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Gibt an, ob der Benutzer über die Berechtigung zum Ausführen der SELECT-Anweisungen in Datenbanktabellen verfügt.</p></td>
</tr>
<tr class="odd">
<td><p>Active-Anweisungen<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Gibt die Anzahl von Handles an, die ein ODBC-Treiber in einer Verbindung unterstützen kann.</p></td>
</tr>
<tr class="even">
<td><p>Treibername<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Gibt den Dateinamen des ODBC-Treibers an.</p></td>
</tr>
<tr class="odd">
<td><p>ODBC-Treiberversion<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Gibt die Version von ODBC an, die von diesem Treiber unterstützt wird.</p></td>
</tr>
<tr class="even">
<td><p>Verwendung der Datei<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Gibt an, wie der Treiber eine Datei in einer Datenquelle behandelt: als Tabelle oder als Katalog.</p></td>
</tr>
<tr class="odd">
<td><p>Wie Escape-Klausel<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Gibt an, ob der Treiber die Definition und Verwendung eines Escapezeichens für das Prozentzeichen (%) und das Unterstrichzeichen (_) im LIKE-Prädikat einer WHERE-Klausel unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>Maximale Anzahl von Spalten in Gruppen von<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Gibt die maximale Anzahl von Spalten an, die in der GROUP BY-Klausel einer SELECT-Anweisung enthalten sein darf.</p></td>
</tr>
<tr class="odd">
<td><p>Maximale Anzahl von Spalten im Index<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Gibt die maximale Anzahl von Spalten an, die in einem Index enthalten sein darf.</p></td>
</tr>
<tr class="even">
<td><p>Maximale Anzahl von Spalten in der Order By-<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Gibt die maximale Anzahl von Spalten an, die in der ORDER BY-Klausel einer SELECT-Anweisung enthalten sein darf.</p></td>
</tr>
<tr class="odd">
<td><p>Maximale Anzahl von Spalten in auswählen<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Gibt die maximale Anzahl von Spalten an, die im SELECT-Teil einer SELECT-Anweisung enthalten sein darf.</p></td>
</tr>
<tr class="even">
<td><p>Maximale Anzahl von Spalten in einer Tabelle<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Gibt die maximale Anzahl von Spalten an, die in einer Tabelle zulässig sind.</p></td>
</tr>
<tr class="odd">
<td><p>Numerische Funktionen<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Gibt an, welche numerischen Funktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Outer Join-Funktionen<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Gibt die vom Anbieter unterstützten OUTER JOIN-Typen an.</p></td>
</tr>
<tr class="odd">
<td><p>Äußere Verknüpfungen<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Gibt an, ob der Anbieter OUTER JOIN-Typen unterstützt.</p></td>
</tr>
<tr class="even">
<td><p>Sonderzeichen<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Gibt an, welche Zeichen eine besondere Bedeutung für den ODBC-Treiber haben.</p></td>
</tr>
<tr class="odd">
<td><p>Gespeicherte Prozeduren<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Gibt an, ob gespeicherte Prozeduren für die Verwendung mit diesem ODBC-Treiber verfügbar sind.</p></td>
</tr>
<tr class="even">
<td><p>Zeichenfolgenfunktionen<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Gibt an, welche Zeichenfolgenfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Systemfunktionen<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Gibt an, welche Systemfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</p></td>
</tr>
<tr class="even">
<td><p>/ Datumsfunktionen<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Gibt an, welche Uhrzeit- und Datumsfunktionen vom ODBC-Treiber unterstützt werden. Eine Liste mit Funktionsnamen und den zugehörigen Werten, die in dieser Bitmaske verwendet werden, finden Sie in Appendix E: Scalar Functions in der Dokumentation zu ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Unterstützung für SQL-Grammatik<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Gibt die SQL-Grammatik an, die von diesem ODBC-Treiber unterstützt wird.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Anwenderspezifische Recordset- und Command-Eigenschaften

Der OLE DB-Anbieter für ODBC fügt der **Properties** -Auflistung der Objekte **Recordset** und **Command** verschiedene Objekte hinzu. In der folgenden Liste sind diese Eigenschaften mit dem entsprechenden OLE DB-Eigenschaftennamen aufgeführt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaftenname</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Abfragebasierte Updates/löschen/fügt<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Gibt an, ob Aktualisierungen und Lösch- und Einfügevorgänge mithilfe von SQL-Abfragen ausgeführt werden können.</p></td>
</tr>
<tr class="even">
<td><p>ODBC-Parallelität-Typ<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Gibt die Methode an, die verwendet wird, um potenzielle Probleme zu reduzieren, die von zwei Benutzern verursacht werden, die gleichzeitig auf dieselben Daten in der Datenquelle zugreifen möchten.</p></td>
</tr>
<tr class="odd">
<td><p>BLOB-Eingabehilfen auf Vorwärtscursor<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Gibt an, ob auf BLOB-<strong>Felder</strong> zugegriffen werden kann, wenn ein Vorwärtscursor verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>SQL_FLOAT, SQL_DOUBLE und SQL_REAL in QBU WHERE-Klausel einschließen<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Gibt an, ob die Werte SQL_FLOAT, SQL_DOUBLE und SQL_REAL in eine QBU WHERE-Klausel eingefügt werden können.</p></td>
</tr>
<tr class="odd">
<td><p>Position in der letzten Zeile nach dem Einfügen<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Gibt an, dass nach dem Einfügen eines neuen Datensatzes in eine Tabelle die letzte Zeile zur aktuellen Zeile wird.</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Gibt an, ob die <strong>IRowsetChange</strong>-Schnittstelle erweiterte Informationsunterstützung bietet.</p></td>
</tr>
<tr class="odd">
<td><p>ODBC-Cursor-Typ<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Gibt den Cursortyp an, der vom <strong>Recordset</strong>-Objekt verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>Generieren eines Rowsets, die gemarshallt werden kann.<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Gibt an, dass der ODBC-Treiber eine Datensatzgruppe generiert, die gemarshallt werden kann.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Befehlstext

Die Verwendung des [Command](command-object-ado.md)-Objekts hängt zum großen Teil von der Datenquelle sowie vom Typ der Abfrage- oder Befehlsanweisung, die akzeptiert wird, ab.

ODBC stellt eine bestimmte Syntax zum Aufrufen von gespeicherten Prozeduren bereit. Für die [CommandText](commandtext-property-ado.md) -Eigenschaft des **Command** -Objekts, das *CommandText* -Argument der **Execute** -Methode für ein [Connection](connection-object-ado.md) -Objekt oder das Argument *Source* an die **Open** -Methode für ein [Recordset-Objekt](recordset-object-ado.md) -Objekt übergibt eine Zeichenfolge mit der folgenden Syntax:

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

Jedes Fragezeichen (**?**) verweist auf ein Objekt in der [Parameters](parameters-collection-ado.md)-Auflistung. Das erste Fragezeichen (**?**) verweist auf **Parameters**(0), das nächste Fragezeichen (**?**) auf **Parameters**(1) usw.

Die Parameterverweise sind optional und hängen von der Struktur der gespeicherten Prozedur ab. Wenn Sie eine gespeicherte Prozedur aufrufen möchten, die keine Parameter definiert, sieht die Zeichenfolge wie folgt aus:

`"{ call procedure }"`

Wenn zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:

`"{ call procedure ( ?, ? ) }"`

Wenn die gespeicherte Prozedur einen Wert zurückgibt, wird der Rückgabewert wie ein weiterer Parameter verwendet. Wenn keine Abfrageparameter verwendet werden, aber ein Rückgabewert vorliegt, sieht die Zeichenfolge wie folgt aus:

`"{ ? = call procedure }"`

Wenn ein Rückgabewert und zwei Abfrageparameter verwendet werden, sieht die Zeichenfolge wie folgt aus:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Recordset-Verhalten

In den folgenden Tabellen sind die für ein mit diesem Anbieter geöffnetes **Recordset** -Objekt verfügbaren ADO-Standardmethoden und -Eigenschaften aufgeführt.

Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die **Properties** -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.

Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaft</p></th>
<th><p>ForwardOnly.</p></th>
<th><p>Dynamic</p></th>
<th><p>Keyset</p></th>
<th><p>Static</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>nicht verfügbar</p></td>
<td><p>nicht verfügbar</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>nicht verfügbar</p></td>
<td><p>nicht verfügbar</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>nicht verfügbar</p></td>
<td><p>nicht verfügbar</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>nicht verfügbar</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>nicht verfügbar</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
<td><p>nur Lesen</p></td>
</tr>
</tbody>
</table>


Die Eigenschaften [AbsolutePosition](absoluteposition-property-ado.md) und [AbsolutePage](absolutepage-property-ado.md) sind schreibgeschützt, wenn ADO mit der Version 1.0 des Microsoft OLE DB-Anbieters für ODBC verwendet wird.

Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>ForwardOnly.</p></th>
<th><p>Dynamic</p></th>
<th><p>Keyset</p></th>
<th><p>Static</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Nein</p></td>
<td><p>Nein</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Nein</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Nein</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a>*</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Nein</p></td>
<td><p>Nein</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Unterstützt</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
<td><p>Ja</p></td>
</tr>
</tbody>
</table>


\*Nicht unterstützt bei Microsoft Access-Datenbanken.

## <a name="dynamic-properties"></a>Dynamische Eigenschaften

Der Microsoft OLE DB-Anbieter für ODBC fügt verschiedene Eigenschaften in die **Properties** -Auflistung der nicht geöffneten Objekte [Connection](connection-object-ado.md), [Recordset](recordset-object-ado.md) und [Command](command-object-ado.md) ein.

Bei den folgenden Tabellen handelt es sich um ein Cross-Index-System der ADO- und OLE DB-Namen für alle dynamischen Eigenschaften. In OLE DB Programmer's Reference wird ein ADO-Eigenschaftenname als "Description" bezeichnet. Weitere Informationen zu diesen Eigenschaften finden Sie in OLE DB Programmer's Reference. Suchen Sie im Index nach dem OLE DB-Eigenschaftennamen, oder lesen Sie Appendix C: OLE DB Properties.

## <a name="connection-dynamic-properties"></a>Dynamische Eigenschaften von "Connection"

Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Connection** -Objekts hinzugefügt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO-Eigenschaftenname</p></th>
<th><p>OLE DB-Eigenschaftenname</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Active Sessions</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Autocommit Isolation Levels</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Catalog Location</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Catalog Term</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Column Definition</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Connect Timeout</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Current Catalog</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Data Source</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Data Source Name</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Data Source Object Threading Model</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>DBMS Name</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>DBMS Version</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Extended Properties</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>GROUP BY Support</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Heterogeneous Table Support</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Identifier Case Sensitivity</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Initial Catalog</p></td>
<td><p>NULL</p></td>
</tr>
<tr class="even">
<td><p>Isolation Levels</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Isolation Retention</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Locale Identifier</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>Location</p></td>
<td><p>STANDARD</p></td>
</tr>
<tr class="even">
<td><p>Maximum Index Size</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Row Size</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Maximum Row Size Includes BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Tables in SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Mode</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Parameter Sets</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Multiple Results</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Multiple Storage Objects</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Multi-Table Update</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>NULL Collation Order</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behavior</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>OLE DB Services</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>OLE DB Version</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>OLE Object Support</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Open Rowset Support</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Output Parameter Availability</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Persist Security Info</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Persistent ID Type</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Prepare Abort Behavior</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Prepare Commit Behavior</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Procedure Term</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Provider Friendly Name</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Provider Name</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Provider Version</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only Data Source</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Conversions on Command</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Schema Term</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Schema Usage</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Support</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Structured Storage</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Subquery Support</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Table Term</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Transaction DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>User ID</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>User Name</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
<td><p>Window Handle</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Dynamische Eigenschaften von "Recordset"

Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Recordset** -Objekts hinzugefügt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO-Eigenschaftenname</p></th>
<th><p>OLE DB-Eigenschaftenname</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Unique Rows</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Dynamische Eigenschaften von "Command"

Die folgenden Eigenschaften werden der **Properties** -Auflistung des **Command** -Objekts hinzugefügt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>ADO-Eigenschaftenname</p></th>
<th><p>OLE DB-Eigenschaftenname</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Access Order</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Blocking Storage Objects</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Bookmark Type</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Change Inserted Rows</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Column Privileges</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Column Set Notification</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Delay Storage Object Updates</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Hold Rows</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Literal Bookmarks</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Literal Row Identity</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Maximum Open Rows</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Maximum Pending Rows</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Maximum Rows</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Notification Granularity</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Notification Phases</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Own Changes Visible</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Own Inserts Visible</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Preserve on Abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Preserve on Commit</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Quick Restart</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Reentrant Events</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Remove Deleted Rows</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Report Multiple Changes</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Return Pending Inserts</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Row Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Row First Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Row Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Privileges</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Row Resynchronization Notification</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Row Threading Model</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Row Undo Delete Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Row Undo Insert Notification</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Row Update Notification</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Release Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Scroll Backwards</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Skip Deleted Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Strong Row Identity</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Use Bookmarks</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

Weitere Informationen zur Implementierung und funktionale Informationen zu den Microsoft OLE DB-Anbieter für ODBC wenden Sie sich an dem [OLE DB Programmer's Guide](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) oder besuchen Sie das [Data Plattform Developer Center](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

