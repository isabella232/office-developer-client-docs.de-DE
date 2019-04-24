---
title: SQL-Unterabfragen (Microsoft Access SQL)
TOCTitle: SQL subqueries (Microsoft Access SQL)
ms:assetid: 3b6c0a5d-ab24-e1cf-0175-3f8e68c2dfbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192664(v=office.15)
ms:contentKeyID: 48544285
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277580
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 7beda04d1f18014101f00078de1d125c1fd67a69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314567"
---
# <a name="sql-subqueries-microsoft-access-sql"></a><span data-ttu-id="1b7ab-102">SQL-Unterabfragen (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1b7ab-102">SQL Subqueries (Microsoft Access SQL)</span></span>


<span data-ttu-id="1b7ab-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b7ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b7ab-104">Eine Unterabfrage ist eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung, die in einer SELECT-, [SELECT…INTO](select-into-statement-microsoft-access-sql.md)-, [INSERT…INTO](insert-into-statement-microsoft-access-sql.md)-, [DELETE](delete-statement-microsoft-access-sql.md)- oder [UPDATE](update-statement-microsoft-access-sql.md)-Anweisung oder in einer anderen Unterabfrage geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-104">A subquery is a [SELECT](select-statement-microsoft-access-sql.md) statement nested inside a SELECT, [SELECT…INTO](select-into-statement-microsoft-access-sql.md), [INSERT…INTO](insert-into-statement-microsoft-access-sql.md), [DELETE](delete-statement-microsoft-access-sql.md), or [UPDATE](update-statement-microsoft-access-sql.md) statement or inside another subquery.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b7ab-105">Syntax</span></span>

<span data-ttu-id="1b7ab-106">Zum Erstellen einer Unterabfrage können Sie eins der folgenden drei Syntaxformate verwenden:</span><span class="sxs-lookup"><span data-stu-id="1b7ab-106">You can use three forms of syntax to create a subquery:</span></span>

<span data-ttu-id="1b7ab-107">*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="1b7ab-107">comparison [ANY | ALL | SOME] (sqlstatement)</span></span>

