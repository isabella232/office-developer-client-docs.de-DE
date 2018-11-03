---
title: Field.Size-Eigenschaft (DAO)
TOCTitle: Size Property
ms:assetid: 15e25201-87b6-f62f-ff18-259414a47891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845510(v=office.15)
ms:contentKeyID: 48543419
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052878
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e1e7d124e06331a043a28c71bcdc9707c4664738
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931330"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="2f317-102">Field.Size-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f317-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="2f317-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f317-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="2f317-104">Legt einen Wert fest, der die maximale Größe eines **[Field](field-object-dao.md)** -Objekts in Byte angibt, oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2f317-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f317-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f317-105">Syntax</span></span>

<span data-ttu-id="2f317-106">*Ausdruck* . Größe</span><span class="sxs-lookup"><span data-stu-id="2f317-106">*expression* .Size</span></span>

<span data-ttu-id="2f317-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="2f317-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f317-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f317-108">Remarks</span></span>

<span data-ttu-id="2f317-109">Für ein Objekt, das noch nicht an die **[Fields](fields-collection-dao.md)** -Auflistung angehängt wurde, besteht Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2f317-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="2f317-p101">Bei Feldern (außer Memofeldern), die Zeichendaten enthalten, gibt die **Size**-Eigenschaft die maximale Anzahl von Zeichen an, die ein Feld enthalten kann. Bei numerischen Feldern gibt die **Size**-Eigenschaft an, wie viel Speicherplatz in Bytes erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2f317-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="2f317-112">Die Verwendung der **Size**-Eigenschaft hängt von dem Objekt ab, das die **Fields**-Auflistung enthält, an die das **Field**-Objekt angehängt ist, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2f317-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f317-113">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="2f317-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="2f317-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="2f317-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f317-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="2f317-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="2f317-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f317-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f317-117"><strong>QueryDef-Objekt</strong></span><span class="sxs-lookup"><span data-stu-id="2f317-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2f317-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2f317-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f317-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="2f317-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="2f317-120">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2f317-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f317-121"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="2f317-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="2f317-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2f317-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f317-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="2f317-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="2f317-124">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2f317-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2f317-p102">Wenn Sie ein Field-Objekt mit einem anderen Datentyp als Text erstellen, legt der Wert der Type-Eigenschaft automatisch die Einstellung des Size-Eigenschaft fest, sodass Sie diese Eigenschaft nicht festlegen müssen. Bei einem Field-Objekt vom Text-Datentyp können Sie jedoch Size auf eine Ganzzahl bis zur maximalen Textgröße festlegen (255 für Microsoft Access-Datenbanken). Wenn Sie die Größe nicht festlegen, hat das Feld die maximale von der Datenbank zugelassene Größe.</span><span class="sxs-lookup"><span data-stu-id="2f317-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="2f317-p103">Bei Field-Objekten der Datentypen Long Binary und Memo hat Size immer den Wert 0. Verwenden Sie die FieldSize-Eigenschaft des Field-Objekts, um die Größe der Daten in einem bestimmten Datensatz festzustellen. Die maximale Größe eines Felds vom Datentyp Long Binary oder Memo ist nur durch die Systemressourcen bzw. die maximale von der Datenbank erlaubte Größe begrenzt.</span><span class="sxs-lookup"><span data-stu-id="2f317-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="2f317-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2f317-131">Example</span></span>

<span data-ttu-id="2f317-132">In diesem Beispiel wird die Size-Eigenschaft veranschaulicht, indem die Namen und Größen der Field-Objekte in der Tabelle Employees durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="2f317-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

```vb
    Sub SizeX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldNew As Field 
     Dim fldLoop As Field 
     
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
