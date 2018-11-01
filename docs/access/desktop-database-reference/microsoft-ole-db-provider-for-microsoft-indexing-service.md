---
title: Microsoft OLE DB-Anbieter für Microsoft Indexdienst
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ac8225430d35d18df224dcfe42e59181a76407cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871535"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Microsoft OLE DB-Anbieter für Microsoft Indexdienst


**Betrifft**: Access 2013, Office 2013

Microsoft OLE DB-Anbieter für Microsoft Indexdienst bietet programmgesteuerten schreibgeschützten Zugriff auf System- und Daten von Microsoft Indexdienst indiziert. ADO-Anwendungen können SQL-Abfragen ausgeben, um Informationen zu Inhalts- und Dateieigenschaften abzurufen.

Der Anbieter ist ein Freethreadanbieter, der Unicode verwendet.

## <a name="connection-string-parameters"></a>Verbindungszeichenfolgen-Parameter

Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das **Provider=** -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:

```vb 
 
MSIDXS 
```

Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.

## <a name="typical-connection-string"></a>Typische Verbindungszeichenfolge

Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
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
<td><p>Gibt den OLE DB-Anbieter für Microsoft Indexdienst an. In der Regel ist dies das einzige Schlüsselwort, das in der Verbindungszeichenfolge angegeben wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Gibt den Katalognamen des Indexdiensts an. Wenn dieses Schlüsselwort nicht angegeben ist, wird der Standardkatalog des Systems verwendet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Gibt eine eindeutige 32-Bit-Zahl (z. B. 1033) an, mit der Einstellungen für die Sprache des Benutzers festgelegt werden. Diese Einstellungen geben an, wie Datum und Uhrzeit formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden usw. Wenn dieses Schlüsselwort nicht angegeben ist, wird die Standard-Gebietsschema-ID des Systems verwendet.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Command Text

Die Syntax für SQL-Abfragen des Indexdiensts besteht aus Erweiterungen der SQL-92 **SELECT** -Anweisung und deren Klauseln **FROM** und **WHERE**. Das Ergebnis der Abfrage wird mithilfe von OLE DB-Rowsets zurückgegeben, die von ADO verwendet werden und als [Recordset](recordset-object-ado.md)-Objekte geändert werden können.

Sie können eine exakte Suche nach Wörtern oder Ausdrücken durchführen oder Platzhalter für die Suche nach Mustern oder Wortstämmen verwenden. Die Suchlogik kann auf booleschen Entscheidungen, gewichteten Ausdrücken oder Näherungen an andere Wörter basieren. Sie können auch eine Freitextsuche durchführen, mit der anstelle von Wortübereinstimmungen Bedeutungsübereinstimmungen gesucht werden.

Der Anbieter akzeptiert weder Aufrufe gespeicherter Prozeduren noch einfache Tabellennamen (die [CommandType](commandtype-property-ado.md)-Eigenschaft lautet beispielsweise immer **adCmdText**).

## <a name="recordset-behavior"></a>Recordset-Verhalten

In den folgenden Tabellen sind die für ein **Recordset** -Objekt verfügbaren Features aufgeführt, das mit diesem Anbieter geöffnet wird. Nur der statische Cursortyp (**AdOpenStatic**) zur Verfügung steht.

Ausführlichere Informationen zum **Recordset** -Verhalten Ihrer Anbieterkonfiguration erhalten Sie, wenn Sie die [Supports](supports-method-ado.md)-Methode ausführen und die [Properties](properties-collection-ado.md) -Auflistung des **Recordset** -Objekts aufzählen, um zu ermitteln, ob anbieterspezifische dynamische Eigenschaften vorhanden sind.

Verfügbarkeit von ADO-Standardeigenschaften des **Recordset** -Objekts:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaft</p></th>
<th><p>Verfügbarkeit</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Lesezeichen</a>*</p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>immer <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>immer <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>immer <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Nicht verf?gbar</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>Lesen/Schreiben</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>nur Lesen</p></td>
</tr>
</tbody>
</table>


\*Lesezeichen müssen auf dem Anbieter für das **Recordset-Objekt**vorhanden ist damit dieses Feature aktiviert sein.

Verfügbarkeit von ADO-Standardmethoden des **Recordset** -Objekts:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>Verfügbar?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Unterstützt</a></p></td>
<td><p>Ja</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>Nein</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Nein</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Siehe auch

Implementierung und funktionale Informationen zu den Microsoft OLE DB-Anbieter für Microsoft Indexdienst finden Sie in der Microsoft OLE DB Programmer's Reference.

