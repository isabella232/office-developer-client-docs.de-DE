---
title: Relation-Objekt (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cfabb36e539aaff1f6e12d431d2cfcfe79ff5d04
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928088"
---
# <a name="relation-object-dao"></a><span data-ttu-id="b344c-102">Relation-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="b344c-102">Relation object (DAO)</span></span>


<span data-ttu-id="b344c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b344c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b344c-104">Ein **Relation**-Objekt stellt eine Beziehung zwischen Feldern in Tabellen oder Abfragen dar (gilt nur für Microsoft Access-Datenbanken).</span><span class="sxs-lookup"><span data-stu-id="b344c-104">A **Relation** object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="remarks"></a><span data-ttu-id="b344c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b344c-105">Remarks</span></span>

<span data-ttu-id="b344c-106">Sie können mit dem **Relation**-Objekt neue Beziehungen erstellen und vorhandene Beziehungen in der Datenbank überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b344c-106">You can use the **Relation** object to create new relationships and examine existing relationships in your database.</span></span>

<span data-ttu-id="b344c-107">Beim Verwenden des **Relation**-Objekts und seiner Eigenschaften können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="b344c-107">Using a **Relation** object and its properties, you can:</span></span>

  - <span data-ttu-id="b344c-108">Geben Sie eine erzwungene Beziehung zwischen Feldern in Basistabellen an (jedoch keine Beziehung, die eine Abfrage oder eine verknüpfte Tabelle einschließt).</span><span class="sxs-lookup"><span data-stu-id="b344c-108">Specify an enforced relationship between fields in base tables (but not a relationship that involves a query or a linked table).</span></span>

  - <span data-ttu-id="b344c-109">Erstellen Sie nicht erzwungene Beziehungen zwischen beliebigen Tabellen- oder Abfragetypen (systemeigen oder verknüpft) her.</span><span class="sxs-lookup"><span data-stu-id="b344c-109">Establish unenforced relationships between any type of table or query— native or linked.</span></span>

  - <span data-ttu-id="b344c-110">Verweisen Sie mit der **Name**-Eigenschaft auf die Beziehung zwischen den Feldern der referenzierten Primärtabelle und der referenzierenden Fremdtabelle.</span><span class="sxs-lookup"><span data-stu-id="b344c-110">Use the **Name** property to refer to the relationship between the fields in the referenced primary table and the referencing foreign table.</span></span>

  - <span data-ttu-id="b344c-111">Bestimmen Sie mit der **Attributes**-Eigenschaft, ob es sich bei der Beziehung zwischen Feldern in der Tabelle um eine 1:1- oder eine 1:n-Beziehung handelt, und wie die referentielle Integrität erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="b344c-111">Use the **Attributes** property to determine whether the relationship between fields in the table is one-to-one or one-to-many and how to enforce referential integrity.</span></span>

  - <span data-ttu-id="b344c-112">Bestimmen Sie mit der **Attributes**-Eigenschaft, ob das Microsoft Access-Datenbankmodul Aktualisierungs- und Löschweitergaben zu Primär- und Fremdtabellen ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="b344c-112">Use the **Attributes** property to determine whether the Microsoft Access database engine can perform cascading update and cascading delete operations on primary and foreign tables.</span></span>

  - <span data-ttu-id="b344c-113">Bestimmen Sie mit der **Attributes**-Eigenschaft, ob es sich bei der Beziehung zwischen Feldern in der Tabelle um eine Linksverknüpfung oder Rechtsverknüpfung handelt.</span><span class="sxs-lookup"><span data-stu-id="b344c-113">Use the **Attributes** property to determine whether the relationship between fields in the table is left join or right join.</span></span>

  - <span data-ttu-id="b344c-114">Verwenden Sie die **Name**-Eigenschaft aller **Field**-Objekte in der **Fields**-Auflistung eines **Relation**-Objekts, um die Namen der Felder im Primärschlüssel der referenzierten Tabelle festzulegen oder zurückzugeben, oder verwenden Sie die Einstellung der **ForeignName**-Eigenschaft des **Field**-Objekts, um die Namen der Felder im Fremdschlüssel der referenzierenden Tabelle festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b344c-114">Use the **Name** property of all **Field** objects in the **Fields** collection of a **Relation** object to set or return the names of the fields in the primary key of the referenced table, or the **ForeignName** property settings of the **Field** objects to set or return the names of the fields in the foreign key of the referencing table.</span></span>

<span data-ttu-id="b344c-p101">Falls Sie Änderungen vornehmen, die gegen die für die Datenbank festgelegten Beziehungen verstoßen, tritt ein abfangbarer Fehler auf. Wenn Sie eine Aktualisierungsweitergabe oder Löschweitergabe anfordern, ändert das Microsoft Access-Datenbankmodul auch die Primärschlüssel- oder Fremdschlüsseltabellen, um die festgelegten Beziehungen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="b344c-p101">If you make changes that violate the relationships established for the database, a trappable error occurs. If you request cascading update or cascading delete operations, the Microsoft Access database engine also modifies the primary key or foreign key tables to enforce the relationships you establish.</span></span>

<span data-ttu-id="b344c-p102">Die Nordwind-Datenbank enthält z. B. eine Beziehung zwischen einer Orders-Tabelle (Bestellungen) und einer Customers-Tabelle (Kunden). Das CustomerID-Feld (Kunden-Nr) der Customers-Tabelle ist der Primärschlüssel, und das CustomerID-Feld der Orders-Tabelle ist der Fremdschlüssel. Damit das Microsoft Access-Datenbankmodul den neuen Datensatz in der Orders-Tabelle akzeptieren kann, durchsucht es die Customers-Tabelle nach einem übereinstimmenden CustomerID-Feld der Orders-Tabelle. Findet das Microsoft Access-Datenbankmodul keine Übereinstimmung, wird der neue Datensatz nicht akzeptiert, und ein abfangbarer Fehler tritt auf.</span><span class="sxs-lookup"><span data-stu-id="b344c-p102">For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.</span></span>

<span data-ttu-id="b344c-p103">Wenn Sie die referentielle Integrität erzwingen, muss bereits ein eindeutiger Index für das Schlüsselfeld der referenzierten Tabelle vorhanden sein. Das Microsoft Access-Datenbankmodul erstellt automatisch einen Index, wobei die **Foreign**-Eigenschaft so festgelegt ist, dass sie in der referenzierenden Tabelle als Fremdschlüssel fungiert.</span><span class="sxs-lookup"><span data-stu-id="b344c-p103">When you enforce referential integrity, a unique index must already exist for the key field of the referenced table. The Microsoft Access database engine automatically creates an index with the **Foreign** property set to act as the foreign key in the referencing table.</span></span>

<span data-ttu-id="b344c-p104">Verwenden Sie die **CreateRelation**-Methode, um ein neues **Relation**-Objekt zu erstellen. Wenn Sie auf ein **Relation**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="b344c-p104">To create a new **Relation** object, use the **CreateRelation** method. To refer to a **Relation** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="b344c-125">**Relations**(0)</span><span class="sxs-lookup"><span data-stu-id="b344c-125">**Relations**(0)</span></span>

<span data-ttu-id="b344c-126">**Relations** ("Name")</span><span class="sxs-lookup"><span data-stu-id="b344c-126">**Relations**("name")</span></span>

<span data-ttu-id="b344c-127">**Relations**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="b344c-127">**Relations**\!\[name\]</span></span>

## <a name="example"></a><span data-ttu-id="b344c-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b344c-128">Example</span></span>

<span data-ttu-id="b344c-p105">Diese Beispiel zeigt, wie ein vorhandenes **Relation**-Objekt die Dateneingabe steuern kann. Die Prozedur versucht mit einer bewusst falschen Kategorienummer (CategoryID) einen Datensatz hinzuzufügen. Dadurch wird die Fehlerbehandlungsroutine ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b344c-p105">This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.</span></span>

```vb 
    Sub RelationX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset 
     Dim prpLoop As Property 
     Dim fldLoop As Field 
     Dim errLoop As Error 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     ' Print a report showing all the different parts of 
     ' the relation and where each part is stored. 
     With dbsNorthwind.Relations!CategoriesProducts 
     Debug.Print "Properties of " & .Name & " Relation" 
     Debug.Print " Table = " & .Table 
     Debug.Print " ForeignTable = " & .ForeignTable 
     Debug.Print "Fields of " & .Name & " Relation" 
     With .Fields!CategoryID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     End With 
     
     ' Attempt to add a record that violates the relation. 
     With rstProducts 
     .AddNew 
     !ProductName = "Trygve's Lutefisk" 
     !CategoryID = 10 
     On Error GoTo Err_Relation 
     .Update 
     On Error GoTo 0 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
     Exit Sub 
     
    Err_Relation: 
     
     ' Notify user of any errors that result from 
     ' the invalid data. 
     If DBEngine.Errors.Count > 0 Then 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Sub 
```

<br/>

<span data-ttu-id="b344c-p106">In diesem Beispiel wird die CreateRelation-Methode zum Erstellen eines Relation-Objekts zwischen dem TableDef-Objekt Employees (Personal) und einem neuen TableDef-Objekt namens Departments (Abteilungen) erstellt. Außerdem veranschaulicht das Beispiel, wie das Erstellen eines neuen Relation-Objekts das Erstellen erforderlicher Indexes-Objekte in der Fremdtabelle nach sich zieht (DepartmentsEmployees-Index in der Employees-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="b344c-p106">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

```vb
    Sub CreateRelationX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim tdfNew As TableDef 
     Dim idxNew As Index 
     Dim relNew As Relation 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Add new field to Employees table. 
     Set tdfEmployees = .TableDefs!Employees 
     tdfEmployees.Fields.Append _ 
     tdfEmployees.CreateField("DeptID", dbInteger, 2) 
     
     ' Create new Departments table. 
     Set tdfNew = .CreateTableDef("Departments") 
     
     With tdfNew 
     ' Create and append Field objects to Fields 
     ' collection of the new TableDef object. 
     .Fields.Append .CreateField("DeptID", dbInteger, 2) 
     .Fields.Append .CreateField("DeptName", dbText, 20) 
     
     ' Create Index object for Departments table. 
     Set idxNew = .CreateIndex("DeptIDIndex") 
     ' Create and append Field object to Fields 
     ' collection of the new Index object. 
     idxNew.Fields.Append idxNew.CreateField("DeptID") 
     ' The index in the primary table must be Unique in 
     ' order to be part of a Relation. 
     idxNew.Unique = True 
     .Indexes.Append idxNew 
     End With 
     
     .TableDefs.Append tdfNew 
     
     ' Create EmployeesDepartments Relation object, using 
     ' the names of the two tables in the relation. 
     Set relNew = .CreateRelation("EmployeesDepartments", _ 
     tdfNew.Name, tdfEmployees.Name, _ 
     dbRelationUpdateCascade) 
     
     ' Create Field object for the Fields collection of the 
     ' new Relation object. Set the Name and ForeignName 
     ' properties based on the fields to be used for the 
     ' relation. 
     relNew.Fields.Append relNew.CreateField("DeptID") 
     relNew.Fields!DeptID.ForeignName = "DeptID" 
     .Relations.Append relNew 
     
     ' Print report. 
     Debug.Print "Properties of " & relNew.Name & _ 
     " Relation" 
     Debug.Print " Table = " & relNew.Table 
     Debug.Print " ForeignTable = " & _ 
     relNew.ForeignTable 
     Debug.Print "Fields of " & relNew.Name & " Relation" 
     
     With relNew.Fields!DeptID 
     Debug.Print " " & .Name 
     Debug.Print " Name = " & .Name 
     Debug.Print " ForeignName = " & .ForeignName 
     End With 
     
     Debug.Print "Indexes in " & tdfEmployees.Name & _ 
     " TableDef" 
     For Each idxLoop In tdfEmployees.Indexes 
     Debug.Print " " & idxLoop.Name & _ 
     ", Foreign = " & idxLoop.Foreign 
     Next idxLoop 
     
     ' Delete new objects because this is a demonstration. 
     .Relations.Delete relNew.Name 
     .TableDefs.Delete tdfNew.Name 
     tdfEmployees.Fields.Delete "DeptID" 
     .Close 
     End With 
     
    End Sub
```
