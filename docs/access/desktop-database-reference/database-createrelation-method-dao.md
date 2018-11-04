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
ms.openlocfilehash: 2a1ad7798fc6236f95d31c18cd864fe64e7a3fd8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949928"
---
# <a name="databasecreaterelation-method-dao"></a><span data-ttu-id="f2265-102">Database.CreateRelation-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="f2265-102">Database.CreateRelation method (DAO)</span></span>

<span data-ttu-id="f2265-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2265-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2265-p101">Erstellt ein neues **[Relation](relation-object-dao.md)** -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="f2265-p101">Creates a new **[Relation](relation-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="f2265-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2265-106">Syntax</span></span>

<span data-ttu-id="f2265-107">*Ausdruck* . CreateRelation (***Name***, ***Tabelle***, ***ForeignTable***, ***Attribute***)</span><span class="sxs-lookup"><span data-stu-id="f2265-107">*expression* .CreateRelation(***Name***, ***Table***, ***ForeignTable***, ***Attributes***)</span></span>

<span data-ttu-id="f2265-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2265-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2265-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2265-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f2265-110">Name</span><span class="sxs-lookup"><span data-stu-id="f2265-110">Name</span></span></p></th>
<th><p><span data-ttu-id="f2265-111">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="f2265-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f2265-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f2265-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f2265-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2265-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f2265-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="f2265-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="f2265-115">Optional</span><span class="sxs-lookup"><span data-stu-id="f2265-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="f2265-116"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f2265-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f2265-p102">Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der das neue <strong>Relation</strong>-Objekt eindeutig benennt. Weitere Informationen zu gültigen <strong>Relation</strong>-Namen finden Sie in dem Thema zur <strong><a href="connection-name-property-dao.md">Name</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2265-p102">A <strong>Variant</strong> (<strong>String</strong> subtype) that uniquely names the new <strong>Relation</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Relation</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2265-119"><em>Table</em></span><span class="sxs-lookup"><span data-stu-id="f2265-119"><em>Table</em></span></span></p></td>
<td><p><span data-ttu-id="f2265-120">Optional</span><span class="sxs-lookup"><span data-stu-id="f2265-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="f2265-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f2265-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f2265-p103">Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die primäre Tabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="f2265-p103">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the primary table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f2265-124"><em>ForeignTable</em></span><span class="sxs-lookup"><span data-stu-id="f2265-124"><em>ForeignTable</em></span></span></p></td>
<td><p><span data-ttu-id="f2265-125">Optional</span><span class="sxs-lookup"><span data-stu-id="f2265-125">Optional</span></span></p></td>
<td><p><span data-ttu-id="f2265-126"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f2265-126"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f2265-p104">Ein <strong>Variant</strong>-Wert (Untertyp <strong>String</strong>), der die Fremdtabelle in der Beziehung eindeutig benennt. Falls die Tabelle vor dem Anfügen des <strong>Relation</strong>-Objekts noch nicht vorhanden ist, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="f2265-p104">A <strong>Variant</strong> (<strong>String</strong> subtype) that names the foreign table in the relation. If the table doesn't exist before you append the <strong>Relation</strong> object, a run-time error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f2265-129"><em>Attributes</em></span><span class="sxs-lookup"><span data-stu-id="f2265-129"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="f2265-130">Optional</span><span class="sxs-lookup"><span data-stu-id="f2265-130">Optional</span></span></p></td>
<td><p><span data-ttu-id="f2265-131"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f2265-131"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f2265-p105">Eine Konstante bzw. Kombination aus Konstanten, die Informationen über den Beziehungstyp enthält. Weitere Informationen finden Sie in dem Thema zur <strong><a href="field-attributes-property-dao.md">Attributes</a></strong>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f2265-p105">A constant or combination of constants that contains information about the relationship type. See the <strong><a href="field-attributes-property-dao.md">Attributes</a></strong> property for details.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="f2265-134">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2265-134">Return value</span></span>

<span data-ttu-id="f2265-135">Relation</span><span class="sxs-lookup"><span data-stu-id="f2265-135">Relation</span></span>

## <a name="remarks"></a><span data-ttu-id="f2265-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2265-136">Remarks</span></span>

<span data-ttu-id="f2265-p106">Das **Relation**-Objekt liefert dem Microsoft Access-Datenbankmodul Informationen über die Beziehung zwischen Feldern in zwei **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekten. Mithilfe der **Attributes**-Eigenschaft können Sie referentielle Integrität implementieren.</span><span class="sxs-lookup"><span data-stu-id="f2265-p106">The **Relation** object provides information to the Microsoft Access database engine about the relationship between fields in two **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** objects. You can implement referential integrity by using the **Attributes** property.</span></span>

<span data-ttu-id="f2265-p107">Wenn Sie die **CreateRelation**-Methode verwenden und einen oder mehrere optionale Teile weglassen, können Sie die entsprechende Eigenschaft mithilfe einer geeigneten Zuweisungsanweisung festlegen oder zurücksetzen, bevor Sie das neue Objekt an eine Auflistung anfügen. Nachdem Sie das Objekt angefügt haben, können Sie dessen Eigenschafteneinstellungen zum Teil ändern. Weitere Informationen hierzu finden Sie in den Themen zu einzelnen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f2265-p107">If you omit one or more of the optional parts when you use the **CreateRelation** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can't alter any of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="f2265-142">Bevor Sie die **[Append](fields-append-method-dao.md)** -Methode für ein **Relation**-Objekt verwenden können, müssen Sie die entsprechenden **[Field](field-object-dao.md)** -Objekte anfügen, um die Tabellen für Primär- und Fremdschlüsselbeziehungen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f2265-142">Before you can use the **[Append](fields-append-method-dao.md)** method on a **Relation** object, you must append the appropriate **[Field](field-object-dao.md)** objects to define the primary and foreign key relationship tables.</span></span>

<span data-ttu-id="f2265-143">Wenn Name auf ein Objekt bezieht, das bereits ein Element der Auflistung ist oder wenn die Namen der **Felder** -Objekt in der untergeordneten **Fields** -Auflistung bereitgestellt, ungültig sind, tritt ein Laufzeitfehler auf, wenn Sie die **Append** -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2265-143">If name refers to an object that is already a member of the collection or if the **Field** object names provided in the subordinate **Fields** collection are invalid, a run-time error occurs when you use the **Append** method.</span></span>

<span data-ttu-id="f2265-144">Zwischen einer replizierten und einer lokalen Tabelle können Sie keine Beziehung herstellen oder beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f2265-144">You can't establish or maintain a relationship between a replicated table and a local table.</span></span>

<span data-ttu-id="f2265-145">Wenn Sie ein **Relation**-Objekt aus der **[Relations](relations-collection-dao.md)** -Auflistung entfernen möchten, verwenden Sie die **[Delete](fields-delete-method-dao.md)** -Methode für die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="f2265-145">To remove a **Relation** object from the **[Relations](relations-collection-dao.md)** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="f2265-146">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2265-146">Example</span></span>

<span data-ttu-id="f2265-p108">In diesem Beispiel wird die CreateRelation-Methode zum Erstellen eines Relation-Objekts zwischen dem TableDef-Objekt Employees (Personal) und einem neuen TableDef-Objekt namens Departments (Abteilungen) erstellt. Außerdem veranschaulicht das Beispiel, wie das Erstellen eines neuen Relation-Objekts das Erstellen erforderlicher Indexes-Objekte in der Fremdtabelle nach sich zieht (DepartmentsEmployees-Index in der Employees-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="f2265-p108">This example uses the **CreateRelation** method to create a **Relation** between the Employees **TableDef** and a new **TableDef** called Departments. This example also demonstrates how creating a new **Relation** will also create any necessary **Indexes** in the foreign table (the DepartmentsEmployees Index in the Employees table).</span></span>

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
