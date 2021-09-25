---
title: Database.QueryTimeout-Eigenschaft (DAO)
TOCTitle: QueryTimeout Property
ms:assetid: c83ca852-715a-c853-429b-80a15c3fc39b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823170(v=office.15)
ms:contentKeyID: 48547648
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 038a88305e8e670f63e11aa5dfc05c078c47bb4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606877"
---
# <a name="databasequerytimeout-property-dao"></a>Database.QueryTimeout-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013


Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, wie viele Sekunden beim Ausführen einer Abfrage zu einer ODBC-Datenquelle gewartet wird, bevor ein Timeoutfehler auftritt.

## <a name="syntax"></a>Syntax

*Ausdruck* . Querytimeout

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="remarks"></a>HinwBemerkungeneise

Der Standardwert beträgt 60.

Bei einer ODBC-Datenbank, wie z. B. Microsoft SQL Server, können aufgrund des Netzwerkverkehrs oder einer hohen Belastung des ODBC-Servers Verzögerungen auftreten. Um eine unbegrenzte Wartezeit zu vermeiden, können Sie die Zeit festlegen.

Wenn Sie die **QueryTimeout**-Eigenschaft bei einem **[Connection](connection-object-dao.md)** - oder **[Database](database-object-dao.md)** -Objekt verwenden, gibt sie den globalen Wert für alle Abfragen an, die der Datenbank zugeordnet sind. Sie können diesen Wert für eine bestimmte Abfrage außer Kraft setzen, indem Sie die **ODBCTimeout**-Eigenschaft des speziellen **[QueryDef](querydef-object-dao.md)** -Objekts festlegen.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Eigenschaften **ODBCTimeout** und **QueryTimeout** verwendet, um zu zeigen, wie die **QueryTimeout**-Einstellung eines **Database**-Objekts die Standardeinstellung von **ODBCTimeout** für ein beliebiges **QueryDef**-Objekt festlegt, das anhand des **Database**-Objekts erstellt wurde.

```vb 
Sub ODBCTimeoutX() 
 
 Dim dbsCurrent As Database 
 Dim qdfStores As QueryDef 
 Dim rstStores As Recordset 
 
 Set dbsCurrent = OpenDatabase("Northwind.mdb") 
 
 ' Change the default QueryTimeout of the Northwind 
 ' database. 
 Debug.Print "Default QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 dbsCurrent.QueryTimeout = 30 
 Debug.Print "New QueryTimeout of Database: " & _ 
 dbsCurrent.QueryTimeout 
 
 ' Create a new QueryDef object. 
 Set qdfStores = dbsCurrent.CreateQueryDef("Stores", _ 
 "SELECT * FROM stores") 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the SQL Server. 
 qdfStores.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 
 ' Change the ODBCTimeout setting of the new QueryDef 
 ' object from its default setting. 
 Debug.Print "Default ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 qdfStores.ODBCTimeout = 0 
 Debug.Print "New ODBCTimeout of QueryDef: " & _ 
 qdfStores.ODBCTimeout 
 
 ' Execute the query and display the results. 
 Set rstStores = qdfStores.OpenRecordset() 
 
 Debug.Print "Contents of recordset:" 
 With rstStores 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 ' Delete new QueryDef because this is a demonstration. 
 dbsCurrent.QueryDefs.Delete qdfStores.Name 
 dbsCurrent.Close 
 
End Sub 
 
```

