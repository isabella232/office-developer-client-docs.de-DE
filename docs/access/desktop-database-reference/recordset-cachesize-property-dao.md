---
title: Recordset. CacheSize-Eigenschaft (DAO)
TOCTitle: CacheSize Property
ms:assetid: 8632f5fb-6e5d-5a3e-1bd7-81e1270e9531
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196807(v=office.15)
ms:contentKeyID: 48546079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 369ff9192bb592c96e17920c9771c10b70dc233b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300595"
---
# <a name="recordsetcachesize-property-dao"></a>Recordset. CacheSize-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Mit dieser Eigenschaft wird die Anzahl von Datensätzen, die aus einer ODBC-Datenquelle abgerufen und lokal gespeichert werden, festgelegt oder zurückgegeben. **Long**-Wert mit Lese-/Schreibzugriff.

## <a name="syntax"></a>Syntax

*Ausdruck* . CacheSize

*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Wert der **CacheSize**-Eigenschaft muss zwischen 5 und 1200 liegen, darf aber nicht größer als der verfügbare Speicherplatz sein. Ein typischer Wert ist 100. Bei der Einstellung 0 wird die Zwischenspeicherung deaktiviert.

Wenn Sie Daten von einem Remoteserver mit **Recordset**-Objekten abrufen, kann die Leistung durch eine Zwischenspeicherung gesteigert werden. Ein Zwischenspeicher ist ein Bereich im lokalen Speicher, an dem die zuletzt vom Server abgerufenen Daten gespeichert werden. Dies ist nützlich, wenn Benutzer dieselben Daten während der Ausführung des Programms wiederholt abrufen. Wenn Benutzer Daten abrufen, überprüft die Microsoft Access-Datenbank-Engine, ob die Daten im Zwischenspeicher enthalten sind, anstatt sie vom Server abzurufen. Dies erfordert weniger Zeit. Im Zwischenspeicher werden nur Daten gespeichert, die aus einer ODBC-Datenquelle stammen.

Jede ODBC-Datenquelle, die mit einer Microsoft Access-Datenbank-Engine verknüpft ist, wie etwa eine verknüpfte Tabelle, kann einen lokalen Zwischenspeicher haben. Zum Erstellen des Zwischenspeichers öffnen Sie ein **Recordset**-Objekt in der Remotedatenquelle und legen die Eigenschaften **CacheSize** und **[CacheStart](recordset-cachestart-property-dao.md)** fest. Anschließend verwenden Sie die **[FillCache](recordset-fillcache-method-dao.md)** -Methode oder durchlaufen die Datensätze mit den **Move**-Methoden.

Sie können die Einstellung der **CacheSize**-Eigenschaft auf die Anzahl der Datensätze basieren, die Ihre Anwendung gleichzeitig verarbeiten kann. Wenn Sie zum Beispiel ein **Recordset**-Objekt als Quelle für die auf dem Bildschirm anzuzeigenden Daten verwenden, können Sie für seine **CacheSize**-Eigenschaft den Wert 20 festlegen, sodass jeweils 20 Datensätze gleichzeitig angezeigt werden.

Die Microsoft Access-Datenbank-Engine ruft Datensätze, die sich im Bereich des Zwischenspeichers befinden, aus dem Zwischenspeicher ab und Datensätze, die sich nicht im Zwischenspeicherbereich befinden, vom Server.

Aus dem Zwischenspeicher abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben.

Sie können die Aktualisierung aller Daten im Zwischenspeicher erzwingen, indem Sie die **CacheSize**-Eigenschaft des **Recordset**-Objekts auf 0 und dann zurück auf die ursprünglich angeforderte Zwischenspeichergröße setzen. Anschließend verwenden Sie die **FillCache**-Methode.

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
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
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
     " No cache: " & Format(sngNoCache, _ 
     "##0.000") & " seconds" & vbCr & _ 
     " 50-record cache: " & Format(sngCache, _ 
     "##0.000") & " seconds" 
     .Close 
     End With 
     
     ' Delete linked table because this is a demonstration. 
     dbsCurrent.TableDefs.Delete tdfRoyalties.Name 
     dbsCurrent.Close 
     
    End Sub
```
