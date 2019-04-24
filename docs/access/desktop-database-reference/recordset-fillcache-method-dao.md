---
title: Recordset. FillCache-Methode (DAO)
TOCTitle: FillCache Method
ms:assetid: d171b939-b904-c6bd-6217-68bc2814e282
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834751(v=office.15)
ms:contentKeyID: 48547861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ef268a821d65732e0a54776872387f62c67e999
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300518"
---
# <a name="recordsetfillcache-method-dao"></a>Recordset. FillCache-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Füllt den lokalen Cache für ein **Recordset**-Objekt, das Daten aus einer mit einem Microsoft Access-Datenbankmodul verbundenen ODBC-Datenquelle enthält (gilt nur für mit dem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquellen), teilweise oder vollständig auf.

## <a name="syntax"></a>Syntax

*Ausdruck* . FillCache (***Rows***, ***Start Bookmark***)

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Rows</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>Integer</strong>), der angibt, wie viele Zeilen im Cache gespeichert werden sollen. Wenn Sie dieses Argument weglassen, wird der Wert durch die Einstellung der <strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong> -Eigenschaft bestimmt.</p></td>
</tr>
<tr class="even">
<td><p><em>Start Bookmark</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der ein Lesezeichen angibt. Der Cache wird ab dem Datensatz gefüllt, der durch dieses Lesezeichen angegeben wurde. Wenn Sie dieses Argument weglassen, wird der Cache beginnend mit dem von der <strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong> -Eigenschaft angegebenen Datensatz gefüllt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Durch Zwischenspeichern wird die Leistung einer Anwendung verbessert, die Daten von einem Remoteserver abruft. Ein Cache ist Platz im lokalen Speicher, der für kürzlich vom Server abgerufene Daten reserviert ist, die voraussichtlich erneut angefordert werden, während die Anwendung ausgeführt wird. Fragt ein Benutzer Daten ab, überprüft das Microsoft Access-Datenbankmodul zuerst, ob die Daten noch im Cache vorhanden sind, bevor es sie vom Server abruft, was länger dauert. Im Cache werden nur die Daten gespeichert, die von einer ODBC-Datenquelle stammen.

Wenn Sie nicht warten möchten, bis der Cache mit Datensätzen gefüllt ist, die abgerufen werden, können Sie mithilfe der **FillCache**-Methode den Cache jederzeit explizit füllen. Das geht schneller, da mit **FillCache** mehrere Datensätze gleichzeitig abgerufen werden. Während Sie beispielsweise die Datensätze bildschirmweise anzeigen, ruft die Anwendung mithilfe von **FillCache** jeweils die Datensätze für den nächsten Bildschirm ab.

Jede mit einem Microsoft Access-Datenbankmodul verbundene ODBC-Datenquelle, auf die Sie mit **Recordset**-Objekten zugreifen, kann einen lokalen Cache haben. Sie können einen Cache erstellen, indem Sie ein **Recordset**-Objekt aus einer Remotedatenquelle öffnen und dann die **CacheSize**- und **CacheStart**-Eigenschaften des **Recordset**-Objekts festlegen.

Wenn Zeilen und Start Bookmark einen Bereich von Datensätzen erstellen, die teilweise oder vollständig außerhalb des von den Eigenschaften **CacheSize** und **CacheStart** angegebenen Datensatzes liegen, wird der Teil des Recordset-Objekts außerhalb dieses Bereichs ignoriert und nicht geladen. in den Cache.

Übersteigen die durch **FillCache** angeforderten Datensätze die in der Remotedatenquelle verbliebene Anzahl, ruft das Microsoft Access-Datenbankmodul nur die verbliebenen Datensätze ab, und es tritt kein Fehler auf.

> [!NOTE]
> - Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.
> - **FillCache** only retrieves records not already cached. To force an update of all the cached data, set the **CacheSize** property of the **Recordset** to 0, reset it to the size of the cache you originally requested, and then use **FillCache**.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die **CreateTableDef**- und **FillCache**-Methoden und die **CacheSize**-, **CacheStart**- und **SourceTableName**-Eigenschaften verwendet, um die Datensätze in einer verknüpften Tabelle zweimal aufzuzählen. Daraufhin werden die Datensätze in einem Cache mit 50 Datensätzen zweimal aufgezählt. Anschließend enthält das Beispiel durch die verknüpfte Tabelle die Leistungsstatistik für die zwischengespeicherten und die nicht zwischengespeicherten Datensätze.

```vb
    Sub ClientServerX3() 
     
       Dim dbsCurrent As Database 
       Dim tdfRoyalties As TableDef 
       Dim rstRemote As Recordset 
       Dim sngStart As Single 
       Dim sngEnd As Single 
       Dim sngNoCache As Single 
       Dim sngCache As Single 
       Dim intLoop As Integer 
       Dim strTemp As String 
       Dim intRecords As Integer 
     
       ' Open a database to which a linked table can be  
       ' appended. 
       Set dbsCurrent = OpenDatabase("DB1.mdb") 
     
       ' Create a linked table that connects to a Microsoft SQL 
       ' Server database. 
       Set tdfRoyalties = _ 
          dbsCurrent.CreateTableDef("Royalties") 
       ' Note: The DSN referenced below must be set to  
       '       use Microsoft Windows NT Authentication Mode to  
       '       authorize user access to the Microsoft SQL Server. 
       tdfRoyalties.Connect = _ 
          "ODBC;DATABASE=pubs;DSN=Publishers" 
       tdfRoyalties.SourceTableName = "roysched" 
       dbsCurrent.TableDefs.Append tdfRoyalties 
       Set rstRemote = _ 
          dbsCurrent.OpenRecordset("Royalties") 
     
       With rstRemote 
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          sngStart = Timer 
     
          For intLoop = 1 To 2 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                .MoveNext 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngNoCache = sngEnd - sngStart 
     
          ' Cache the first 50 records. 
          .MoveFirst 
          .CacheSize = 50 
          .FillCache 
          sngStart = Timer 
     
          ' Enumerate the Recordset object twice and record 
          ' the elapsed time. 
          For intLoop = 1 To 2 
             intRecords = 0 
             .MoveFirst 
             Do While Not .EOF 
                ' Execute a simple operation for the 
                ' performance test. 
                strTemp = !title_id 
                ' Count the records. If the end of the 
                ' cache is reached, reset the cache to the 
                ' next 50 records. 
                intRecords = intRecords + 1 
                .MoveNext 
                If intRecords Mod 50 = 0 Then 
                   .CacheStart = .Bookmark 
                   .FillCache 
                End If 
             Loop 
          Next intLoop 
     
          sngEnd = Timer 
          sngCache = sngEnd - sngStart 
     
          ' Display performance results. 
          MsgBox "Caching Performance Results:" & vbCr & _ 
             "  No cache: " & Format(sngNoCache, _ 
             "##0.000") & " seconds" & vbCr & _ 
             "  50-record cache: " & Format(sngCache, _ 
             "##0.000") & " seconds" 
          .Close 
       End With 
     
       ' Delete linked table because this is a demonstration. 
       dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
       dbsCurrent.Close 
     
    End Sub
```
