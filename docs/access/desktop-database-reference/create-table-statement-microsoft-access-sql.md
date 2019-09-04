---
title: CREATE TABLE statement (Microsoft Access SQL)
TOCTitle: CREATE TABLE statement (Microsoft Access SQL)
ms:assetid: fc45d36e-6e43-c030-5016-cca8bb1379fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837200(v=office.15)
ms:contentKeyID: 48548888
ms.date: 09/03/2019
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277563
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: dfcbbd55f2d20589849f63f260d40b507c8639f1
ms.sourcegitcommit: b27eedbc4538f78ee15134bf19abbc319605c3bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2019
ms.locfileid: "36706173"
---
# <a name="create-table-statement-microsoft-access-sql"></a><span data-ttu-id="b8187-102">CREATE TABLE statement (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="b8187-102">CREATE TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="b8187-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8187-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8187-104">Erstellt eine neue Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8187-104">Creates a new table.</span></span>

> [!NOTE]
> <span data-ttu-id="b8187-105">Das Microsoft Access-Datenbankmodul unterstützt nicht die Verwendung von CREATE TABLE oder einer der DDL-Anweisungen für Datenbanken, die nicht mit dem Microsoft Access-Datenbankmodul erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="b8187-105">The Microsoft Access database engine does not support the use of CREATE TABLE, or any of the DDL statements, with non-Microsoft Access database engine databases.</span></span> <span data-ttu-id="b8187-106">Verwenden Sie stattdessen die **Create**-Methoden von DAO.</span><span class="sxs-lookup"><span data-stu-id="b8187-106">Use the DAO **Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8187-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8187-107">Syntax</span></span>

<span data-ttu-id="b8187-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span><span class="sxs-lookup"><span data-stu-id="b8187-108">CREATE \[TEMPORARY\] TABLE *table* (*field1 type* \[(*size*)\] \[NOT NULL\] \[WITH COMPRESSION | WITH COMP\] \[*index1*\] \[, *field2* *type* \[(*size*)\] \[NOT NULL\] \[*index2*\] \[, …\]\] \[, CONSTRAINT *multifieldindex* \[, …\]\])</span></span>

<span data-ttu-id="b8187-109">Die CREATE TABLE-Anweisung setzt sich wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="b8187-109">The CREATE TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8187-110">Part</span><span class="sxs-lookup"><span data-stu-id="b8187-110">Part</span></span></p></th>
<th><p><span data-ttu-id="b8187-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b8187-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8187-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="b8187-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-113">Der Name der zu erstellenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8187-113">The name of the table to be created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8187-114"><em>Feld1</em>, <em>Feld2</em></span><span class="sxs-lookup"><span data-stu-id="b8187-114"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-p102">Der Name des Felds oder der Felder, das/die in der neuen Tabelle erstellt werden soll(en). Sie müssen mindestens ein Feld erstellen.</span><span class="sxs-lookup"><span data-stu-id="b8187-p102">The name of field or fields to be created in the new table. You must create at least one field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8187-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="b8187-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-118">Der Datentyp des <em>Felds</em> in der neuen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b8187-118">The data type of <em>field</em> in the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8187-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="b8187-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-120">Die Feldgröße in Zeichen (nur Text- und binäre Felder).</span><span class="sxs-lookup"><span data-stu-id="b8187-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8187-121"><em>Index1</em>, <em>Index2</em></span><span class="sxs-lookup"><span data-stu-id="b8187-121"><em>index1</em>, <em>index2</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-122">Eine CONSTRAINT-Klausel, die einen einfachen Index definiert.</span><span class="sxs-lookup"><span data-stu-id="b8187-122">A CONSTRAINT clause defining a single-field index.</span></span> <span data-ttu-id="b8187-123">Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="b8187-123">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8187-124"><em>zusammengesetzter Index</em></span><span class="sxs-lookup"><span data-stu-id="b8187-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="b8187-125">Eine CONSTRAINT-Klausel, die einen zusammengesetzten Index definiert.</span><span class="sxs-lookup"><span data-stu-id="b8187-125">A CONSTRAINT clause defining a multiple-field index.</span></span> <span data-ttu-id="b8187-126">Weitere Informationen zum Erstellen dieses Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="b8187-126">For more information about how to create this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b8187-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8187-127">Remarks</span></span>

<span data-ttu-id="b8187-128">Verwenden Sie die CREATE TABLE-Anweisung, um eine neue Tabelle und deren Felder sowie Feldeinschränkungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="b8187-128">Use the CREATE TABLE statement to define a new table and its fields and field constraints.</span></span> <span data-ttu-id="b8187-129">Wenn für ein Feld NOT NULL angegeben ist, müssen neue Datensätze gültige Daten in diesem Feld aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b8187-129">If NOT NULL is specified for a field, new records are required to have valid data in that field.</span></span>

