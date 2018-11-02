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
ms.openlocfilehash: 72d9d9d27ac128ec587621231b5c899bc89c2752
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925950"
---
# <a name="sql-subqueries-microsoft-access-sql"></a>SQL-Unterabfragen (Microsoft Access SQL)


**Betrifft**: Access 2013, Office 2013

Eine Unterabfrage ist eine [SELECT](select-statement-microsoft-access-sql.md)-Anweisung, die in einer SELECT-, [SELECT…INTO](select-into-statement-microsoft-access-sql.md)-, [INSERT…INTO](insert-into-statement-microsoft-access-sql.md)-, [DELETE](delete-statement-microsoft-access-sql.md)- oder [UPDATE](update-statement-microsoft-access-sql.md)-Anweisung oder in einer anderen Unterabfrage geschachtelt ist.

## <a name="syntax"></a>Syntax

Zum Erstellen einer Unterabfrage können Sie eins der folgenden drei Syntaxformate verwenden:

*Vergleich* \[ANY | ALLE | Einige\] (*SQL-Anweisung*)

*Ausdruck* \[Nicht\] IN (*SQL-Anweisung*)

\[NICHT\] EXISTS (*SQL-Anweisung*)

Eine Unterabfrage enthält die folgenden Bestandteile:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Vergleich</em></p></td>
<td><p>Ein Ausdruck und ein Vergleichsoperator, der den Ausdruck mit den Ergebnissen einer Unterabfrage vergleicht.</p></td>
</tr>
<tr class="even">
<td><p><em>Ausdruck</em></p></td>
<td><p>Ein Ausdruck, nach dem die Ergebnisgruppe der Unterabfrage durchsucht wird.</p></td>
</tr>
<tr class="odd">
<td><p><em>SQL-Anweisung</em></p></td>
<td><p>Eine SELECT-Anweisung, die dasselbe Format und dieselben Regeln wie jede andere SELECT-Anweisung befolgt. Sie muss in Klammern eingeschlossen sein.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Anstelle eines Ausdrucks können Sie in der Feldliste einer SELECT-Anweisung oder in einer [WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\))- oder [HAVING](https://msdn.microsoft.com/library/ff193795\(v=office.15\))-Klausel auch eine Unterabfrage verwenden. In einer Unterabfrage geben Sie mithilfe einer SELECT-Anweisung mindestens einen genauen Wert an, der im Ausdruck in der WHERE- oder HAVING-Klausel ausgewertet wird.

Verwenden Sie eines der synonymen Prädikate ANY oder SOME, um in der Hauptabfrage Datensätze abzurufen, die den Vergleich mit einem der in der Unterabfrage abgerufenen Datensätze erfüllen. Im folgenden Beispiel werden alle Artikel zurückgegeben, deren Einzelpreis höher als der Preis irgendeines Artikels ist, der mindestens zu einem Preisnachlass von 25 %verkauft wird:

```sql
SELECT * FROM Products 
WHERE UnitPrice > ANY 
(SELECT UnitPrice FROM OrderDetails 
WHERE Discount >= .25);
```

Verwenden Sie das Prädikat [ALL](https://msdn.microsoft.com/library/ff195711\(v=office.15\)), um in der Hauptabfrage nur die Datensätze abzurufen, die dem Vergleich mit allen in der Unterabfrage abgerufenen Datensätzen standhalten. Wenn Sie das vorherige Beispiel mit ALL anstelle von ANY ausführen, gibt die Abfrage nur die Artikel zurück, deren Einzelpreis höher als der Preis sämtlicher Artikel ist, die mindestens zu einem Preisnachlass von 25 % verkauft werden. Dies ist wesentlich restriktiver.

Verwenden Sie das Prädikat IN, um in der Hauptabfrage nur die Datensätze abzurufen, für die ein identischer Wert in einem Datensatz in der Unterabfrage vorhanden ist. Im folgenden Beispiel werden alle Artikel mit einem Preisnachlass von mindestens 25 % zurückgegeben:

```sql
SELECT * FROM Products 
WHERE ProductID IN 
(SELECT ProductID FROM OrderDetails 
WHERE Discount >= .25);
```

Sie können das Prädikat IN jedoch nicht verwenden, um in der Hauptabfrage nur die Datensätze abzurufen, für die in einem Datensatz in der Unterabfrage kein identischer Wert vorhanden ist.

Verwenden Sie das Prädikat EXISTS (mit dem optionalen reservierten Wort NOT) in Wahr/Falsch-Vergleichen, um zu ermitteln, ob die Unterabfrage Datensätze zurückgibt.

Sie können auch mithilfe der Aliase für Tabellennamen in einer Unterabfrage auf Tabellen verweisen, die in einer FROM-Klausel außerhalb der Unterabfrage aufgeführt sind. Im folgenden Beispiel werden die Namen der Mitarbeiter zurückgegeben, deren Gehalt jeweils mindestens dem Durchschnittsgehalt aller Mitarbeiter in derselben Position entspricht. Die Employees-Tabelle erhält den Aliasnamen "T1":

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

In diesem Beispiel werden die Namen und Kontaktdaten aller Kunden aufgeführt, die im zweiten Quartal 1995 eine Bestellung aufgegeben haben.

In diesem Beispiel wird die EnumFields-Prozedur aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.

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
