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
ms.openlocfilehash: 26d2b4b6281dd762e95113d5ca022e7c0d136755
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937044"
---
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="0d84e-102">CONSTRAINT-Klausel (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="0d84e-102">CONSTRAINT clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="0d84e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d84e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d84e-104">Eine Einschränkung ähnelt einem Index, obwohl sie auch zur Verknüpfung mit einer anderen Tabelle verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d84e-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="0d84e-p101">Verwenden Sie die CONSTRAINT-Klausel in den [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)- und [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisungen, um Einschränkungen zu erstellen oder zu löschen. Es gibt zwei Arten von CONSTRAINT-Klauseln: eine zum Erstellen einer Einschränkung für ein einzelnes Feld oder zum Erstellen einer Einschränkung für mehrere Felder.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>

> [!NOTE]
> <span data-ttu-id="0d84e-107">[!HINWEIS] Die Datenbank-Engine von Microsoft Access unterstützt CONSTRAINT-Klauseln nicht, genauso wie DDL-Anweisungen mit Datenbank-Engine-Datenbanken, die nicht auf Microsoft Access basieren.</span><span class="sxs-lookup"><span data-stu-id="0d84e-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="0d84e-108">Verwenden Sie stattdessen Methoden DAO **Erstellen** .</span><span class="sxs-lookup"><span data-stu-id="0d84e-108">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d84e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d84e-109">Syntax</span></span>

### <a name="single-field-constraint"></a><span data-ttu-id="0d84e-110">Beschränkung für ein Feld</span><span class="sxs-lookup"><span data-stu-id="0d84e-110">Single-field constraint</span></span>

<span data-ttu-id="0d84e-111">CONSTRAINT *Name* {PRIMARY KEY | EINDEUTIGE | NOT NULL | REFERENCES *Fremdtabelle* \[(*fremdfeld1, fremdfeld2*)\] \[ON UPDATE CASCADE | Legen Sie NULL\] \[ON DELETE CASCADE | Legen Sie NULL\]}</span><span class="sxs-lookup"><span data-stu-id="0d84e-111">CONSTRAINT *name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *foreigntable* \[(*foreignfield1, foreignfield2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

### <a name="multiple-field-constraint"></a><span data-ttu-id="0d84e-112">Beschränkung für mehrere Felder</span><span class="sxs-lookup"><span data-stu-id="0d84e-112">Multiple-field constraint</span></span>

<span data-ttu-id="0d84e-113">CONSTRAINT *Name* {PRIMARY KEY (*primär1*\[, *primär2* \[,... \]\]) | EINDEUTIGE (*eindeutig1*\[, *eindeutig2* \[,... \]\]) | NOT NULL (*nichtnull1*\[, *nichtnull2* \[,... \]\]) | FREMDSCHLÜSSEL \[kein INDEX\] (*Bezug1*\[, *Bezug2* \[,... \] \]) Verweise *Foreigntable* \[(*fremdfeld1* \[, *fremdfeld2* \[,... \] \])\] \[ON UPDATE CASCADE | Legen Sie NULL\] \[ON DELETE CASCADE | Legen Sie NULL\]}</span><span class="sxs-lookup"><span data-stu-id="0d84e-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="0d84e-114">Die CONSTRAINT-Klausel enthält folgende Teile:</span><span class="sxs-lookup"><span data-stu-id="0d84e-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d84e-115">Teil</span><span class="sxs-lookup"><span data-stu-id="0d84e-115">Part</span></span></p></th>
<th><p><span data-ttu-id="0d84e-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0d84e-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d84e-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-118">Der Name der zu erstellenden Einschränkung.</span><span class="sxs-lookup"><span data-stu-id="0d84e-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d84e-119"><em>primär1</em>, <em>primär2</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-119"><em>primary1</em>, <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-120">Die Namen der Felder, die als Primärschlüssel gekennzeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d84e-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d84e-121"><em>eindeutig1</em>, <em>eindeutig2</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-121"><em>unique1</em>, <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-122">Die Namen der Felder, die als eindeutiger Schlüssel gekennzeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0d84e-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d84e-123"><em>nichtNull1, nichtNull2</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-124">Die Namen der Felder, deren Wert nicht Null sein darf.</span><span class="sxs-lookup"><span data-stu-id="0d84e-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d84e-125"><em>ref1</em>, <em>ref2</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-125"><em>ref1</em>, <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-126">Die Namen fremder Felder, die sich auf Felder in anderen Tabellen beziehen.</span><span class="sxs-lookup"><span data-stu-id="0d84e-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d84e-127"><em>fremdeTabelle</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-128">Der Name der fremden Tabelle, in der die Felder <em>fremdesFeld</em> enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0d84e-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d84e-129"><em>fremdesFeld1</em>, <em>fremdesFeld2</em></span><span class="sxs-lookup"><span data-stu-id="0d84e-129"><em>foreignfield1</em>, <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="0d84e-p103">Die Namen der Felder in <em>fremdeTabelle</em>, angegeben in <em>ref1</em>, <em>ref2</em>. Sie können die Klausel auslassen, wenn das referenzierte Feld der Primärschlüssel von <em>fremdeTabelle</em> ist.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0d84e-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d84e-132">Remarks</span></span>

<span data-ttu-id="0d84e-133">Es handelt sich um eine Beschränkung für ein Feld, wenn die Syntax in der Felddefinitionsklausel einer ALTER TABLE- oder CREATE TABLE-Anweisung direkt auf den Datentyp des Feldes folgt.</span><span class="sxs-lookup"><span data-stu-id="0d84e-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="0d84e-134">Es handelt sich um eine Einschränkung für mehrere Felder, wenn das Schlüsselwort CONSTRAINT in einer ALTER TABLE- oder CREATE TABLE-Anweisung außerhalb einer Felddefinitionsklausel vorkommt.</span><span class="sxs-lookup"><span data-stu-id="0d84e-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="0d84e-135">Mit der Klausel CONSTRAINT können Sie ein Feld als einen der folgenden Ausnahmetypen kennzeichnen:</span><span class="sxs-lookup"><span data-stu-id="0d84e-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="0d84e-p104">Mit dem reservierten Wort UNIQUE können Sie ein Feld als eindeutigen Schlüssel kennzeichnen. Das bedeutet, dass zwei Datensätze in dieser Tabelle in diesem Feld nicht denselben Wert haben dürfen. Sie können ein beliebiges Feld oder eine beliebige Anzahl von Feldern mit dieser Einschränkung belegen. Wird eine Einschränkung für mehrere Felder als eindeutiger Schlüssel gekennzeichnet, müssen lediglich die kombinierten Werte aller Felder eindeutig sein, auch wenn zwei oder mehr Datensätze denselben Wert in einem Feld aufweisen.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="0d84e-p105">Mit dem reservierten Wort PRIMARY KEY können Sie ein Feld oder eine Auswahl von Feldern in einer Tabelle als Primärschlüssel kennzeichnen. Es ist nur ein eindeutiger Primärschlüssel pro Tabelle zulässig, der zudem nicht **Null** sein darf.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="0d84e-142">[!HINWEIS] Legen Sie keine PRIMARY KEY-Einschränkung für eine Tabelle fest, die bereits einen Primärschlüssel hat. Ansonsten tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0d84e-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="0d84e-p106">Mit dem reservierten Word FOREIGN KEY können Sie ein Feld als fremden Schlüssel kennzeichnen. Wenn der Primärschlüssel der fremden Tabelle aus mehreren Felder besteht, müssen Sie eine Einschränkung für mehrere Felder definieren, in der alle referenzierten Felder, der Name der fremden Tabelle und die Namen der referenzierten Felder in der fremden Tabelle (in derselben Reihenfolge wie die referenzierten Felder) aufgeführt sind. Handelt es sich bei referenzierten Feldern um den Primärschlüssel der fremden Tabelle, müssen Sie die referenzierten Felder nicht angeben. Standardmäßig behandelt die Datenbank-Engine den Primärschlüssel der fremden Tabelle als referenzierte Felder. Einschränkungen für fremde Schlüssel legen bestimmte Aktionen fest, die durchgeführt werden, wenn sich der Wert des entsprechenden Primärschlüssels ändert:</span><span class="sxs-lookup"><span data-stu-id="0d84e-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="0d84e-p107">Sie können festlegen, welche Aktionen auf die fremde Tabelle angewendet werden sollen. Diese Festlegung basiert auf der Aktion, die auf den Primärschlüssel angewendet wird, für den die CONSTRAINT-Klausel definiert wurde. Betrachten Sie beispielsweise die folgende Definition für die Tabelle "Customers":</span><span class="sxs-lookup"><span data-stu-id="0d84e-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="0d84e-150">Betrachten Sie die folgende Definition der Tabelle "Orders", bei eine Verknüpfung mit einem fremden Schlüssel erstellt wird, die den Primärschlüssel der Tabelle "Customers" referenziert:</span><span class="sxs-lookup"><span data-stu-id="0d84e-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="0d84e-p108">Für den fremden Schlüssel wurde sowohl eine ON UPDATE CASCADE- als eine ON DELETE CASCADE-Klausel definiert. Mit der ON UPDATE CASCADE-Klausel wird die Kundennummer (CustId) bei Änderung in der Tabelle "Customers" and die Tabelle "Orders" weitergegeben. Jeder Auftrag mit der entsprechenden Kundennummer als Wert wird automatisch durch die neue Kundennummer aktualisiert. Mit der ON DELETE CASCADE-Klausel werden für einen Kunde, der in der Tabelle "Customers" gelöscht wurde, in der Tabelle "Orders" alle Zeilen mit dieser Kundennummer gelöscht. Betrachten Sie die abweichende Definition der Tabelle "Orders", bei der anstelle der CASCADE-Aktion die Aktion SET NULL verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="0d84e-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="0d84e-p109">Mit der ON UPDATE SET NULL-Klausel werden bei Änderung der Kundennummer (CustId) in der Tabelle "Customers" die entsprechenden Werte in der fremden Tabelle "Orders" automatisch auf "NULL" gesetzt. Dementsprechend werden bei der ON DELETE SET NULL-Klausel alle fremden Schlüssel in der Tabelle "Orders" automatisch auf NULL gesetzt, sobald der Kunde in der Tabelle "Customers" gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="0d84e-p110">Um die automatische Erstellung von Indizes für Fremdschlüssel zu verhindern, kann der NO INDEX-Modifizierer verwendet werden. Diese Art der Fremdschlüsseldefinition sollte nur in Fällen verwendet werden, bei denen sich ergebenden Indexwerte häufig dupliziert würden. Werden fremde Indexwerte häufig dupliziert, ist ein Index möglichweise ineffizienter als ein ein Tabellenscan. Durch diese Art der Indizierung, bei der Zeilen eingefügt und aus der Tabelle gelöscht werden, beeinträchtigt die Leistung und bietet keinerlei Vorteile.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="0d84e-162">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d84e-162">Example</span></span>

<span data-ttu-id="0d84e-163">In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.</span><span class="sxs-lookup"><span data-stu-id="0d84e-163">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="0d84e-164">Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.</span><span class="sxs-lookup"><span data-stu-id="0d84e-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="0d84e-p111">Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="0d84e-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

