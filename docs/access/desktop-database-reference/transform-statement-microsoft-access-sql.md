---
title: TRANSFORM-Anweisung (Microsoft Access SQL)
TOCTitle: TRANSFORM statement (Microsoft Access SQL)
ms:assetid: 419770b1-c833-959d-a84d-56c68764799f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192901(v=office.15)
ms:contentKeyID: 48544455
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277581
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9abe91d4ce6996a725e246da6922015d15a8bd39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314042"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM-Anweisung (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine Kreuztabellenabfrage.

## <a name="syntax"></a>Syntax

TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]

Die TRANSFORM-Anweisung setzt sich wie folgt zusammen:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Part</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Aggregatfunktion</em></p></td>
<td><p>Eine <a href="sql-aggregate-functions-sql.md">SQL-Aggregatfunktion</a>, die für die ausgewählten Daten ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p><em>SELECT-Anweisung</em></p></td>
<td><p>Eine <a href="select-statement-microsoft-access-sql.md">SELECT</a>-Anweisung.</p></td>
</tr>
<tr class="odd">
<td><p><em>Pivotfeld</em></p></td>
<td><p>Das Feld oder der Ausdruck, das bzw. den Sie zum Erstellen von Spaltenüberschriften im Resultset der Abfrage verwenden möchten.</p></td>
</tr>
<tr class="even">
<td><p><em>Wert1</em>, <em>Wert2</em></p></td>
<td><p>Feste Werte, die zum Erstellen von Spaltenüberschriften verwendet werden.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Bemerkungen

Wenn Sie Daten mithilfe einer Kreuztabellenabfrage zusammenfassen, wählen Sie Werte aus angegebenen Feldern oder Ausdrücken als Spaltenüberschriften aus, sodass Sie Daten in einem kompakteren Format als bei einer Auswahlabfrage anzeigen können.

TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.

Die in *Pivotfeld* zurückgegebenen Werte werden als Spaltenüberschriften im Resultset der Abfrage verwendet. Beispielsweise würde das Pivotieren der Umsatzzahlen auf den Monat des Verkaufs in einer Kreuztabellenabfrage 12 Spalten erzeugen. Sie können *Pivotfeld* einschränken, um Überschriften anhand von festen Werten (*Wert1*, *Wert2*) zu erzeugen, die in der optionalen IN-Klausel aufgeführt sind. Sie können auch feste Werte verwenden, für die keine Daten vorhanden ist, um zusätzliche Spalten zu erstellen.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die SQL TRANSFORM-Klausel zum Erstellen einer Kreuztabellenabfrage verwendet, die die Anzahl der Bestellungen anzeigt, die von jedem Mitarbeiter für jedes Quartals des Jahrs 1994 entgegengenommen wurden. Die SQLTRANSFORMOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub TransformX1() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SHORT; TRANSFORM " _ 
            & "Count(OrderID) " _ 
            & "SELECT FirstName & "" "" & LastName AS " _ 
            & "FullName FROM Employees INNER JOIN Orders " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart " _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
       
           strSQL = strSQL & "GROUP BY FirstName & " _ 
            & """ "" & LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"", OrderDate)" 
         
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub
```

<br/>

In diesem Beispiel wird die SQL TRANSFORM-Klausel zum Erstellen einer etwas komplexeren Kreuztabellenabfrage verwendet, die den Gesamtwert in Dollar der Bestellungen anzeigt, die von jedem Mitarbeiter für jedes Quartals des Jahrs 1994 entgegengenommen wurden. Die SQLTRANSFORMOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.

```vb
    Sub TransformX2() 
     
        Dim dbs As Database 
        Dim strSQL As String 
        Dim qdfTRANSFORM As QueryDef 
     
        strSQL = "PARAMETERS prmYear SMALLINT; TRANSFORM " _ 
            & "Sum(Subtotal) SELECT FirstName & "" """ _ 
            & "& LastName AS FullName " _ 
            & "FROM Employees INNER JOIN " _ 
            & "(Orders INNER JOIN [Order Subtotals] " _ 
            & "ON Orders.OrderID = " _ 
            & "[Order Subtotals].OrderID) " _ 
            & "ON Employees.EmployeeID = " _ 
            & "Orders.EmployeeID WHERE DatePart" _ 
            & "(""yyyy"", OrderDate) = [prmYear] " 
        
           strSQL = strSQL & "GROUP BY FirstName & "" """ _ 
            & "& LastName " _ 
            & "ORDER BY FirstName & "" "" & LastName " _ 
            & "PIVOT DatePart(""q"",OrderDate)"         
             
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        Set qdfTRANSFORM = dbs.CreateQueryDef _ 
            ("", strSQL) 
         
        SQLTRANSFORMOutput qdfTRANSFORM, 1994 
         
        dbs.Close 
     
    End Sub 
     
    Function SQLTRANSFORMOutput(qdfTemp As QueryDef, _ 
        intYear As Integer) 
         
        Dim rstTRANSFORM As Recordset 
        Dim fldLoop As Field 
        Dim booFirst As Boolean 
     
        qdfTemp.PARAMETERS!prmYear = intYear 
        Set rstTRANSFORM = qdfTemp.OpenRecordset() 
         
        Debug.Print qdfTemp.SQL 
        Debug.Print 
        Debug.Print , , "Quarter" 
     
        With rstTRANSFORM 
            booFirst = True 
            For Each fldLoop In .Fields 
                If booFirst = True Then 
                    Debug.Print fldLoop.Name 
                    Debug.Print , ; 
                    booFirst = False 
                Else 
                    Debug.Print , fldLoop.Name; 
                End If 
            Next fldLoop 
            Debug.Print 
             
            Do While Not .EOF 
                booFirst = True 
                For Each fldLoop In .Fields 
                    If booFirst = True Then 
                        Debug.Print fldLoop 
                        Debug.Print , ; 
                        booFirst = False 
                    Else 
                        Debug.Print , fldLoop; 
                    End If 
                Next fldLoop 
                Debug.Print 
                .MoveNext 
            Loop 
        End With 
         
    End Function
```
