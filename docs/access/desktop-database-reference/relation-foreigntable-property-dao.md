---
title: Relation.ForeignTable-Eigenschaft (DAO)
TOCTitle: ForeignTable Property
ms:assetid: 3f896433-2962-1c7c-f5a2-4e030ba8d4a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192853(v=office.15)
ms:contentKeyID: 48544401
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052989
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fc7ee9b5bc832cc2a125024c592db2c7b13e72f7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718973"
---
# <a name="relationforeigntable-property-dao"></a><span data-ttu-id="cbc0c-102">Relation.ForeignTable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="cbc0c-102">Relation.ForeignTable property (DAO)</span></span>


<span data-ttu-id="cbc0c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbc0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbc0c-p101">Legt den Namen der Fremdtabelle in einer Beziehung fest oder gibt den Namen zurück (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="cbc0c-p101">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc0c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc0c-106">Syntax</span></span>

<span data-ttu-id="cbc0c-107">*Ausdruck* . ForeignTable</span><span class="sxs-lookup"><span data-stu-id="cbc0c-107">*expression* .ForeignTable</span></span>

<span data-ttu-id="cbc0c-108">*Ausdruck* Eine Variable, die ein **Relation** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-108">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc0c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cbc0c-109">Remarks</span></span>

<span data-ttu-id="cbc0c-110">Für diese Eigenschaft besteht bei einem neuen **[Relation](relation-object-dao.md)** -Objekt, das noch keiner Auflistung angefügt wurde, Lese-/Schreibzugriff, und bei einem vorhandenen **Relation**-Objekt in der **[Relations](relations-collection-dao.md)** -Auflistung ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-110">This property is read/write for a new **[Relation](relation-object-dao.md)** object not yet appended to a collection and read-only for an existing **Relation** object in the **[Relations](relations-collection-dao.md)** collection.</span></span>

<span data-ttu-id="cbc0c-111">Die Einstellung der **ForeignTable**-Eigenschaft eines **Relation**-Objekts ist die Einstellung der **[Name](connection-name-property-dao.md)** -Eigenschaft des **[TableDef](tabledef-object-dao.md)** - oder **[QueryDef](querydef-object-dao.md)** -Objekts, das die Fremdtabelle oder Abfrage darstellt. Die Einstellung der **[Table](relation-table-property-dao.md)** -Eigenschaft ist die Einstellung der **Name**-Eigenschaft des **TableDef**- oder **QueryDef**-Objekts, das die Primärtabelle oder Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-111">The **ForeignTable** property setting of a **Relation** object is the **[Name](connection-name-property-dao.md)** property setting of the **[TableDef](tabledef-object-dao.md)** or **[QueryDef](querydef-object-dao.md)** object that represents the foreign table or query; the **[Table](relation-table-property-dao.md)** property setting is the **Name** property setting of the **TableDef** or **QueryDef** object that represents the primary table or query.</span></span>

<span data-ttu-id="cbc0c-p102">Angenommen, Sie besitzen eine Liste mit gültigen Artikelcodes (in einem Feld namens Artikelnr) in einer GültigeArtikel-Tabelle. Sie können dann eine Beziehung zu einer Bestellelement-Tabelle erstellen, sodass ein Artikelcode, der in der Bestellelement-Tabelle eingegeben wird, bereits in der GültigeArtikel-Tabelle vorhanden sein muss. Ist der Artikelcode nicht in der GültigeArtikel-Tabelle vorhanden, und Sie legen die Attributes-Eigenschaft des Relation-Objekts nicht auf dbRelationDontEnforce fest, tritt ein abfangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-p102">For example, if you had a list of valid part codes (in a field named PartNo) stored in a ValidParts table, you could establish a relationship with an OrderItem table such that if a part code were entered into the OrderItem table, it would have to already be in the ValidParts table. If the part code didn't exist in the ValidParts table and you had not set the **[Attributes](field-attributes-property-dao.md)** property of the **Relation** object to **dbRelationDontEnforce**, a trappable error would occur.</span></span>

<span data-ttu-id="cbc0c-114">In diesem Fall ist die Tabelle Artikel der Primärtabelle, damit die **Table** -Eigenschaft des **Relation** -Objekts auf Artikel fest und "Bestellung" die **ForeignTable** -Eigenschaft des **Relation** -Objekts festgelegt werden würde.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-114">In this case, the ValidParts table is the primary table, so the **Table** property of the **Relation** object would be set to ValidParts and the **ForeignTable** property of the **Relation** object would be set to OrderItem.</span></span> <span data-ttu-id="cbc0c-115">PartNo würde die Eigenschaften **Name** und **ForeignName** des **Field** -Objekts in **Fields** -Auflistung für das **Relation** -Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-115">The **Name** and **ForeignName** properties of the **Field** object in the **Relation** object's **Fields** collection would be set to PartNo.</span></span>

## <a name="example"></a><span data-ttu-id="cbc0c-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cbc0c-116">Example</span></span>

<span data-ttu-id="cbc0c-117">Dieses Beispiel zeigt, wie die Eigenschaften **Table**, **ForeignTable** und **ForeignName** die Bedingungen eines **Relation**-Objekts zwischen zwei Tabellen definieren.</span><span class="sxs-lookup"><span data-stu-id="cbc0c-117">This example shows how the **Table**, **ForeignTable**, and **ForeignName** properties define the terms of a **Relation** between two tables.</span></span>

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
