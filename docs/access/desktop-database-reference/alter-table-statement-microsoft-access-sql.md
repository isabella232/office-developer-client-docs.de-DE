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
localization_priority: Priority
ms.openlocfilehash: b8bd9abac3aee8be8fe52e555fcd5247e804f258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297158"
---
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="a8fac-102">ALTER TABLE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="a8fac-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="a8fac-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8fac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8fac-104">Ändert den Entwurf einer Tabelle, nachdem diese mit der [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8fac-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>

> [!NOTE]
> <span data-ttu-id="a8fac-105">Vom Microsoft Access-Datenbankmodul wird die Verwendung von ALTER TABLE- oder anderen DDL-Anweisungen (Data Definition Language, Datendefinitionssprache) in Nicht-Microsoft Access-Datenbanken nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-105">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases.</span></span> <span data-ttu-id="a8fac-106">Verwenden Sie stattdessen die **Create**-Methoden von DAO.</span><span class="sxs-lookup"><span data-stu-id="a8fac-106">Use the DAO Create methods instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fac-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8fac-107">Syntax</span></span>

<span data-ttu-id="a8fac-108">ALTER TABLE *Tabelle* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *Index*\] | ALTER COLUMN *Feldtyp*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *Feld* I CONSTRAINT *indexname*} }</span><span class="sxs-lookup"><span data-stu-id="a8fac-108">ALTER TABLE table {ADD {COLUMN field type[(size)] [NOT NULL]     [CONSTRAINT index] | 
    ALTER COLUMN field type[(size)] | 
    CONSTRAINT multifieldindex} | 
    DROP {COLUMN field I CONSTRAINT indexname} }</span></span>

<span data-ttu-id="a8fac-109">Die ALTER TABLE-Anweisung verfügt über drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="a8fac-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8fac-110">Komponente</span><span class="sxs-lookup"><span data-stu-id="a8fac-110">Part</span></span></p></th>
<th><p><span data-ttu-id="a8fac-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8fac-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8fac-112"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-113">Der Name der zu ändernden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a8fac-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8fac-114"><em>Feld</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-p102">Der Name des Felds, das der <em>Tabelle</em> hinzugefügt bzw. aus ihr gelöscht werden soll, oder der Name des in der <em>Tabelle</em> zu ändernden Felds.</span><span class="sxs-lookup"><span data-stu-id="a8fac-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8fac-117"><em>Typ</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-118">Der Datentyp der <em>Feld</em>-Komponente.</span><span class="sxs-lookup"><span data-stu-id="a8fac-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8fac-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-120">Die Feldgröße in Zeichen (nur Text- und binäre Felder).</span><span class="sxs-lookup"><span data-stu-id="a8fac-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8fac-121"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-122">Der Index für <em>Feld</em>.</span><span class="sxs-lookup"><span data-stu-id="a8fac-122">The index for <em>field</em>.</span></span> <span data-ttu-id="a8fac-123">Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="a8fac-123">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8fac-124"><em>multifieldindex</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-125">Die Definition eines zusammengesetzten Index, der zur <em>Tabelle</em> hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8fac-125">The definition of a multiple-field index to be added to <em>table</em>.</span></span> <span data-ttu-id="a8fac-126">Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="a8fac-126">For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8fac-127"><em>Indexname</em></span><span class="sxs-lookup"><span data-stu-id="a8fac-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="a8fac-128">Der Name des aus mehreren Feldern bestehenden Indexes, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8fac-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a8fac-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8fac-129">Remarks</span></span>

<span data-ttu-id="a8fac-130">Mithilfe der ALTER TABLE-Anweisung können Sie eine bestehende Tabelle auf verschiedene Arten ändern.</span><span class="sxs-lookup"><span data-stu-id="a8fac-130">Using the ALTER TABLE statement you can alter an existing table in several ways.</span></span> <span data-ttu-id="a8fac-131">Sie können:</span><span class="sxs-lookup"><span data-stu-id="a8fac-131">You can:</span></span>

