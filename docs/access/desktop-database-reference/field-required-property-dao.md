---
title: Field.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77214fcad0f5b2cafe794282782df4446d37fcf6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887159"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="c23cc-102">Field.Required Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c23cc-102">Field.Required Property (DAO)</span></span>


<span data-ttu-id="c23cc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c23cc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c23cc-104">Gibt einen Wert zurück, der angibt, ob ein **[Field](field-object-dao.md)** -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="c23cc-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c23cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c23cc-105">Syntax</span></span>

<span data-ttu-id="c23cc-106">*Ausdruck* . Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c23cc-106">*expression* .Required</span></span>

<span data-ttu-id="c23cc-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c23cc-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c23cc-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c23cc-108">Remarks</span></span>

<span data-ttu-id="c23cc-109">Ein **Field**-Objekt, das noch nicht an die **Fields**-Auflistung angehängt wurde, hat Lese-/Schreibzugriff für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c23cc-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="c23cc-110">Die Verfügbarkeit der **Required**-Eigenschaft hängt von dem Objekt ab, das die [Fields](fields-collection-dao.md)-Auflistung enthält, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c23cc-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c23cc-111">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="c23cc-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="c23cc-112">Required-Wert</span><span class="sxs-lookup"><span data-stu-id="c23cc-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c23cc-113"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="c23cc-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c23cc-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c23cc-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c23cc-115"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="c23cc-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c23cc-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c23cc-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c23cc-117"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="c23cc-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c23cc-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c23cc-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c23cc-119"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="c23cc-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c23cc-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c23cc-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c23cc-121"><strong>TableDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="c23cc-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="c23cc-122">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="c23cc-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c23cc-p101">Mit der **Required**-Eigenschaft können Sie in Kombination mit der **[AllowZeroLength](field-allowzerolength-property-dao.md)** -, **[ValidateOnSet](field-validateonset-property-dao.md)** - oder **[ValidationRule](field-validationrule-property-dao.md)** -Eigenschaft die Gültigkeit des Werts der **[Value](field-value-property-dao.md)** -Eigenschaft für dieses **Field**-Objekt überprüfen. Wenn die **Required**-Eigenschaft den Wert **False**hat, kann das Feld **null**-Werte enthalten und ebenso Werte, die die von den Eigenschaften **AllowZeroLength** und **ValidationRule** festgelegten Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c23cc-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c23cc-p102">[!HINWEIS] Wenn Sie diese Eigenschaft sowohl für ein <STRONG>Index</STRONG>- als auch für ein <STRONG>Field</STRONG>-Objekt festlegen können, sollten Sie es für das <STRONG>Field</STRONG>-Objekt angeben. Die Gültigkeit des Werts dieser Eigenschaft wird zuerst für das <STRONG>Field</STRONG>-Objekt und erst danach für das <STRONG>Index</STRONG>-Objekt überprüft.</span><span class="sxs-lookup"><span data-stu-id="c23cc-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="c23cc-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c23cc-127">Example</span></span>

<span data-ttu-id="c23cc-p103">Dieses Beispiel verwendet die Required-Eigenschaft, um anzugeben, welche Felder in drei verschiedenen Tabellen Daten enthalten müssen, damit ein neuer Datensatz hinzugefügt wird.  Die RequiredOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c23cc-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

