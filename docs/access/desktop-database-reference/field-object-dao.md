---
title: Field-Objekt - Datenzugriff Objekte (DAO)
TOCTitle: Field Object
ms:assetid: 47282ce2-9b49-ccf9-ad37-c4bb25cfd037
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193203(v=office.15)
ms:contentKeyID: 48544587
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c58896fb0d0a5c5a28844fdd3a6df922dd587f32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703643"
---
# <a name="field-object-dao"></a><span data-ttu-id="20de2-102">Field-Objekt (DAO)</span><span class="sxs-lookup"><span data-stu-id="20de2-102">Field object (DAO)</span></span>

<span data-ttu-id="20de2-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20de2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20de2-104">Ein **Field**-Objekt stellt Daten mit einem gemeinsamen Datentyp in einer Spalte und einer typischen Gruppe von Eigenschaften dar.</span><span class="sxs-lookup"><span data-stu-id="20de2-104">A **Field** object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="20de2-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20de2-105">Remarks</span></span>

<span data-ttu-id="20de2-p101">Die **Fields**-Auflistung der Objekte **Index**, **QueryDef**, **Relation** und **TableDef** enthält die Spezifikationen für die Felder, die diese Objekte darstellen. Die **Fields**-Auflistung eines **Recordset**-Objekts stellt die **Field**-Objekte in einer Zeile mit Daten oder einem Datensatz dar. Verwenden Sie die **Field**-Objekte in einem **Recordset**-Objekt, um Werte für die Felder im aktuellen Datensatz des **Recordset**-Objekts zu lesen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20de2-p101">The **Fields** collections of **Index**, **QueryDef**, **Relation**, and **TableDef** objects contain the specifications for the fields those objects represent. The **Fields** collection of a **Recordset** object represents the **Field** objects in a row of data, or in a record. You use the **Field** objects in a **Recordset** object to read and set values for the fields in the current record of the **Recordset** object.</span></span>

<span data-ttu-id="20de2-p102">In einem Microsoft Access-Arbeitsbereich verwenden Sie ein **Field**-Objekt und dessen Methoden und Eigenschaften, um ein Feld zu bearbeiten. Sie können z. B. die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="20de2-p102">In a Microsoft Access workspacee, you manipulate a field using a **Field** object and its methods and properties. For example, you can:</span></span>

  - <span data-ttu-id="20de2-111">Verwenden Sie die **OrdinalPosition**-Eigenschaft, um die Präsentationsreihenfolge des **Field**-Objekts in einer **Fields**-Auflistung festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20de2-111">Use the **OrdinalPosition** property to set or return the presentation order of the **Field** object in a **Fields** collection.</span></span>

  - <span data-ttu-id="20de2-112">Verwenden Sie die **Value**-Eigenschaft eines Felds in einem **Recordset**-Objekt, um gespeicherte Daten festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20de2-112">Use the **Value** property of a field in a **Recordset** object to set or return stored data.</span></span>

  - <span data-ttu-id="20de2-113">Verwenden Sie die Methoden **AppendChunk** und **GetChunk** sowie die **FieldSize**-Eigenschaft, um einen Wert in einem OLE-Objekt- oder Memofeld eines **Recordset**-Objekts abzurufen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20de2-113">Use the **AppendChunk** and **GetChunk** methods and the **FieldSize** property to get or set a value in an OLE Object or Memo field of a **Recordset** object.</span></span>

  - <span data-ttu-id="20de2-114">Ermitteln Sie mit den Eigenschaften **Type**, **Size** und **Attributes**, welche Art Daten in einem Feld gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="20de2-114">Use the **Type**, **Size**, and **Attributes** properties to determine the type of data that can be stored in the field.</span></span>

  - <span data-ttu-id="20de2-115">Ermitteln Sie mit den Eigenschaften **SourceField** und **SourceTable** die ursprüngliche Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="20de2-115">Use the **SourceField** and **SourceTable** properties to determine the original source of the data.</span></span>

  - <span data-ttu-id="20de2-116">Verwenden Sie die **ForeignName**-Eigenschaft, um Informationen zu einem fremden Feld in einem **Relation**-Objekt festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20de2-116">Use the **ForeignName** property to set or return information about a foreign field in a **Relation** object.</span></span>

  - <span data-ttu-id="20de2-117">Verwenden Sie die Eigenschaften **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule** oder **ValidationText**, um Gültigkeitsbedingungen festzulegen oder zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="20de2-117">Use the **AllowZeroLength**, **DefaultValue**, **Required**, **ValidateOnSet**, **ValidationRule**, or **ValidationText** properties to set or return validation conditions.</span></span>

  - <span data-ttu-id="20de2-118">Verwenden Sie die **DefaultValue**-Eigenschaft eines Felds für ein **TableDef**-Objekt, um den Standardwert beim Hinzfügen neuer Datensätze für dieses Feld festzulegen.</span><span class="sxs-lookup"><span data-stu-id="20de2-118">Use the **DefaultValue** property of a field on a **TableDef** object to set the default value for this field when new records are added.</span></span>

