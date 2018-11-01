---
title: CONSTRAINT-Klausel (Microsoft Access SQL)
TOCTitle: CONSTRAINT clause (Microsoft Access SQL)
ms:assetid: f8e89a91-a69e-1811-42a7-921692110bcb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836971(v=office.15)
ms:contentKeyID: 48548797
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277561
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b55bf1897c6b5fc5cd7ee70402e466f2180b7d92
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2018
ms.locfileid: "25890925"
---
# <a name="constraint-clause-microsoft-access-sql"></a>CONSTRAINT-Klausel (Microsoft Access SQL)

**Betrifft**: Access 2013, Office 2013

Eine Einschränkung ähnelt einem Index, obwohl sie auch zur Verknüpfung mit einer anderen Tabelle verwendet werden kann.

Verwenden Sie die CONSTRAINT-Klausel in den [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)- und [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisungen, um Einschränkungen zu erstellen oder zu löschen. Es gibt zwei Arten von CONSTRAINT-Klauseln: eine zum Erstellen einer Einschränkung für ein einzelnes Feld oder zum Erstellen einer Einschränkung für mehrere Felder.

> [!NOTE]
> [!HINWEIS] Die Datenbank-Engine von Microsoft Access unterstützt CONSTRAINT-Klauseln nicht, genauso wie DDL-Anweisungen mit Datenbank-Engine-Datenbanken, die nicht auf Microsoft Access basieren. Verwenden Sie stattdessen Methoden DAO **Erstellen** .

## <a name="syntax"></a>Syntax

**Beschränkung für ein Feld**:

CONSTRAINT *Name* {PRIMARY KEY | EINDEUTIGE | NOT NULL | REFERENCES *Fremdtabelle* \[(*fremdfeld1, fremdfeld2*)\] \[ON UPDATE CASCADE | Legen Sie NULL\] \[ON DELETE CASCADE | Legen Sie NULL\]}

**Beschränkung für mehrere Felder**:

CONSTRAINT *Name* {PRIMARY KEY (*primär1*\[, *primär2* \[,... \]\]) | EINDEUTIGE (*eindeutig1*\[, *eindeutig2* \[,... \]\]) | NOT NULL (*nichtnull1*\[, *nichtnull2* \[,... \]\]) | FREMDSCHLÜSSEL \[kein INDEX\] (*Bezug1*\[, *Bezug2* \[,... \] \]) Verweise *Foreigntable* \[(*fremdfeld1* \[, *fremdfeld2* \[,... \] \])\] \[ON UPDATE CASCADE | Legen Sie NULL\] \[ON DELETE CASCADE | Legen Sie NULL\]}

Die CONSTRAINT-Klausel enthält folgende Teile:

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
<td><p><em>name</em></p></td>
<td><p>Der Name der zu erstellenden Einschränkung.</p></td>
</tr>
<tr class="even">
<td><p><em>primär1</em>, <em>primär2</em></p></td>
<td><p>Die Namen der Felder, die als Primärschlüssel gekennzeichnet werden sollen.</p></td>
</tr>
<tr class="odd">
<td><p><em>eindeutig1</em>, <em>eindeutig2</em></p></td>
<td><p>Die Namen der Felder, die als eindeutiger Schlüssel gekennzeichnet werden sollen.</p></td>
</tr>
<tr class="even">
<td><p><em>nichtNull1, nichtNull2</em></p></td>
<td><p>Die Namen der Felder, deren Wert nicht Null sein darf.</p></td>
</tr>
<tr class="odd">
<td><p><em>ref1</em>, <em>ref2</em></p></td>
<td><p>Die Namen fremder Felder, die sich auf Felder in anderen Tabellen beziehen.</p></td>
</tr>
<tr class="even">
<td><p><em>fremdeTabelle</em></p></td>
<td><p>Der Name der fremden Tabelle, in der die Felder <em>fremdesFeld</em> enthalten sind.</p></td>
</tr>
<tr class="odd">
<td><p><em>fremdesFeld1</em>, <em>fremdesFeld2</em></p></td>
<td><p>Die Namen der Felder in <em>fremdeTabelle</em>, angegeben in <em>ref1</em>, <em>ref2</em>. Sie können die Klausel auslassen, wenn das referenzierte Feld der Primärschlüssel von <em>fremdeTabelle</em> ist.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Es handelt sich um eine Beschränkung für ein Feld, wenn die Syntax in der Felddefinitionsklausel einer ALTER TABLE- oder CREATE TABLE-Anweisung direkt auf den Datentyp des Feldes folgt.

Es handelt sich um eine Einschränkung für mehrere Felder, wenn das Schlüsselwort CONSTRAINT in einer ALTER TABLE- oder CREATE TABLE-Anweisung außerhalb einer Felddefinitionsklausel vorkommt.

Mit der Klausel CONSTRAINT können Sie ein Feld als einen der folgenden Ausnahmetypen kennzeichnen:

- Mit dem reservierten Wort UNIQUE können Sie ein Feld als eindeutigen Schlüssel kennzeichnen. Das bedeutet, dass zwei Datensätze in dieser Tabelle in diesem Feld nicht denselben Wert haben dürfen. Sie können ein beliebiges Feld oder eine beliebige Anzahl von Feldern mit dieser Einschränkung belegen. Wird eine Einschränkung für mehrere Felder als eindeutiger Schlüssel gekennzeichnet, müssen lediglich die kombinierten Werte aller Felder eindeutig sein, auch wenn zwei oder mehr Datensätze denselben Wert in einem Feld aufweisen.

- Mit dem reservierten Wort PRIMARY KEY können Sie ein Feld oder eine Auswahl von Feldern in einer Tabelle als Primärschlüssel kennzeichnen. Es ist nur ein eindeutiger Primärschlüssel pro Tabelle zulässig, der zudem nicht **Null** sein darf.
    
  > [!NOTE]
  > [!HINWEIS] Legen Sie keine PRIMARY KEY-Einschränkung für eine Tabelle fest, die bereits einen Primärschlüssel hat. Ansonsten tritt ein Fehler auf.

- Mit dem reservierten Word FOREIGN KEY können Sie ein Feld als fremden Schlüssel kennzeichnen. Wenn der Primärschlüssel der fremden Tabelle aus mehreren Felder besteht, müssen Sie eine Einschränkung für mehrere Felder definieren, in der alle referenzierten Felder, der Name der fremden Tabelle und die Namen der referenzierten Felder in der fremden Tabelle (in derselben Reihenfolge wie die referenzierten Felder) aufgeführt sind. Handelt es sich bei referenzierten Feldern um den Primärschlüssel der fremden Tabelle, müssen Sie die referenzierten Felder nicht angeben. Standardmäßig behandelt die Datenbank-Engine den Primärschlüssel der fremden Tabelle als referenzierte Felder. Einschränkungen für fremde Schlüssel legen bestimmte Aktionen fest, die durchgeführt werden, wenn sich der Wert des entsprechenden Primärschlüssels ändert:

- Sie können festlegen, welche Aktionen auf die fremde Tabelle angewendet werden sollen. Diese Festlegung basiert auf der Aktion, die auf den Primärschlüssel angewendet wird, für den die CONSTRAINT-Klausel definiert wurde. Betrachten Sie beispielsweise die folgende Definition für die Tabelle "Customers":
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Betrachten Sie die folgende Definition der Tabelle "Orders", bei eine Verknüpfung mit einem fremden Schlüssel erstellt wird, die den Primärschlüssel der Tabelle "Customers" referenziert:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Für den fremden Schlüssel wurde sowohl eine ON UPDATE CASCADE- als eine ON DELETE CASCADE-Klausel definiert. Mit der ON UPDATE CASCADE-Klausel wird die Kundennummer (CustId) bei Änderung in der Tabelle "Customers" and die Tabelle "Orders" weitergegeben. Jeder Auftrag mit der entsprechenden Kundennummer als Wert wird automatisch durch die neue Kundennummer aktualisiert. Mit der ON DELETE CASCADE-Klausel werden für einen Kunde, der in der Tabelle "Customers" gelöscht wurde, in der Tabelle "Orders" alle Zeilen mit dieser Kundennummer gelöscht. Betrachten Sie die abweichende Definition der Tabelle "Orders", bei der anstelle der CASCADE-Aktion die Aktion SET NULL verwendet wird:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  Mit der ON UPDATE SET NULL-Klausel werden bei Änderung der Kundennummer (CustId) in der Tabelle "Customers" die entsprechenden Werte in der fremden Tabelle "Orders" automatisch auf "NULL" gesetzt. Dementsprechend werden bei der ON DELETE SET NULL-Klausel alle fremden Schlüssel in der Tabelle "Orders" automatisch auf NULL gesetzt, sobald der Kunde in der Tabelle "Customers" gelöscht wird.

Um die automatische Erstellung von Indizes für Fremdschlüssel zu verhindern, kann der NO INDEX-Modifizierer verwendet werden. Diese Art der Fremdschlüsseldefinition sollte nur in Fällen verwendet werden, bei denen sich ergebenden Indexwerte häufig dupliziert würden. Werden fremde Indexwerte häufig dupliziert, ist ein Index möglichweise ineffizienter als ein ein Tabellenscan. Durch diese Art der Indizierung, bei der Zeilen eingefügt und aus der Tabelle gelöscht werden, beeinträchtigt die Leistung und bietet keinerlei Vorteile.

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

<br/>

