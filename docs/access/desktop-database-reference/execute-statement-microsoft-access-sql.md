---
title: EXECUTE-Anweisung (Microsoft Access SQL)
TOCTitle: EXECUTE statement (Microsoft Access SQL)
ms:assetid: 9ec4d9ee-db2a-0319-3ccf-c035d67a1496
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198330(v=office.15)
ms:contentKeyID: 48546667
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277471
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: df70d2728732f33161622ce71fc9273bd9f016f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701942"
---
# <a name="execute-statement-microsoft-access-sql"></a>EXECUTE-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Wird verwendet, um die Ausführung einer Prozedur aufzurufen.

## <a name="syntax"></a>Syntax

EXECUTE *Prozedur* \[ *param1*\[, *param2*\[,...\]\]

Die EXECUTE-Anweisung besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Komponente</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Prozedur</em></p></td>
<td><p>Der Name der auszuführenden Prozedur.</p></td>
</tr>
<tr class="even">
<td><p><em>Param1, Param2, …</em></p></td>
<td><p>Die von der Prozedur definierten Werte für die Parameter.</p></td>
</tr>
</tbody>
</table>


## <a name="example"></a>Beispiel

In diesem Beispiel wird die Abfrage categoryList verwendet, und es wird die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.

```vb
    Sub ProcedureX() 
     
        Dim dbs As Database, rst As Recordset 
        Dim qdf As QueryDef, strSql As String 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        strSql = "PROCEDURE CategoryList; " _ 
            & "SELECT DISTINCTROW CategoryName, " _ 
            & "CategoryID FROM Categories " _ 
            & "ORDER BY CategoryName;" 
         
        ' Create a named QueryDef based on the SQL 
        ' statement. 
        Set qdf = dbs.CreateQueryDef("NewQry", strSql) 
     
        ' Create a temporary snapshot-type Recordset. 
        Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
        ' Populate the Recordset. 
        rst.MoveLast 
                 
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        Execute EnumFields rst, 15 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "NewQry" 
         
        dbs.Close 
     
    End Sub
```
