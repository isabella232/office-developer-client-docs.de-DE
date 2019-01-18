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
# <a name="left-join-right-join-operations-microsoft-access-sql"></a>LEFT JOIN-, RIGHT JOIN-Operationen (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Kombiniert bei Verwendung in einer [FROM](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/from-clause-microsoft-access-sql)-Klausel Datensätze der Herkunftstabellen.

## <a name="syntax"></a>Syntax

FROM *Tabelle1* \[ links | RECHTS \] JOIN *Tabelle2* ON Tabelle2 *table1.field1* *Compopr Tabelle2. Feld2* .

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
<td><p>Die Namen der Tabellen, deren Datensätze kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Die Namen der verknüpften Felder. Die Felder müssen denselben Datentyp aufweisen und dieselbe Art von Daten enthalten, doch sie müssen nicht denselben Namen tragen.</p></td>
</tr>
<tr class="odd">
<td><p><em>Vergleichsoperator</em></p></td>
<td><p>Ein beliebiger Vergleichsoperator: &quot;=,&quot; &quot; &lt;,&quot; &quot; &gt;,&quot; &quot; &lt;=,&quot; &quot; &gt;=,&quot; oder &quot; &lt; &gt;.&quot;</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Verwenden Sie eine LEFT JOIN-Operation, um eine linke äußere Verknüpfung zu erstellen. Eine linke äußere Verknüpfung enthält alle Datensätze aus der ersten (linken) der beiden Tabellen, selbst wenn die zweite (rechte) Tabelle keine übereinstimmenden Werte enthält.

Verwenden Sie eine RIGHT JOIN-Operation, um eine rechte äußere Verknüpfung zu erstellen. Eine rechte äußere Verknüpfung enthält alle Datensätze aus der zweiten (rechten) der beiden Tabellen, selbst wenn die erste (linke) Tabelle keine übereinstimmenden Werte enthält.

Sie können z. B. eine LEFT JOIN-Operation für die Tabellen Departments (links) und Employees (rechts) verwenden, um alle Abteilungen auszuwählen, einschließlich Abteilungen, denen keine Mitarbeiter zugewiesen sind. Wenn Sie alle Mitarbeiter auswählen möchten, einschließlich Mitarbeitern, die keiner Abteilung zugewiesen sind, verwenden Sie die RIGHT JOIN-Operation.

Im folgenden Beispiel wird gezeigt, wie Sie die Tabellen Categories und Products für das Feld CategoryID verknüpfen. Die Abfrage erzeugt eine Liste aller Kategorien, einschließlich der Kategorien, die keine Produkte enthalten:

```sql
SELECT CategoryName, 
ProductName 
FROM Categories LEFT JOIN Products 
ON Categories.CategoryID = Products.CategoryID;
```

In diesem Beispiel ist "CategoryID" das verknüpfte Feld, ist aber nicht im Abfrageergebnis enthalten, da es nicht in der [SELECT](select-statement-microsoft-access-sql.md)-Anweisung enthalten ist. Geben Sie zum Einbeziehen von verknüpften Felds der Name des Felds in der SELECT-Anweisung – in diesem Fall also Kategorien.Kategorie-Nr..

> [!NOTE]
> - Wenn Sie eine Abfrage erstellen möchten, die nur Datensätze mit jeweils identischen Daten in den verknüpften Feldern enthält, verwenden Sie eine [INNER JOIN](inner-join-operation-microsoft-access-sql.md)-Operation.
> - Eine LEFT JOIN- bzw. eine RIGHT JOIN-Operation kann in einer INNER JOIN-Operation geschachtelt sein, doch eine INNER JOIN-Operation kann nicht in einer LEFT JOIN- oder einer RIGHT JOIN-Operation geschachtelt sein. Informationen zum Schachteln von Verknüpfungen finden Sie in der Erläuterung zum Schachteln im Thema zur INNER JOIN-Operation.
> - Sie können mehrere ON-Klauseln verknüpfen. Entsprechende Informationen finden Sie in der Erläuterung zum Verknüpfen von Klauseln im Thema zur INNER JOIN-Operation.
> - Wenn Sie Felder verknüpfen, die Memo- oder OLE-Objektdaten enthalten, tritt ein Fehler auf.

## <a name="example"></a>Beispiel

In diesem Beispiel wird:
- Setzt das Vorhandensein von hypothetische Abteilungsnamen und Department ID Felder in einer Tabelle Employees. Beachten Sie, dass diese Felder nicht tatsächlich in die Employees-Tabelle der Northwind-Datenbank vorhanden sind.

- Wählt alle Abteilungen, einschließlich derjenigen ohne Mitarbeiter.

- Ruft die EnumFields-Prozedur, die Sie in diesem Beispiel wird die SELECT-Anweisung finden.


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