- <span data-ttu-id="a8fac-p106">Verwenden Sie ADD COLUMN, um der Tabelle ein neues Feld hinzuzufügen. Sie geben den Feldnamen, den Datentyp und (für Text- und binäre Felder) optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Employees-Tabelle (Personal) ein 25 Zeichen langes Textfeld namens Notes (Bemerkungen) hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="a8fac-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
  ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
  ```
    
  <span data-ttu-id="a8fac-135">Sie können auch einen Index für dieses Feld definieren.</span><span class="sxs-lookup"><span data-stu-id="a8fac-135">You can also define an index on that field.</span></span> <span data-ttu-id="a8fac-136">Weitere Informationen zu Einzelfeldindexes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a8fac-136">For more information on single-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
  <span data-ttu-id="a8fac-137">Wenn Sie für ein Feld NICHT NULL angeben, sind neue Datensätze erforderlich, damit gültige Daten für das Feld vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a8fac-137">If you specify NOT NULL for a field then new records are required to have valid data in that field.</span></span>

- <span data-ttu-id="a8fac-p108">Verwenden Sie ALTER COLUMN, um den Datentyp eines bestehenden Felds zu ändern. Sie geben den Feldnamen, den Datentyp und für Text- und binäre Felder optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Datentyp des ZipCode-Felds (PLZ) in der Employees-Tabelle (ursprünglich Integer) in ein 10 Zeichen langes Textfeld geändert:</span><span class="sxs-lookup"><span data-stu-id="a8fac-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
  ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
  ```

- <span data-ttu-id="a8fac-141">Sie können ADD CONSTRAINT verwenden, um einen zusammengesetzten Index hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a8fac-141">Use ADD CONSTRAINT to add a multiple-field index.</span></span> <span data-ttu-id="a8fac-142">Weitere Informationen zu zusammengesetzten Indexes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="a8fac-142">For more information on multiple-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>

- <span data-ttu-id="a8fac-p110">Verwenden Sie DROP COLUMN, um ein Feld zu löschen. Sie geben lediglich den Namen des Felds an.</span><span class="sxs-lookup"><span data-stu-id="a8fac-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

- <span data-ttu-id="a8fac-p111">Verwenden Sie DROP CONSTRAINT, um einen aus mehreren Feldern bestehenden Index zu löschen. Sie geben lediglich den Namen des Indexes, gefolgt vom reservierten Wort CONSTRAINT, an.</span><span class="sxs-lookup"><span data-stu-id="a8fac-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE] 
> - <span data-ttu-id="a8fac-147">Sie können immer nur ein Feld bzw. einen Index gleichzeitig hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="a8fac-147">You cannot add or delete more than one field or index at a time.</span></span>
> - <span data-ttu-id="a8fac-148">Mithilfe der [CREATE INDEX](create-index-statement-microsoft-access-sql.md)-Anweisung können Sie einer Tabelle einen Index mit einem oder mehreren Feldern hinzufügen, und Sie können ALTER TABLE oder die [DROP](drop-statement-microsoft-access-sql.md)-Anweisung zum Löschen eines mit ALTER TABLE oder CREATE INDEX erstellten Indexes verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8fac-148">You can use the [CREATE INDEX](create-index-statement-microsoft-access-sql.md) statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the [DROP](drop-statement-microsoft-access-sql.md) statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span>
> - <span data-ttu-id="a8fac-149">Sie können NOT NULL für ein einzelnes Feld oder in einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes Feld oder für mehrere Felder mit dem Namen CONSTRAINT gilt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-149">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT.</span></span> <span data-ttu-id="a8fac-150">Sie können die NOT NULL-Einschränkung jedoch nur einmal auf ein Feld anwenden.</span><span class="sxs-lookup"><span data-stu-id="a8fac-150">However, you can apply the NOT NULL restriction only once to a field.</span></span> <span data-ttu-id="a8fac-151">Der Versuch, diese Einschränkung mehrmals zu verwenden, führt zu einem Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="a8fac-151">Attempting to apply this restriction more than once restuls in a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="a8fac-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a8fac-152">Example</span></span>

<span data-ttu-id="a8fac-153">In diesem Beispiel wird der Employees-Tabelle (Personal) ein Salary-Feld (Gehalt) mit dem **Money**-Datentyp hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

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

<span data-ttu-id="a8fac-154">In diesem Beispiel wird der Datentyp des Salary-Felds von **Money** in **Char** geändert.</span><span class="sxs-lookup"><span data-stu-id="a8fac-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

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

<span data-ttu-id="a8fac-155">In diesem Beispiel wird das Salary-Feld aus der Employees-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-155">This example removes the Salary field from the Employees table.</span></span>

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

<span data-ttu-id="a8fac-p113">Im folgenden Beispiel wird der Orders-Tabelle (Bestellungen) ein Fremdschlüssel hinzugefügt. Der Fremdschlüssel basiert und verweist auf das EmployeeID-Feld (Personal-Nr) in der Employees-Tabelle. In diesem Beispiel muss das EmployeeID-Feld nicht nach der Employees-Tabelle in der REFERENCES-Klausel aufgelistet werden, da es sich bei EmployeeID um den Primärschlüssel der Employees-Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

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

<span data-ttu-id="a8fac-159">In diesem Beispiel wird der Fremdschlüssel aus der Orders-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="a8fac-159">This example removes the foreign key from the Orders table.</span></span>

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
