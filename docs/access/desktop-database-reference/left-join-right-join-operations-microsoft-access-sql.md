---
title: LEFT JOIN-, RIGHT JOIN-Operationen (Microsoft Access SQL)
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704721"
---
# <a name="left-join-right-join-operations-microsoft-access-sql"></a><span data-ttu-id="31313-102">LEFT JOIN-, RIGHT JOIN-Operationen (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="31313-102">LEFT JOIN, RIGHT JOIN operations (Microsoft Access SQL)</span></span>

<span data-ttu-id="31313-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="31313-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="31313-104">Kombiniert bei Verwendung in einer [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel Datensätze der Herkunftstabellen.</span><span class="sxs-lookup"><span data-stu-id="31313-104">Combines source-table records when used in any [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="31313-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31313-105">Syntax</span></span>

<span data-ttu-id="31313-106">FROM *Tabelle1* \[ links | RECHTS \] JOIN *Tabelle2* ON Tabelle2 *table1.field1* *Compopr Tabelle2. Feld2* .</span><span class="sxs-lookup"><span data-stu-id="31313-106">FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*</span></span>

<span data-ttu-id="31313-107">Die Operationen LEFT JOIN und RIGHT JOIN enthalten die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="31313-107">The LEFT JOIN and RIGHT JOIN operations have these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31313-108">Teil</span><span class="sxs-lookup"><span data-stu-id="31313-108">Part</span></span></p></th>
<th><p><span data-ttu-id="31313-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31313-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31313-110"><em>Tabelle1</em>, <em>Tabelle2</em></span><span class="sxs-lookup"><span data-stu-id="31313-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="31313-111">Die Namen der Tabellen, deren Datensätze kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="31313-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31313-112"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="31313-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="31313-p101">Die Namen der verknüpften Felder. Die Felder müssen denselben Datentyp aufweisen und dieselbe Art von Daten enthalten, doch sie müssen nicht denselben Namen tragen.</span><span class="sxs-lookup"><span data-stu-id="31313-p101">The names of the fields that are joined. The fields must be of the same data type and contain the same kind of data, but they do not need to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31313-115"><em>Vergleichsoperator</em></span><span class="sxs-lookup"><span data-stu-id="31313-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="31313-116">Ein beliebiger Vergleichsoperator: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; oder &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="31313-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="31313-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31313-117">Remarks</span></span>

<span data-ttu-id="31313-p102">Verwenden Sie eine LEFT JOIN-Operation, um eine linke äußere Verknüpfung zu erstellen. Eine linke äußere Verknüpfung enthält alle Datensätze aus der ersten (linken) der beiden Tabellen, selbst wenn die zweite (rechte) Tabelle keine übereinstimmenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="31313-p102">Use a LEFT JOIN operation to create a left outer join. Left outer joins include all of the records from the first (left) of two tables, even if there are no matching values for records in the second (right) table.</span></span>

<span data-ttu-id="31313-p103">Verwenden Sie eine RIGHT JOIN-Operation, um eine rechte äußere Verknüpfung zu erstellen. Eine rechte äußere Verknüpfung enthält alle Datensätze aus der zweiten (rechten) der beiden Tabellen, selbst wenn die erste (linke) Tabelle keine übereinstimmenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="31313-p103">Use a RIGHT JOIN operation to create a right outer join. Right outer joins include all of the records from the second (right) of two tables, even if there are no matching values for records in the first (left) table.</span></span>

<span data-ttu-id="31313-p104">Sie können z. B. eine LEFT JOIN-Operation für die Tabellen Departments (links) und Employees (rechts) verwenden, um alle Abteilungen auszuwählen, einschließlich Abteilungen, denen keine Mitarbeiter zugewiesen sind. Wenn Sie alle Mitarbeiter auswählen möchten, einschließlich Mitarbeitern, die keiner Abteilung zugewiesen sind, verwenden Sie die RIGHT JOIN-Operation.</span><span class="sxs-lookup"><span data-stu-id="31313-p104">For example, you could use LEFT JOIN with the Departments (left) and Employees (right) tables to select all departments, including those that have no employees assigned to them. To select all employees, including those who are not assigned to a department, you would use RIGHT JOIN.</span></span>

<span data-ttu-id="31313-p105">Im folgenden Beispiel wird gezeigt, wie Sie die Tabellen Categories und Products für das Feld CategoryID verknüpfen. Die Abfrage erzeugt eine Liste aller Kategorien, einschließlich der Kategorien, die keine Produkte enthalten:</span><span class="sxs-lookup"><span data-stu-id="31313-p105">The following example shows how you could join the Categories and Products tables on the CategoryID field. The query produces a list of all categories, including those that contain no products:</span></span>

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="31313-126">In diesem Beispiel ist "CategoryID" das verknüpfte Feld, ist aber nicht im Abfrageergebnis enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="31313-126">In this example, CategoryID is the joined field, but it is not included in the query results because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="31313-127">Geben Sie zum Einbeziehen von verknüpften Felds der Name des Felds in der SELECT-Anweisung – in diesem Fall also Kategorien.Kategorie-Nr..</span><span class="sxs-lookup"><span data-stu-id="31313-127">To include the joined field, enter the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

> [!NOTE]
> - <span data-ttu-id="31313-128">Wenn Sie eine Abfrage erstellen möchten, die nur Datensätze mit jeweils identischen Daten in den verknüpften Feldern enthält, verwenden Sie eine [INNER JOIN](inner-join-operation-microsoft-access-sql.md)-Operation.</span><span class="sxs-lookup"><span data-stu-id="31313-128">To create a query that includes only records in which the data in the joined fields is the same, use an [INNER JOIN](inner-join-operation-microsoft-access-sql.md) operation.</span></span>
> - <span data-ttu-id="31313-p107">Eine LEFT JOIN- bzw. eine RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt sein, doch eine INNER JOIN-Operation kann nicht in einer LEFT JOIN- oder einer RIGHT JOIN-Operation geschachtelt sein. Informationen zum Schachteln von Verknüpfungen finden Sie in der Erläuterung zum Schachteln im Thema zur INNER JOIN-Operation.</span><span class="sxs-lookup"><span data-stu-id="31313-p107">A LEFT JOIN or a RIGHT JOIN can be nested inside an INNER JOIN, but an INNER JOIN cannot be nested inside a LEFT JOIN or a RIGHT JOIN. See the discussion of nesting in the INNER JOIN topic to see how to nest joins within other joins.</span></span>
> - <span data-ttu-id="31313-p108">Sie können mehrere ON-Klauseln verknüpfen. Entsprechende Informationen finden Sie in der Erläuterung zum Verknüpfen von Klauseln im Thema zur INNER JOIN-Operation.</span><span class="sxs-lookup"><span data-stu-id="31313-p108">You can link multiple ON clauses. See the discussion of clause linking in the INNER JOIN topic to see how this is done.</span></span>
> - <span data-ttu-id="31313-133">Wenn Sie Felder verknüpfen, die Memo- oder OLE-Objektdaten enthalten, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="31313-133">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="31313-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="31313-134">Example</span></span>

<span data-ttu-id="31313-135">In diesem Beispiel wird:</span><span class="sxs-lookup"><span data-stu-id="31313-135">This example:</span></span>
- <span data-ttu-id="31313-136">Setzt das Vorhandensein von hypothetische Abteilungsnamen und Department ID Felder in einer Tabelle Employees.</span><span class="sxs-lookup"><span data-stu-id="31313-136">Assumes the existence of hypothetical Department Name and Department ID fields in an Employees table.</span></span> <span data-ttu-id="31313-137">Beachten Sie, dass diese Felder nicht tatsächlich in die Employees-Tabelle der Northwind-Datenbank vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="31313-137">Note that these fields do not actually exist in the Northwind database Employees table.</span></span>

- <span data-ttu-id="31313-138">Wählt alle Abteilungen, einschließlich derjenigen ohne Mitarbeiter.</span><span class="sxs-lookup"><span data-stu-id="31313-138">Selects all departments, including those without employees.</span></span>

- <span data-ttu-id="31313-139">Ruft die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.</span><span class="sxs-lookup"><span data-stu-id="31313-139">Calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>


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
