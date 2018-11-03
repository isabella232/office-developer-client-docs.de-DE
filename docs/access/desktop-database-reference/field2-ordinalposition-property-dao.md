---
title: Field2.Ordinalposition-Eigenschaft (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 600fe2855ba10e1ab36413f6395d3455bb7bd00b
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937057"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="8413f-102">Field2.Ordinalposition-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="8413f-102">Field2.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="8413f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8413f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="8413f-p101">Mit dieser Eigenschaft wird die relative Position eines **Field2**-Objekts in einer **[Fields](fields-collection-dao.md)** -Auflistung festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8413f-p101">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection. .</span></span>

## <a name="syntax"></a><span data-ttu-id="8413f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="8413f-106">Syntax</span></span>

<span data-ttu-id="8413f-107">*Ausdruck* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8413f-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="8413f-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="8413f-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8413f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8413f-109">Remarks</span></span>

<span data-ttu-id="8413f-110">Bei einem Objekt, das noch nicht der **Fields**-Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8413f-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="8413f-111">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="8413f-111">The default is 0.</span></span>

<span data-ttu-id="8413f-112">Die Verfügbarkeit der **OrdinalPosition**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="8413f-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8413f-113">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="8413f-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="8413f-114">
Verfügbarkeit von OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="8413f-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8413f-115"><strong>Index</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="8413f-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8413f-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8413f-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8413f-117"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="8413f-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8413f-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8413f-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8413f-119"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="8413f-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8413f-120">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="8413f-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8413f-121"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="8413f-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8413f-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8413f-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8413f-123"><strong>TableDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="8413f-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="8413f-124">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="8413f-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8413f-p102">In der Regel hängt die Position eines Objekts, das Sie einer Auflistung anfügen, von der Reihenfolge der Anfügung ab. Das erste angefügte Objekt befindet sich an der ersten Position (0), das zweite an der zweiten Position (1) usw. Das letzte hinzugefügte Objekt befindet sich an Position Count – 1, wobei Count der Anzahl von Objekten in der Auflistung entspricht, wie durch die Einstellung der **[Count](containers-count-property-dao.md)**-Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="8413f-p102">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object. The first appended object is in the first position (0), the second appended object is in the second position (1), and so on. The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="8413f-128">Sie können mithilfe der **OrdinalPosition**-Eigenschaft eine Position für neue **Field2**-Objekte angeben, die von der Reihenfolge abweicht, in der Sie diese Objekte der Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="8413f-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="8413f-129">Dadurch können Sie eine Feldreihenfolge für Tabellen, Abfragen und Recordsets angeben, die Sie in einer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8413f-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="8413f-130">Beispielsweise die Reihenfolge, in der Felder in einer SELECT-Anweisung zurückgegeben werden \* Abfrage wird durch die aktuellen Werte der **OrdinalPosition** -Eigenschaft bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8413f-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="8413f-131">Sie können die Reihenfolge, in der Felder in Recordsets zurückgegeben werden, dauerhaft zurücksetzen, indem Sie die **OrdinalPosition**-Eigenschaft auf eine positive ganze Zahl festlegen.</span><span class="sxs-lookup"><span data-stu-id="8413f-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="8413f-p104">Zwei oder mehr Field2-Objekte in derselben Auflistung können denselben OrdinalPosition-Eigenschaftswert besitzen. In diesem Fall werden sie alphabetisch angeordnet. Wenn Sie z. B. ein Feld namens Alter auf 4 und ein zweites Feld namens Gewicht auf 4 festlegen, wird das Gewicht nach dem Alter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8413f-p104">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically. For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="8413f-p105">Sie können einen Wert angeben, der größer als die Anzahl der Felder minus 1 ist. Das Feld wird in einer Reihenfolge relativ zum größten Wert zurückgegeben. Wenn Sie z. B. die **OrdinalPosition**-Eigenschaft eines Felds auf 20 festlegen (und nur 5 Felder vorhanden sind) und Sie die **OrdinalPosition**-Eigenschaft für zwei anderen Felder auf 10 und 30 gesetzt haben, wird das Feld mit dem Wert 20 zwischen den Feldern mit den Werten 10 und 30 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8413f-p105">You can specify a number that is greater than the number of fields minus 1. The field will be returned in an order relative to the largest number. For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <span data-ttu-id="8413f-137">Auch wenn die **Fields** -Auflistung ein **[TableDef](tabledef-object-dao.md)** -Objekt nicht aktualisiert wurde, wird die Reihenfolge der Felder in einem **[Recordset-Objekt](recordset-object-dao.md)** aus der **TableDef** geöffnet die **OrdinalPosition** -Daten des **TableDef** -Objekts widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="8413f-137">Even if the **Fields** collection of a **[TableDef](tabledef-object-dao.md)** object has not been refreshed, the field order in a **[Recordset](recordset-object-dao.md)** opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="8413f-138">Ein **Recordset-Objekt** vom Typ Tabelle wird die gleichen **OrdinalPosition** Daten wie der zugrunde liegenden Tabelle, aber eine andere Art von **Recordset-Objekt** werden neue **OrdinalPosition** -Daten (beginnend mit 0), die die Reihenfolge der **Folgen haben OrdinalPosition** Daten des **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="8413f-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>



## <a name="example"></a><span data-ttu-id="8413f-139">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8413f-139">Example</span></span>

<span data-ttu-id="8413f-p107">Dieses Beispiel ändert die Werte der OrdinalPosition-Eigenschaft des TableDef-Objekts in der Employees-Tabelle (Personal), um die Field2-Reihenfolge in einem resultierenden Recordset-Objekt zu steuern. Indem die OrdinalPosition-Eigenschaft aller Felder der Fields-Auflistung auf 1 festgelegt wird, ordnen resultierende Recordset-Objekte die Fields-Auflistung alphabetisch an. Beachten Sie, dass die OrdinalPosition-Werte im Recordset-Objekt nicht mit den Werten im TableDef-Objekt übereinstimmen, sondern lediglich das Endergebnis der TableDef-Änderungen wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="8413f-p107">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**. By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically. Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
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
