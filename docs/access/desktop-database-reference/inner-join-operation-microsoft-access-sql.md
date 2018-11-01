---
title: INNER JOIN-Operation (Microsoft Access SQL)
TOCTitle: INNER JOIN Operation (Microsoft Access SQL)
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
ms.openlocfilehash: 874f685a1db38c4a381f08289cb0c612e7e2eb4c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888895"
---
# <a name="inner-join-operation-microsoft-access-sql"></a><span data-ttu-id="0a2f2-102">INNER JOIN-Operation (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0a2f2-102">INNER JOIN Operation (Microsoft Access SQL)</span></span>


<span data-ttu-id="0a2f2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a2f2-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="0a2f2-104">Fasst Datensätze aus zwei Tabellen zusammen, wenn in einem gemeinsamen Feld entsprechende Datensätze enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-104">Combines records from two tables whenever there are matching values in a common field.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a2f2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a2f2-105">Syntax</span></span>

<span data-ttu-id="0a2f2-106">AUS *Tabelle1* INNER JOIN *Tabelle2* für *Tabelle1*. *Feld1* *Compopr Tabelle2*. *Field2*</span><span class="sxs-lookup"><span data-stu-id="0a2f2-106">FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr table2*.*field2*</span></span>

<span data-ttu-id="0a2f2-107">Die INNER JOIN-Operation besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="0a2f2-107">The INNER JOIN operation has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a2f2-108">Teil</span><span class="sxs-lookup"><span data-stu-id="0a2f2-108">Part</span></span></p></th>
<th><p><span data-ttu-id="0a2f2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a2f2-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a2f2-110"><em>Tabelle1</em>, <em>Tabelle2</em></span><span class="sxs-lookup"><span data-stu-id="0a2f2-110"><em>table1</em>, <em>table2</em></span></span></p></td>
<td><p><span data-ttu-id="0a2f2-111">Die Namen der Tabellen, deren Datensätze kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-111">The names of the tables from which records are combined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a2f2-112"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="0a2f2-112"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="0a2f2-p101">Die Namen der Felder, die verknüpft werden. Wenn es sich nicht um numerische Felder handelt, müssen sie über den gleichen Datentyp verfügen und die gleich Art von Daten enthalten. Die Felder müssen aber nicht über den gleichen Namen verfügen.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p101">The names of the fields that are joined. If they are not numeric, the fields must be of the same data type and contain the same kind of data, but they do not have to have the same name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a2f2-115"><em>Vergleichsoperator</em></span><span class="sxs-lookup"><span data-stu-id="0a2f2-115"><em>compopr</em></span></span></p></td>
<td><p><span data-ttu-id="0a2f2-116">Ein beliebiger Vergleichsoperator: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; oder &quot; &lt; &gt;.&quot;</span><span class="sxs-lookup"><span data-stu-id="0a2f2-116">Any relational comparison operator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; or &quot;&lt;&gt;.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0a2f2-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a2f2-117">Remarks</span></span>

<span data-ttu-id="0a2f2-p102">Sie können eine INNER JOIN-Operation in jeder [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\))-Klausel verwenden. Hierbei handelt es sich um den Verknüpfungstyp, der im Allgemeinen verwendet wird. Innere Verknüpfungen fassen Datensätze aus zwei Tabellen zusammen, wenn sich in Feldern, die in beiden Tabellen enthalten sind, übereinstimmende Werte befinden.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p102">You can use an INNER JOIN operation in any [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\)) clause. This is the most common type of join. Inner joins combine records from two tables whenever there are matching values in a field common to both tables.</span></span>

<span data-ttu-id="0a2f2-p103">Sie können die INNER JOIN-Operation in Kombination mit der Departments-Tabelle (Abteilungen) und der Employees-Tabelle (Personal) verwenden, um alle Mitarbeiter in jeder Abteilung auszuwählen. Umgekehrt können Sie eine LEFT JOIN- oder RIGHT JOIN-Operation zur Erstellung einer äußeren Verknüpfung verwenden, um alle Abteilungen (selbst wenn den Abteilungen kein Personal zugewiesen wurde) oder das gesamte Personal (selbst wenn einige Mitarbeiter keiner Abteilung zugewiesen wurden) auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p103">You can use INNER JOIN with the Departments and Employees tables to select all the employees in each department. In contrast, to select all departments (even if some have no employees assigned to them) or all employees (even if some are not assigned to a department), you can use a [LEFT JOIN or RIGHT JOIN](left-join-right-join-operations-microsoft-access-sql.md) operation to create an outer join.</span></span>

<span data-ttu-id="0a2f2-123">Wenn Sie versuchen, Felder zu verknüpfen, die Daten vom Typ Memo oder OLE-Objekt enthalten, wird ein Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-123">If you try to join fields containing Memo or OLE Object data, an error occurs.</span></span>

<span data-ttu-id="0a2f2-p104">Sie können zwei beliebige numerische Felder vom Typ LIKE miteinander verknüpfen. So können beispielsweise Felder vom Datentyp AutoWert und Long verknüpft werden, da es sich in beiden Fällen um Felder vom Typ LIKE handelt. Felder vom Datentyp Single und Double können dagegen nicht miteinander verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p104">You can join any two numeric fields of like types. For example, you can join on AutoNumber and Long fields because they are like types. However, you cannot join Single and Double types of fields.</span></span>

