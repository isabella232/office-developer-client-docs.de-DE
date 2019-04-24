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
localization_priority: Priority
ms.openlocfilehash: 356620376658bb927c690056f4de9a01554aa47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295646"
---
# <a name="constraint-clause-microsoft-access-sql"></a>CONSTRAINT-Klausel (Microsoft Access SQL)

**Gilt für**: Access 2013, Office 2013

Eine Einschränkung ähnelt einem Index, obwohl sie auch zur Verknüpfung mit einer anderen Tabelle verwendet werden kann.

Verwenden Sie die CONSTRAINT-Klausel in den [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)- und [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisungen, um Einschränkungen zu erstellen oder zu löschen. Es gibt zwei Arten von CONSTRAINT-Klauseln: eine zum Erstellen einer Einschränkung für ein einzelnes Feld oder zum Erstellen einer Einschränkung für mehrere Felder.

> [!NOTE]
> Die Datenbank-Engine von Microsoft Access unterstützt CONSTRAINT-Klauseln nicht, genauso wie DDL-Anweisungen mit Datenbank-Engine-Datenbanken, die nicht auf Microsoft Access basieren. Verwenden Sie stattdessen die **Create**-Methoden von DAO.

## <a name="syntax"></a>Syntax

### <a name="single-field-constraint"></a>Beschränkung für ein einzelnes Feld

CONSTRAINT *Name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *fremde Tabelle* \[(*fremdesFeld1, fremdesFeld2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}

### <a name="multiple-field-constraint"></a>Einschränkung für mehrere Felder

CONSTRAINT-*Name*{PRIMARY KEY (*Primärschlüssel1*\[, *Primärschlüssel2* \[, …\]\]) |UNIQUE (*EindeutigesFeld1*\[, *EindeutigesFeld2* \[, …\]\]) |NOT NULL (*NichtNULLFeld1*\[, *NichtNULLFeld2* \[, …\]\]) |FOREIGN KEY \[NO INDEX\] (*Bezug1*\[, *Bezug2* \[, …\]\]) REFERENCES *Fremdtabelle* \[(*Fremdfeld1* \[, *Fremdfeld2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\]\[ON DELETE CASCADE | SET NULL\]}

Die CONSTRAINT-Klausel besteht aus diesen Teilen:

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
<td><p><em>name</em></p></td>
<td><p>Der Name der Einschränkung, die erstellt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><em>Primärschlüssel1</em>, <em>Primärschlüssel2</em></p></td>
<td><p>Die Namen der Felder, die als Primärschlüssel gekennzeichnet werden sollen.</p></td>
</tr>
<tr class="odd">
<td><p><em>EindeutigesFeld1</em>, <em>EindeutigesFeld2</em></p></td>
<td><p>Der Name des Felds oder der Felder, die als Eindeutiger Schlüssel festgelegt werden.</p></td>
</tr>
<tr class="even">
<td><p><em>NichtNULLFeld1, NichtNULLFeld2</em></p></td>
<td><p>Der Name des Felds/der Felder, die auf NULL ausschließende Werte eingeschränkt sind.</p></td>
</tr>
<tr class="odd">
<td><p><em>Bezug1</em>, <em>Bezug2</em></p></td>
<td><p>Die Namen fremder Felder, die sich auf Felder in anderen Tabellen beziehen.</p></td>
</tr>
<tr class="even">
<td><p><em>Fremdtabelle</em></p></td>
<td><p>Der Name der fremden Tabelle, in der die Felder <em>fremdesFeld</em> enthalten sind.</p></td>
</tr>
<tr class="odd">
<td><p><em>Fremdfeld1</em>, <em>Fremdfeld2</em></p></td>
<td><p>Der Name des Felds oder der Felder in <em>Fremdtabelle</em>, das bzw. die durch <em>Bezug1</em>, <em>Bezug2</em> angegeben wird/werden. Sie können diese Klausel fortlassen, wenn das Feld, auf das verwiesen wird, den Primärschlüssel der <em>Fremdtabelle</em> darstellt.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie können die Syntax für die Einschränkung für ein einzelnes Feld in der Felddefinitionsklausel einer ALTER TABLE- oder CREATE TABLE-Anweisung unmittelbar im Anschluss an die Angabe des Datentyps des Felds verwenden.

Es handelt sich um eine Einschränkung für mehrere Felder, wenn das Schlüsselwort CONSTRAINT in einer ALTER TABLE- oder CREATE TABLE-Anweisung außerhalb einer Felddefinitionsklausel vorkommt.

Mithilfe von CONSTRAINT können Sie ein Feld als eine der folgenden Arten von Einschränkungen bestimmen:

- Sie können das reservierte Wort UNIQUE verwenden, um ein Feld als eindeutigen Schlüssel zu bestimmen. Dies bedeutet, dass keine zwei Datensätze in der Tabelle in diesem Feld den gleichen Wert aufweisen können. Sie können ein beliebiges Feld oder eine beliebige Feldliste als eindeutig bestimmen. Wenn eine mehrere Felder umfassende Einschränkung als eindeutiger Schlüssel bestimmt wird, müssen die kombinierten Werte aller Felder im Index eindeutig sein, selbst wenn zwei oder mehr Datensätze in auch nur einem der Felder den gleichen Wert aufweisen.

- Sie können die reservierten Wörter PRIMARY KEY verwenden, um ein Feld oder eine Menge von Feldern in einer Tabelle als Primärschlüssel festzulegen. Alle Werte im Primärschlüssel müssen eindeutig und dürfen nicht **NULL** sein, und es kann nur einen Primärschlüssel für eine Tabelle geben.
    
  > [!NOTE]
  > Legen Sie keine Einschränkung PRIMARY KEY für eine Tabelle fest, die bereits einen Primärschlüssel aufweist; andernfalls tritt ein Fehler auf.

- Mit dem reservierten Word FOREIGN KEY können Sie ein Feld als fremden Schlüssel kennzeichnen. Wenn der Primärschlüssel der fremden Tabelle aus mehreren Felder besteht, müssen Sie eine Einschränkung für mehrere Felder definieren, in der alle referenzierten Felder, der Name der fremden Tabelle und die Namen der referenzierten Felder in der fremden Tabelle (in derselben Reihenfolge wie die referenzierten Felder) aufgeführt sind. Handelt es sich bei referenzierten Feldern um den Primärschlüssel der fremden Tabelle, müssen Sie die referenzierten Felder nicht angeben. Standardmäßig behandelt die Datenbank-Engine den Primärschlüssel der fremden Tabelle als referenzierte Felder. Einschränkungen für fremde Schlüssel legen bestimmte Aktionen fest, die durchgeführt werden, wenn sich der Wert des entsprechenden Primärschlüssels ändert:

- Sie können Aktionen angeben, die für die Fremdtabelle ausgeführt werden sollen. Die Grundlage bildet eine entsprechende Aktion, die für den Primärschlüssel in der Tabelle ausgeführt wird, in der die CONSTRAINT-Einschränkung definiert ist. Als Beispiel kann die folgende Definition für die Tabelle "Customers" dienen:
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  Betrachten Sie die folgende Definition der Tabelle "Orders", die eine Fremdschlüsselbeziehung definiert, die auf den Primärschlüssel der Tabelle "Customers" verweist:
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  Für den fremden Schlüssel wurde sowohl eine ON UPDATE CASCADE- als eine ON DELETE CASCADE-Klausel definiert. Mit der ON UPDATE CASCADE-Klausel wird die Kundennummer (CustId) bei Änderung in der Tabelle "Customers" and die Tabelle "Orders" weitergegeben. Jeder Auftrag mit der entsprechenden Kundennummer als Wert wird automatisch durch die neue Kundennummer aktualisiert. Mit der ON DELETE CASCADE-Klausel werden für einen Kunde, der in der Tabelle "Customers" gelöscht wurde, in der Tabelle "Orders" alle Zeilen mit dieser Kundennummer gelöscht. Betrachten Sie die abweichende Definition der Tabelle "Orders", bei der anstelle der CASCADE-Aktion die Aktion SET NULL verwendet wird:
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  Die Klausel ON UPDATE SET NULL bedeutet, dass im Fall der Aktualisierung eines Kundenbezeichners (CustId) in der Tabelle "Customer" die entsprechenden Fremdschlüsselwerte in der Tabelle "Orders" automatisch auf NULL festgelegt werden. Analog dazu bedeutet die Klausel ON DELETE SET NULL, dass bei Löschung eines Kunden aus der Tabelle "Customer" alle entsprechenden Fremdschlüssel in der Tabelle "Orders" automatisch auf NULL festgelegt werden.

Um die automatische Erstellung von Indizes für Fremdschlüssel zu verhindern, kann der Modifizierer NO INDEX verwendet werden. Diese Form der Fremdschlüsseldefinition sollte nur in Fällen verwendet werden, in denen die sich ergebenden Indexwerte häufig dupliziert würden. Wenn die Werte in einem Fremdschlüsselindex häufig dupliziert werden, kann die Verwendung eines Index weniger effizient sein als ein einfacher Tabellenscan. Die Wartung dieses Indextyps verringert die Leistung und bietet keinerlei Vorteile, wenn Zeilen in die Tabelle eingefügt und aus ihr gelöscht werden.

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

