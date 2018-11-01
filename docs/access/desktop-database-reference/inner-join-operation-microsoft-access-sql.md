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
# <a name="inner-join-operation-microsoft-access-sql"></a>INNER JOIN-Operation (Microsoft Access SQL)


**Betrifft**: Access 2013, Office 2013


Fasst Datensätze aus zwei Tabellen zusammen, wenn in einem gemeinsamen Feld entsprechende Datensätze enthalten sind.

## <a name="syntax"></a>Syntax

AUS *Tabelle1* INNER JOIN *Tabelle2* für *Tabelle1*. *Feld1* *Compopr Tabelle2*. *Field2*

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
<td><p>Die Namen der Tabellen, deren Datensätze kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der Felder, die verknüpft werden. Wenn es sich nicht um numerische Felder handelt, müssen sie über den gleichen Datentyp verfügen und die gleich Art von Daten enthalten. Die Felder müssen aber nicht über den gleichen Namen verfügen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Vergleichsoperator</em></p></td>
<td><p>Ein beliebiger Vergleichsoperator: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; oder &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie können eine INNER JOIN-Operation in jeder [FROM](https://msdn.microsoft.com/library/ff836674\(v=office.15\))-Klausel verwenden. Hierbei handelt es sich um den Verknüpfungstyp, der im Allgemeinen verwendet wird. Innere Verknüpfungen fassen Datensätze aus zwei Tabellen zusammen, wenn sich in Feldern, die in beiden Tabellen enthalten sind, übereinstimmende Werte befinden.

Sie können die INNER JOIN-Operation in Kombination mit der Departments-Tabelle (Abteilungen) und der Employees-Tabelle (Personal) verwenden, um alle Mitarbeiter in jeder Abteilung auszuwählen. Umgekehrt können Sie eine LEFT JOIN- oder RIGHT JOIN-Operation zur Erstellung einer äußeren Verknüpfung verwenden, um alle Abteilungen (selbst wenn den Abteilungen kein Personal zugewiesen wurde) oder das gesamte Personal (selbst wenn einige Mitarbeiter keiner Abteilung zugewiesen wurden) auszuwählen.

Wenn Sie versuchen, Felder zu verknüpfen, die Daten vom Typ Memo oder OLE-Objekt enthalten, wird ein Fehler generiert.

Sie können zwei beliebige numerische Felder vom Typ LIKE miteinander verknüpfen. So können beispielsweise Felder vom Datentyp AutoWert und Long verknüpft werden, da es sich in beiden Fällen um Felder vom Typ LIKE handelt. Felder vom Datentyp Single und Double können dagegen nicht miteinander verknüpft werden.

Im folgenden Beispiel wird gezeigt, wie die Categories-Tabelle (Kategorien) und die Products-Tabelle (Artikel) über das CategoryID-Feld (Kategorie-Nr.) verknüpft werden können:

```sql
SELECT CategoryName, ProductName 
FROM Categories INNER JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

Klicken Sie im vorstehenden Beispiel CategoryID ist das verknüpfte Feld, aber es ist nicht in den Abfrageergebnissen enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md) -Anweisung enthalten ist. Der Name des Felds in der SELECT-Anweisung zum Einbeziehen von verknüpften Felds einschließen – in diesem Fall also Kategorien.Kategorie-Nr..

Sie können unter Verwendung der folgenden Syntax auch verschiedene ON-Klauseln in einer JOIN-Anweisung verknüpfen:

Wählen SIE die *Felder* FROM *Tabelle1* INNER JOIN *Tabelle2* ON *Tabelle1*. *Feld1* *compopr* *Tabelle2*. *Feld1* UND für *Tabelle1*. *Field2* *compopr* *Tabelle2*. *field2*) ODER klicken Sie auf *Tabelle1*. *feld3* *compopr* *Tabelle2*. *feld3*) \];

Sie können unter Verwendung der folgenden Syntax JOIN-Anweisungen auch schachteln:

Wählen Sie *Felder* FROM *Tabelle1* INNER JOIN (*Tabelle2* INNER JOIN \[( \] *Tabelle3* \[INNER JOIN \[( \] *tabellex* \[INNER JOIN...) \] Auf *Tabelle3*. *feld3* *compopr* *tabellex*. *Fieldx*) \] Für *Tabelle2*. *Field2* *compopr* *Tabelle3*. *feld3*) FÜR *Tabelle1*. *Feld1* *compopr* *Tabelle2*. *Feld2*;

Eine LEFT JOIN- oder eine RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, aber umgekehrt kann eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder einen RIGHT JOIN-Operation geschachtelt werden.

## <a name="example"></a>Beispiel

Im folgenden Beispiel werden zwei gleichwertige Verknüpfungen erstellt: eine Verknüpfung zwischen der Order Details-Tabelle (Bestelldetails) und der Orders-Tabelle (Bestellungen) und eine andere Verknüpfung zwischen der Orders-Tabelle und der Employees-Tabelle (Personal). Dies ist erforderlich, weil die Employees-Tabelle keine Verkaufsdaten und die Order Details-Tabelle keine Personaldaten enthält. Die Abfrage gibt eine Liste der Mitarbeiter unter Aufführung ihrer Gesamtverkäufe zurück.  


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
