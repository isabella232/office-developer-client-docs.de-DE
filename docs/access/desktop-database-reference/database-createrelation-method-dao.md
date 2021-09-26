---
title: Database.CreateRelation-Methode (DAO)
TOCTitle: CreateRelation Method
ms:assetid: e240c7e3-c293-5e19-afcc-34d9a5549c64
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835692(v=office.15)
ms:contentKeyID: 48548279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052969
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 61c666aaddbdb3da94be04048cc522605cab1a24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612274"
---
# <a name="databasecreaterelation-method-dao"></a>Database.CreateRelation-Methode (DAO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues **[Relation](relation-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateRelation(***Name** _, _*_Table_*_, _*_ForeignTable_*_, _*_Attributes_**)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

## <a name="parameters"></a>Parameter

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Erforderlich/optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der das neue <strong>Relation</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Relation</strong>-Namen finden Sie in dem Thema zur <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p><em>Table</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die primäre Tabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</p></td>
</tr>
<tr class="odd">
<td><p><em>ForeignTable</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die Fremdtabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</p></td>
</tr>
<tr class="even">
<td><p><em>Attributes</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante oder Eine Kombination aus Konstanten, die Informationen zum Beziehungstyp enthält. Weitere <strong><a href="field-attributes-property-dao.md"></a></strong> Informationen finden Sie in der Attributes-Eigenschaft.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Rückgabewert

Beziehung

## <a name="remarks"></a>HinwBemerkungeneise

Das **Relation**-Objekt liefert dem Microsoft Access-Datenbankmodul Informationen über die Beziehung zwischen Feldern in zwei **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekten. Mithilfe der **Attributes**-Eigenschaft können Sie referentielle Integrität implementieren.

Wenn Sie die **CreateRelation**-Methode verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zu einzelnen Eigenschaften.

Bevor Sie die **[Append](fields-append-method-dao.md)** -Methode für ein **Relation**-Objekt verwenden können, müssen Sie die entsprechenden **[Field](field-object-dao.md)** -Objekte anfügen, um die Tabellen für Primär- und Fremdschlüsselbeziehungen zu definieren.

Wenn sich name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist, oder wenn die in der untergeordneten **Fields-Auflistung** angegebenen **Field-Objektnamen** ungültig sind, tritt bei Verwendung der **Append-Methode** ein Laufzeitfehler auf.

Zwischen einer replizierten und einer lokalen Tabelle können Sie keine Beziehung herstellen oder beibehalten.

Wenn Sie ein **Relation**-Objekt aus der **[Relations](relations-collection-dao.md)** -Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung.

## <a name="example"></a>Beispiel

This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).

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
