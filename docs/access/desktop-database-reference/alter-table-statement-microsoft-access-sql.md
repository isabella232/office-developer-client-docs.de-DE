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
# <a name="alter-table-statement-microsoft-access-sql"></a><span data-ttu-id="c25af-102">ALTER TABLE-Anweisung (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c25af-102">ALTER TABLE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="c25af-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c25af-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="c25af-104">Ändert den Entwurf einer Tabelle, nachdem diese mit der [CREATE TABLE](create-table-statement-microsoft-access-sql.md)-Anweisung erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c25af-104">Modifies the design of a table after it has been created with the [CREATE TABLE](create-table-statement-microsoft-access-sql.md) statement.</span></span>


> [!NOTE]
> <span data-ttu-id="c25af-p101">[!HINWEIS] Vom Microsoft Access-Datenbankmodul wird die Verwendung von ALTER TABLE- oder anderen DDL-Anweisungen (Data Definition Language, Datendefinitionssprache) in Nicht-Microsoft Access-Datenbanken nicht unterstützt. Verwenden Sie stattdessen die Create-Methoden von DAO.</span><span class="sxs-lookup"><span data-stu-id="c25af-p101">The Microsoft Access database engine does not support the use of ALTER TABLE, or any of the data definition language (DDL) statements, with non-Microsoft Access databases. Use the DAO Create methods instead.</span></span>



## <a name="syntax"></a><span data-ttu-id="c25af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c25af-107">Syntax</span></span>

<span data-ttu-id="c25af-108">ALTER TABLE *Tabelle* {ADD {Spalte *Feldtyp*\[(*Größe*)\] \[nicht "NULL"\] \[CONSTRAINT *Index* \] | ALTER COLUMN *Feldtyp*\[(*Größe*)\] | CONSTRAINT *indexmitmehrerenfeldern*} | DROP {COLUMN *Feld* I CONSTRAINT *Indexname*}}</span><span class="sxs-lookup"><span data-stu-id="c25af-108">ALTER TABLE *table* {ADD {COLUMN *field type*\[(*size*)\] \[NOT NULL\] \[CONSTRAINT *index*\] | ALTER COLUMN *field type*\[(*size*)\] | CONSTRAINT *multifieldindex*} | DROP {COLUMN *field* I CONSTRAINT *indexname*} }</span></span>

