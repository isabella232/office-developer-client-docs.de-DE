---
title: Microsoft Cursor Service für OLE DB (ADO-Dienstkomponente)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 175023f12d1efa23422afb15e693d44976421cc0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473480"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a>Microsoft Cursor Service für OLE DB (ADO-Dienstkomponente)


**Betrifft**: Access 2013 | Office 2013

Der Microsoft Cursor Service für OLE DB ergänzt die Cursor-Hilfsfunktionen von Datenanbietern. Der Benutzer nimmt daher eine relativ einheitliche Funktionalität aller Datenprovider wahr.

Der Cursordienst macht dynamische Eigenschaften verfügbar und verbessert das Verhalten bestimmter Methoden. Beispiel: Die dynamische [Optimize](optimize-property-dynamic-ado.md)-Eigenschaft ermöglicht das Erstellen temporärer Indizes, um bestimmte Vorgänge, wie die [Find](find-method-ado.md)-Methode, zu erleichtern.

Der Cursordienst ermöglicht die Unterstützung von Batchaktualisierungen in allen Fällen. Er simuliert darüber hinaus auch leistungsfähigere Cursortypen, wie dynamische Cursor, wenn ein Datenprovider nur weniger leistungsfähige Cursor, wie statische Cursor, bereitstellen kann.

## <a name="keyword"></a>Schlüsselwort

Um diese Dienstkomponente aufzurufen, legen Sie die [CursorLocation](recordset-object-ado.md)-Eigenschaft der Objekte [Recordset](connection-object-ado.md) oder [Connection](cursorlocation-property-ado.md) auf **adUseClient** fest.

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a>Dynamische Eigenschaften

Wenn der Microsoft Cursor Service für OLE DB aufgerufen wird, werden der **Properties**-Auflistung des [Recordset](properties-collection-ado.md) -Objekts die folgenden dynamischen Eigenschaften hinzugefügt. Eine vollständige Liste mit den dynamischen Eigenschaften der Objekte **Connection** und **Recordset** finden Sie im [Index zu dynamischen ADO-Eigenschaften](ado-dynamic-property-index.md). Die zugehörigen OLE DB-Eigenschaftennamen sind ggf. nach den ADO-Eigenschaftennamen in Klammern angegeben.

Nach dem Aufrufen des Cursordiensts sind Änderungen an einigen dynamischen Eigenschaften für die zugrunde liegende Datenquelle nicht erkennbar. Beispielsweise wird durch Festlegen der *Befehl Zeitlimit* -Eigenschaft für ein **Recordset-Objekt** für die zugrunde liegenden Datenprovider nicht angezeigt.

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

Wenn Ihre Anwendung den Cursordienst erfordert, Sie jedoch dynamische Eigenschaften im zugrunde liegenden Anbieter festlegen müssen, tun Sie dies, bevor Sie den Cursordienst aufrufen. Einstellungen für Eigenschaften von Befehlsobjekten werden unabhängig von der Cursorplatzierung immer an den zugrundeliegenden Datenprovider weitergeleitet. Sie können daher auch jederzeit ein Befehlsobjekt zum Festlegen der Eigenschaften verwenden.

