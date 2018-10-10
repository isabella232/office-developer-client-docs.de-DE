---
title: Database.CreateRelation Method (DAO)
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
ms.openlocfilehash: c7b3c69090a9879f622153f67e2aa264d18a8497
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475879"
---
# <a name="databasecreaterelation-method-dao"></a>Database.CreateRelation Method (DAO)

**Betrifft**: Access 2013 | Office 2013

Erstellt ein neues **[Relation](relation-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).

## <a name="syntax"></a>Syntax

*Ausdruck* . CreateRelation (***Name***, ***Tabelle***, ***ForeignTable***, ***Attribute***)

*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.

### <a name="parameters"></a>Parameter

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
<th><p>Erforderlich/Optional</p></th>
<th><p>Datentyp</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der das neue <strong>Relation</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Relation</strong>-Namen finden Sie in dem Thema zur <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft.</p></td>
</tr>
<tr class="even">
<td><p>Tabelle</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die primäre Tabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</p></td>
</tr>
<tr class="odd">
<td><p>ForeignTable</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die Fremdtabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</p></td>
</tr>
<tr class="even">
<td><p>Attribute</p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Eine Konstante bzw. Kombination aus Konstanten, die Informationen über den Beziehungstyp enthält. Weitere Informationen finden Sie in dem Thema zur <strong><a href="field-attributes-property-dao.md">Attributes</a></strong>-Eigenschaft.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Rückgabewert

Relation

## <a name="remarks"></a>Bemerkungen

Das **Relation**-Objekt liefert dem Microsoft Access-Datenbankmodul Informationen über die Beziehung zwischen Feldern in zwei **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekten. Mithilfe der **Attributes**-Eigenschaft können Sie referentielle Integrität implementieren.

Wenn Sie die **CreateRelation**-Methode verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zu einzelnen Eigenschaften.

Bevor Sie die **[Append](fields-append-method-dao.md)** -Methode für ein **Relation**-Objekt verwenden können, müssen Sie die entsprechenden **[Field](field-object-dao.md)** -Objekte anfügen, um die Tabellen für Primär- und Fremdschlüsselbeziehungen zu definieren.

Wenn Name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist oder wenn die Namen der **Felder** -Objekt in der untergeordneten **Fields** -Auflistung bereitgestellt, ungültig sind, tritt ein Laufzeitfehler auf, wenn Sie die **Append** -Methode verwenden.

Zwischen einer replizierten und einer lokalen Tabelle können Sie keine Beziehung herstellen oder beibehalten.

Wenn Sie ein **Relation**-Objekt aus der **[Relations](relations-collection-dao.md)** -Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung.

## <a name="example"></a>Beispiel

In diesem Beispiel wird die CreateRelation-Methode zum Erstellen eines Relation-Objekts zwischen dem TableDef-Objekt Employees (Personal) und einem neuen TableDef-Objekt namens Departments (Abteilungen) erstellt. Außerdem veranschaulicht das Beispiel, wie das Erstellen eines neuen Relation-Objekts das Erstellen erforderlicher Indexes-Objekte in der Fremdtabelle nach sich zieht (DepartmentsEmployees-Index in der Employees-Tabelle).

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