<span data-ttu-id="b8187-p106">Eine CONSTRAINT-Klausel erstellt verschiedene Einschränkungen für ein Feld und kann zum Erstellen des Primärschlüssels verwendet werden. Sie können auch die [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung zum Erstellen eines Primärschlüssels oder zusätzlicher Indizes für vorhandene Tabellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8187-p106">A CONSTRAINT clause establishes various restrictions on a field, and can be used to establish the primary key. You can also use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to create a primary key or additional indexes on existing tables.</span></span>

<span data-ttu-id="b8187-p107">Sie können NOT NULL für ein einzelnes Feld oder in einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes Feld oder für mehrere Felder mit dem Namen CONSTRAINT gilt. Sie können die NOT NULL-Einschränkung jedoch nur einmal auf ein Feld anwenden. Der Versuch, diese Einschränkung mehrmals zu verwenden, führt zu einem Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="b8187-p107">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once results in a run-time error.</span></span>

<span data-ttu-id="b8187-135">Beim Erstellen der Tabelle vom Typ TEMPORARY ist diese nur in der Sitzung sichtbar, in der sie erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b8187-135">When a TEMPORARY table is created, it is visible only within the session in which it was created.</span></span> <span data-ttu-id="b8187-136">Sie wird automatisch gelöscht, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8187-136">It is automatically deleted when the session is terminated.</span></span> <span data-ttu-id="b8187-137">Auf temporäre Tabellen können mehrere Benutzer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b8187-137">Temporary tables can be accessed by more than one user.</span></span>

<span data-ttu-id="b8187-138">Das Attribut WITH COMPRESSION kann nur mit den Datentypen CHARACTER und MEMO (auch als TEXT bezeichnet) und deren Synonymen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8187-138">The WITH COMPRESSION attribute can be used only with the CHARACTER and MEMO (also known as TEXT) data types and their synonyms.</span></span>

<span data-ttu-id="b8187-139">Das Attribut WITH COMPRESSION wurde aufgrund der Änderung des Darstellungsformats von Unicode-Zeichen für Zeichenspalten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b8187-139">The WITH COMPRESSION attribute was added for CHARACTER columns because of the change to the Unicode character representation format.</span></span> <span data-ttu-id="b8187-140">Unicode-Zeichen benötigen jeweils zwei Byte, um jedes Zeichen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b8187-140">Unicode characters uniformly require two bytes for each character.</span></span> <span data-ttu-id="b8187-141">Für vorhandene Microsoft Jet-Datenbanken, die überwiegend Zeichendaten enthalten, kann dies bedeuten, dass die Datenbankdatei bei Konvertierung in das Microsoft Access-Datenbankformat ihre Größe nahezu verdoppelt.</span><span class="sxs-lookup"><span data-stu-id="b8187-141">For existing Microsoft Jet databases that contain predominately character data, this could mean that the database file would nearly double in size when converted to the Microsoft Access database engine format.</span></span> <span data-ttu-id="b8187-142">Jedoch kann die Unicode-Darstellung vieler Zeichensätze, die früher als Single-Byte Character Sets (SBCS) bezeichnet wurden, auf einfache Weise zu einem einzelnen Byte komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8187-142">However, Unicode representation of many character sets, those formerly denoted as Single-Byte Character Sets (SBCS), can easily be compressed to a single byte.</span></span> <span data-ttu-id="b8187-143">Wenn Sie eine Zeichenspalte (CHARACTER) mit diesem Attribut definieren, werden die Daten beim Speichern automatisch komprimiert und beim Abrufen aus der Spalte dekomprimiert.</span><span class="sxs-lookup"><span data-stu-id="b8187-143">If you define a CHARACTER column with this attribute, data will automatically be compressed as it is stored and uncompressed when retrieved from the column.</span></span>

<span data-ttu-id="b8187-p110">MEMO-Spalten können auch definiert werden, um Daten in einem komprimierten Format zu speichern. Es gibt jedoch eine Einschränkung. Nur Instanzen von MEMO-Spalten, die in komprimierter Form in 4096 Byte oder weniger passen, werden komprimiert. Alle anderen Instanzen von MEMO-Spalten bleiben dekomprimiert. Dies bedeutet, dass innerhalb einer bestimmten Tabelle für eine bestimmte MEMO-Spalte einige Daten möglicherweise komprimiert werden und einige Daten möglicherweise nicht komprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="b8187-p110">MEMO columns can also be defined to store data in a compressed format. However, there is a limitation. Only instances of MEMO columns that, when compressed, will fit within 4096 bytes or less, will be compressed. All other instances of MEMO columns will remain uncompressed. This means that within a given table, for a given MEMO column, some data may be compressed and some data may not be compressed.</span></span>

## <a name="example"></a><span data-ttu-id="b8187-149">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b8187-149">Example</span></span>

<span data-ttu-id="b8187-150">In diesem Beispiel wird eine neue Tabelle namens "ThisTable" mit zwei Textfeldern erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8187-150">This example creates a new table called ThisTable with two text fields.</span></span>

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

<span data-ttu-id="b8187-151">Bei diesem Beispiel wird eine neue Tabelle mit dem Namen "myTable" und zwei Textfeldern erstellt: einem Datums-/Uhrzeitfeld und einen eindeutigen Index, der aus allen drei Feldern besteht.</span><span class="sxs-lookup"><span data-stu-id="b8187-151">This example creates a new table called MyTable with two text fields, a Date/Time field, and a unique index made up of all three fields.</span></span>

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

<span data-ttu-id="b8187-p111">Im folgenden Beispiel wird eine neue Tabelle mit zwei Textfeldern und einem Feld vom Typ **Integer** erstellt. Das Feld "SSN" ist der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b8187-p111">This example creates a new table with two text fields and an **Integer** field. The SSN field is the primary key.</span></span>

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

<span data-ttu-id="b8187-154">In diesem Beispiel wird eine neue Tabelle mit dem Namen `~~Kitsch'n Sync` erstellt, die alle unterschiedlichen Feld- und Indextypen zeigt.</span><span class="sxs-lookup"><span data-stu-id="b8187-154">This example creates a new table called `~~Kitsch'n Sync` that demonstrates all the different field and index types.</span></span> <span data-ttu-id="b8187-155">Das Feld „AutoWert“ ist der Primärschlüssel.</span><span class="sxs-lookup"><span data-stu-id="b8187-155">The SSN field is the primary key.</span></span>

```vb
    Sub CreateTableX6()
        On Error Resume Next
        Application.CurrentDb.Execute "Drop Table [~~Kitsch'n Sync];"
        On Error GoTo 0
        
        'This example uses ADODB instead of the DAO shown in the previous
        'ones because DAO does not support the DECIMAL and GUID data types
        Dim con As ADODB.Connection
        Set con = CurrentProject.Connection
        con.Execute "" _
            & "CREATE TABLE [~~Kitsch'n Sync](" _
                & " [Auto]                  COUNTER" _
                & ",[Byte]                  BYTE" _
                & ",[Integer]               SMALLINT" _
                & ",[Long]                  INTEGER" _
                & ",[Single]                REAL" _
                & ",[Double]                FLOAT" _
                & ",[Decimal]               DECIMAL(18,5)" _
                & ",[Currency]              MONEY" _
                & ",[ShortText]             CHAR" _
                & ",[LongText]              MEMO" _
                & ",[PlaceHolder1]          MEMO" _
                & ",[DateTime]              DATETIME" _
                & ",[YesNo]                 BIT" _
                & ",[OleObject]             IMAGE" _
                & ",[ReplicationID]         UNIQUEIDENTIFIER" _
                & ",[Required]              INTEGER NOT NULL" _
                & ",[Unicode Compression]   MEMO WITH COMP" _
                & ",[Indexed]               INTEGER" _
                & ",CONSTRAINT [PrimaryKey] PRIMARY KEY ([Auto])" _
                & ",CONSTRAINT [Unique Index] UNIQUE ([Byte],[Integer],[Long])" _
            & ");"
        con.Execute "CREATE INDEX [Single-Field Index] ON [~~Kitsch'n Sync]([Indexed]);"
        con.Execute "CREATE INDEX [Multi-Field Index] ON [~~Kitsch'n Sync]([Auto],[Required]);"
        con.Execute "CREATE INDEX [IgnoreNulls Index] ON [~~Kitsch'n Sync]([Single],[Double]) WITH IGNORE NULL;"
        con.Execute "CREATE UNIQUE INDEX [Combined Index] ON [~~Kitsch'n Sync]([ShortText],[LongText]) WITH IGNORE NULL;"
        Set con = Nothing
    
        'Add a Hyperlink Field
        Dim AllDefs As DAO.TableDefs, TblDef As DAO.TableDef, Fld As DAO.Field
        Set AllDefs = Application.CurrentDb.TableDefs
        Set TblDef = AllDefs("~~Kitsch'n Sync")
        Set Fld = TblDef.CreateField("Hyperlink", dbMemo)
        Fld.Attributes = dbHyperlinkField + dbVariableField
        Fld.OrdinalPosition = 10
        TblDef.Fields.Append Fld
        
        DoCmd.RunSQL "ALTER TABLE [~~Kitsch'n Sync] DROP COLUMN [PlaceHolder1];"
    End Sub
```
