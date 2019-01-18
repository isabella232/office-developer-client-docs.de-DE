---
title: Field2.Size-Eigenschaft (DAO)
TOCTitle: Size Property
ms:assetid: e252759a-cea9-25cb-667d-80b422fbf97e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835700(v=office.15)
ms:contentKeyID: 48548282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f1467414729f4ea82bc2779eeb2bd162465b5ccd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699037"
---
# <a name="field2size-property-dao"></a><span data-ttu-id="83834-102">Field2.Size-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="83834-102">Field2.Size property (DAO)</span></span>


<span data-ttu-id="83834-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83834-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="83834-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der die maximale Größe eines **Field2**-Objekts in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="83834-104">Sets or returns a value that indicates the maximum size, in bytes, of a **Field2** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="83834-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83834-105">Syntax</span></span>

<span data-ttu-id="83834-106">*Ausdruck* . Größe</span><span class="sxs-lookup"><span data-stu-id="83834-106">*expression* .Size</span></span>

<span data-ttu-id="83834-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="83834-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="83834-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83834-108">Remarks</span></span>

<span data-ttu-id="83834-109">Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="83834-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="83834-p101">Bei Feldern (außer Memofeldern), die Zeichendaten enthalten, gibt die **Size**-Eigenschaft die maximale Anzahl von Zeichen an, die ein Feld enthalten kann. Bei numerischen Feldern gibt die **Size**-Eigenschaft an, wie viel Speicherplatz in Bytes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="83834-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="83834-112">Die Verwendung der **Size**-Eigenschaft hängt vom Objekt ab, das die **Fields**-Auflistung enthält, der das **Field2**-Objekt angefügt wird (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="83834-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="83834-113">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="83834-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="83834-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="83834-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="83834-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="83834-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="83834-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="83834-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83834-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="83834-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="83834-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83834-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83834-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="83834-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="83834-120">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83834-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="83834-121"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="83834-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="83834-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="83834-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="83834-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="83834-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="83834-124">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="83834-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="83834-p102">Wenn Sie ein Field2-Objekt mit einem anderen Datentyp als Text erstellen, bestimmt die Einstellung der Type-Eigenschaft automatisch die Einstellung der Size-Eigenschaft, und Sie müssen die Eigenschaft nicht festlegen. Bei einem  Field2-Objekt mit dem Datentyp Text können Sie die Size-Eigenschaft jedoch auf eine ganze Zahl bis zu einer maximalen Textgröße festlegen (255 bei Microsoft Access-Datenbanken). Wenn Sie die Größe nicht festlegen, besitzt das Feld die in der Datenbank zulässige Größe.</span><span class="sxs-lookup"><span data-stu-id="83834-p102">When you create a **Field2** object with a data type other than Text, the **Type** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field2** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access database engine databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="83834-p103">Bei Field2-Objekten vom Datentyp Long Binary und Memo ist die Size-Eigenschaft immer auf 0 festgelegt. Bestimmen Sie mit der FieldSize-Eigenschaft des Field2-Objekts den Umfang der Daten in einem bestimmten Datensatz. Die maximale Größe eines Felds vom Typ Long Binary oder Memo wird nur durch die Systemressourcen oder die maximal in der Datenbank zulässige Größe beschränkt.</span><span class="sxs-lookup"><span data-stu-id="83834-p103">For Long Binary and Memo **Field2** objects, **Size** is always set to 0. Use the **FieldSize** property of the **Field2** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="83834-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="83834-131">Example</span></span>

<span data-ttu-id="83834-132">Dieses Beispiel veranschaulicht die Size-Eigenschaft, indem es die Namen und Größen des Field2-Objekts in der Employees-Tabelle (Personal) aufzählt.</span><span class="sxs-lookup"><span data-stu-id="83834-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field2** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field2 
     Dim fldLoop As Field2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     With tdfEmployees 
     
     ' Create and append a new Field object to the 
     ' Employees table. 
     Set fldNew = .CreateField("FaxPhone") 
     fldNew.Type = dbText 
     fldNew.Size = 20 
     .Fields.Append fldNew 
     
     Debug.Print "TableDef: " & .Name 
     Debug.Print " Field.Name - Field.Type - Field.Size" 
     
     ' Enumerate Fields collection; print field names, 
     ' types, and sizes. 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name & " - " & _ 
     fldLoop.Type & " - " & fldLoop.Size 
     Next fldLoop 
     
     ' Delete new field because this is a demonstration. 
     .Fields.Delete fldNew.Name 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
