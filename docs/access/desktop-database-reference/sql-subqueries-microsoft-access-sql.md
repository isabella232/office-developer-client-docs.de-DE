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
# <a name="sql-subqueries-microsoft-access-sql"></a>SQL-Unterabfragen (Microsoft Access SQL)


**Gilt für**: Access 2013, Office 2013

Eine Unterabfrage ist eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung, die in einer SELECT-, [SELECT…INTO](select-into-statement-microsoft-access-sql.md)-, [INSERT…INTO](insert-into-statement-microsoft-access-sql.md)-, [DELETE](delete-statement-microsoft-access-sql.md)- oder [UPDATE](update-statement-microsoft-access-sql.md)-Anweisung oder in einer anderen Unterabfrage geschachtelt ist.

## <a name="syntax"></a>Syntax

Zum Erstellen einer Unterabfrage können Sie eins der folgenden drei Syntaxformate verwenden:

*comparison* \[ANY | ALL | SOME\] (*sqlstatement*)

*expression* \[NOT\] IN (*sqlstatement*)

\[NOT\] EXISTS (*sqlstatement*)

Eine Unterabfrage enthält die folgenden Bestandteile:

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
<td><p><em>comparison</em></p></td>
<td><p>Ein Ausdruck und ein Vergleichsoperator, der den Ausdruck mit den Ergebnissen einer Unterabfrage vergleicht.</p></td>
</tr>
<tr class="even">
<td><p><em>expression</em></p></td>
<td><p>Ein Ausdruck, nach dem die Ergebnisgruppe der Unterabfrage durchsucht wird.</p></td>
</tr>
<tr class="odd">
<td><p><em>SQL-Anweisung</em></p></td>
<td><p>Eine SELECT-Anweisung, die dasselbe Format und dieselben Regeln wie jede andere SELECT-Anweisung befolgt. Sie muss in Klammern eingeschlossen sein.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Anstelle eines Ausdrucks können Sie in der Feldliste einer SELECT-Anweisung oder in einer [WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql)- oder [HAVING](https://docs.microsoft.com/office/vba/access/concepts/structured-query-language/having-clause-microsoft-access-sql)-Klausel auch eine Unterabfrage verwenden. In einer Unterabfrage geben Sie mithilfe einer SELECT-Anweisung mindestens einen genauen Wert an, der im Ausdruck in der WHERE- oder HAVING-Klausel ausgewertet wird.

Verwenden Sie eines der synonymen Prädikate ANY oder SOME, um in der Hauptabfrage Datensätze abzurufen, die den Vergleich mit einem der in der Unterabfrage abgerufenen Datensätze erfüllen. Im folgenden Beispiel werden alle Artikel zurückgegeben, deren Einzelpreis höher als der Preis irgendeines Artikels ist, der mindestens zu einem Preisnachlass von 25 %verkauft wird:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Verwenden Sie das Prädikat [ALL](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/all-distinct-distinctrow-top-predicates-microsoft-access-sql), um in der Hauptabfrage nur die Datensätze abzurufen, die dem Vergleich mit allen in der Unterabfrage abgerufenen Datensätzen standhalten. Wenn Sie das vorherige Beispiel mit ALL anstelle von ANY ausführen, gibt die Abfrage nur die Artikel zurück, deren Einzelpreis höher als der Preis sämtlicher Artikel ist, die mindestens zu einem Preisnachlass von 25 % verkauft werden. Dies ist wesentlich restriktiver.

Verwenden Sie das Prädikat IN, um in der Hauptabfrage nur die Datensätze abzurufen, für die ein identischer Wert in einem Datensatz in der Unterabfrage vorhanden ist. Im folgenden Beispiel werden alle Artikel mit einem Preisnachlass von mindestens 25 % zurückgegeben:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

Sie können das Prädikat IN jedoch nicht verwenden, um in der Hauptabfrage nur die Datensätze abzurufen, für die in einem Datensatz in der Unterabfrage kein identischer Wert vorhanden ist.

Verwenden Sie das Prädikat EXISTS (mit dem optionalen reservierten Wort NOT) in Wahr/Falsch-Vergleichen, um zu ermitteln, ob die Unterabfrage Datensätze zurückgibt.

You can also use table name aliases in a subquery to refer to tables listed in a [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql) clause outside the subquery. The following example returns the names of employees whose salaries are equal to or greater than the average salary of all employees having the same job title. The Employees table is given the alias "T1":

```sql
SELECT LastName,
FirstName, Title, Salary 
FROM Employees AS T1 
WHERE Salary >= (SELECT Avg(Salary) 
FROM Employees 
WHERE T1.Title = Employees.Title) Order by Title;
```

Im obigen Beispiel ist das reservierte Wort AS optional.

Bestimmte Unterabfragen sind in Kreuztabellenabfragen zulässig, insbesondere als Prädikate (in der WHERE-Klausel). Als Ausgabe verwendete Unterabfragen (in der SELECT-Liste) sind in Kreuztabellenabfragen nicht zulässig.

## <a name="example"></a>Beispiel

In diesem Beispiel werden die Namen und Kontaktdaten jedes Kunden aufgelistet, der im zweiten Quartal 1995 eine Bestellung aufgegeben hat. Dabei wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.

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
