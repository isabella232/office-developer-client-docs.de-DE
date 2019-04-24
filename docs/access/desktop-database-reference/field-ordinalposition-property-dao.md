---
title: Field. OrdinalPosition-Eigenschaft (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293035"
---
# <a name="fieldordinalposition-property-dao"></a><span data-ttu-id="8588d-102">Field. OrdinalPosition-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="8588d-102">Field.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="8588d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8588d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8588d-104">Legt die relative Position eines **[Field](field-object-dao.md)** -Objekts in einer Fields **[](fields-collection-dao.md)** -Auflistung fest oder gibt Sie zurück.</span><span class="sxs-lookup"><span data-stu-id="8588d-104">Sets or returns the relative position of a **[Field](field-object-dao.md)** object within a **[Fields](fields-collection-dao.md)** collection.</span></span> <span data-ttu-id="8588d-105">.</span><span class="sxs-lookup"><span data-stu-id="8588d-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="8588d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8588d-106">Syntax</span></span>

<span data-ttu-id="8588d-107">*Ausdruck* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8588d-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="8588d-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8588d-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8588d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8588d-109">Remarks</span></span>

<span data-ttu-id="8588d-110">Bei einem Objekt, das noch nicht der **Fields**-Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8588d-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8588d-111">The default is 0.</span><span class="sxs-lookup"><span data-stu-id="8588d-111">The default is 0.</span></span>

<span data-ttu-id="8588d-112">Die Verfügbarkeit der **OrdinalPosition**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="8588d-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8588d-113">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="8588d-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="8588d-114">OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8588d-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8588d-115"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="8588d-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8588d-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8588d-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8588d-117"><strong>QueryDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="8588d-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8588d-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8588d-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8588d-119"><strong>Recordset</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="8588d-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8588d-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="8588d-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8588d-121"><strong>Relation</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="8588d-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8588d-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8588d-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8588d-123"><strong>TableDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="8588d-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8588d-124">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="8588d-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8588d-125">In der Regel hängt die Position eines Objekts, das Sie einer Auflistung anfügen, von der Reihenfolge der Anfügung ab.</span><span class="sxs-lookup"><span data-stu-id="8588d-125">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object.</span></span> <span data-ttu-id="8588d-126">Das erste angefügte Objekt befindet sich an der ersten Position (0), das zweite an der zweiten Position (1) usw.</span><span class="sxs-lookup"><span data-stu-id="8588d-126">The first appended object is in the first position (0), the second appended object is in the second position (1), and so on.</span></span> <span data-ttu-id="8588d-127">Das letzte angefügte Objekt befindet sich in der Ordnungsposition count-1, wobei count die Anzahl der Objekte in der Auflistung ist, wie durch die **[count](containers-count-property-dao.md)** -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8588d-127">The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="8588d-128">Mit der **OrdinalPosition**-Eigenschaft können Sie eine Ordnungsposition für neue **Field**-Objekte festlegen, die sich von der Reihenfolge unterscheidet, in der Sie diese Objekte an eine Auflistung anhängen.</span><span class="sxs-lookup"><span data-stu-id="8588d-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="8588d-129">Dadurch können Sie eine Feldreihenfolge für Tabellen, Abfragen und Recordsets angeben, die Sie in einer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8588d-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="8588d-130">Die Reihenfolge, in der Felder in einer SELECT \* -Abfrage zurückgegeben werden, wird beispielsweisedurch die aktuellen Werte der **Ordinalposition** -Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8588d-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="8588d-131">Sie können die Reihenfolge, in der Felder in Datensatzgruppen zurückgegeben werden, dauerhaft festlegen, indem Sie die **OrdinalPosition**-Eigenschaft auf eine positive Ganzzahl setzen.</span><span class="sxs-lookup"><span data-stu-id="8588d-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="8588d-p104">Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span><span class="sxs-lookup"><span data-stu-id="8588d-p104">Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="8588d-p105">Sie können einen Wert angeben, der größer als die Anzahl der Felder minus 1 ist. Das Feld wird in einer Reihenfolge relativ zum größten Wert zurückgegeben. Wenn Sie z. B. die **OrdinalPosition**-Eigenschaft eines Felds auf 20 festlegen (und nur 5 Felder vorhanden sind) und Sie die **OrdinalPosition**-Eigenschaft für zwei anderen Felder auf 10 und 30 gesetzt haben, wird das Feld mit dem Wert 20 zwischen den Feldern mit den Werten 10 und 30 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8588d-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>

> [!NOTE]
> <span data-ttu-id="8588d-137">Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span><span class="sxs-lookup"><span data-stu-id="8588d-137">Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="8588d-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8588d-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>

## <a name="example"></a><span data-ttu-id="8588d-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8588d-139">Example</span></span>

<span data-ttu-id="8588d-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span><span class="sxs-lookup"><span data-stu-id="8588d-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
