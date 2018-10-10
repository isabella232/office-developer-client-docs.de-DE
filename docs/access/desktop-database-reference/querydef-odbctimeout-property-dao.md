---
title: QueryDef.ODBCTimeout Property (DAO)
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
ms.openlocfilehash: dcb15511f3052366eb3d322c26cdd31d72c9beab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475757"
---
# <a name="querydefodbctimeout-property-dao"></a>QueryDef.ODBCTimeout Property (DAO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, wie viele Sekunden gewartet werden soll, bevor ein Timeoutfehler auftritt, wenn ein **[QueryDef](querydef-object-dao.md)** -Objekt in einer ODBC-Datenbank ausgeführt wird.

## <a name="syntax"></a>Syntax

*Ausdruck* . ODBCTimeout

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Wenn die ODBCTimeout-Eigenschaft den Wert -1 erhält, wird für das Timeout standardmäßig die aktuelle Einstellung der QueryTimeout-Eigenschaft des Connection- oder Database-Objekts verwendet, das das QueryDef-Objekt enthält. Wenn die ODBCTimeout-Eigenschaft den Wert 0 hat, tritt kein Timeoutfehler auf.

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

