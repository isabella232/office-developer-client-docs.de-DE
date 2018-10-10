---
title: QueryDef.MaxRecords Property (DAO)
TOCTitle: MaxRecords Property
ms:assetid: 7492cde9-be30-3473-dabc-9602465910d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195877(v=office.15)
ms:contentKeyID: 48545664
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053583
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3960eb5227e3b2efc6f2b6fa39de2b3d72ca89f9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474181"
---
# <a name="querydefmaxrecords-property-dao"></a>QueryDef.MaxRecords Property (DAO)


**Betrifft**: Access 2013 | Office 2013


Legt die maximale Anzahl von Datensätzen fest, die von einer Abfrage an eine ODBC-Datenquelle zurückgegeben werden sollen, oder gibt den betreffenden Wert zurück.

## <a name="syntax"></a>Syntax

*Ausdruck* . MaxRecords

*Ausdruck* Eine Variable, die ein **QueryDef** -Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Standardwert ist 0. Bei diesem Wert gibt es keine Beschränkung der Anzahl der zurückzugebenden Datensätze.

Wenn die von **MaxRecords** festgelegte Anzahl der Zeilen an die Anwendung in einem **[Recordset](recordset-object-dao.md)** -Objekt zurückgegeben wird, beendet der Abfrageprozessor die Rückgabe der Datensätze, selbst wenn noch weitere Datensätze in das **Recordset** einbezogen werden sollten. Diese Eigenschaft ist nützlich, wenn beschränkte Clientressourcen die Verarbeitung einer großen Anzahl von Datensätzen nicht zulassen.


> [!NOTE]
> <P>[!HINWEIS] Die <STRONG>MaxRecords</STRONG>-Eigenschaft kann nur für eine ODBC-Datenquelle verwendet werden.</P>



## <a name="example"></a>Beispiel

In diesem Beispiel wird die **MaxRecords**-Eigenschaft verwendet, um eine Beschränkung der Anzahl der Datensätze festzulegen, die von einer Abfrage einer ODBC-Datenquelle zurückgegeben werden können.

```vb 
Sub MaxRecordsX() 
 
 Dim dbsCurrent As Database 
 Dim qdfPassThrough As QueryDef 
 Dim qdfLocal As QueryDef 
 Dim rstTemp As Recordset 
 
 ' Open a database from which QueryDef objects can be 
 ' created. 
 Set dbsCurrent = OpenDatabase("DB1.mdb") 
 
 ' Create a pass-through query to retrieve data from 
 ' a Microsoft SQL Server database. 
 Set qdfPassThrough = _ 
 dbsCurrent.CreateQueryDef("") 
 
 ' Set the properties of the new query, limiting the 
 ' number of returnable records to 20. 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 qdfPassThrough.Connect = _ 
 "ODBC;DATABASE=pubs;DSN=Publishers" 
 qdfPassThrough.SQL = "SELECT * FROM titles" 
 qdfPassThrough.ReturnsRecords = True 
 qdfPassThrough.MaxRecords = 20 
 
 Set rstTemp = qdfPassThrough.OpenRecordset() 
 
 ' Display results of query. 
 Debug.Print "Query results:" 
 With rstTemp 
 Do While Not .EOF 
 Debug.Print , .Fields(0), .Fields(1) 
 .MoveNext 
 Loop 
 .Close 
 End With 
 
 dbsCurrent.Close 
 
End Sub 
 
```