<span data-ttu-id="0a2f2-127">Im folgenden Beispiel wird gezeigt, wie die Categories-Tabelle (Kategorien) und die Products-Tabelle (Artikel) über das CategoryID-Feld (Kategorie-Nr.) verknüpft werden können:</span><span class="sxs-lookup"><span data-stu-id="0a2f2-127">The following example shows how you could join the Categories and Products tables on the CategoryID field:</span></span>

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

<span data-ttu-id="0a2f2-128">Klicken Sie im vorstehenden Beispiel CategoryID ist das verknüpfte Feld, aber es ist nicht in den Abfrageergebnissen enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md) -Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-128">In the preceding example, CategoryID is the joined field, but it is not included in the query output because it is not included in the [SELECT](select-statement-microsoft-access-sql.md) statement.</span></span> <span data-ttu-id="0a2f2-129">Der Name des Felds in der SELECT-Anweisung zum Einbeziehen von verknüpften Felds einschließen – in diesem Fall also Kategorien.Kategorie-Nr..</span><span class="sxs-lookup"><span data-stu-id="0a2f2-129">To include the joined field, include the field name in the SELECT statement — in this case, Categories.CategoryID.</span></span>

<span data-ttu-id="0a2f2-130">Sie können unter Verwendung der folgenden Syntax auch verschiedene ON-Klauseln in einer JOIN-Anweisung verknüpfen:</span><span class="sxs-lookup"><span data-stu-id="0a2f2-130">You can also link several ON clauses in a JOIN statement, using the following syntax:</span></span>

<span data-ttu-id="0a2f2-131">Wählen SIE die *Felder* FROM *Tabelle1* INNER JOIN *Tabelle2* ON *Tabelle1*. *Feld1* *compopr* *Tabelle2*. *Feld1* UND für *Tabelle1*. *Field2* *compopr* *Tabelle2*. *field2*) ODER klicken Sie auf *Tabelle1*. *feld3* *compopr* *Tabelle2*. *feld3*) \];</span><span class="sxs-lookup"><span data-stu-id="0a2f2-131">SELECT *fields* FROM *table1* INNER JOIN *table2* ON *table1*.*field1* *compopr* *table2*.*field1* AND ON *table1*.*field2* *compopr* *table2*.*field2*) OR ON *table1*.*field3* *compopr* *table2*.*field3*)\];</span></span>

<span data-ttu-id="0a2f2-132">Sie können unter Verwendung der folgenden Syntax JOIN-Anweisungen auch schachteln:</span><span class="sxs-lookup"><span data-stu-id="0a2f2-132">You can also nest JOIN statements using the following syntax:</span></span>

<span data-ttu-id="0a2f2-133">Wählen Sie *Felder* FROM *Tabelle1* INNER JOIN (*Tabelle2* INNER JOIN \[( \] *Tabelle3* \[INNER JOIN \[( \] *tabellex* \[INNER JOIN...) \] Auf *Tabelle3*. *feld3* *compopr* *tabellex*. *Fieldx*) \] Für *Tabelle2*. *Field2* *compopr* *Tabelle3*. *feld3*) FÜR *Tabelle1*. *Feld1* *compopr* *Tabelle2*. *Feld2*;</span><span class="sxs-lookup"><span data-stu-id="0a2f2-133">SELECT *fields* FROM *table1* INNER JOIN (*table2* INNER JOIN \[( \]*table3* \[INNER JOIN \[( \]*tablex* \[INNER JOIN …)\] ON *table3*.*field3* *compopr* *tablex*.*fieldx*)\] ON *table2*.*field2* *compopr* *table3*.*field3*) ON *table1*.*field1* *compopr* *table2*.*field2*;</span></span>

<span data-ttu-id="0a2f2-134">Eine LEFT JOIN- oder eine RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, aber umgekehrt kann eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder einen RIGHT JOIN-Operation geschachtelt werden.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-134">A LEFT JOIN or a RIGHT JOIN may be nested inside an INNER JOIN, but an INNER JOIN may not be nested inside a LEFT JOIN or a RIGHT JOIN.</span></span>

## <a name="example"></a><span data-ttu-id="0a2f2-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0a2f2-135">Example</span></span>

<span data-ttu-id="0a2f2-p106">Im folgenden Beispiel werden zwei gleichwertige Verknüpfungen erstellt: eine Verknüpfung zwischen der Order Details-Tabelle (Bestelldetails) und der Orders-Tabelle (Bestellungen) und eine andere Verknüpfung zwischen der Orders-Tabelle und der Employees-Tabelle (Personal). Dies ist erforderlich, weil die Employees-Tabelle keine Verkaufsdaten und die Order Details-Tabelle keine Personaldaten enthält. Die Abfrage gibt eine Liste der Mitarbeiter unter Aufführung ihrer Gesamtverkäufe zurück.  
</span><span class="sxs-lookup"><span data-stu-id="0a2f2-p106">This example creates two equi-joins: one between the Order Details and Orders tables and another between the Orders and Employees tables. This is necessary because the Employees table does not contain sales data, and the Order Details table does not contain employee data. The query produces a list of employees and their total sales.</span></span>

<span data-ttu-id="0a2f2-139">In diesem Beispiel wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0a2f2-139">This example calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

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