> [!NOTE]
> Die dynamische Eigenschaft DBPROP_SERVERDATAONINSERT wird vom Cursordienst nicht unterstützt, auch wenn sie vom zugrunde liegenden Datenprovider unterstützt wird.



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
<td><p>Auto Recalc<br />
(DBPROP_ADC_AUTORECALC)</p></td>
<td><p>Bei Datensatzgruppen, die mit dem Datenstrukturierungsdienst erstellt wurden, gibt dieser Wert an, wie häufig berechnete und Aggregatspalten berechnet werden. Der Standardwert (Wert=1) bedeutet, dass eine Neuberechnung durchgeführt wird, wenn der Datenstrukturierungsdienst feststellt, dass sich die Werte geändert haben. Wenn der Wert 0 ist, werden die berechneten und Aggregatspalten nur berechnet, wenn die Hierarchie zum ersten Mal erstellt wird.</p></td>
</tr>
<tr class="even">
<td><p>Batch Size<br />
(DBPROP_ADC_BATCHSIZE)</p></td>
<td><p>Gibt die Anzahl von Aktualisierungsanweisungen an, die vor dem Senden an die Datenquelle als Batch verarbeitet werden können. Je mehr Anweisungen in einem Batch, umso weniger Schleifen zum Datenspeicher sind erforderlich.</p></td>
</tr>
<tr class="odd">
<td><p>Cache Child Rows<br />
(DBPROP_ADC_CACHECHILDROWS)</p></td>
<td><p>Bei Datensatzgruppen, die mit dem Datenstrukturierungsdienst erstellt wurden, gibt dieser Wert an, ob untergeordnete Datensatzgruppen zur späteren Verwendung in einem Cache gespeichert werden.</p></td>
</tr>
<tr class="even">
<td><p>Cursor Engine Version<br />
(DBPROP_ADC_CEVER)</p></td>
<td><p>Gibt die Version des verwendeten Cursordiensts an.</p></td>
</tr>
<tr class="odd">
<td><p>Maintain Change Status<br />
(DBPROP_ADC_MAINTAINCHANGESTATUS)</p></td>
<td><p>Gibt den Text des Befehls an, der zum erneuten Synchronisieren einer oder mehrerer Zeilen in einer Verknüpfung aus mehreren Tabellen verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="optimize-property-dynamic-ado.md">Optimieren der Leistung von</a></p></td>
<td><p>Gibt an, ob ein Index erstellt werden soll. Wenn diese Eigenschaft auf <strong>True</strong> festgelegt ist, wird das temporäre Erstellen von Indizes zum Verbessern der Ausführung bestimmter Vorgänge zugelassen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p>Gibt den Namen des <strong>Recordset</strong>-Objekts an. Darauf kann in aktuellen oder nachfolgenden Datenstrukturierungsbefehlen verwiesen werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p>Gibt eine benutzerdefinierte Befehlszeichenfolge an, die von der <a href="resync-method-ado.md">Resync</a>-Methode verwendet wird, wenn die <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a>-Eigenschaft aktiv ist.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></p></td>
<td><p>Gibt den Namen der Datenbank an, der die Tabelle enthält, auf die in der <strong>Unique Table</strong>-Eigenschaft verwiesen wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></p></td>
<td><p>Gibt den Namen der Besitzers der Tabelle an, auf die in der <strong>Unique Table</strong>-Eigenschaft verwiesen wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></p></td>
<td><p>Gibt den Namen der Tabelle in einem aus mehreren Tabellen erstellten <strong>Recordset</strong>-Objekt an, die durch Einfügungen, Aktualisierungen oder Löschvorgänge geändert werden kann.</p></td>
</tr>
<tr class="even">
<td><p>Update Criteria<br />
(DBPROP_ADC_UPDATECRITERIA)</p></td>
<td><p>Gibt an, welche Felder in der <strong>WHERE</strong>-Klausel zum Behandeln von Konflikten bei einer Aktualisierung verwendet werden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</p></td>
<td><p>Gibt an, ob die <strong>Resync</strong>-Methode nach der <a href="updatebatch-method-ado.md">UpdateBatch</a>-Methode (und dem jeweiligen Verhalten) implizit aufgerufen wird, wenn die <strong>Unique Table</strong>-Eigenschaft aktiv ist.</p></td>
</tr>
</tbody>
</table>


Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die **Properties** -Auflistung angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft [Optimize](optimize-property-dynamic-ado.md) ab, und drucken Sie ihn. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a>Verhalten integrierter Eigenschaften

Der Microsoft Cursor Service für OLE DB hat auch Auswirkungen auf das Verhalten bestimmter integrierter Eigenschaften.

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
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Ergänzt die für ein <strong>Recordset</strong>-Objekt verfügbaren Cursortypen.</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Ergänzt die für ein <strong>Recordset</strong>-Objekt verfügbaren Typen von Sperren. Ermöglicht Batchaktualisierungen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Gibt einen oder mehrere Feldnamen an, nach denen das <strong>Recordset</strong>-Objekt sortiert ist. Gibt außerdem an, ob die einzelnen Felder in auf- oder absteigender Folge sortiert sind.</p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a>Methodenverhalten

Der Microsoft Cursor Service für OLE DB ermöglicht oder beeinflusst das Verhalten der [Append](field-object-ado.md)-Methode des [Field](append-method-ado.md)-Objekts sowie der Methoden **Open**, [Resync](open-method-ado-recordset.md), [UpdateBatch](resync-method-ado.md) und [Save](updatebatch-method-ado.md) des [Recordset](save-method-ado.md) -Objekts.

