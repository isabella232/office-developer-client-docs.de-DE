---
title: ALTER TABLE-Anweisung (Microsoft Access SQL)
TOCTitle: ALTER TABLE statement (Microsoft Access SQL)
ms:assetid: 78e6c92c-e88c-e55f-6b89-435360c166a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196148(v=office.15)
ms:contentKeyID: 48545763
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277560
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 83ba764fa23c972c93156d418bffcde6f3239145
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863696"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="4c6bb-102">ALTER TABLE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="4c6bb-102">ALTER TABLE statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="4c6bb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="4c6bb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4c6bb-104">Ändert den Entwurf einer Tabelle, nachdem diese mit der [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="4c6bb-105">[!HINWEIS] Vom Microsoft Access-Datenbankmodul wird die Verwendung von ALTER TABLE- oder anderen DDL-Anweisungen (Data Definition Language, Datendefinitionssprache) in Nicht-Microsoft Access-Datenbanken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="4c6bb-106">Verwenden Sie stattdessen Methoden **DAO erstellen** .</span><span class="sxs-lookup"><span data-stu-id="4c6bb-106">Use the **DAO Create** methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c6bb-107">Syntax</span></span>

<span data-ttu-id="4c6bb-108">ALTER TABLE *Tabelle* {ADD {Spalte *Feldtyp*\[(*Größe*)\] \[nicht "NULL"\] \[CONSTRAINT *Index* \] | ALTER COLUMN *Feldtyp*\[(*Größe*)\] | CONSTRAINT *indexmitmehrerenfeldern*} | DROP {COLUMN *Feld* I CONSTRAINT *Indexname*}}</span><span class="sxs-lookup"><span data-stu-id="4c6bb-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="4c6bb-109">Die ALTER TABLE-Anweisung verfügt über drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="4c6bb-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4c6bb-110">Teil</span><span class="sxs-lookup"><span data-stu-id="4c6bb-110">Part</span></span></p></th>
<th><p><span data-ttu-id="4c6bb-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c6bb-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c6bb-112"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-113">Der Name der zu ändernden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6bb-114"><em>Feld</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-p102">Der Name des Felds, das der <em>Tabelle</em> hinzugefügt bzw. aus ihr gelöscht werden soll, oder der Name des in der <em>Tabelle</em> zu ändernden Felds.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6bb-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-118">Der Datentyp der <em>Feld</em>-Komponente.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6bb-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-120">Die Feldgröße in Zeichen (nur Text- und binäre Felder).</span><span class="sxs-lookup"><span data-stu-id="4c6bb-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6bb-121"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-122">Der Index für <em>dar</em>.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-122">The index for <em>field</em>.</span></span> <span data-ttu-id="4c6bb-123">Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-123">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c6bb-124"><em>IndexMitMehrerenFeldern</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-125">Die Definition eines mehreren Feldern bestehenden Indexes, <em>Tabelle</em>hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="4c6bb-126">Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-126">For more information about how to construct this index, see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c6bb-127"><em>Indexname</em></span><span class="sxs-lookup"><span data-stu-id="4c6bb-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="4c6bb-128">Der Name des aus mehreren Feldern bestehenden Indexes, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4c6bb-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4c6bb-129">Remarks</span></span>

<span data-ttu-id="4c6bb-130">Mithilfe der ALTER TABLE-Anweisung können Sie eine vorhandene Tabelle auf verschiedene Weise ändern.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-130">By using the ALTER TABLE statement, you can alter an existing table in several ways.</span></span> <span data-ttu-id="4c6bb-131">Folgende Möglichkeiten stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="4c6bb-131">You can:</span></span>

- <span data-ttu-id="4c6bb-p106">Verwenden Sie ADD COLUMN, um der Tabelle ein neues Feld hinzuzufügen. Sie geben den Feldnamen, den Datentyp und (für Text- und binäre Felder) optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Employees-Tabelle (Personal) ein 25 Zeichen langes Textfeld namens Notes (Bemerkungen) hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="4c6bb-135">Sie können auch einen Index für das Feld definieren.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-135">You can also define an index on that field.</span></span> <span data-ttu-id="4c6bb-136">Weitere Informationen zu einem einzigen Feld Indizes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="4c6bb-136">For more information about single-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="4c6bb-137">Wenn Sie NOT NULL für ein Feld angeben, sind neue Datensätze erforderlich, damit in diesem Feld gültige Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-137">If you specify NOT NULL for a field, new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="4c6bb-p108">Verwenden Sie ALTER COLUMN, um den Datentyp eines bestehenden Felds zu ändern. Sie geben den Feldnamen, den Datentyp und für Text- und binäre Felder optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Datentyp des ZipCode-Felds (PLZ) in der Employees-Tabelle (ursprünglich Integer) in ein 10 Zeichen langes Textfeld geändert:</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```
  
- <span data-ttu-id="4c6bb-141">Verwenden Sie ADD CONSTRAINT, um einen aus mehreren Feldern bestehenden Index hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="4c6bb-142">Weitere Informationen zu mehreren Feldern bestehenden Indexes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="4c6bb-142">For more information about multiple-field indexes, see [CONSTRAINT clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="4c6bb-p110">Verwenden Sie DROP COLUMN, um ein Feld zu löschen. Sie geben lediglich den Namen des Felds an.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="4c6bb-p111">Verwenden Sie DROP CONSTRAINT, um einen aus mehreren Feldern bestehenden Index zu löschen. Sie geben lediglich den Namen des Indexes, gefolgt vom reservierten Wort CONSTRAINT, an.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>

> [!NOTE] 
> - <span data-ttu-id="4c6bb-147">Sie können immer nur ein Feld bzw. einen Index gleichzeitig hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="4c6bb-148">Mithilfe der [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung können Sie einer Tabelle einen Index mit einem oder mehreren Feldern hinzufügen, und Sie können ALTER TABLE oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung zum Löschen eines mit ALTER TABLE oder CREATE INDEX erstellten Indexes verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="4c6bb-p112">Sie können NOT NULL für ein einzelnes Feld oder innerhalb einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes oder mehrere Felder mit dem Namen CONSTRAINT gilt. Sie können die NOT NULL-Beschränkung nur einmal auf ein Feld anwenden. Andernfalls tritt ein Laufzeitfehler auf. 
</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p112">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="4c6bb-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4c6bb-152">Example</span></span>

<span data-ttu-id="4c6bb-153">In diesem Beispiel wird der Employees-Tabelle (Personal) ein Salary-Feld (Gehalt) mit dem **Money** -Datentyp hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

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

<span data-ttu-id="4c6bb-154">In diesem Beispiel wird der Datentyp des Salary-Felds von **Money** in **Char** geändert.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

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

<span data-ttu-id="4c6bb-155">In diesem Beispiel wird das Salary-Feld aus der Employees-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-155">This example removes the Salary field from the Employees table.</span></span>

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

<span data-ttu-id="4c6bb-p113">Im folgenden Beispiel wird der Orders-Tabelle (Bestellungen) ein Fremdschlüssel hinzugefügt. Der Fremdschlüssel basiert und verweist auf das EmployeeID-Feld (Personal-Nr) in der Employees-Tabelle. In diesem Beispiel muss das EmployeeID-Feld nicht nach der Employees-Tabelle in der REFERENCES-Klausel aufgelistet werden, da es sich bei EmployeeID um den Primärschlüssel der Employees-Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

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

<span data-ttu-id="4c6bb-159">In diesem Beispiel wird der Fremdschlüssel aus der Orders-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="4c6bb-159">This example removes the foreign key from the Orders table.</span></span>

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
