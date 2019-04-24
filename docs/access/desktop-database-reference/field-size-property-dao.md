---
title: Field. Size-Eigenschaft (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 16ce8a9e63c18ded2738035f23e9a1baeff4cc8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293015"
---
# <a name="fieldsize-property-dao"></a><span data-ttu-id="e726c-102">Field. Size-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="e726c-102">Field.Size property (DAO)</span></span>


<span data-ttu-id="e726c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e726c-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e726c-104">Legt einen Wert fest, der die maximale Größe eines **[Field](field-object-dao.md)** -Objekts in Byte angibt, oder gibt den betreffenden Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e726c-104">Sets or returns a value that indicates the maximum size, in bytes, of a **[Field](field-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e726c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e726c-105">Syntax</span></span>

<span data-ttu-id="e726c-106">*Ausdruck* . Größe</span><span class="sxs-lookup"><span data-stu-id="e726c-106">*expression* .Size</span></span>

<span data-ttu-id="e726c-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e726c-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e726c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e726c-108">Remarks</span></span>

<span data-ttu-id="e726c-109">Bei einem Objekt, das noch nicht der **[Fields](fields-collection-dao.md)** -Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="e726c-109">For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="e726c-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span><span class="sxs-lookup"><span data-stu-id="e726c-p101">For fields (other than Memo type fields) that contain character data, the **Size** property indicates the maximum number of characters that the field can hold. For numeric fields, the **Size** property indicates how many bytes of storage are required.</span></span>

<span data-ttu-id="e726c-112">Die Verwendung der **Size**-Eigenschaft hängt von dem Objekt ab, das die **Fields**-Auflistung enthält, an die das **Field**-Objekt angehängt ist, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e726c-112">Use of the **Size** property depends on the object that contains the **Fields** collection to which the **Field** object is appended, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e726c-113">Zugehörigkeit zu Objekt</span><span class="sxs-lookup"><span data-stu-id="e726c-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="e726c-114">Verwendung</span><span class="sxs-lookup"><span data-stu-id="e726c-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e726c-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e726c-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="e726c-116">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e726c-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e726c-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e726c-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e726c-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e726c-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e726c-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e726c-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="e726c-120">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e726c-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e726c-121"><strong>Beziehung</strong></span><span class="sxs-lookup"><span data-stu-id="e726c-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="e726c-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e726c-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e726c-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e726c-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e726c-124">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="e726c-124">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e726c-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span><span class="sxs-lookup"><span data-stu-id="e726c-p102">When you create a **Field** object with a data type other than Text, the **[Type](field-type-property-dao.md)** property setting automatically determines the **Size** property setting; you don't need to set it. For a **Field** object with the Text data type, however, you can set **Size** to any integer up to the maximum text size (255 for Microsoft Access databases). If you do not set the size, the field will be as large as the database allows.</span></span>

<span data-ttu-id="e726c-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span><span class="sxs-lookup"><span data-stu-id="e726c-p103">For Long Binary and Memo **Field** objects, **Size** is always set to 0. Use the **[FieldSize](field-fieldsize-property-dao.md)** property of the **Field** object to determine the size of the data in a specific record. The maximum size of a Long Binary or Memo field is limited only by your system resources or the maximum size that the database allows.</span></span>

## <a name="example"></a><span data-ttu-id="e726c-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e726c-131">Example</span></span>

<span data-ttu-id="e726c-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span><span class="sxs-lookup"><span data-stu-id="e726c-132">This example demonstrates the **Size** property by enumerating the names and sizes of the **Field** objects in the Employees table.</span></span>

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
