---
title: Relation.Table Property (DAO)
TOCTitle: Table Property
ms:assetid: cc4f64ef-c4e9-1a14-9263-5f8220d89840
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834423(v=office.15)
ms:contentKeyID: 48547736
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053068
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bdc58837cea3f54e46a3e805523e77c27cb21e7c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870828"
---
# <a name="relationtable-property-dao"></a><span data-ttu-id="98e8d-102">Relation.Table Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="98e8d-102">Relation.Table Property (DAO)</span></span>


<span data-ttu-id="98e8d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="98e8d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="98e8d-p101">Gibt den Namen der Primärtabelle eines **[Relation](relation-object-dao.md)** -Objekts an. Dieser Name sollte mit dem Wert der **[Name](connection-name-property-dao.md)** -Eigenschaft eines **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts übereinstimmen (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="98e8d-p101">Indicates the name of a **[Relation](relation-object-dao.md)** object's primary table. This should be equal to the **[Name](connection-name-property-dao.md)** property setting of a **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="98e8d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="98e8d-106">Syntax</span></span>

<span data-ttu-id="98e8d-107">*Ausdruck* . Tabelle</span><span class="sxs-lookup"><span data-stu-id="98e8d-107">*expression* .Table</span></span>

<span data-ttu-id="98e8d-108">*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="98e8d-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98e8d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98e8d-109">Remarks</span></span>

<span data-ttu-id="98e8d-110">Ein neues **Relation**-Objekt, das noch an keine Auflistung angefügt wurde, hat Lese-/Schreibzugriff auf den Wert der **Table**-Eigenschaft. Für ein vorhandenes **Relation**-Objekt in einer **[Relations](relations-collection-dao.md)** -Auflistung ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="98e8d-110">The **Table** property setting is read/write for a new **Relation** object not yet appended to a collection and read-only for an existing **Relation** object in a **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="98e8d-p102">Verwenden Sie die **Table**-Eigenschaft zusammen mit der **[ForeignTable](relation-foreigntable-property-dao.md)** -Eigenschaft, um ein **Relation**-Objekt zu definieren, das die Beziehung zwischen Feldern in zwei Tabellen oder Abfragen darstellt. Legen Sie die **Table**-Eigenschaft auf den Wert der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts der Primärtabelle fest und die **ForeignTable**-Eigenschaft auf den Wert der **Name**-Eigenschaft des verweisenden **TableDef**- oder **QueryDef**-Objekts der Fremdtabelle. Die **[Attributes](field-attributes-property-dao.md)** -Eigenschaft bestimmt den Typ der Beziehung zwischen den beiden Objekten.</span><span class="sxs-lookup"><span data-stu-id="98e8d-p102">Use the **Table** property with the **[ForeignTable](relation-foreigntable-property-dao.md)** property to define a **Relation** object, which represents the relationship between fields in two tables or queries. Set the **Table** property to the **Name** property setting of the primary **TableDef** or **QueryDef** object, and set the **ForeignTable** property to the **Name** property setting of the foreign (referencing) **TableDef** or **QueryDef** object. The **[Attributes](field-attributes-property-dao.md)** property determines the type of relationship between the two objects.</span></span>

<span data-ttu-id="98e8d-p103">Wenn Sie z. B. eine Liste gültiger Teilecodes (in einem Feld namens PartNo) in der Tabelle ValidParts gespeichert haben, könnten Sie eine 1:n-Beziehung mit einer Tabelle namens OrderItem einrichten. Wenn ein Teilecode in die Tabelle OrderItem eingegeben wird, muss dieser bereits in der Tabelle ValidParts vorhanden sein. Wenn der Teilecode in der Tabelle ValidParts nicht vorhanden ist und Sie die Attributes-Eigenschaft des Relation-Objekts nicht auf den Wert dbRelationDontEnforce festgelegt haben, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="98e8d-p103">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a one-to-many relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **Attributes** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="98e8d-p104">In diesem Fall ist die Tabelle ValidParts die Primärtabelle, sodass die Table-Eigenschaft des Relation-Objekts auf den Wert ValidParts und die ForeignTable-Eigenschaft des Relation-Objekts auf OrderItem festgelegt wird. Die Eigenschaften Name und ForeignName des Field-Objekts in der Fields-Auflistung des Relation-Objekts werden dann auf PartNo gesetzt.</span><span class="sxs-lookup"><span data-stu-id="98e8d-p104">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem. The **Name** and **ForeignName** properties of the **[Field](field-object-dao.md)** object in the **Relation** object's **[Fields](fields-collection-dao.md)** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="98e8d-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="98e8d-118">Example</span></span>

<span data-ttu-id="98e8d-119">Dieses Beispiel zeigt, wie die Eigenschaften **Table**, **ForeignTable** und **ForeignName** die Bedingungen eines **Relation**-Objekts zwischen zwei Tabellen definieren.</span><span class="sxs-lookup"><span data-stu-id="98e8d-119">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