<span data-ttu-id="1b7ab-108">*expression* \[NOT\] IN (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="1b7ab-108">*expression* \[NOT\] IN (*sqlstatement*)</span></span>

<span data-ttu-id="1b7ab-109">\[NOT\] EXISTS (*sqlstatement*)</span><span class="sxs-lookup"><span data-stu-id="1b7ab-109">[NOT] EXISTS (sqlstatement)</span></span>

<span data-ttu-id="1b7ab-110">Eine Unterabfrage enthält die folgenden Bestandteile:</span><span class="sxs-lookup"><span data-stu-id="1b7ab-110">A subquery has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1b7ab-111">Part</span><span class="sxs-lookup"><span data-stu-id="1b7ab-111">Part</span></span></p></th>
<th><p><span data-ttu-id="1b7ab-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b7ab-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1b7ab-113"><em>comparison</em></span><span class="sxs-lookup"><span data-stu-id="1b7ab-113"><em>Comparison</em></span></span></p></td>
<td><p><span data-ttu-id="1b7ab-114">Ein Ausdruck und ein Vergleichsoperator, der den Ausdruck mit den Ergebnissen einer Unterabfrage vergleicht.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-114">An expression and a comparison operator that compares the expression with the results of the subquery.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1b7ab-115"><em>expression</em></span><span class="sxs-lookup"><span data-stu-id="1b7ab-115"><em>expression</em></span></span></p></td>
<td><p><span data-ttu-id="1b7ab-116">Ein Ausdruck, nach dem die Ergebnisgruppe der Unterabfrage durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-116">An expression for which the result set of the subquery is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1b7ab-117"><em>SQL-Anweisung</em></span><span class="sxs-lookup"><span data-stu-id="1b7ab-117"><em>SQLStatement</em></span></span></p></td>
<td><p><span data-ttu-id="1b7ab-118">Eine SELECT-Anweisung, die dasselbe Format und dieselben Regeln wie jede andere SELECT-Anweisung befolgt.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-118">A SELECT statement, following the same format and rules as any other SELECT statement.</span></span> <span data-ttu-id="1b7ab-119">Sie muss in Klammern eingeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-119">It must be enclosed in parentheses.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1b7ab-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b7ab-120">Remarks</span></span>

<span data-ttu-id="1b7ab-p102">Anstelle eines Ausdrucks können Sie in der Feldliste einer SELECT-Anweisung oder in einer [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)- oder [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql)-Klausel auch eine Unterabfrage verwenden. In einer Unterabfrage geben Sie mithilfe einer SELECT-Anweisung mindestens einen genauen Wert an, der im Ausdruck in der WHERE- oder HAVING-Klausel ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p102">You can use a subquery instead of an expression in the field list of a SELECT statement or in a [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) or [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql) clause. In a subquery, you use a SELECT statement to provide a set of one or more specific values to evaluate in the WHERE or HAVING clause expression.</span></span>

<span data-ttu-id="1b7ab-p103">Verwenden Sie eines der synonymen Prädikate ANY oder SOME, um in der Hauptabfrage Datensätze abzurufen, die den Vergleich mit einem der in der Unterabfrage abgerufenen Datensätze erfüllen. Im folgenden Beispiel werden alle Artikel zurückgegeben, deren Einzelpreis höher als der Preis irgendeines Artikels ist, der mindestens zu einem Preisnachlass von 25 %verkauft wird:</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p103">Use the ANY or SOME predicate, which are synonymous, to retrieve records in the main query that satisfy the comparison with any records retrieved in the subquery. The following example returns all products whose unit price is greater than that of any product sold at a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="1b7ab-p104">Verwenden Sie das Prädikat [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql), um in der Hauptabfrage nur die Datensätze abzurufen, die dem Vergleich mit allen in der Unterabfrage abgerufenen Datensätzen standhalten. Wenn Sie das vorherige Beispiel mit ALL anstelle von ANY ausführen, gibt die Abfrage nur die Artikel zurück, deren Einzelpreis höher als der Preis sämtlicher Artikel ist, die mindestens zu einem Preisnachlass von 25 % verkauft werden. Dies ist wesentlich restriktiver.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p104">Use the [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql) predicate to retrieve only those records in the main query that satisfy the comparison with all records retrieved in the subquery. If you changed ANY to ALL in the previous example, the query would return only those products whose unit price is greater than that of all products sold at a discount of 25 percent or more. This is much more restrictive.</span></span>

<span data-ttu-id="1b7ab-p105">Verwenden Sie das Prädikat IN, um in der Hauptabfrage nur die Datensätze abzurufen, für die ein identischer Wert in einem Datensatz in der Unterabfrage vorhanden ist. Im folgenden Beispiel werden alle Artikel mit einem Preisnachlass von mindestens 25 % zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p105">Use the IN predicate to retrieve only those records in the main query for which some record in the subquery contains an equal value. The following example returns all products with a discount of 25 percent or more:</span></span>

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

<span data-ttu-id="1b7ab-130">Sie können das Prädikat IN jedoch nicht verwenden, um in der Hauptabfrage nur die Datensätze abzurufen, für die in einem Datensatz in der Unterabfrage kein identischer Wert vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-130">Conversely, you can use NOT IN to retrieve only those records in the main query for which no record in the subquery contains an equal value.</span></span>

<span data-ttu-id="1b7ab-131">Verwenden Sie das Prädikat EXISTS (mit dem optionalen reservierten Wort NOT) in Wahr/Falsch-Vergleichen, um zu ermitteln, ob die Unterabfrage Datensätze zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-131">Use the EXISTS predicate (with the optional NOT reserved word) in true/false comparisons to determine whether the subquery returns any records.</span></span>

<span data-ttu-id="1b7ab-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p106">You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":</span></span>

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

<span data-ttu-id="1b7ab-135">Im obigen Beispiel ist das reservierte Wort AS optional.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-135">In the preceding example, the AS reserved word is optional.</span></span>

<span data-ttu-id="1b7ab-p107">Bestimmte Unterabfragen sind in Kreuztabellenabfragen zulässig, insbesondere als Prädikate (in der WHERE-Klausel). Als Ausgabe verwendete Unterabfragen (in der SELECT-Liste) sind in Kreuztabellenabfragen nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-p107">Some subqueries are allowed in crosstab queries— specifically, as predicates (those in the WHERE clause). Subqueries as output (those in the SELECT list) are not allowed in crosstab queries.</span></span>

## <a name="example"></a><span data-ttu-id="1b7ab-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1b7ab-138">Example</span></span>

<span data-ttu-id="1b7ab-139">In diesem Beispiel werden die Namen und Kontaktdaten jedes Kunden aufgelistet, der im zweiten Quartal 1995 eine Bestellung aufgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-139">This example lists the name and contact of every customer who placed an order in the second quarter of 1995.</span></span> <span data-ttu-id="1b7ab-140">Dabei wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1b7ab-140">It calls the EnumFields procedure, which you can find in the SELECT statement example.</span></span>

```vb
    Sub SubQueryX() 
     
        Dim dbs As Database, rst As Recordset 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' List the name and contact of every customer  
        ' who placed an order in the second quarter of 
        ' 1995. 
        Set rst = dbs.OpenRecordset("SELECT ContactName," _ 
            & " CompanyName, ContactTitle, Phone" _ 
            & " FROM Customers" _ 
            & " WHERE CustomerID" _ 
            & " IN (SELECT CustomerID FROM Orders" _ 
            & " WHERE OrderDate Between #04/1/95#" _ 
            & " And #07/1/95#);") 
         
        ' Populate the Recordset. 
        rst.MoveLast 
         
        ' Call EnumFields to print the contents of the  
        ' Recordset. Pass the Recordset object and desired 
        ' field width. 
        EnumFields rst, 25 
     
        dbs.Close 
     
    End Sub
```
