---
title: Field2.Attributes Property (DAO)
TOCTitle: Attributes Property
ms:assetid: 08ae9b6b-21e4-9b7e-0852-cfc6639027a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845025(v=office.15)
ms:contentKeyID: 48543102
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052896
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6742e8b97e3444df38a7c52d048aaa6a2f023cb0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475414"
---
# <a name="field2attributes-property-dao"></a><span data-ttu-id="9e4eb-102">Field2.Attributes Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="9e4eb-102">Field2.Attributes Property (DAO)</span></span>


<span data-ttu-id="9e4eb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e4eb-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="9e4eb-p101">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines **Field2**-Objekts angibt. **Long**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-p101">Sets or returns a value that indicates one or more characteristics of a **Field2** object. Read/write **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e4eb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e4eb-106">Syntax</span></span>

<span data-ttu-id="9e4eb-107">*Ausdruck* . Attribute</span><span class="sxs-lookup"><span data-stu-id="9e4eb-107">*expression* .Attributes</span></span>

<span data-ttu-id="9e4eb-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e4eb-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e4eb-109">Remarks</span></span>

<span data-ttu-id="9e4eb-110">Dieser Wert gibt die Merkmale des Felds an, das durch das **Field2**-Objekt dargestellt wird. Er kann aus einer Kombinationen der folgenden Konstanten bestehen.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-110">The value specifies characteristics of the field represented by the **Field2** object and can be a combination of these constants.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e4eb-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="9e4eb-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="9e4eb-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9e4eb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-113"><strong>dbAutoIncrField festgelegt</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-113"><strong>dbAutoIncrField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-114">Der Feldwert für neue Datensätze wird automatisch auf einen eindeutigen Long Integer-Wert erhöht, der nicht geändert werden kann (wird in einem Microsoft Access-Arbeitsbereich nur bei Microsoft Access-Datenbanktabellen unterstützt).</span><span class="sxs-lookup"><span data-stu-id="9e4eb-114">The field value for new records is automatically incremented to a unique Long integer that can't be changed (in a Microsoft Access workspace, supported only for Microsoft Access database engine database tables).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4eb-115"><strong>dbDescending</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-115"><strong>dbDescending</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-p102">Das Feld wird in absteigender Reihenfolge sortiert (von Z bis A oder von 100 bis 0). Diese Option trifft nur auf ein <strong>Field2</strong>-Objekt in einer <strong>Fields</strong>-Auflistung eines <strong>Index</strong>-Objekts zu. Wenn Sie diese Konstante auslassen, wird das Feld in aufsteigender Reihenfolge sortiert (von A bis Z oder von 0 bis 100). Das ist der Standardwert für <strong>Index</strong>- und <strong>TableDef</strong>-Felder (gilt nur für Microsoft Access-Arbeitsbereiche)..</span><span class="sxs-lookup"><span data-stu-id="9e4eb-p102">The field is sorted in descending (Z to A or 100 to 0) order; this option applies only to a <strong>Field2</strong> object in a <strong>Fields</strong> collection of an <strong>Index</strong> object. If you omit this constant, the field is sorted in ascending (A to Z or 0 to 100) order. This is the default value for <strong>Index</strong> and <strong>TableDef</strong> fields (Microsoft Access workspaces only)..</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-119"><strong>dbFixedField</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-119"><strong>dbFixedField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-120">Die Feldgröße ist fest (Standard bei numerischen Feldern).</span><span class="sxs-lookup"><span data-stu-id="9e4eb-120">The field size is fixed (default for Numeric fields).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4eb-121"><strong>dbHyperlinkField</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-121"><strong>dbHyperlinkField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-122">Das Feld enthält Hyperlinkinformation (nur Memofelder).</span><span class="sxs-lookup"><span data-stu-id="9e4eb-122">The field contains hyperlink information (Memo fields only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-123"><strong>dbSystemField</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-123"><strong>dbSystemField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-124">Das Feld speichert Replikationsinformationen für Replikate. Dieser Feldtyp kann nicht gelöscht werden (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="9e4eb-124">The field stores replication information for replicas; you can't delete this type of field (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4eb-125"><strong>dbUpdatableField</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-125"><strong>dbUpdatableField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-126">Der Feldwert kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-126">The field value can be changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-127"><strong>dbVariableField</strong></span><span class="sxs-lookup"><span data-stu-id="9e4eb-127"><strong>dbVariableField</strong></span></span></p></td>
<td><p><span data-ttu-id="9e4eb-128">Die Feldgröße ist variabel (nur Textfelder).</span><span class="sxs-lookup"><span data-stu-id="9e4eb-128">The field size is variable (Text fields only).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e4eb-p103">Bei Objekten, die noch keiner Auflistung angefügt sind, besteht für diese Eigenschaft Lese-/Schreibzugriff. Bei einem angefügten **Field2**-Objekt hängt die Verfügbarkeit der **Attributes**-Eigenschaft vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-p103">For an object not yet appended to a collection, this property is read/write. For an appended **Field2** object, the availability of the **Attributes** property depends on the object that contains the **Fields** collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e4eb-131">Zugehörigkeit des Field-Objekts</span><span class="sxs-lookup"><span data-stu-id="9e4eb-131">If the Field object belongs to an</span></span></p></th>
<th><p><span data-ttu-id="9e4eb-132">Verfügbarkeit von Attributes</span><span class="sxs-lookup"><span data-stu-id="9e4eb-132">Then Attributes is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-133"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-133"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e4eb-134">Mit Lese-/Schreibzugriff bis das <strong>TableDef</strong>-Objekt, dem das <strong>Index</strong>-Objekt angefügt wird, einem <strong>Database</strong>-Objekt angefügt wird; dann ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-134">Read/write until the <strong>TableDef</strong> object that the <strong>Index</strong> object is appended to is appended to a <strong>Database</strong> object; then the property is read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4eb-135"><strong>QueryDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-135"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e4eb-136">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-136">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-137"><strong>Recordset</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-137"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e4eb-138">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-138">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e4eb-139"><strong>Relation</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-139"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e4eb-140">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-140">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e4eb-141"><strong>TableDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e4eb-141"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="9e4eb-142">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="9e4eb-142">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9e4eb-p104">Wenn Sie mehrere Attribute festlegen, können Sie sie kombinieren, indem Sie die entsprechenden Konstanten addieren. Ungültige Werte werden ohne Auftreten eines Fehlers ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-p104">When you set multiple attributes, you can combine them by summing the appropriate constants. Any invalid values are ignored without producing an error.</span></span>

## <a name="example"></a><span data-ttu-id="9e4eb-145">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9e4eb-145">Example</span></span>

<span data-ttu-id="9e4eb-146">Dieses Beispiel zeigt die **Attributes**-Eigenschaft für die Objekte **Field2**, **Relation** und **TableDef** in der Nordwind-Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="9e4eb-146">This example displays the **Attributes** property for **Field2**, **Relation**, and **TableDef** objects in the Northwind database.</span></span>

```vb 
Sub AttributesX() 
 
 Dim dbsNorthwind As Database 
 Dim fldLoop As Field2 
 Dim relLoop As Relation 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 
 ' Display the attributes of a TableDef object's 
 ' fields. 
 Debug.Print "Attributes of fields in " & _ 
 .TableDefs(0).Name & " table:" 
 For Each fldLoop In .TableDefs(0).Fields 
 Debug.Print " " & fldLoop.Name & " = " & _ 
 fldLoop.Attributes 
 Next fldLoop 
 
 ' Display the attributes of the Northwind database's 
 ' relations. 
 Debug.Print "Attributes of relations in " & _ 
 .Name & ":" 
 For Each relLoop In .Relations 
 Debug.Print " " & relLoop.Name & " = " & _ 
 relLoop.Attributes 
 Next relLoop 
 
 ' Display the attributes of the Northwind database's 
 ' tables. 
 Debug.Print "Attributes of tables in " & .Name & ":" 
 For Each tdfloop In .TableDefs 
 Debug.Print " " & tdfloop.Name & " = " & _ 
 tdfloop.Attributes 
 Next tdfloop 
 
 .Close 
 End With 
 
End Sub 
 
```

