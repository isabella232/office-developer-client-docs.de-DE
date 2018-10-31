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
# <a name="transform-statement-microsoft-access-sql"></a><span data-ttu-id="b7a42-102">TRANSFORM-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b7a42-102">TRANSFORM statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b7a42-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7a42-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b7a42-104">Erstellt eine Kreuztabellenabfrage.</span><span class="sxs-lookup"><span data-stu-id="b7a42-104">Creates a crosstab query.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7a42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7a42-105">Syntax</span></span>

<span data-ttu-id="b7a42-106">TRANSFORM *aggregatfunktionselect-Anweisung* PIVOT *Pivotfield* \[IN (*Wert1*\[, *Wert2*\[,... \]\])\]</span><span class="sxs-lookup"><span data-stu-id="b7a42-106">TRANSFORM *aggfunctionselectstatement* PIVOT *pivotfield* \[IN (*value1*\[, *value2*\[, …\]\])\]</span></span>

<span data-ttu-id="b7a42-107">Die TRANSFORM-Anweisung besteht aus folgenden Teilen:</span><span class="sxs-lookup"><span data-stu-id="b7a42-107">The TRANSFORM statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b7a42-108">Komponente</span><span class="sxs-lookup"><span data-stu-id="b7a42-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b7a42-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7a42-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7a42-110"><em>AggFunktion</em></span><span class="sxs-lookup"><span data-stu-id="b7a42-110"><em>aggfunction</em></span></span></p></td>
<td><p><span data-ttu-id="b7a42-111">Eine <a href="sql-aggregate-functions-sql.md">SQL-Aggregatfunktion</a>, die für die ausgewählten Daten ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b7a42-111">An <a href="sql-aggregate-functions-sql.md">SQL aggregate function</a> that operates on the selected data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a42-112"><em>SelectAnweisung</em></span><span class="sxs-lookup"><span data-stu-id="b7a42-112"><em>selectstatement</em></span></span></p></td>
<td><p><span data-ttu-id="b7a42-113">Eine <a href="select-statement-microsoft-access-sql.md">SELECT</a>-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b7a42-113">A <a href="select-statement-microsoft-access-sql.md">SELECT</a> statement.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7a42-114"><em>PivotFeld</em></span><span class="sxs-lookup"><span data-stu-id="b7a42-114"><em>pivotfield</em></span></span></p></td>
<td><p><span data-ttu-id="b7a42-115">Das Feld oder der Ausdruck, das bzw. den Sie zum Erstellen von Spaltenüberschriften im Resultset der Abfrage verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="b7a42-115">The field or expression you want to use to create column headings in the query's result set.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7a42-116"><em>Wert1</em>, <em>Wert2</em></span><span class="sxs-lookup"><span data-stu-id="b7a42-116"><em>value1</em>, <em>value2</em></span></span></p></td>
<td><p><span data-ttu-id="b7a42-117">Feste Werte, die zum Erstellen von Spaltenüberschriften verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7a42-117">Fixed values used to create column headings.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="b7a42-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b7a42-118">Remarks</span></span>

<span data-ttu-id="b7a42-119">Wenn Sie Daten mithilfe einer Kreuztabellenabfrage zusammenfassen, wählen Sie Werte aus angegebenen Feldern oder Ausdrücken als Spaltenüberschriften aus, sodass Sie Daten in einem kompakteren Format als bei einer Auswahlabfrage anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="b7a42-119">When you summarize data using a crosstab query, you select values from specified fields or expressions as column headings so you can view data in a more compact format than with a select query.</span></span>

<span data-ttu-id="b7a42-p101">TRANSFORM ist eine optionale Anweisung, aber wenn sie verwendet wird, ist sie die erste Anweisung in einer SQL-Zeichenfolge. Sie steht vor einer SELECT-Anweisung, die die Felder angibt, die als Zeilenüberschriften verwendet werden, und einer GROUP BY-Klausel, die die Zeilengruppierung angibt. Optional können Sie andere Klauseln einschließen, z. B. WHERE-Klauseln, die zusätzliche Auswahl- oder Sortierkriterien angeben. Sie können auch Unterabfragen als Prädikate in einer Kreuztabellenabfrage verwenden – insbesondere die in der WHERE-Klausel.</span><span class="sxs-lookup"><span data-stu-id="b7a42-p101">TRANSFORM is optional but when included is the first statement in an SQL string. It precedes a SELECT statement that specifies the fields used as row headings and a [GROUP BY](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/group-by-clause-microsoft-access-sql) clause that specifies row grouping. Optionally, you can include other clauses, such as [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql), that specify additional selection or sorting criteria. You can also use subqueries as predicates — specifically, those in the WHERE clause — in a crosstab query.</span></span>

<span data-ttu-id="b7a42-p102">Die im *PivotFeld* zurückgegebenen Werte werden als Spaltenüberschriften im Resultset der Abfrage verwendet. Wenn Sie z. B. die Verkaufszahlen des Verkaufsmonats in einer Kreuztabellenabfrage pivotieren, werden 12 Spalten erstellt. Sie können das *PivotFeld* darauf beschränken, Überschriften aus festen Werten (*Wert1*, *Wert2*) zu erstellen, die in der optionalen IN-Klausel aufgeführt sind. Außerdem können Sie feste Werte einschließen, für die keine Daten vorhanden sind, um zusätzliche Spalten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b7a42-p102">The values returned in *pivotfield* are used as column headings in the query's result set. For example, pivoting the sales figures on the month of the sale in a crosstab query would create 12 columns. You can restrict *pivotfield* to create headings from fixed values (*value1*, *value2* ) listed in the optional IN clause. You can also include fixed values for which no data exists to create additional columns.</span></span>

## <a name="example"></a><span data-ttu-id="b7a42-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b7a42-128">Example</span></span>

<span data-ttu-id="b7a42-p103">In diesem Beispiel wird die SQL TRANSFORM-Klausel zum Erstellen einer Kreuztabellenabfrage verwendet, die die Anzahl der Bestellungen anzeigt, die von jedem Mitarbeiter für jedes Quartals des Jahrs 1994 entgegengenommen wurden. Die SQLTRANSFORMOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7a42-p103">This example uses the SQL TRANSFORM clause to create a crosstab query showing the number of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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

<span data-ttu-id="b7a42-p104">In diesem Beispiel wird die SQL TRANSFORM-Klausel zum Erstellen einer etwas komplexeren Kreuztabellenabfrage verwendet, die den Gesamtwert in Dollar der Bestellungen anzeigt, die von jedem Mitarbeiter für jedes Quartals des Jahrs 1994 entgegengenommen wurden. Die SQLTRANSFORMOutput-Funktion ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b7a42-p104">This example uses the SQL TRANSFORM clause to create a slightly more complex crosstab query showing the total dollar amount of orders taken by each employee for each calendar quarter of 1994. The SQLTRANSFORMOutput function is required for this procedure to run.</span></span>

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
