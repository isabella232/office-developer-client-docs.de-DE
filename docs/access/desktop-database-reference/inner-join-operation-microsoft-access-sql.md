---
title: INNER JOIN-Operation (Microsoft Access SQL)
TOCTitle: INNER JOIN operation (Microsoft Access SQL)
ms:assetid: 8d16c74c-02c6-12b7-b180-3e7744ef65f3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197346(v=office.15)
ms:contentKeyID: 48546247
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277574
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: d865d005604ed7422c8e33ff8508551b720c30ba
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734217"
---
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN-Operation (Microsoft Access SQL)


**Gilt für**: Access 2013, Office 2013


Kombiniert Datensätze aus zwei Tabellen, wenn in einem gemeinsamen Feld übereinstimmende Werte vorhanden sind.

## <a name="syntax"></a>Syntax

FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*

Die INNER JOIN-Operation besteht aus folgenden Komponenten:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Teil</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Tabelle1</em>, <em>Tabelle2</em></p></td>
<td><p>Die Namen der Tabellen, aus denen Datensätze zusammengefasst werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der Felder, die verknüpft werden. Wenn es sich nicht um numerische Felder handelt, müssen sie über den gleichen Datentyp verfügen und die gleich Art von Daten enthalten. Die Felder müssen aber nicht über den gleichen Namen verfügen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Vergleichsoperator</em></p></td>
<td><p>Ein beliebiger relationaler Vergleichsoperator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; oder &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können eine INNER JOIN-Operation in jeder [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel verwenden. Hierbei handelt es sich um den Verknüpfungstyp, der im Allgemeinen verwendet wird. Innere Verknüpfungen fassen Datensätze aus zwei Tabellen zusammen, wenn sich in Feldern, die in beiden Tabellen enthalten sind, übereinstimmende Werte befinden.

You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.

Wenn Sie versuchen, Felder mit Memo- oder OLE-Objektdaten zu verknüpfen, tritt ein Fehler auf.

Sie können zwei beliebige numerische Felder gleicher Art miteinander verknüpfen. Sie können z. B. eine Verknüpfung anhand von "AutoNumber"- und "Long"-Feldern vornehmen, da diese gleicher Art sind. Es ist jedoch nicht möglich, Felder der Typen "Single" und "Double" zu verknüpfen.

Das folgende Beispiel zeigt, wie Sie die Tabellen "Categories" und "Products" anhand des Felds "CategoryID" verknüpfen können.

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Im vorigen Beispiel ist "CategoryID" das verknüpfte Feld, wird aber nicht in die Abfrageausgabe einbezogen, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist. Um das verknüpfte Feld einzuschließen, geben Sie den Feldnamen in die SELECT-Anweisung ein, in diesem Fall Categories.CategoryID.

Sie können auch mehrere ON-Klauseln in einer JOIN-Anweisung mit der folgenden Syntax verknüpfen:

SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;

Sie können JOIN-Anweisungen auch mithilfe der folgenden Syntax schachteln:

SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;

Eine LEFT JOIN- oder RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, wohingegen eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder RIGHT JOIN-Operation geschachtelt werden kann.

## <a name="example"></a>Beispiel

This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.

In diesem Beispiel wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.

```vb
    Sub InnerJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Create a join between the Order Details and  
        ' Orders tables and another between the Orders and  
        ' Employees tables. Get a list of employees and  
        ' their total sales. 
        Set rst = dbs.OpenRecordset("SELECT DISTINCTROW " _ 
            & "Sum(UnitPrice * Quantity) AS Sales, " _ 
            & "(FirstName & Chr(32) & LastName) AS Name " _ 
            & "FROM Employees INNER JOIN(Orders " _ 
            & "INNER JOIN [Order Details] " _ 
            & "ON [Order Details].OrderID = " _ 
            & "Orders.OrderID ) " _ 
            & "ON Orders.EmployeeID = " _ 
            & "Employees.EmployeeID " _ 
            & "GROUP BY (FirstName & Chr(32) & LastName);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
