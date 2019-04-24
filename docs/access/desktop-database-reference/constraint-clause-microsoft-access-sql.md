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
# <a name="constraint-clause-microsoft-access-sql"></a><span data-ttu-id="4dee4-102">CONSTRAINT-Klausel (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4dee4-102">CONSTRAINT Clause (Microsoft Access SQL)</span></span>

<span data-ttu-id="4dee4-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4dee4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4dee4-104">Eine Einschränkung ähnelt einem Index, obwohl sie auch zur Verknüpfung mit einer anderen Tabelle verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4dee4-104">A constraint is similar to an index, although it can also be used to establish a relationship with another table.</span></span>

<span data-ttu-id="4dee4-p101">Verwenden Sie die CONSTRAINT-Klausel in den [ALTER TABLE](alter-table-statement-microsoft-access-sql.md)- und [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisungen, um Einschränkungen zu erstellen oder zu löschen. Es gibt zwei Arten von CONSTRAINT-Klauseln: eine zum Erstellen einer Einschränkung für ein einzelnes Feld oder zum Erstellen einer Einschränkung für mehrere Felder.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p101">You use the CONSTRAINT clause in [ALTER TABLE](alter-table-statement-microsoft-access-sql.md) and [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statements to create or delete constraints. There are two types of CONSTRAINT clauses: one for creating a constraint on a single field and one for creating a constraint on more than one field.</span></span>

> [!NOTE]
> <span data-ttu-id="4dee4-107">Die Datenbank-Engine von Microsoft Access unterstützt CONSTRAINT-Klauseln nicht, genauso wie DDL-Anweisungen mit Datenbank-Engine-Datenbanken, die nicht auf Microsoft Access basieren.</span><span class="sxs-lookup"><span data-stu-id="4dee4-107">The Microsoft Access database engine does not support the use of CONSTRAINT, or any of the data definition language (DDL) statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="4dee4-108">Verwenden Sie stattdessen die **Create**-Methoden von DAO.</span><span class="sxs-lookup"><span data-stu-id="4dee4-108">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dee4-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dee4-109">Syntax</span></span>

### <a name="single-field-constraint"></a><span data-ttu-id="4dee4-110">Beschränkung für ein einzelnes Feld</span><span class="sxs-lookup"><span data-stu-id="4dee4-110">Single-field constraint:</span></span>

<span data-ttu-id="4dee4-111">CONSTRAINT *Name* {PRIMARY KEY | UNIQUE | NOT NULL | REFERENCES *fremde Tabelle* \[(*fremdesFeld1, fremdesFeld2*)\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="4dee4-111">CONSTRAINT name {PRIMARY KEY | UNIQUE | NOT NULL | 
    REFERENCES foreigntable [(foreignfield1, foreignfield2)] 
    [ON UPDATE CASCADE | SET NULL] 
    [ON DELETE CASCADE | SET NULL]}</span></span>

### <a name="multiple-field-constraint"></a><span data-ttu-id="4dee4-112">Einschränkung für mehrere Felder</span><span class="sxs-lookup"><span data-stu-id="4dee4-112">Multiple-field constraint:</span></span>

<span data-ttu-id="4dee4-113">CONSTRAINT-*Name*{PRIMARY KEY (*Primärschlüssel1*\[, *Primärschlüssel2* \[, …\]\]) |UNIQUE (*EindeutigesFeld1*\[, *EindeutigesFeld2* \[, …\]\]) |NOT NULL (*NichtNULLFeld1*\[, *NichtNULLFeld2* \[, …\]\]) |FOREIGN KEY \[NO INDEX\] (*Bezug1*\[, *Bezug2* \[, …\]\]) REFERENCES *Fremdtabelle* \[(*Fremdfeld1* \[, *Fremdfeld2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\]\[ON DELETE CASCADE | SET NULL\]}</span><span class="sxs-lookup"><span data-stu-id="4dee4-113">CONSTRAINT *name* {PRIMARY KEY (*primary1*\[, *primary2* \[, …\]\]) | UNIQUE (*unique1*\[, *unique2* \[, …\]\]) | NOT NULL (*notnull1*\[, *notnull2* \[, …\]\]) | FOREIGN KEY \[NO INDEX\] (*ref1*\[, *ref2* \[, …\]\]) REFERENCES *foreigntable* \[(*foreignfield1* \[, *foreignfield2* \[, …\]\])\] \[ON UPDATE CASCADE | SET NULL\] \[ON DELETE CASCADE | SET NULL\]}</span></span>

<span data-ttu-id="4dee4-114">Die CONSTRAINT-Klausel besteht aus diesen Teilen:</span><span class="sxs-lookup"><span data-stu-id="4dee4-114">The CONSTRAINT clause has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4dee4-115">Part</span><span class="sxs-lookup"><span data-stu-id="4dee4-115">Part</span></span></p></th>
<th><p><span data-ttu-id="4dee4-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dee4-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4dee4-117"><em>name</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-117"><em>name</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-118">Der Name der Einschränkung, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4dee4-118">The name of the constraint to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dee4-119"><em>Primärschlüssel1</em>, <em>Primärschlüssel2</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-119"><em>primary1</em>  ,  <em>primary2</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-120">Die Namen der Felder, die als Primärschlüssel gekennzeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4dee4-120">The name of the field or fields to be designated the primary key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dee4-121"><em>EindeutigesFeld1</em>, <em>EindeutigesFeld2</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-121"><em>unique1</em>  ,  <em>unique2</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-122">Der Name des Felds oder der Felder, die als Eindeutiger Schlüssel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4dee4-122">The name of the field or fields to be designated as a unique key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dee4-123"><em>NichtNULLFeld1, NichtNULLFeld2</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-123"><em>notnull1, notnull2</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-124">Der Name des Felds/der Felder, die auf NULL ausschließende Werte eingeschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="4dee4-124">The name of the field or fields that are restricted to non-Null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dee4-125"><em>Bezug1</em>, <em>Bezug2</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-125"><em>ref1</em>  ,  <em>ref2</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-126">Die Namen fremder Felder, die sich auf Felder in anderen Tabellen beziehen.</span><span class="sxs-lookup"><span data-stu-id="4dee4-126">The name of a foreign key field or fields that refer to fields in another table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4dee4-127"><em>Fremdtabelle</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-127"><em>foreigntable</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-128">Der Name der fremden Tabelle, in der die Felder <em>fremdesFeld</em> enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4dee4-128">The name of the foreign table containing the field or fields specified by <em>foreignfield</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4dee4-129"><em>Fremdfeld1</em>, <em>Fremdfeld2</em></span><span class="sxs-lookup"><span data-stu-id="4dee4-129"><em>foreignfield1</em>  ,  <em>foreignfield2</em></span></span></p></td>
<td><p><span data-ttu-id="4dee4-p103">Der Name des Felds oder der Felder in <em>Fremdtabelle</em>, das bzw. die durch <em>Bezug1</em>, <em>Bezug2</em> angegeben wird/werden. Sie können diese Klausel fortlassen, wenn das Feld, auf das verwiesen wird, den Primärschlüssel der <em>Fremdtabelle</em> darstellt.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p103">The name of the field or fields in <em>foreigntable</em> specified by <em>ref1</em>, <em>ref2</em>. You can omit this clause if the referenced field is the primary key of <em>foreigntable</em>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4dee4-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4dee4-132">Remarks</span></span>

<span data-ttu-id="4dee4-133">Sie können die Syntax für die Einschränkung für ein einzelnes Feld in der Felddefinitionsklausel einer ALTER TABLE- oder CREATE TABLE-Anweisung unmittelbar im Anschluss an die Angabe des Datentyps des Felds verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dee4-133">You use the syntax for a single-field constraint in the field-definition clause of an ALTER TABLE or CREATE TABLE statement immediately following the specification of the field's data type.</span></span>

<span data-ttu-id="4dee4-134">Es handelt sich um eine Einschränkung für mehrere Felder, wenn das Schlüsselwort CONSTRAINT in einer ALTER TABLE- oder CREATE TABLE-Anweisung außerhalb einer Felddefinitionsklausel vorkommt.</span><span class="sxs-lookup"><span data-stu-id="4dee4-134">You use the syntax for a multiple-field constraint whenever you use the reserved word CONSTRAINT outside a field-definition clause in an ALTER TABLE or CREATE TABLE statement.</span></span>

<span data-ttu-id="4dee4-135">Mithilfe von CONSTRAINT können Sie ein Feld als eine der folgenden Arten von Einschränkungen bestimmen:</span><span class="sxs-lookup"><span data-stu-id="4dee4-135">Using CONSTRAINT you can designate a field as one of the following types of constraints:</span></span>

- <span data-ttu-id="4dee4-p104">Sie können das reservierte Wort UNIQUE verwenden, um ein Feld als eindeutigen Schlüssel zu bestimmen. Dies bedeutet, dass keine zwei Datensätze in der Tabelle in diesem Feld den gleichen Wert aufweisen können. Sie können ein beliebiges Feld oder eine beliebige Feldliste als eindeutig bestimmen. Wenn eine mehrere Felder umfassende Einschränkung als eindeutiger Schlüssel bestimmt wird, müssen die kombinierten Werte aller Felder im Index eindeutig sein, selbst wenn zwei oder mehr Datensätze in auch nur einem der Felder den gleichen Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p104">You can use the UNIQUE reserved word to designate a field as a unique key. This means that no two records in the table can have the same value in this field. You can constrain any field or list of fields as unique. If a multiple-field constraint is designated as a unique key, the combined values of all fields in the index must be unique, even if two or more records have the same value in just one of the fields.</span></span>

- <span data-ttu-id="4dee4-p105">Sie können die reservierten Wörter PRIMARY KEY verwenden, um ein Feld oder eine Menge von Feldern in einer Tabelle als Primärschlüssel festzulegen. Alle Werte im Primärschlüssel müssen eindeutig und dürfen nicht **NULL** sein, und es kann nur einen Primärschlüssel für eine Tabelle geben.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p105">You can use the PRIMARY KEY reserved words to designate one field or set of fields in a table as a primary key. All values in the primary key must be unique and not **Null**, and there can be only one primary key for a table.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="4dee4-142">Legen Sie keine Einschränkung PRIMARY KEY für eine Tabelle fest, die bereits einen Primärschlüssel aufweist; andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4dee4-142">Do not set a PRIMARY KEY constraint on a table that already has a primary key; if you do, an error occurs.</span></span>

- <span data-ttu-id="4dee4-p106">Mit dem reservierten Word FOREIGN KEY können Sie ein Feld als fremden Schlüssel kennzeichnen. Wenn der Primärschlüssel der fremden Tabelle aus mehreren Felder besteht, müssen Sie eine Einschränkung für mehrere Felder definieren, in der alle referenzierten Felder, der Name der fremden Tabelle und die Namen der referenzierten Felder in der fremden Tabelle (in derselben Reihenfolge wie die referenzierten Felder) aufgeführt sind. Handelt es sich bei referenzierten Feldern um den Primärschlüssel der fremden Tabelle, müssen Sie die referenzierten Felder nicht angeben. Standardmäßig behandelt die Datenbank-Engine den Primärschlüssel der fremden Tabelle als referenzierte Felder. Einschränkungen für fremde Schlüssel legen bestimmte Aktionen fest, die durchgeführt werden, wenn sich der Wert des entsprechenden Primärschlüssels ändert:</span><span class="sxs-lookup"><span data-stu-id="4dee4-p106">You can use the FOREIGN KEY reserved words to designate a field as a foreign key. If the foreign table's primary key consists of more than one field, you must use a multiple-field constraint definition, listing all of the referencing fields, the name of the foreign table, and the names of the referenced fields in the foreign table in the same order that the referencing fields are listed. If the referenced field or fields are the foreign table's primary key, you do not have to specify the referenced fields. By default the database engine behaves as if the foreign table's primary key is the referenced fields. Foreign key constraints define specific actions to be performed when a corresponding primary key value is changed:</span></span>

- <span data-ttu-id="4dee4-p107">Sie können Aktionen angeben, die für die Fremdtabelle ausgeführt werden sollen. Die Grundlage bildet eine entsprechende Aktion, die für den Primärschlüssel in der Tabelle ausgeführt wird, in der die CONSTRAINT-Einschränkung definiert ist. Als Beispiel kann die folgende Definition für die Tabelle "Customers" dienen:</span><span class="sxs-lookup"><span data-stu-id="4dee4-p107">You can specify actions to be performed on the foreign table based on a corresponding action performed on a primary key in the table on which the CONSTRAINT is defined. For example, consider the following definition for the table Customers:</span></span>
    
  ``` sql
    CREATE TABLE Customers (CustId INTEGER PRIMARY KEY, CLstNm NCHAR VARYING (50))
  ```
    
  <span data-ttu-id="4dee4-150">Betrachten Sie die folgende Definition der Tabelle "Orders", die eine Fremdschlüsselbeziehung definiert, die auf den Primärschlüssel der Tabelle "Customers" verweist:</span><span class="sxs-lookup"><span data-stu-id="4dee4-150">Consider the following definition of the table Orders, which defines a foreign key relationship referencing the primary key of the Customers table:</span></span>
    
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE CASCADE ON DELETE CASCADE
  ```
    
  <span data-ttu-id="4dee4-p108">Für den fremden Schlüssel wurde sowohl eine ON UPDATE CASCADE- als eine ON DELETE CASCADE-Klausel definiert. Mit der ON UPDATE CASCADE-Klausel wird die Kundennummer (CustId) bei Änderung in der Tabelle "Customers" and die Tabelle "Orders" weitergegeben. Jeder Auftrag mit der entsprechenden Kundennummer als Wert wird automatisch durch die neue Kundennummer aktualisiert. Mit der ON DELETE CASCADE-Klausel werden für einen Kunde, der in der Tabelle "Customers" gelöscht wurde, in der Tabelle "Orders" alle Zeilen mit dieser Kundennummer gelöscht. Betrachten Sie die abweichende Definition der Tabelle "Orders", bei der anstelle der CASCADE-Aktion die Aktion SET NULL verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="4dee4-p108">Both an ON UPDATE CASCADE and an ON DELETE CASCADE clause are defined on the foreign key. The ON UPDATE CASCADE clause means that if a customer's identifier (CustId) is updated in the Customer table, the update will be cascaded through the Orders table. Each order containing a corresponding customer identifier value will be updated automatically with the new value. The ON DELETE CASCADE clause means that if a customer is deleted from the Customer table, all rows in the Orders table containing the same customer identifier value will also be deleted. Consider the following different definition of the table Orders, using the SET NULL action instead of the CASCADE action:</span></span>
  
  ``` sql
    CREATE TABLE Orders (OrderId INTEGER PRIMARY KEY, CustId INTEGER, OrderNotes NCHAR VARYING (255), CONSTRAINT FKOrdersCustId FOREIGN KEY (CustId) REFERENCES Customers ON UPDATE SET NULL ON DELETE SET NULL
  ```
    
  <span data-ttu-id="4dee4-p109">Die Klausel ON UPDATE SET NULL bedeutet, dass im Fall der Aktualisierung eines Kundenbezeichners (CustId) in der Tabelle "Customer" die entsprechenden Fremdschlüsselwerte in der Tabelle "Orders" automatisch auf NULL festgelegt werden. Analog dazu bedeutet die Klausel ON DELETE SET NULL, dass bei Löschung eines Kunden aus der Tabelle "Customer" alle entsprechenden Fremdschlüssel in der Tabelle "Orders" automatisch auf NULL festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p109">The ON UPDATE SET NULL clause means that if a customer's identifier (CustId) is updated in the Customer table, the corresponding foreign key values in the Orders table will automatically be set to NULL. Similarly, the ON DELETE SET NULL clause means that if a customer is deleted from the Customer table, all corresponding foreign keys in the Orders table will automatically be set to NULL.</span></span>

<span data-ttu-id="4dee4-p110">Um die automatische Erstellung von Indizes für Fremdschlüssel zu verhindern, kann der Modifizierer NO INDEX verwendet werden. Diese Form der Fremdschlüsseldefinition sollte nur in Fällen verwendet werden, in denen die sich ergebenden Indexwerte häufig dupliziert würden. Wenn die Werte in einem Fremdschlüsselindex häufig dupliziert werden, kann die Verwendung eines Index weniger effizient sein als ein einfacher Tabellenscan. Die Wartung dieses Indextyps verringert die Leistung und bietet keinerlei Vorteile, wenn Zeilen in die Tabelle eingefügt und aus ihr gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p110">To prevent the automatic creation of indexes for foreign keys, the modifier NO INDEX can be used. This form of foreign key definition should be used only in cases where the resulting index values would be frequently duplicated. Where the values in a foreign key index are frequently duplicated, using an index can be less efficient than simply performing a table scan. Maintaining this type of index, with rows inserted and deleted from the table, degrades performance and does not provide any benefit.</span></span>

## <a name="example"></a><span data-ttu-id="4dee4-162">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4dee4-162">Example</span></span>

<span data-ttu-id="4dee4-163">In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.</span><span class="sxs-lookup"><span data-stu-id="4dee4-163">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="4dee4-164">Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.</span><span class="sxs-lookup"><span data-stu-id="4dee4-164">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="4dee4-p111">Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="4dee4-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

