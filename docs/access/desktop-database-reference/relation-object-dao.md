---
title: Relation-Objekt (DAO)
TOCTitle: Relation Object
ms:assetid: 46d6dfaf-a97d-3abd-0b4b-396a41eb3be7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193195(v=office.15)
ms:contentKeyID: 48544578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e7621bb40aa7515ab24c914fc5b3460cae91ef04
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611658"
---
# <a name="relation-object-dao"></a>Relation-Objekt (DAO)


**Gilt für**: Access 2013, Office 2013

Ein **Relation**-Objekt stellt eine Beziehung zwischen Feldern in Tabellen oder Abfragen dar (gilt nur für Microsoft Access-Datenbanken).

## <a name="remarks"></a>HinwBemerkungeneise

Sie können mit dem **Relation**-Objekt neue Beziehungen erstellen und vorhandene Beziehungen in der Datenbank überprüfen.

Beim Verwenden des **Relation**-Objekts und seiner Eigenschaften können Sie die folgenden Aktionen ausführen:

  - Geben Sie eine erzwungene Beziehung zwischen Feldern in Basistabellen an (jedoch keine Beziehung, die eine Abfrage oder eine verknüpfte Tabelle einschließt).

  - Erstellen Sie nicht erzwungene Beziehungen zwischen beliebigen Tabellen- oder Abfragetypen (systemeigen oder verknüpft) her.

  - Verweisen Sie mit der **Name**-Eigenschaft auf die Beziehung zwischen den Feldern der referenzierten Primärtabelle und der referenzierenden Fremdtabelle.

  - Bestimmen Sie mit der **Attributes**-Eigenschaft, ob es sich bei der Beziehung zwischen Feldern in der Tabelle um eine 1:1- oder eine 1:n-Beziehung handelt, und wie die referentielle Integrität erzwungen wird.

  - Bestimmen Sie mit der **Attributes**-Eigenschaft, ob das Microsoft Access-Datenbankmodul Aktualisierungs- und Löschweitergaben zu Primär- und Fremdtabellen ausführen kann.

  - Bestimmen Sie mit der **Attributes**-Eigenschaft, ob es sich bei der Beziehung zwischen Feldern in der Tabelle um eine Linksverknüpfung oder Rechtsverknüpfung handelt.

  - Verwenden Sie die **Name**-Eigenschaft aller **Field**-Objekte in der **Fields**-Auflistung eines **Relation**-Objekts, um die Namen der Felder im Primärschlüssel der referenzierten Tabelle festzulegen oder zurückzugeben, oder verwenden Sie die Einstellung der **ForeignName**-Eigenschaft des **Field**-Objekts, um die Namen der Felder im Fremdschlüssel der referenzierenden Tabelle festzulegen oder zurückzugeben.

Falls Sie Änderungen vornehmen, die gegen die für die Datenbank festgelegten Beziehungen verstoßen, tritt ein abfangbarer Fehler auf. Wenn Sie eine Aktualisierungsweitergabe oder Löschweitergabe anfordern, ändert das Microsoft Access-Datenbankmodul auch die Primärschlüssel- oder Fremdschlüsseltabellen, um die festgelegten Beziehungen zu erzwingen.

For example, the Northwind database contains a relationship between an Orders table and a Customers table. The CustomerID field of the Customers table is the primary key, and the CustomerID field of the Orders table is the foreign key. For the Microsoft Access database engine to accept a new record in the Orders table, it searches the Customers table for a match on the CustomerID field of the Orders table. If the Microsoft Access database engine doesn't find a match, it doesn't accept the new record, and a trappable error occurs.

Wenn Sie die referentielle Integrität erzwingen, muss bereits ein eindeutiger Index für das Schlüsselfeld der referenzierten Tabelle vorhanden sein. Das Microsoft Access-Datenbankmodul erstellt automatisch einen Index, wobei die **Foreign**-Eigenschaft so festgelegt ist, dass sie in der referenzierenden Tabelle als Fremdschlüssel fungiert.

Verwenden Sie die **CreateRelation**-Methode, um ein neues **Relation**-Objekt zu erstellen. Wenn Sie auf ein **Relation**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:

**Relations**(0)

**Beziehungen**("Name")

 \! Beziehungen \[ Namen\]

## <a name="example"></a>Beispiel

This example shows how an existing **Relation** object can control data entry. The procedure attempts to add a record with a deliberately incorrect CategoryID; this triggers the error-handling routine.

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

This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. Außerdem wird veranschaulicht, wie durch das Erstellen einer neuen **Beziehung** auch alle erforderlichen **Indizes** in der Fremdtabelle erstellt werden (die Tabelle "DepartmentsEmployees Index" in der Tabelle "Employees").

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
