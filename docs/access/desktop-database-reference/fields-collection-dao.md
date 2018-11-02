---
title: Fields-Auflistung (DAO)
TOCTitle: Fields Collection
ms:assetid: 4be3ba07-20c1-d958-c1b8-7dd8b4731f60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193530(v=office.15)
ms:contentKeyID: 48544702
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 79515c413918bca1b83d18abec41c78f3fd52447
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921238"
---
# <a name="fields-collection-dao"></a><span data-ttu-id="9815a-102">Fields-Auflistung (DAO)</span><span class="sxs-lookup"><span data-stu-id="9815a-102">Fields collection (DAO)</span></span>


<span data-ttu-id="9815a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9815a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9815a-104">Eine **Fields** -Auflistung enthält alle gespeicherten **Field** -Objekte eines **Index** -, **QueryDef** -, **Recordset** -, **Relation** - oder **TableDef** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="9815a-104">A **Fields** collection contains all stored **Field** objects of an **Index**, **QueryDef**, **Recordset**, **Relation**, or **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9815a-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9815a-105">Remarks</span></span>

<span data-ttu-id="9815a-p101">Die **Fields** -Auflistung der Objekte **Index**, **QueryDef**, **Relation**, and **TableDef** enthält die Spezifikationen für die Felder, die diese Objekte darstellen. Die **Fields** -Auflistung eines **Recordset** -Objekts stellt die **Field** -Objekte in einer Zeile mit Daten oder einem Datensatz dar. Verwenden Sie die **Field** -Objekte in einem **Recordset** -Objekt, um Werte für die Felder im aktuellen Datensatz des **Recordset** -Objekts zu lesen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9815a-p101">The **Fields** collections of the **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and to set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="9815a-109">Wenn Sie auf ein **Field** -Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name** -Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="9815a-109">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="9815a-110">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="9815a-110">**Fields**(0)</span></span>

<span data-ttu-id="9815a-111">**Felder** ("Name")</span><span class="sxs-lookup"><span data-stu-id="9815a-111">**Fields**("name")</span></span>

<span data-ttu-id="9815a-112">**Felder**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="9815a-112">**Fields**\!\[name\]</span></span>

<span data-ttu-id="9815a-p102">Mit denselben Syntaxformen können Sie auch auf die **Value**-Eigenschaft eines von Ihnen erstellten **Field**-Objekts verweisen, das Sie einer **Fields**-Auflistung anfügen. Der Kontext des Feldverweises bestimmt, ob sich der Verweis auf das **Field**-Objekt oder die **Value**-Eigenschaft des **Field**-Objekts bezieht.</span><span class="sxs-lookup"><span data-stu-id="9815a-p102">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="9815a-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9815a-115">Example</span></span>

<span data-ttu-id="9815a-p103">Dieses Beispiel zeigt, welche Eigenschaften für ein **Field** -Objekt gültig sind, abhängig davon, wo sich das **Field** -Objekt befindet (z. B. **Fields** -Auflistung eines **TableDef** -Objekts, **Fields** -Auflistung eines **QueryDef** -Objekts usw.). Zum Ausführen dieser Prozedur ist die FieldOutput-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9815a-p103">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

```vb
    Sub FieldX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim fldTableDef As Field 
     Dim fldQueryDef As Field 
     Dim fldRecordset As Field 
     Dim fldRelation As Field 
     Dim fldIndex As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     ' Assign a Field object from different Fields 
     ' collections to object variables. 
     Set fldTableDef = _ 
     dbsNorthwind.TableDefs(0).Fields(0) 
     Set fldQueryDef =dbsNorthwind.QueryDefs(0).Fields(0) 
     Set fldRecordset = rstEmployees.Fields(0) 
     Set fldRelation =dbsNorthwind.Relations(0).Fields(0) 
     Set fldIndex = _ 
     dbsNorthwind.TableDefs(0).Indexes(0).Fields(0) 
     
     ' Print report. 
     FieldOutput "TableDef", fldTableDef 
     FieldOutput "QueryDef", fldQueryDef 
     FieldOutput "Recordset", fldRecordset 
     FieldOutput "Relation", fldRelation 
     FieldOutput "Index", fldIndex 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub FieldOutput(strTemp As String, fldTemp As Field) 
     ' Report function for FieldX. 
     
     Dim prpLoop As Property 
     
     Debug.Print "Valid Field properties in " & strTemp 
     
     ' Enumerate Properties collection of passed Field 
     ' object. 
     For Each prpLoop In fldTemp.Properties 
     ' Some properties are invalid in certain 
     ' contexts (the Value property in the Fields 
     ' collection of a TableDef for example). Any 
     ' attempt to use an invalid property will 
     ' trigger an error. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " = " & _ 
     prpLoop.Value 
     On Error GoTo 0 
     Next prpLoop 
     
    End Sub 
```

<br/>

<span data-ttu-id="9815a-p104">In diesem Beispiel wird die **CreateField**-Methode zum Erstellen dreier **Fields**-Objekte für ein neues **TableDef**-Objekt verwendet. Anschließend werden die Eigenschaften der **Field**-Objekte angezeigt, die nicht automatisch von der **CreateField**-Methode festgelegt werden. (Eigenschaften, deren Werte zum Zeitpunkt der Erstellung des **Field**-Objekts leer sind, werden nicht gezeigt.)</span><span class="sxs-lookup"><span data-stu-id="9815a-p104">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

```vb
    Sub CreateFieldX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfNew As TableDef 
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
     
     ' Create and append new Field objects for the new 
     ' TableDef object. 
     With tdfNew 
     ' The CreateField method will set a default Size 
     ' for a new Field object if one is not specified. 
     .Fields.Append .CreateField("TextField", dbText) 
     .Fields.Append .CreateField("IntegerField", dbInteger) 
     .Fields.Append .CreateField("DateField", dbDate) 
     End With 
     
     dbsNorthwind.TableDefs.Append tdfNew 
     
     Debug.Print "Properties of new Fields in " & tdfNew.Name 
     
     ' Enumerate Fields collection to show the properties of 
     ' the new Field objects. 
     For Each fldLoop In tdfNew.Fields 
     Debug.Print " " & fldLoop.Name 
     
     For Each prpLoop In fldLoop.Properties 
     ' Properties that are invalid in the context of 
     ' TableDefs will trigger an error if an attempt 
     ' is made to read their values. 
     On Error Resume Next 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     On Error GoTo 0 
     Next prpLoop 
     
     Next fldLoop 
     
     ' Delete new TableDef because this is a demonstration. 
     dbsNorthwind.TableDefs.Delete tdfNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
