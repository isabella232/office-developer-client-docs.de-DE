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
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="b707c-102">INNER JOIN-Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b707c-102">INNER JOIN operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="b707c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b707c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b707c-104">Kombiniert Datensätze aus zwei Tabellen, wenn in einem gemeinsamen Feld übereinstimmende Werte vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b707c-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="b707c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b707c-105">Syntax</span></span>

<span data-ttu-id="b707c-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span><span class="sxs-lookup"><span data-stu-id="b707c-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="b707c-107">Die INNER JOIN-Operation besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="b707c-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b707c-108">Teil</span><span class="sxs-lookup"><span data-stu-id="b707c-108">Part</span></span></p></th>
<th><p><span data-ttu-id="b707c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b707c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b707c-110"><em>Tabelle1</em>, <em>Tabelle2</em></span><span class="sxs-lookup"><span data-stu-id="b707c-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="b707c-111">Die Namen der Tabellen, aus denen Datensätze zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="b707c-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b707c-112"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="b707c-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b707c-p101">Die Namen der Felder, die verknüpft werden. Wenn es sich nicht um numerische Felder handelt, müssen sie über den gleichen Datentyp verfügen und die gleich Art von Daten enthalten. Die Felder müssen aber nicht über den gleichen Namen verfügen.</span><span class="sxs-lookup"><span data-stu-id="b707c-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b707c-115"><em>Vergleichsoperator</em></span><span class="sxs-lookup"><span data-stu-id="b707c-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="b707c-116">Ein beliebiger relationaler Vergleichsoperator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; oder &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="b707c-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b707c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b707c-117">Remarks</span></span>

<span data-ttu-id="b707c-p102">Sie können eine INNER JOIN-Operation in jeder [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel verwenden. Hierbei handelt es sich um den Verknüpfungstyp, der im Allgemeinen verwendet wird. Innere Verknüpfungen fassen Datensätze aus zwei Tabellen zusammen, wenn sich in Feldern, die in beiden Tabellen enthalten sind, übereinstimmende Werte befinden.</span><span class="sxs-lookup"><span data-stu-id="b707c-p102">You can use an INNER JOIN operation in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="b707c-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span><span class="sxs-lookup"><span data-stu-id="b707c-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="b707c-123">Wenn Sie versuchen, Felder mit Memo- oder OLE-Objektdaten zu verknüpfen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b707c-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="b707c-p104">Sie können zwei beliebige numerische Felder gleicher Art miteinander verknüpfen. Sie können z. B. eine Verknüpfung anhand von "AutoNumber"- und "Long"-Feldern vornehmen, da diese gleicher Art sind. Es ist jedoch nicht möglich, Felder der Typen "Single" und "Double" zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="b707c-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="b707c-127">Das folgende Beispiel zeigt, wie Sie die Tabellen "Categories" und "Products" anhand des Felds "CategoryID" verknüpfen können.</span><span class="sxs-lookup"><span data-stu-id="b707c-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="b707c-128">Im vorigen Beispiel ist "CategoryID" das verknüpfte Feld, wird aber nicht in die Abfrageausgabe einbezogen, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b707c-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="b707c-129">Um das verknüpfte Feld einzuschließen, geben Sie den Feldnamen in die SELECT-Anweisung ein, in diesem Fall Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="b707c-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="b707c-130">Sie können auch mehrere ON-Klauseln in einer JOIN-Anweisung mit der folgenden Syntax verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="b707c-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="b707c-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span><span class="sxs-lookup"><span data-stu-id="b707c-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND *table1*.*field2* *compopr* *table2*.*field2* OR *table1*.*field3* *compopr* *table2*.*field3*;</span></span>

<span data-ttu-id="b707c-132">Sie können JOIN-Anweisungen auch mithilfe der folgenden Syntax schachteln:</span><span class="sxs-lookup"><span data-stu-id="b707c-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="b707c-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span><span class="sxs-lookup"><span data-stu-id="b707c-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="b707c-134">Eine LEFT JOIN- oder RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, wohingegen eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder RIGHT JOIN-Operation geschachtelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b707c-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="b707c-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b707c-135">Example</span></span>

<span data-ttu-id="b707c-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span><span class="sxs-lookup"><span data-stu-id="b707c-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="b707c-139">In diesem Beispiel wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b707c-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
