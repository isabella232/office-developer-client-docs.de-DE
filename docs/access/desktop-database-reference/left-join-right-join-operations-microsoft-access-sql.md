---
title: LEFT JOIN- und RIGHT JOIN-Operation (Microsoft Access SQL)
TOCTitle: LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)
ms:assetid: 9c10525f-98b1-fd4f-8b40-07a32c5c6502
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198084(v=office.15)
ms:contentKeyID: 48546586
ms.date: 09/18/2015
mtps_version: v=office.15
dev_langs:
- sql
localization_priority: Priority
ms.openlocfilehash: c6e37cd68d586e39a06fd650ccb453f35477253f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290145"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="f7567-102">LEFT JOIN- und RIGHT JOIN-Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="f7567-102">LEFT JOIN, RIGHT JOIN Operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="f7567-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7567-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7567-104">Kombiniert bei Verwendung in einer [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel Datensätze der Herkunftstabellen.</span><span class="sxs-lookup"><span data-stu-id="f7567-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7567-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7567-105">Syntax</span></span>

<span data-ttu-id="f7567-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span><span class="sxs-lookup"><span data-stu-id="f7567-106">FROM *table1* \[ [ LEFT | RIGHT ] JOIN *table2* 
    ON \*table1.field1 \* *compopr table2.field2*</span></span>

<span data-ttu-id="f7567-107">Die Operationen LEFT JOIN und RIGHT JOIN enthalten die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="f7567-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f7567-108">Teil</span><span class="sxs-lookup"><span data-stu-id="f7567-108">Part</span></span></p></th>
<th><p><span data-ttu-id="f7567-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7567-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7567-110"><em>Tabelle1</em>, <em>Tabelle2</em></span><span class="sxs-lookup"><span data-stu-id="f7567-110"><em>table1</em>  ,  <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="f7567-111">Die Namen der Tabellen, aus denen Datensätze zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="f7567-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7567-112"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="f7567-112"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="f7567-p101">Die Namen der verknüpften Felder. Die Felder müssen denselben Datentyp aufweisen und dieselbe Art von Daten enthalten, doch sie müssen nicht denselben Namen tragen.</span><span class="sxs-lookup"><span data-stu-id="f7567-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7567-115"><em>Vergleichsoperator</em></span><span class="sxs-lookup"><span data-stu-id="f7567-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="f7567-116">Ein beliebiger relationaler Vergleichsoperator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; oder &quot;&lt;&gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="f7567-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f7567-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7567-117">Remarks</span></span>

<span data-ttu-id="f7567-p102">Verwenden Sie eine LEFT JOIN-Operation, um eine linke äußere Verknüpfung zu erstellen. Eine linke äußere Verknüpfung enthält alle Datensätze aus der ersten (linken) der beiden Tabellen, selbst wenn die zweite (rechte) Tabelle keine übereinstimmenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="f7567-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="f7567-p103">Verwenden Sie eine RIGHT JOIN-Operation, um eine rechte äußere Verknüpfung zu erstellen. Eine rechte äußere Verknüpfung enthält alle Datensätze aus der zweiten (rechten) der beiden Tabellen, selbst wenn die erste (linke) Tabelle keine übereinstimmenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="f7567-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="f7567-p104">Beispielsweise können Sie LEFT JOIN mit den Tabellen "Abteilungen" (links) und "Mitarbeiter" (rechts) verwenden, um alle Abteilungen auszuwählen, einschließlich der Abteilungen, denen keine Mitarbeiter zugewiesen sind. Um alle Mitarbeiter (einschließlich derjenigen, die keiner Abteilung zugewiesen sind) auszuwählen, verwenden Sie RIGHT JOIN.</span><span class="sxs-lookup"><span data-stu-id="f7567-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="f7567-p105">Das folgende Beispiel zeigt, wie Sie die Tabellen "Categories" und "Products" im Feld "CategoryID" verknüpfen können. Die Abfrage erzeugt eine Liste aller Kategorien, einschließlich derjenigen, die keine Produkte enthalten:</span><span class="sxs-lookup"><span data-stu-id="f7567-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="f7567-126">In diesem Beispiel ist "CategoryID" das verknüpfte Feld, ist aber nicht im Abfrageergebnis enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f7567-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="f7567-127">Um das verknüpfte Feld einzuschließen, geben Sie den Feldnamen in die SELECT-Anweisung ein, in diesem Fall Categories.CategoryID.</span><span class="sxs-lookup"><span data-stu-id="f7567-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="f7567-128">Wenn Sie eine Abfrage erstellen möchten, die nur Datensätze mit jeweils identischen Daten in den verknüpften Feldern enthält, verwenden Sie eine [INNER JOIN](inner-join-operation-microsoft-access-sql.md)-Operation.</span><span class="sxs-lookup"><span data-stu-id="f7567-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="f7567-p107">Eine LEFT JOIN- oder RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, wohingegen eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder RIGHT JOIN-Operation geschachtelt werden kann. Im Thema "INNER JOIN-Operation" erfahren Sie, wie Joins in anderen Joins geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="f7567-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="f7567-p108">Sie können mehrere ON-Klauseln verknüpfen. Im Thema "INNER JOIN-Operation" wird erläutert, wie das Verknüpfen von Klauseln funktioniert.</span><span class="sxs-lookup"><span data-stu-id="f7567-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="f7567-133">Wenn Sie versuchen, Felder mit Memo- oder OLE-Objektdaten zu verknüpfen, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="f7567-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="f7567-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7567-134">Example</span></span>

<span data-ttu-id="f7567-135">In diesem Beispiel:</span><span class="sxs-lookup"><span data-stu-id="f7567-135">This example sets</span></span>
- <span data-ttu-id="f7567-136">Wird davon ausgegangen, dass die Employees-Tabelle die hypothetischen Felder Department Name und Department ID enthält.</span><span class="sxs-lookup"><span data-stu-id="f7567-136">This example assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="f7567-137">Beachten Sie, dass diese Felder nicht in der Mitarbeitertabelle der Northwind-Datenbank vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f7567-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="f7567-138">Es werden alle Abteilungen ausgewählt, auch die Abteilungen ohne Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="f7567-138">This example selects all departments, including those without employees.</span></span>

- <span data-ttu-id="f7567-139">Die EnumFields-Prozedur wird aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f7567-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.

</span></span>


```vb
    Sub LeftRightJoinX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Select all departments, including those  
        ' without employees. 
        Set rst = dbs.OpenRecordset _ 
            ("SELECT [Department Name], " _ 
            & "FirstName & Chr(32) & LastName AS Name " _ 
            & "FROM Departments LEFT JOIN Employees " _ 
            & "ON Departments.[Department ID] = " _ 
            & "Employees.[Department ID] " _ 
            & "ORDER BY [Department Name];") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 20 
     
        dbs.Close 
     
    End Sub
```
