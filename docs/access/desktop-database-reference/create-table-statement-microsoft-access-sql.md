---
title: CREATE TABLE statement (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 296e1405245d6204d136888e78b6a3846b468a1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295359"
---
# <a name="create-table-statement-microsoft-access-sql"></a>CREATE TABLE statement (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Erstellt eine neue Tabelle.

> [!NOTE]
> Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung von CREATE TABLE oder einer der DDL-Anweisungen für Datenbanken, die nicht mit dem Microsoft Access-Datenbankmodul erstellt wurden. Verwenden Sie stattdessen die **Create**-Methoden von DAO.

## <a name="syntax"></a>Syntax

CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])

Die CREATE TABLE-Anweisung setzt sich wie folgt zusammen:

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
<td><p><em>table</em></p></td>
<td><p>Der Name der zu erstellenden Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld1</em>, <em>Feld2</em></p></td>
<td><p>Der Name des Felds oder der Felder, das/die in der neuen Tabelle erstellt werden soll(en). Sie müssen mindestens ein Feld erstellen.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Der Datentyp des <em>Felds</em> in der neuen Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Die Feldgröße in Zeichen (nur Text- und binäre Felder).</p></td>
</tr>
<tr class="odd">
<td><p><em>Index1</em>, <em>Index2</em></p></td>
<td><p>Eine CONSTRAINT-Klausel, die einen einfachen Index definiert. Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>zusammengesetzter Index</em></p></td>
<td><p>Eine CONSTRAINT-Klausel, die einen zusammengesetzten Index definiert. Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Verwenden Sie die CREATE TABLE-Anweisung, um eine neue Tabelle und deren Felder sowie Feldeinschränkungen zu definieren. Wenn für ein Feld NOT NULL angegeben ist, müssen neue Datensätze gültige Daten in diesem Feld aufweisen.

Eine CONSTRAINT-Klausel erstellt verschiedene Einschränkungen für ein Feld und kann zum Erstellen des Primärschlüssels verwendet werden. Sie können auch die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung zum Erstellen eines Primärschlüssels oder zusätzlicher Indizes für vorhandene Tabellen verwenden.

Sie können NOT NULL für ein einzelnes Feld oder in einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes Feld oder für mehrere Felder mit dem Namen CONSTRAINT gilt. Sie können die NOT NULL-Einschränkung jedoch nur einmal auf ein Feld anwenden. Der Versuch, diese Einschränkung mehrmals zu verwenden, führt zu einem Laufzeitfehler.

Beim Erstellen der Tabelle vom Typ TEMPORARY ist diese nur in der Sitzung sichtbar, in der sie erstellt wurde. Sie wird automatisch gelöscht, wenn die Sitzung beendet wird. Auf temporäre Tabellen können mehrere Benutzer zugreifen.

Das Attribut WITH COMPRESSION kann nur mit den Datentypen CHARACTER und MEMO (auch als TEXT bezeichnet) und deren Synonymen verwendet werden.

Das Attribut WITH COMPRESSION wurde aufgrund der Änderung des Darstellungsformats von Unicode-Zeichen für Zeichenspalten hinzugefügt. Unicode-Zeichen benötigen jeweils zwei Byte, um jedes Zeichen zu speichern. Für vorhandene Microsoft Jet-Datenbanken, die überwiegend Zeichendaten enthalten, kann dies bedeuten, dass die Datenbankdatei bei Konvertierung in das Microsoft Access-Datenbankformat ihre Größe nahezu verdoppelt. Jedoch kann die Unicode-Darstellung vieler Zeichensätze, die früher als Single-Byte Character Sets (SBCS) bezeichnet wurden, auf einfache Weise zu einem einzelnen Byte komprimiert werden. Wenn Sie eine Zeichenspalte (CHARACTER) mit diesem Attribut definieren, werden die Daten beim Speichern automatisch komprimiert und beim Abrufen aus der Spalte dekomprimiert.

MEMO-Spalten können auch definiert werden, um Daten in einem komprimierten Format zu speichern. Es gibt jedoch eine Einschränkung. Nur Instanzen von MEMO-Spalten, die in komprimierter Form in 4096 Byte oder weniger passen, werden komprimiert. Alle anderen Instanzen von MEMO-Spalten bleiben dekomprimiert. Dies bedeutet, dass innerhalb einer bestimmten Tabelle für eine bestimmte MEMO-Spalte einige Daten möglicherweise komprimiert werden und einige Daten möglicherweise nicht komprimiert werden.

## <a name="example"></a>Beispiel

In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.

```vb
    Sub CreateTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with two text fields. 
        dbs.Execute "CREATE TABLE ThisTable " _ 
            & "(FirstName CHAR, LastName CHAR);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.

```vb
    Sub CreateTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
     
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a unique 
        ' index made up of all three fields. 
        dbs.Execute "CREATE TABLE MyTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "DateOfBirth DATETIME, " _ 
            & "CONSTRAINT MyTableConstraint UNIQUE " _ 
            & "(FirstName, LastName, DateOfBirth));" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.

```vb
    Sub CreateTableX3() 
     
         Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Create a table with three fields and a primary 
        ' key. 
        dbs.Execute "CREATE TABLE NewTable " _ 
            & "(FirstName CHAR, LastName CHAR, " _ 
            & "SSN INTEGER CONSTRAINT MyFieldConstraint " _ 
            & "PRIMARY KEY);" 
     
        dbs.Close 
     
    End Sub
```
