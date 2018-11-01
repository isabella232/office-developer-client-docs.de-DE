---
title: Field2.Required Property (DAO)
TOCTitle: Required Property
ms:assetid: 7d14dfd7-a50d-6044-469e-1511c74c148d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196390(v=office.15)
ms:contentKeyID: 48545848
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6d4963ed10f2bf886a7445dfa05f1a3fcef460
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872942"
---
# <a name="field2required-property-dao"></a><span data-ttu-id="88ad6-102">Field2.Required Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="88ad6-102">Field2.Required Property (DAO)</span></span>


<span data-ttu-id="88ad6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88ad6-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="88ad6-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der angibt, ob ein **Field2**-Objekt einen Nicht-Nullwert erfordert.</span><span class="sxs-lookup"><span data-stu-id="88ad6-104">Sets or returns a value that indicates whether a **Field2** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ad6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="88ad6-105">Syntax</span></span>

<span data-ttu-id="88ad6-106">*Ausdruck* . Erforderlich</span><span class="sxs-lookup"><span data-stu-id="88ad6-106">*expression* .Required</span></span>

<span data-ttu-id="88ad6-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="88ad6-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ad6-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88ad6-108">Remarks</span></span>

<span data-ttu-id="88ad6-109">Bei einem **Field2**-Objekt, das der **Fields**-Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="88ad6-109">For a **Field2** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="88ad6-110">Die Verfügbarkeit der **Required**-Eigenschaft hängt vom Objekt ab, in dem die **[Fields](fields-collection-dao.md)** -Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="88ad6-110">The availability of the **Required** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88ad6-111">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="88ad6-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="88ad6-112">Required-Wert</span><span class="sxs-lookup"><span data-stu-id="88ad6-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88ad6-113"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="88ad6-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="88ad6-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88ad6-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ad6-115"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="88ad6-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="88ad6-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="88ad6-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88ad6-117"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="88ad6-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="88ad6-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="88ad6-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ad6-119"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="88ad6-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="88ad6-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="88ad6-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88ad6-121"><strong>TableDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="88ad6-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="88ad6-122">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="88ad6-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="88ad6-123">Die Eigenschaft **Required** und **AllowZeroLength**, **ValidateOnSet**oder **ValidationRule** -Eigenschaft können Sie um die Gültigkeit der Einstellung der **Value** -Eigenschaft für das **Field2** -Objekt zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="88ad6-123">You can use the **Required** property along with the **AllowZeroLength**, **ValidateOnSet**, or **ValidationRule** property to determine the validity of the **Value** property setting for that **Field2** object.</span></span> <span data-ttu-id="88ad6-124">Wenn die **Required**-Eigenschaft den Wert **False**hat, kann das Feld **null**-Werte enthalten und ebenso Werte, die die von den Eigenschaften **AllowZeroLength** und **ValidationRule** festgelegten Bedingungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="88ad6-124">If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="88ad6-p102">[!HINWEIS] Wenn Sie diese Eigenschaft für ein <STRONG>Index</STRONG>-Objekt oder ein <STRONG>Field2</STRONG>-Objekt festlegen können, legen Sie sie für das <STRONG>Field2</STRONG>-Objekt fest. Die Gültigkeit der Eigenschafteneinstellung für ein <STRONG>Field2</STRONG>-Objekt wird vor der eines <STRONG>Index</STRONG>-Objekts überprüft.</span><span class="sxs-lookup"><span data-stu-id="88ad6-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field2</STRONG> object, set it for the <STRONG>Field2</STRONG> object. The validity of the property setting for a <STRONG>Field2</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="88ad6-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="88ad6-127">Example</span></span>

<span data-ttu-id="88ad6-p103">Dieses Beispiel verwendet die Required-Eigenschaft, um anzugeben, welche Felder in drei verschiedenen Tabellen Daten enthalten müssen, damit ein neuer Datensatz hinzugefügt wird.  Die RequiredOutput-Prozedur ist zum Ausführen dieser Prozedur erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ad6-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

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

