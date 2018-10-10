---
title: Microsoft OLE DB-Anbieter für Remoting (ADO-Dienstanbieter)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 907686e0dcd1be8ef24747d9ff655a7ff0f7f91f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474510"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Microsoft OLE DB-Anbieter für Remoting (ADO-Dienstanbieter)

**Betrifft**: Access 2013 | Office 2013

Mithilfe des Microsoft OLE DB-Anbieter für Remoting kann ein lokaler Benutzer auf einem Clientcomputer Datenanbieter auf einem Remotecomputer aufrufen. Geben Sie die Parameter des Datenanbieters für den Remotecomputer so an, als wären Sie ein lokaler Benutzer am Remotecomputer. Geben Sie anschließend die Parameter an, die vom Anbieter für Remoting für den Zugriff auf den Remotecomputer verwendet werden. So haben Sie auf den Remotecomputer Zugriff, als wären Sie ein lokaler Benutzer.

## <a name="provider-keyword"></a>Schlüsselwort für den Anbieter

Um den OLE DB-Anbieter für Remoting aufzurufen, geben Sie das folgende Schlüsselwort und den folgenden Wert in die Verbindungszeichenfolge ein. (Beachten Sie das Leerzeichen im Namen des Anbieters.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Zusätzliche Schlüsselwörter

Beim Aufrufen dieses Dienstanbieters sind die folgenden zusätzlichen Schlüsselwörter relevant.

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
<td><p><strong>Data Source</strong></p></td>
<td><p>Gibt den Namen der Remotedatenquelle an. Es wird an den OLE DB-Anbieter für Remoting zur Verarbeitung übergeben. Dieses Schlüsselwort entspricht der <a href="connect-property-rds.md">Connect</a>-Eigenschaft des <a href="datacontrol-object-rds.md">RDS.DataControl</a>-Objekts.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Dynamische Eigenschaften

Beim Aufrufen dieses Dienstanbieters werden der [Properties](connection-object-ado.md)-Auflistung des [Connection](properties-collection-ado.md)-Objekts die folgenden dynamischen Eigenschaften hinzugefügt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name der dynamischen Eigenschaft</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Gibt den DataFactory-Modus. Eine Zeichenfolge, die die gewünschte Version des <a href="datafactory-object-rdsserver.md">DataFactory</a> -Objekts gibt an, auf dem Server. Legen Sie diese Eigenschaft vor dem Öffnen einer Verbindungs zum Anfordern einer bestimmten Version von <strong>DataFactory</strong>. Wenn die angeforderte Version nicht verfügbar ist, wird versucht werden, verwenden Sie die vorhergehende Version. Wenn keine vorhergehende Version vorhanden ist, tritt ein Fehler auf. Wenn <strong>DFMode</strong> kleiner als die verfügbare Version ist, tritt ein Fehler auf. Diese Eigenschaft ist schreibgeschützt, nachdem eine Verbindung hergestellt wird. Kann einen der folgenden gültigen Werte vom Typ String annehmen:</p>
<p></p>
<ul>
<li><p>&quot;25&quot; – Version 2.5 (Default)</p></li>
<li><p>&quot;21&quot; – Version 2.1</p></li>
<li><p>&quot;20&quot; – Version 2.0</p></li>
<li><p>&quot;15&quot; – Version 1.5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Command Properties</strong></p></td>
<td><p>Gibt Werte an, die der Zeichenfolge der Command-Eigenschaften (Rowset) hinzugefügt werden, die vom Microsoft OLE DB-Anbieter für Remoting an den Server gesendet werden. Der Standardwert für diese Zeichenfolge lautet vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>Gibt die aktuelle Versionsnummer des <strong>DataFactory</strong> auf dem Server an. Überprüfen Sie diese Eigenschaft, um festzustellen, ob die in der Eigenschaft <strong>DFMode</strong> angeforderte Version berücksichtigt wurde. Kann einen der folgenden gültigen Werte vom Typ Long integer annehmen:</p>
<p></p>
<ul>
<li><p>25 – Version 2.5 (Default)</p></li>
<li><p>21 – Version 2.1</p></li>
<li><p>20 – Version 2.0</p></li>
<li><p>15 – Version 1.5</p></li>
</ul>
<p></p>
<p>Hinzufügen von &quot;DFMode = 20; &quot; für Ihre Verbindung bei Verwendung des Providers <strong>MSRemote</strong> Zeichenfolge beim Aktualisieren von Daten die Leistung Ihres Servers verbessern kann. Bei dieser Einstellung verwendet das <strong>RDSServer.DataFactory</strong> -Objekt auf dem Server einen weniger ressourcenintensiven Modus. In dieser Konfiguration sind die folgenden Features jedoch nicht verfügbar:</p>
<p></p>
<ul>
<li><p>Verwenden parametrisierter Abfragen.</p></li>
<li><p>Abrufen von Parameter- oder Spalteninformationen vor dem Aufrufen der <strong>Execute</strong> -Methode.</p></li>
<li><p>Festlegen von <strong>Transact Updates</strong> auf <strong>True</strong>.</p></li>
<li><p>Abrufen von Zeilenstatus.</p></li>
<li><p>Aufrufen der <strong>Resync</strong>-Methode.</p></li>
<li><p>Aktualisieren (explizit oder automatisch) mithilfe der <strong>Update Resync</strong>-Eigenschaft.</p></li>
<li><p>Festlegen der Eigenschaften von <strong>Command</strong> oder <strong>Recordset</strong>.</p></li>
<li><p>Verwenden von <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Ereignishandler</strong></p></td>
<td><p>Gibt den Namen eines serverseitigen Anpassungsprogramms (oder Handler), die die Funktionalität des <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>und keine Parameter vom Handler verwendeten<em>,</em> alle durch Kommas getrennt erweitert (&quot;,&quot;). Ein <strong>String</strong> -Wert.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Gibt die Zeitdauer in Millisekunden an, die verstreicht, bis eine Anforderung vom und zum Server gelangt. (Der Standardwert beträgt 5 Minuten).</p></td>
</tr>
<tr class="even">
<td><p><strong>Remote Provider</strong></p></td>
<td><p>Gibt den Namen des Datenproviders an, der auf dem Remoteserver verwendet werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remote Server</strong></p></td>
<td><p>Gibt den Servernamen und das Kommunikationsprotokoll an, das von dieser Verbindung verwendet werden soll. Diese Eigenschaft entspricht der <a href="server-property-rds.md">Server</a>-Eigenschaft des <a href="datacontrol-object-rds.md">RDS.DataControl</a>-Objekts.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>Wenn diese Eigenschaft auf True gesetzt ist, gibt dieser Wert an, dass beim Ausführen von UpdateBatch auf dem Server die Ausführung innerhalb einer Transaktion erfolgt. Der Standardwert für diese boolesche dynamische Eigenschaft ist False.</p></td>
</tr>
</tbody>
</table>


Sie können auch beschreibbare dynamische Eigenschaften festlegen, indem Sie die zugehörigen Namen in der Verbindungszeichenfolge als Schlüsselwörter angeben. Legen Sie beispielsweise die dynamische Eigenschaft **Internet Timeout** auf fünf Sekunden fest, indem Sie Folgendes angeben:

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Sie können auch eine dynamische Eigenschaft festlegen oder abrufen, indem Sie deren Namen als Index für die **Properties** -Eigenschaft angeben. Beispiel: Rufen Sie den aktuellen Wert der dynamischen Eigenschaft **Internet Timeout** ab, und drucken Sie diesen. Legen Sie anschließend einen neuen Wert fest. Gehen Sie dazu wie folgt vor:

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Hinweise

In ADO 2.0 konnte der OLE DB-Anbieter für Remoting nur in der *ActiveConnection* -Parameter der **Open** -Methode des [Recordset](recordset-object-ado.md) -Objekts angegeben werden. ADO 2.1 ab, kann der Anbieter auch in der *ConnectionString* -Parameter der **Open** -Methode des [Connection](connection-object-ado.md) -Objekts angegeben werden.

Die Entsprechung der **SQL**-Eigenschaft des [RDS.DataControl](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) -Objekts ist nicht verfügbar. Stattdessen wird das [Recordset](recordset-object-ado.md) -Objekt **Open** *Source* -Argument-Methode verwendet.

Wenn Sie "...;Remote Provider=MS Remote;..." angeben, wird ein vierstufiges Szenario erstellt. Szenarien mit mehr als drei Stufen wurden noch nicht getestet und sollten nicht erforderlich sein.

## <a name="example"></a>Beispiel

Mit diesem Beispiel wird die **Authors**-Tabelle in der **Pubs**-Datenbank auf dem Server *Server* abgefragt. Die Namen der Remotedatenquelle und des Remoteservers werden in der [Open](open-method-ado-connection.md)-Methode des [Connection](connection-object-ado.md)-Objekts bereitgestellt, und die SQL-Abfrage wird in der [Open-Methode](open-method-ado-recordset.md) des [Recordset](recordset-object-ado.md)-Objekts angegeben. Ein **Recordset**-Objekt wird zurückgegeben, bearbeitet und verwendet, um die Datenquelle zu aktualisieren.

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

