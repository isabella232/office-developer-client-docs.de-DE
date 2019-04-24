---
title: Field2. Required-Eigenschaft (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6b1950c8a864fbf23bee26be89e07e49357840b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292720"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="c63e5-102">Field2. Required-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="c63e5-102">Field2.Required property (DAO)</span></span>


<span data-ttu-id="c63e5-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c63e5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="c63e5-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein **Field2**-Objekt einen Nicht-Nullwert erfordert.</span><span class="sxs-lookup"><span data-stu-id="c63e5-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c63e5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c63e5-105">Syntax</span></span>

<span data-ttu-id="c63e5-106">*Ausdruck* . Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c63e5-106">*expression* .Required</span></span>

<span data-ttu-id="c63e5-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c63e5-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c63e5-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c63e5-108">Remarks</span></span>

<span data-ttu-id="c63e5-109">Bei einem **Field2**-Objekt, das der **Fields**-Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="c63e5-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c63e5-110">Die Verfügbarkeit der **Required**-Eigenschaft hängt vom Objekt ab, in dem die **[Fields](fields-collection-dao.md)** -Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="c63e5-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c63e5-111">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="c63e5-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="c63e5-112">Required-Wert</span><span class="sxs-lookup"><span data-stu-id="c63e5-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c63e5-113"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c63e5-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c63e5-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c63e5-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63e5-115"><strong>QueryDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c63e5-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c63e5-116">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c63e5-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63e5-117"><strong>Recordset</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c63e5-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c63e5-118">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c63e5-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c63e5-119"><strong>Relation</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c63e5-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c63e5-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c63e5-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c63e5-121"><strong>TableDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c63e5-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c63e5-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c63e5-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c63e5-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span><span class="sxs-lookup"><span data-stu-id="c63e5-p101">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <span data-ttu-id="c63e5-p102">[!HINWEIS] Wenn Sie diese Eigenschaft für ein **Index**-Objekt oder ein **Field2**-Objekt festlegen können, legen Sie sie für das **Field2**-Objekt fest. Die Gültigkeit der Eigenschafteneinstellung für ein **Field2**-Objekt wird vor der eines **Index**-Objekts überprüft.</span><span class="sxs-lookup"><span data-stu-id="c63e5-p102">When you can set this property for either an **Index** object or a **Field2** object, set it for the **Field2** object. The validity of the property setting for a **Field2** object is checked before that of an **Index** object.</span></span>



## <a name="example"></a><span data-ttu-id="c63e5-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c63e5-127">Example</span></span>

<span data-ttu-id="c63e5-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span><span class="sxs-lookup"><span data-stu-id="c63e5-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field2 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

