---
title: QueryDef.ODBCTimeout-Eigenschaft (DAO)
TOCTitle: ODBCTimeout Property
ms:assetid: b251c4fb-64a8-aa95-deed-64425df3e00c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822019(v=office.15)
ms:contentKeyID: 48547166
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053052
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: a79f403d49db1137d8b67d2dc7fb27b3ea140fc3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589239"
---
# <a name="querydefodbctimeout-property-dao"></a>QueryDef.ODBCTimeout-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Gibt an, wie viele Sekunden gewartet werden soll, bevor ein Timeoutfehler auftritt, wenn ein **[QueryDef](querydef-object-dao.md)** -Objekt in einer ODBC-Datenbank ausgeführt wird.

## <a name="syntax"></a>Syntax

*Ausdruck* . ODBCTimeout

*Ausdruck* Eine Variable, die ein **QueryDef**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

When the **ODBCTimeout** property is set to -1, the timeout defaults to the current setting of the **[QueryTimeout](database-querytimeout-property-dao.md)** property of the **[Connection](connection-object-dao.md)** or **[Database](database-object-dao.md)** object that contains the **QueryDef**. When the **ODBCTimeout** property is set to 0, no timeout error occurs.

Wenn Sie eine ODBC-Datenbank verwenden, wie etwa Microsoft SQL Server, kann es aufgrund einer hohen Auslastung des Netzwerks oder des ODBC-Server zu Verzögerungen kommen. Anstatt zu warten, können Sie einen Zeitraum festlegen, nach dessen Ablauf ein Fehler zurückgegeben wird.

Der Wert der **ODBCTimeout**-Eigenschaft eines **QueryDef**-Objekts hat Vorrang vor dem für die **QueryTimeout**-Eigenschaft angegebenen Wert des **Connection** - oder **Database**-Objekts, das das **QueryDef**-Objekt enthält. Dies gilt jedoch nur für das betreffende **QueryDef**-Objekt.

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

