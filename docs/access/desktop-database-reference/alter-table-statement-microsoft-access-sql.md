---
title: ALTER TABLE-Anweisung (Microsoft Access SQL)
TOCTitle: ALTER TABLE Statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8fc826d438973b4d079e9b90d3663ab755821cc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475629"
---
# <a name="alter-table-statement-microsoft-access-sql"></a>ALTER TABLE-Anweisung (Microsoft Access SQL)


**Betrifft**: Access 2013 | Office 2013



Ändert den Entwurf einer Tabelle, nachdem diese mit der [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung erstellt wurde.


> [!NOTE]
> [!HINWEIS] Vom Microsoft Access-Datenbankmodul wird die Verwendung von ALTER TABLE- oder anderen DDL-Anweisungen (Data Definition Language, Datendefinitionssprache) in Nicht-Microsoft Access-Datenbanken nicht unterstützt. Verwenden Sie stattdessen die Create-Methoden von DAO.



## <a name="syntax"></a>Syntax

ALTER TABLE *Tabelle* {ADD {Spalte *Feldtyp*\[(*Größe*)\] \[nicht "NULL"\] \[CONSTRAINT *Index* \] | ALTER COLUMN *Feldtyp*\[(*Größe*)\] | CONSTRAINT *indexmitmehrerenfeldern*} | DROP {COLUMN *Feld* I CONSTRAINT *Indexname*}}

Die ALTER TABLE-Anweisung verfügt über drei Komponenten:

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
<td><p><em>Tabelle</em></p></td>
<td><p>Der Name der zu ändernden Tabelle.</p></td>
</tr>
<tr class="even">
<td><p><em>Feld</em></p></td>
<td><p>Der Name des Felds, das der <em>Tabelle</em> hinzugefügt bzw. aus ihr gelöscht werden soll, oder der Name des in der <em>Tabelle</em> zu ändernden Felds.</p></td>
</tr>
<tr class="odd">
<td><p><em>type</em></p></td>
<td><p>Der Datentyp der <em>Feld</em>-Komponente.</p></td>
</tr>
<tr class="even">
<td><p><em>size</em></p></td>
<td><p>Die Feldgröße in Zeichen (nur Text- und binäre Felder).</p></td>
</tr>
<tr class="odd">
<td><p><em>Index</em></p></td>
<td><p>Der Index für das <em>Feld</em>. Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</p></td>
</tr>
<tr class="even">
<td><p><em>IndexMitMehrerenFeldern</em></p></td>
<td><p>Die Definition eines aus mehreren Feldern bestehenden Indexes, der der <em>Tabelle</em> hinzugefügt werden soll. Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</p></td>
</tr>
<tr class="odd">
<td><p><em>Indexname</em></p></td>
<td><p>Der Name des aus mehreren Feldern bestehenden Indexes, der entfernt werden soll.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Mithilfe der ALTER TABLE-Anweisung können Sie eine bestehende Tabelle auf verschiedene Arten ändern. Folgende Möglichkeiten stehen zur Verfügung:

  - Verwenden Sie ADD COLUMN, um der Tabelle ein neues Feld hinzuzufügen. Sie geben den Feldnamen, den Datentyp und (für Text- und binäre Felder) optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Employees-Tabelle (Personal) ein 25 Zeichen langes Textfeld namens Notes (Bemerkungen) hinzugefügt:
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    Sie können auch einen Index für das Feld definieren. Weitere Informationen zu Einzelfeldindizes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).
    
    Wenn Sie für ein Feld NICHT NULL angeben, sind neue Datensätze erforderlich, damit gültige Daten für das Feld vorhanden sind.

  - Verwenden Sie ALTER COLUMN, um den Datentyp eines bestehenden Felds zu ändern. Sie geben den Feldnamen, den Datentyp und für Text- und binäre Felder optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Datentyp des ZipCode-Felds (PLZ) in der Employees-Tabelle (ursprünglich Integer) in ein 10 Zeichen langes Textfeld geändert:
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - Verwenden Sie ADD CONSTRAINT, um einen aus mehreren Feldern bestehenden Index hinzuzufügen. Weitere Informationen zu Indizes mit mehreren Feldern finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).

  - Verwenden Sie DROP COLUMN, um ein Feld zu löschen. Sie geben lediglich den Namen des Felds an.

  - Verwenden Sie DROP CONSTRAINT, um einen aus mehreren Feldern bestehenden Index zu löschen. Sie geben lediglich den Namen des Indexes, gefolgt vom reservierten Wort CONSTRAINT, an.


> [!NOTE]
> <UL>
> <LI>
> <P>Sie können immer nur ein Feld bzw. einen Index gleichzeitig hinzufügen oder löschen.</P>
> <LI>
> <P>Mithilfe der <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A>-Anweisung können Sie einer Tabelle einen Index mit einem oder mehreren Feldern hinzufügen, und Sie können ALTER TABLE oder die <A href="drop-statement-microsoft-access-sql.md">DROP</A>-Anweisung zum Löschen eines mit ALTER TABLE oder CREATE INDEX erstellten Indexes verwenden.</P>
> <LI>
> <P>Sie können NOT NULL für ein einzelnes Feld oder innerhalb einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes oder mehrere Felder mit dem Namen CONSTRAINT gilt. Sie können die NOT NULL-Beschränkung nur einmal auf ein Feld anwenden. Andernfalls tritt ein Laufzeitfehler auf. 
</P></LI></UL>



## <a name="example"></a>Beispiel

In diesem Beispiel wird der Employees-Tabelle (Personal) ein Salary-Feld (Gehalt) mit dem **Money** -Datentyp hinzugefügt.

```vb
    Sub AlterTableX1() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ADD COLUMN Salary MONEY;" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel wird der Datentyp des Salary-Felds von **Money** in **Char** geändert.

```vb
    Sub AlterTableX2() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add the Salary field to the Employees table  
        ' and make it a Money data type. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "ALTER COLUMN Salary CHAR(20);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel wird das Salary-Feld aus der Employees-Tabelle entfernt.

```vb
    Sub AlterTableX3() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Delete the Salary field from the Employees table. 
        dbs.Execute "ALTER TABLE Employees " _ 
            & "DROP COLUMN Salary;" 
     
        dbs.Close 
     
    End Sub
```

<br/>

Im folgenden Beispiel wird der Orders-Tabelle (Bestellungen) ein Fremdschlüssel hinzugefügt. Der Fremdschlüssel basiert und verweist auf das EmployeeID-Feld (Personal-Nr) in der Employees-Tabelle. In diesem Beispiel muss das EmployeeID-Feld nicht nach der Employees-Tabelle in der REFERENCES-Klausel aufgelistet werden, da es sich bei EmployeeID um den Primärschlüssel der Employees-Tabelle handelt.

```vb
    Sub AlterTableX4() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Add a foreign key to the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "ADD CONSTRAINT OrdersRelationship " _ 
            & "FOREIGN KEY (EmployeeID) " _ 
            & "REFERENCES Employees (EmployeeID);" 
     
        dbs.Close 
     
    End Sub 
```

<br/>

In diesem Beispiel wird der Fremdschlüssel aus der Orders-Tabelle entfernt.

```vb
    Sub AlterTableX5() 
     
        Dim dbs As Database 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Remove the OrdersRelationship foreign key from 
        ' the Orders table. 
        dbs.Execute "ALTER TABLE Orders " _ 
            & "DROP CONSTRAINT OrdersRelationship;" 
     
        dbs.Close 
     
    End Sub
```
