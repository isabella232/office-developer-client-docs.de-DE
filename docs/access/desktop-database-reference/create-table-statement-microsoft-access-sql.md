---
title: CREATE TABLE-Anweisung (Microsoft Access SQL)
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
ms.openlocfilehash: 4beb013b09ce136d6ffa7558225e01fae80da645
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937092"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="e0e41-102">CREATE TABLE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="e0e41-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="e0e41-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0e41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e0e41-104">Erstellt eine neue Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0e41-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="e0e41-105">[!HINWEIS] Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung der CREATE TABLE- oder anderer DDL-Anweisungen für Datenbanken ohne das Microsoft Access-Datenbankmodul.</span><span class="sxs-lookup"><span data-stu-id="e0e41-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="e0e41-106">Verwenden Sie stattdessen Methoden DAO **Erstellen** .</span><span class="sxs-lookup"><span data-stu-id="e0e41-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0e41-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0e41-107">Syntax</span></span>

<span data-ttu-id="e0e41-108">Erstellen von \[temporäre\] Tabelle *Tabelle* (*Feld1 Typ* \[(*Größe*)\] \[nicht "NULL"\] \[WITH COMPRESSION | WITH COMP\] \[ *index1* \] \[, *Feld2* *Typ* \[(*Größe*)\] \[nicht "NULL"\] \[ *index2* \] \[,... \] \] \[, CONSTRAINT *mehrerefelderindex* \[,... \]\])</span><span class="sxs-lookup"><span data-stu-id="e0e41-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="e0e41-109">Die CREATE TABLE-Anweisung besteht aus folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="e0e41-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0e41-110">Teil</span><span class="sxs-lookup"><span data-stu-id="e0e41-110">Part</span></span></p></th>
<th><p><span data-ttu-id="e0e41-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0e41-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0e41-112"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0e41-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e41-114"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-p102">Die Namen der in der neuen Tabelle zu erstellenden Felder. Sie müssen mindestens ein Feld erstellen.</span><span class="sxs-lookup"><span data-stu-id="e0e41-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e41-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-118">Der Datentyp des <em>Felds</em> in der neuen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e0e41-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e41-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-120">Die Feldgröße in Zeichen (nur Text- und binäre Felder).</span><span class="sxs-lookup"><span data-stu-id="e0e41-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e0e41-121"><em>Index1</em>, <em>Index2</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-122">Eine CONSTRAINT-Klausel, die einen Index mit einem Feld definiert.</span><span class="sxs-lookup"><span data-stu-id="e0e41-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="e0e41-123">Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="e0e41-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0e41-124"><em>Index_mit_mehreren_Feldern</em></span><span class="sxs-lookup"><span data-stu-id="e0e41-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="e0e41-125">Eine CONSTRAINT-Klausel, die einen Index mit mehreren Feldern definiert.</span><span class="sxs-lookup"><span data-stu-id="e0e41-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="e0e41-126">Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="e0e41-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e0e41-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e0e41-127">Remarks</span></span>

<span data-ttu-id="e0e41-128">Verwenden Sie die CREATE TABLE-Anweisung, um eine neue Tabelle und deren Felder und Feldeinschränkungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e0e41-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="e0e41-129">Wenn nicht NULL für ein Feld angegeben ist, neue Datensätze sind erforderlich, damit in diesem Feld gültige Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="e0e41-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="e0e41-p106">Eine CONSTRAINT-Klausel erstellt verschiedene Einschränkungen für ein Feld und kann zum Erstellen des Primärschlüssels verwendet werden. Sie können auch die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung zum Erstellen eines Primärschlüssels oder zusätzlicher Indizes für vorhandene Tabellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0e41-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="e0e41-p107">NOT NULL kann für ein einzelnes Feld oder in einer benannten CONSTRAINT-Klausel verwendet werden, die entweder für ein einzelnes Feld oder mehrere Felder namens CONSTRAINT gilt. Jedoch können Sie die NOT NULL-Einschränkung nur einmal auf ein Feld anwenden. Der Versuch, diese Einschränkung mehrmals anzuwenden, führt zu einem Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="e0e41-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="e0e41-135">Wenn eine temporäre Tabelle erstellt wird, ist sichtbar nur innerhalb der Sitzung in der es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e0e41-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="e0e41-136">Sie wird automatisch gelöscht, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0e41-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="e0e41-137">Auf temporäre Tabellen können mehrere Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e0e41-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="e0e41-138">Das WITH COMPRESSION-Attribut kann nur zusammen mit den Datentypen CHARACTER und MEMO (auch TEXT genannt) und den entsprechenden Synonymen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0e41-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="e0e41-139">Das WITH COMPRESSION-Attribut wurde für Zeichenspalten vom Typ CHARACTER aufgrund der Änderung am Unicode-Zeichendarstellungsformat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e0e41-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="e0e41-140">Unicode-Zeichen benötigen jeweils zwei Bytes für jedes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e0e41-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="e0e41-141">Für vorhandene Microsoft Jet-Datenbanken, die vorwiegend Zeichendaten enthalten, kann dies bedeuten, dass die Datenbankdatei beinahe die doppelte Größe, wenn Sie in das Microsoft Access-Datenbank-Engine-Format konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="e0e41-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="e0e41-142">Unicode-Darstellung vieler Zeichensätze, die früher bezeichnet als Einzelbyte-Zeichen (SBCS), jedoch kann auf einfache Weise auf ein einzelnes Byte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0e41-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="e0e41-143">Wenn Sie eine CHARACTER-Spalte mit diesem Attribut definieren, werden die Daten automatisch komprimiert gespeichert und dekomprimiert, wenn der Abruf aus der Spalte erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e0e41-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="e0e41-p110">MEMO-Spalten können auch zum Speichern von Daten in einem komprimierten Format definiert werden, wobei jedoch eine Einschränkung gilt. Nur Instanzen von MEMO-Spalten, die in komprimierten Zustand maximal 4096 Byte groß sind, werden komprimiert. Alle anderen Instanzen von MEMO-Spalten bleiben unkomprimiert. Dies bedeutet, dass in einer Tabelle bei einer bestimmten MEMO-Spalte einige Daten möglicherweise komprimiert werden und andere nicht.</span><span class="sxs-lookup"><span data-stu-id="e0e41-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="e0e41-149">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e0e41-149">Example</span></span>

<span data-ttu-id="e0e41-150">In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0e41-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="e0e41-151">Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.</span><span class="sxs-lookup"><span data-stu-id="e0e41-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="e0e41-p111">Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="e0e41-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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