<span data-ttu-id="c25af-109">Die ALTER TABLE-Anweisung verfügt über drei Komponenten:</span><span class="sxs-lookup"><span data-stu-id="c25af-109">The ALTER TABLE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c25af-110">Teil</span><span class="sxs-lookup"><span data-stu-id="c25af-110">Part</span></span></p></th>
<th><p><span data-ttu-id="c25af-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c25af-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c25af-112"><em>Tabelle</em></span><span class="sxs-lookup"><span data-stu-id="c25af-112"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-113">Der Name der zu ändernden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c25af-113">The name of the table to be altered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c25af-114"><em>Feld</em></span><span class="sxs-lookup"><span data-stu-id="c25af-114"><em>field</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-p102">Der Name des Felds, das der <em>Tabelle</em> hinzugefügt bzw. aus ihr gelöscht werden soll, oder der Name des in der <em>Tabelle</em> zu ändernden Felds.</span><span class="sxs-lookup"><span data-stu-id="c25af-p102">The name of the field to be added to or deleted from <em>table</em>. Or, the name of the field to be altered in <em>table</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c25af-117"><em>type</em></span><span class="sxs-lookup"><span data-stu-id="c25af-117"><em>type</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-118">Der Datentyp der <em>Feld</em>-Komponente.</span><span class="sxs-lookup"><span data-stu-id="c25af-118">The data type of <em>field</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c25af-119"><em>size</em></span><span class="sxs-lookup"><span data-stu-id="c25af-119"><em>size</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-120">Die Feldgröße in Zeichen (nur Text- und binäre Felder).</span><span class="sxs-lookup"><span data-stu-id="c25af-120">The field size in characters (Text and Binary fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c25af-121"><em>Index</em></span><span class="sxs-lookup"><span data-stu-id="c25af-121"><em>index</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-p103">Der Index für das <em>Feld</em>. Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="c25af-p103">The index for <em>field</em>. For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c25af-124"><em>IndexMitMehrerenFeldern</em></span><span class="sxs-lookup"><span data-stu-id="c25af-124"><em>multifieldindex</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-p104">Die Definition eines aus mehreren Feldern bestehenden Indexes, der der <em>Tabelle</em> hinzugefügt werden soll. Weitere Informationen zum Aufbau des Indexes finden Sie unter <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT-Klausel</a>.</span><span class="sxs-lookup"><span data-stu-id="c25af-p104">The definition of a multiple-field index to be added to <em>table</em>. For more information on how to construct this index see <a href="constraint-clause-microsoft-access-sql.md">CONSTRAINT Clause</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c25af-127"><em>Indexname</em></span><span class="sxs-lookup"><span data-stu-id="c25af-127"><em>indexname</em></span></span></p></td>
<td><p><span data-ttu-id="c25af-128">Der Name des aus mehreren Feldern bestehenden Indexes, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c25af-128">The name of the multiple-field index to be removed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c25af-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c25af-129">Remarks</span></span>

<span data-ttu-id="c25af-p105">Mithilfe der ALTER TABLE-Anweisung können Sie eine bestehende Tabelle auf verschiedene Arten ändern. Folgende Möglichkeiten stehen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="c25af-p105">Using the ALTER TABLE statement you can alter an existing table in several ways. You can:</span></span>

  - <span data-ttu-id="c25af-p106">Verwenden Sie ADD COLUMN, um der Tabelle ein neues Feld hinzuzufügen. Sie geben den Feldnamen, den Datentyp und (für Text- und binäre Felder) optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Employees-Tabelle (Personal) ein 25 Zeichen langes Textfeld namens Notes (Bemerkungen) hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="c25af-p106">Use ADD COLUMN to add a new field to the table. You specify the field name, data type, and (for Text and Binary fields) an optional size. For example, the following statement adds a 25-character Text field called Notes to the Employees table:</span></span>
    
    ```sql
    ALTER TABLE Employees ADD COLUMN Notes TEXT(25)
    ```
    
    <span data-ttu-id="c25af-p107">Sie können auch einen Index für das Feld definieren. Weitere Informationen zu Einzelfeldindizes finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c25af-p107">You can also define an index on that field. For more information on single-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>
    
    <span data-ttu-id="c25af-137">Wenn Sie für ein Feld NICHT NULL angeben, sind neue Datensätze erforderlich, damit gültige Daten für das Feld vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="c25af-137">If you specify NOT NULL for a field then new records are required to have valid data in that field.</span></span>

  - <span data-ttu-id="c25af-p108">Verwenden Sie ALTER COLUMN, um den Datentyp eines bestehenden Felds zu ändern. Sie geben den Feldnamen, den Datentyp und für Text- und binäre Felder optional eine Größe an. In der Anweisung im folgenden Beispiel wird der Datentyp des ZipCode-Felds (PLZ) in der Employees-Tabelle (ursprünglich Integer) in ein 10 Zeichen langes Textfeld geändert:</span><span class="sxs-lookup"><span data-stu-id="c25af-p108">Use ALTER COLUMN to change the data type of an existing field. You specify the field name, the new data type, and an optional size for Text and Binary fields. For example, the following statement changes the data type of a field in the Employees table called ZipCode (originally defined as Integer) to a 10-character Text field:</span></span>
    
    ```sql
    ALTER TABLE Employees ALTER COLUMN ZipCode TEXT(10)
    ```

  - <span data-ttu-id="c25af-p109">Verwenden Sie ADD CONSTRAINT, um einen aus mehreren Feldern bestehenden Index hinzuzufügen. Weitere Informationen zu Indizes mit mehreren Feldern finden Sie unter [CONSTRAINT-Klausel](constraint-clause-microsoft-access-sql.md).</span><span class="sxs-lookup"><span data-stu-id="c25af-p109">Use ADD CONSTRAINT to add a multiple-field index. For more information on multiple-field indexes see [CONSTRAINT Clause](constraint-clause-microsoft-access-sql.md).</span></span>

  - <span data-ttu-id="c25af-p110">Verwenden Sie DROP COLUMN, um ein Feld zu löschen. Sie geben lediglich den Namen des Felds an.</span><span class="sxs-lookup"><span data-stu-id="c25af-p110">Use DROP COLUMN to delete a field. You specify only the name of the field.</span></span>

  - <span data-ttu-id="c25af-p111">Verwenden Sie DROP CONSTRAINT, um einen aus mehreren Feldern bestehenden Index zu löschen. Sie geben lediglich den Namen des Indexes, gefolgt vom reservierten Wort CONSTRAINT, an.</span><span class="sxs-lookup"><span data-stu-id="c25af-p111">Use DROP CONSTRAINT to delete a multiple-field index. You specify only the index name following the CONSTRAINT reserved word.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="c25af-147">Sie können immer nur ein Feld bzw. einen Index gleichzeitig hinzufügen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="c25af-147">You cannot add or delete more than one field or index at a time.</span></span></P>
> <LI>
> <P><span data-ttu-id="c25af-148">Mithilfe der <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A>-Anweisung können Sie einer Tabelle einen Index mit einem oder mehreren Feldern hinzufügen, und Sie können ALTER TABLE oder die <A href="drop-statement-microsoft-access-sql.md">DROP</A>-Anweisung zum Löschen eines mit ALTER TABLE oder CREATE INDEX erstellten Indexes verwenden.</span><span class="sxs-lookup"><span data-stu-id="c25af-148">You can use the <A href="create-index-statement-microsoft-access-sql.md">CREATE INDEX</A> statement to add a single- or multiple-field index to a table, and you can use ALTER TABLE or the <A href="drop-statement-microsoft-access-sql.md">DROP</A> statement to delete an index created with ALTER TABLE or CREATE INDEX.</span></span></P>
> <LI>
> <P><span data-ttu-id="c25af-p112">Sie können NOT NULL für ein einzelnes Feld oder innerhalb einer benannten CONSTRAINT-Klausel verwenden, die entweder für ein einzelnes oder mehrere Felder mit dem Namen CONSTRAINT gilt. Sie können die NOT NULL-Beschränkung nur einmal auf ein Feld anwenden. Andernfalls tritt ein Laufzeitfehler auf. 
</span><span class="sxs-lookup"><span data-stu-id="c25af-p112">You can use NOT NULL on a single field or within a named CONSTRAINT clause that applies to either a single field or to a multiple-field named CONSTRAINT. However, you can apply the NOT NULL restriction only once to a field. Attempting to apply this restriction more than once restuls in a run-time error.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="c25af-152">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c25af-152">Example</span></span>

<span data-ttu-id="c25af-153">In diesem Beispiel wird der Employees-Tabelle (Personal) ein Salary-Feld (Gehalt) mit dem **Money** -Datentyp hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c25af-153">This example adds a Salary field with the data type **Money** to the Employees table.</span></span>

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

<span data-ttu-id="c25af-154">In diesem Beispiel wird der Datentyp des Salary-Felds von **Money** in **Char** geändert.</span><span class="sxs-lookup"><span data-stu-id="c25af-154">This example changes the Salary field from the data type **Money** to the data type **Char**.</span></span>

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

<span data-ttu-id="c25af-155">In diesem Beispiel wird das Salary-Feld aus der Employees-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="c25af-155">This example removes the Salary field from the Employees table.</span></span>

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

<span data-ttu-id="c25af-p113">Im folgenden Beispiel wird der Orders-Tabelle (Bestellungen) ein Fremdschlüssel hinzugefügt. Der Fremdschlüssel basiert und verweist auf das EmployeeID-Feld (Personal-Nr) in der Employees-Tabelle. In diesem Beispiel muss das EmployeeID-Feld nicht nach der Employees-Tabelle in der REFERENCES-Klausel aufgelistet werden, da es sich bei EmployeeID um den Primärschlüssel der Employees-Tabelle handelt.</span><span class="sxs-lookup"><span data-stu-id="c25af-p113">This example adds a foreign key to the Orders table. The foreign key is based on the EmployeeID field and refers to the EmployeeID field of the Employees table. In this example, you do not have to list the EmployeeID field after the Employees table in the REFERENCES clause because EmployeeID is the primary key of the Employees table.</span></span>

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

<span data-ttu-id="c25af-159">In diesem Beispiel wird der Fremdschlüssel aus der Orders-Tabelle entfernt.</span><span class="sxs-lookup"><span data-stu-id="c25af-159">This example removes the foreign key from the Orders table.</span></span>

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
