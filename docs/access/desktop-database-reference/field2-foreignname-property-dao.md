---
title: Field2. ForeignName-Eigenschaft (DAO)
TOCTitle: ForeignName Property
ms:assetid: 76da233a-efb4-63cd-a2a2-d18d9e2fb2fb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196027(v=office.15)
ms:contentKeyID: 48545708
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052932
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a8368165f73fc52c51cf1503da9c2cc02e969bf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292811"
---
# <a name="field2foreignname-property-dao"></a><span data-ttu-id="42a8f-102">Field2. ForeignName-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="42a8f-102">Field2.ForeignName property (DAO)</span></span>


<span data-ttu-id="42a8f-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42a8f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42a8f-104">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Namen des **Field2**-Objekts in einer Fremdtabelle angibt, das einem Feld in einer Primärtabelle für eine Beziehung entspricht (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="42a8f-104">Sets or returns a value that specifies the name of the **Field2** object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="42a8f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="42a8f-105">Syntax</span></span>

<span data-ttu-id="42a8f-106">*Ausdruck* . ForeignName</span><span class="sxs-lookup"><span data-stu-id="42a8f-106">*expression* .ForeignName</span></span>

<span data-ttu-id="42a8f-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="42a8f-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="42a8f-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42a8f-108">Remarks</span></span>

<span data-ttu-id="42a8f-p101">Wenn das **[Relation](relation-object-dao.md)** -Objekt nicht dem **[Database](database-object-dao.md)** -Objekt sondern das **Field2**-Objekt dem **Relation**-Objekt angefügt wird, ist die **ForeignName**-Eigenschaft nicht schreibgeschützt. Sobald das **Relation**-Objekt der Datenbank angefügt wurde, ist die **ForeignName**-Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="42a8f-p101">If the **[Relation](relation-object-dao.md)** object isn't appended to the **[Database](database-object-dao.md)**, but the **Field2** is appended to the **Relation** object, the **ForeignName** property is read/write. Once the **Relation** object is appended to the database, the **ForeignName** property is read-only.</span></span>

<span data-ttu-id="42a8f-111">Nur ein **Field2**-Objekt, das zur **Fields**-Auflistung eines **Relation**-Objekts gehört, kann die **ForeignName**-Eigenschaft unterstützten.</span><span class="sxs-lookup"><span data-stu-id="42a8f-111">Only a **Field2** object that belongs to the **Fields** collection of a **Relation** object can support the **ForeignName** property.</span></span>

<span data-ttu-id="42a8f-p102">Die Einstellungen der Eigenschaften **[Name](connection-name-property-dao.md)** und **ForeignName** für ein **Field2**-Objekt geben die Namen der entsprechenden Felder in den Primär- und Fremdtabellen einer Beziehung an. Die Einstellungen der Eigenschaften **[Table](relation-table-property-dao.md)** und **[ForeignTable](relation-foreigntable-property-dao.md)** für ein **Relation**-Objekt bestimmen die Primär- und Fremdtabellen einer Beziehung.</span><span class="sxs-lookup"><span data-stu-id="42a8f-p102">The **[Name](connection-name-property-dao.md)** and **ForeignName** property settings for a **Field2** object specify the names of the corresponding fields in the primary and foreign tables of a relationship. The **[Table](relation-table-property-dao.md)** and **[ForeignTable](relation-foreigntable-property-dao.md)** property settings for a **Relation** object determine the primary and foreign tables of a relationship.</span></span>

<span data-ttu-id="42a8f-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span><span class="sxs-lookup"><span data-stu-id="42a8f-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already exist in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="42a8f-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field2** object in the **Relation** object's **Fields** collection would be set to PartNo.</span><span class="sxs-lookup"><span data-stu-id="42a8f-p104">In this case, the ValidParts table is the foreign table, so the **ForeignTable** property of the **Relation** object would be set to ValidParts and the **Table** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **Field2** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="42a8f-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="42a8f-118">Example</span></span>

<span data-ttu-id="42a8f-119">In diesem Beispiel wird gezeigt, wie die Eigenschaften **Table**, **ForeignTable** und **ForeignName** die Beziehungen eines **Relation**-Objekts zwischen zwei Tabellen definieren.</span><span class="sxs-lookup"><span data-stu-id="42a8f-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

```vb
    Sub ForeignNameX() 
     
     Dim dbsNorthwind As Database 
     Dim relLoop As Relation 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     Debug.Print "Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print ".Table - .Fields(0).Name" 
     Debug.Print " Foreign (Many) "; 
     Debug.Print ".ForeignTable - .Fields(0).ForeignName" 
     
     ' Enumerate the Relations collection of the Northwind 
     ' database to report on the property values of 
     ' the Relation objects and their Field objects. 
     For Each relLoop In dbsNorthwind.Relations 
     With relLoop 
     Debug.Print 
     Debug.Print .Name & " Relation" 
     Debug.Print " Table - Field" 
     Debug.Print " Primary (One) "; 
     Debug.Print .Table & " - " & .Fields(0).Name 
     Debug.Print " Foreign (Many) "; 
     Debug.Print .ForeignTable & " - " & _ 
     .Fields(0).ForeignName 
     End With 
     Next relLoop 
     
     dbsNorthwind.Close 
     
    End Sub
```
