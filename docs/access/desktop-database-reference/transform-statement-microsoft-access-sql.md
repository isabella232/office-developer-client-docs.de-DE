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
ms.openlocfilehash: 16b88f2cf441802c6246425d5bb7bb2efb71a679
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861218"
---
# <a name="transform-statement-microsoft-access-sql"></a>TRANSFORM-Anweisung (Microsoft Access SQL)

**Betrifft**: Access 2013 | Office 2013

Erstellt eine Kreuztabellenabfrage.

## <a name="syntax"></a>Syntax

TRANSFORM *aggregatfunktionselect-Anweisung* PIVOT *Pivotfield* \[IN (*Wert1*\[, *Wert2*\[,... \]\])\]

Die TRANSFORM-Anweisung besteht aus folgenden Teilen:

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
<td><p><em>AggFunktion</em></p></td>
<td><p>Eine <a href="sql-aggregate-functions-sql.md">SQL-Aggregatfunktion</a>, die für die ausgewählten Daten ausgeführt wird.</p></td>
</tr>
<tr class="even">
<td><p><em>SelectAnweisung</em></p></td>
<td><p>Eine <a href="select-statement-microsoft-access-sql.md">SELECT</a>-Anweisung.</p></td>
</tr>
<tr class="odd">
<td><p><em>PivotFeld</em></p></td>
<td><p>Das Feld oder der Ausdruck, das bzw. den Sie zum Erstellen von Spaltenüberschriften im Resultset der Abfrage verwenden möchten.</p></td>
</tr>
<tr class="even">
<td><p><em>Wert1</em>, <em>Wert2</em></p></td>
<td><p>Feste Werte, die zum Erstellen von Spaltenüberschriften verwendet werden.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Wenn Sie Daten mithilfe einer Kreuztabellenabfrage zusammenfassen, wählen Sie Werte aus angegebenen Feldern oder Ausdrücken als Spaltenüberschriften aus, sodass Sie Daten in einem kompakteren Format als bei einer Auswahlabfrage anzeigen können.

TRANSFORM ist eine optionale Anweisung, aber wenn sie verwendet wird, ist sie die erste Anweisung in einer SQL-Zeichenfolge. Sie steht vor einer SELECT-Anweisung, die die Felder angibt, die als Zeilenüberschriften verwendet werden, und einer GROUP BY-Klausel, die die Zeilengruppierung angibt. Optional können Sie andere Klauseln einschließen, z. B. WHERE-Klauseln, die zusätzliche Auswahl- oder Sortierkriterien angeben. Sie können auch Unterabfragen als Prädikate in einer Kreuztabellenabfrage verwenden – insbesondere die in der WHERE-Klausel.

Die im *PivotFeld* zurückgegebenen Werte werden als Spaltenüberschriften im Resultset der Abfrage verwendet. Wenn Sie z. B. die Verkaufszahlen des Verkaufsmonats in einer Kreuztabellenabfrage pivotieren, werden 12 Spalten erstellt. Sie können das *PivotFeld* darauf beschränken, Überschriften aus festen Werten (*Wert1*, *Wert2*) zu erstellen, die in der optionalen IN-Klausel aufgeführt sind. Außerdem können Sie feste Werte einschließen, für die keine Daten vorhanden sind, um zusätzliche Spalten zu erstellen.

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