<span data-ttu-id="20de2-119">Verwenden Sie zum Erstellen eines neuen **Field**-Objekts in einem der Objekte **Index**, **TableDef** oder **Relation** die **CreateField**-Methode.</span><span class="sxs-lookup"><span data-stu-id="20de2-119">To create a new **Field** object in an **Index**, **TableDef**, or **Relation** object, use the **CreateField** method.</span></span>

<span data-ttu-id="20de2-p103">Wenn Sie auf ein **Field**-Objekt zugreifen, das Teil eines **Recordset**-Objekts ist, sind Daten aus dem aktuellen Datensatz in der **Value**-Eigenschaft des **Field**-Objekts sichtbar. In der Regel verweisen Sie zum Bearbeiten von Daten im **Recordset**-Objekt nicht direkt auf die **Fields**-Auflistung. Sie verweisen stattdessen indirekt auf die **Value**-Eigenschaft des **Field**-Objekts in der **Fields**-Auflistung des **Recordset**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="20de2-p103">When you access a **Field** object as part of a **Recordset** object, data from the current record is visible in the **Field** object's **Value** property. To manipulate data in the **Recordset** object, you don't usually reference the **Fields** collection directly; instead, you indirectly reference the **Value** property of the **Field** object in the **Fields** collection of the **Recordset** object.</span></span>

<span data-ttu-id="20de2-122">Wenn Sie auf ein **Field**-Objekt in einer Auflistung mit seiner Ordnungszahl oder mit der Einstellung seiner **Name**-Eigenschaft verweisen möchten, verwenden Sie eine der folgenden Syntaxformen:</span><span class="sxs-lookup"><span data-stu-id="20de2-122">To refer to a **Field** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="20de2-123">**Fields**(0)</span><span class="sxs-lookup"><span data-stu-id="20de2-123">**Fields**(0)</span></span>

- <span data-ttu-id="20de2-124">**Felder** ("Name")</span><span class="sxs-lookup"><span data-stu-id="20de2-124">**Fields**("name")</span></span>

- <span data-ttu-id="20de2-125">**Felder**\!\[Namen\]</span><span class="sxs-lookup"><span data-stu-id="20de2-125">**Fields**\!\[name\]</span></span>

<span data-ttu-id="20de2-p104">Mit denselben Syntaxformen können Sie auch auf die **Value**-Eigenschaft eines von Ihnen erstellten **Field**-Objekts verweisen, das Sie einer **Fields**-Auflistung anfügen. Der Kontext des Feldverweises bestimmt, ob sich der Verweis auf das **Field**-Objekt oder die **Value**-Eigenschaft des **Field**-Objekts bezieht.</span><span class="sxs-lookup"><span data-stu-id="20de2-p104">With the same syntax forms, you can also refer to the **Value** property of a **Field** object that you create and append to a **Fields** collection. The context of the field reference will determine whether you are referring to the **Field** object or the **Value** property of the **Field** object.</span></span>

## <a name="example"></a><span data-ttu-id="20de2-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="20de2-128">Example</span></span>

<span data-ttu-id="20de2-p105">Dieses Beispiel zeigt, welche Eigenschaften für ein **Field** -Objekt gültig sind, abhängig davon, wo sich das **Field** -Objekt befindet (z. B. **Fields** -Auflistung eines **TableDef** -Objekts, **Fields** -Auflistung eines **QueryDef** -Objekts usw.). Zum Ausführen dieser Prozedur ist die FieldOutput-Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="20de2-p105">This example shows what properties are valid for a **Field** object depending on where the **Field** resides (for example, the **Fields** collection of a **TableDef**, the **Fields** collection of a **QueryDef**, and so forth). The FieldOutput procedure is required for this procedure to run.</span></span>

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

<span data-ttu-id="20de2-p106">In diesem Beispiel wird die **CreateField**-Methode zum Erstellen dreier **Fields**-Objekte für ein neues **TableDef**-Objekt verwendet. Anschließend werden die Eigenschaften der **Field**-Objekte angezeigt, die nicht automatisch von der **CreateField**-Methode festgelegt werden. (Eigenschaften, deren Werte zum Zeitpunkt der Erstellung des **Field**-Objekts leer sind, werden nicht gezeigt.)</span><span class="sxs-lookup"><span data-stu-id="20de2-p106">This example uses the **CreateField** method to create three **Fields** for a new **TableDef**. It then displays the properties of those **Field** objects that are automatically set by the **CreateField** method. (Properties whose values are empty at the time of **Field** creation are not shown.)</span></span>

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
