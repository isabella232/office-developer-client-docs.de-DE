---
title: PARAMETERS-Deklaration (Microsoft Access SQL)
TOCTitle: PARAMETERS declaration (Microsoft Access SQL)
ms:assetid: 0dcaad68-6a5f-93dc-e62a-b82b36e1e69c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845220(v=office.15)
ms:contentKeyID: 48543230
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277577
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e906e90fd6f7bf6e26898ed5381ef687c2ee8514
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937342"
---
# <a name="parameters-declaration-microsoft-access-sql"></a>PARAMETERS-Deklaration (Microsoft Access SQL)


**Betrifft**: Access 2013, Office 2013

Deklariert den Namen und Datentyp der einzelnen Parameter in einer Parameterabfrage.

## <a name="syntax"></a>Syntax

PARAMETERS *Name Datentyp* \[, *Name Datentyp* \[,...\]\]

Die PARAMETERS-Deklaration enthält die folgenden Bestandteile:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>name</em></p></td>
<td><p>Der Name des Parameters. Wird der <strong>Name</strong> -Eigenschaft des <strong>Parameter</strong> -Objekts zugewiesen und wird verwendet, um diesen Parameter in der <strong>Parameters</strong> -Auflistung zu identifizieren. Sie können <em>Name</em> als Zeichenfolge, die in einem Dialogfeld angezeigt wird, während die Anwendung die Abfrage ausführt. Umgeben Sie Text, der Leerzeichen oder Satzzeichen enthält, mit Klammern ([ ]). Beispielsweise [Low Price] und [Bericht mit welcher Month? beginnen] sind gültigen <em>Namen</em> Argumente.</p></td>
</tr>
<tr class="even">
<td><p><em>Datentyp</em></p></td>
<td><p>Einer der wichtigsten <a href="sql-data-types.md">Microsoft Access SQL-Datentypen</a> oder eines der Synonyme.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Für regelmäßig ausgeführte Abfragen können Sie zum Erstellen der Parameterabfrage eine PARAMETERS-Deklaration verwenden. Eine Parameterabfrage kann Sie dabei unterstützen, das Ändern der Abfragekriterien zu automatisieren. Bei einer Parameterabfrage müssen die Parameter jedes Mal, wenn die Abfrage ausgeführt wird, im Code angegeben werden.

Die PARAMETERS-Deklaration ist optional, doch wenn sie angegeben wird, wird sie vor allen anderen Anweisungen angegeben, selbst vor einer [SELECT](select-statement-microsoft-access-sql.md)-Anweisung.

Wenn die Deklaration mehrere Parameter einschließt, müssen diese durch Kommas getrennt werden. Im folgenden Beispiel sind zwei Parameter eingeschlossen:

```sql
PARAMETERS [Low price] Currency, [Beginning date] DateTime;
```

Sie können *Name* , aber nicht den *Datentyp* in einer [, in dem](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) oder eine [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\)) -Klausel verwenden. In den folgenden Beispielen wird die Angabe von zwei Parametern erwartet, anschließend werden die Kriterien auf die Datensätze in der Orders-Tabelle angewendet:

```sql
PARAMETERS [Low price] Currency, 
[Beginning date] DateTime; 
SELECT OrderID, OrderAmount
FROM Orders 
WHERE OrderAmount > [Low price] 
AND OrderDate >= [Beginning date];
```

## <a name="example"></a>Beispiel

In diesem Beispiel muss der Benutzer eine Position angeben, die dann als Kriterium in der Abfrage verwendet wird.

Sie ruft die EnumFields-Prozedur, die im Beispiel ["SELECT"-Anweisung](select-statement-microsoft-access-sql.md) gefunden werden können.

```vb
    Sub ParametersX() 
     
        Dim dbs As Database, qdf As QueryDef 
        Dim rst As Recordset 
        Dim strSql As String, strParm As String 
        Dim strMessage As String 
        Dim intCommand As Integer 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("NorthWind.mdb") 
         
        ' Define the parameters clause. 
        strParm = "PARAMETERS [Employee Title] CHAR; " 
     
        ' Define an SQL statement with the parameters 
        ' clause. 
        strSql = strParm & "SELECT LastName, FirstName, " _ 
            & "EmployeeID " _ 
            & "FROM Employees " _ 
            & "WHERE Title =[Employee Title];" 
         
        ' Create a QueryDef object based on the  
        ' SQL statement. 
        Set qdf = dbs.CreateQueryDef _ 
            ("Find Employees", strSql) 
         
        Do While True 
            strMessage = "Find Employees by Job " _ 
                & "title:" & Chr(13) _ 
                & "  Choose Job Title:" & Chr(13) _ 
                & "   1 - Sales Manager" & Chr(13) _ 
                & "   2 - Sales Representative" & Chr(13) _ 
                & "   3 - Inside Sales Coordinator" 
             
            intCommand = Val(InputBox(strMessage)) 
             
            Select Case intCommand 
                Case 1 
                    qdf("Employee Title") = _ 
                        "Sales Manager" 
                Case 2 
                    qdf("Employee Title") = _ 
                        "Sales Representative" 
                Case 3 
                    qdf("Employee Title") = _ 
                        "Inside Sales Coordinator" 
                Case Else 
                    Exit Do 
            End Select 
             
            ' Create a temporary snapshot-type Recordset. 
            Set rst = qdf.OpenRecordset(dbOpenSnapshot) 
     
            ' Populate the Recordset. 
            rst.MoveLast 
                 
            ' Call EnumFields to print the contents of the  
            ' Recordset. Pass the Recordset object and desired 
            ' field width. 
            EnumFields rst, 12 
     
        Loop 
         
        ' Delete the QueryDef because this is a 
        ' demonstration. 
        dbs.QueryDefs.Delete "Find Employees" 
         
        dbs.Close 
     
    End Sub
```
