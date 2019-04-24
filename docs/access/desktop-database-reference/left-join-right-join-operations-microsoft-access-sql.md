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
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN- und RIGHT JOIN-Operation (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Kombiniert bei Verwendung in einer [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel Datensätze der Herkunftstabellen.

## <a name="syntax"></a>Syntax

FROM *table1* \[ LEFT | RIGHT \] JOIN *table2* ON *table1.field1* *compopr table2.field2*

Die Operationen LEFT JOIN und RIGHT JOIN enthalten die folgenden Bestandteile:

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
<td><p>Die Namen der verknüpften Felder. Die Felder müssen denselben Datentyp aufweisen und dieselbe Art von Daten enthalten, doch sie müssen nicht denselben Namen tragen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Vergleichsoperator</em></p></td>
<td><p>Ein beliebiger relationaler Vergleichsoperator: &quot;=,&quot; &quot;&lt;,&quot; &quot;&gt;,&quot; &quot;&lt;=,&quot; &quot;&gt;=,&quot; oder &quot;&lt;&gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Verwenden Sie eine LEFT JOIN-Operation, um eine linke äußere Verknüpfung zu erstellen. Eine linke äußere Verknüpfung enthält alle Datensätze aus der ersten (linken) der beiden Tabellen, selbst wenn die zweite (rechte) Tabelle keine übereinstimmenden Werte enthält.

Verwenden Sie eine RIGHT JOIN-Operation, um eine rechte äußere Verknüpfung zu erstellen. Eine rechte äußere Verknüpfung enthält alle Datensätze aus der zweiten (rechten) der beiden Tabellen, selbst wenn die erste (linke) Tabelle keine übereinstimmenden Werte enthält.

Beispielsweise können Sie LEFT JOIN mit den Tabellen "Abteilungen" (links) und "Mitarbeiter" (rechts) verwenden, um alle Abteilungen auszuwählen, einschließlich der Abteilungen, denen keine Mitarbeiter zugewiesen sind. Um alle Mitarbeiter (einschließlich derjenigen, die keiner Abteilung zugewiesen sind) auszuwählen, verwenden Sie RIGHT JOIN.

Das folgende Beispiel zeigt, wie Sie die Tabellen "Categories" und "Products" im Feld "CategoryID" verknüpfen können. Die Abfrage erzeugt eine Liste aller Kategorien, einschließlich derjenigen, die keine Produkte enthalten:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

In diesem Beispiel ist "CategoryID" das verknüpfte Feld, ist aber nicht im Abfrageergebnis enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist. Um das verknüpfte Feld einzuschließen, geben Sie den Feldnamen in die SELECT-Anweisung ein, in diesem Fall Categories.CategoryID.

> [!NOTE]
> - Wenn Sie eine Abfrage erstellen möchten, die nur Datensätze mit jeweils identischen Daten in den verknüpften Feldern enthält, verwenden Sie eine [INNER JOIN](inner-join-operation-microsoft-access-sql.md)-Operation.
> - Eine LEFT JOIN- oder RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt werden, wohingegen eine INNER JOIN-Operation nicht in einer LEFT JOIN- oder RIGHT JOIN-Operation geschachtelt werden kann. Im Thema "INNER JOIN-Operation" erfahren Sie, wie Joins in anderen Joins geschachtelt werden.
> - Sie können mehrere ON-Klauseln verknüpfen. Im Thema "INNER JOIN-Operation" wird erläutert, wie das Verknüpfen von Klauseln funktioniert.
> - Wenn Sie versuchen, Felder mit Memo- oder OLE-Objektdaten zu verknüpfen, tritt ein Fehler auf.

## <a name="example"></a>Beispiel

In diesem Beispiel:
- Wird davon ausgegangen, dass die Employees-Tabelle die hypothetischen Felder Department Name und Department ID enthält. Beachten Sie, dass diese Felder nicht in der Mitarbeitertabelle der Northwind-Datenbank vorhanden sind.

- Es werden alle Abteilungen ausgewählt, auch die Abteilungen ohne Mitarbeiter.

- Die EnumFields-Prozedur wird aufgerufen, die im Beispiel für die SELECT-Anweisung enthalten ist.


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
