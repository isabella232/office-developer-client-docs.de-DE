---
title: Member-Objekt (ADO MD)
TOCTitle: Member Object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: caa3bd6e36c26864e263653cc63a85d35d2d1232
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475078"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="353fb-102">Member-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="353fb-102">Member Object (ADO MD)</span></span>


<span data-ttu-id="353fb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="353fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="353fb-104">Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.</span><span class="sxs-lookup"><span data-stu-id="353fb-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="353fb-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="353fb-105">Remarks</span></span>

<span data-ttu-id="353fb-p101">Die Eigenschaften eines\*\*\*\* Elements unterscheiden sich je nach Kontext. Ein\*\*\*\* Element einer [Ebene](level-object-ado-md.md) in einem [CubeDef](cubedef-object-ado-md.md)-Objekt besitzt eine [Children](children-property-ado-md.md)-Eigenschaft, die die\*\*\*\* Elemente der nächstniedrigeren Ebene in der Hierarchie in Bezug auf das aktuelle **Member**-Objekt zurückgibt. Die **Children**-Auflistung für das\*\*\*\* Element einer [Position](position-object-ado-md.md) ist immer leer. Die [Type](type-property-ado-md.md)-Eigenschaft gilt nur für\*\*\*\* Elemente einer\*\*\*\* Ebene.</span><span class="sxs-lookup"><span data-stu-id="353fb-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="353fb-p102">Das **Member**-Objekt einer\*\*\*\* Position hat zwei Eigenschaften ([DrilledDown](drilleddown-property-ado-md.md) und [ParentSameAsPrev](parentsameasprev-property-ado-md.md)), die zum Anzeigen der [Zellmenge](cellset-object-ado-md.md) verwendet werden. Wenn auf diese Eigenschaften für das **Member**-Objekt einer\*\*\*\* Ebene zugegriffen wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="353fb-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="353fb-112">Die Auflistungen und Eigenschaften des **Member**-Objekts einer Ebene\*\*\*\* ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="353fb-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="353fb-113">Identifizieren des\*\*\*\* Elements, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="353fb-114">Zurückgeben einer Zeichenfolge, die zum Anzeigen des\*\*\*\* Elements verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-115">Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-116">Bestimmen der Art des\*\*\*\* Elements, indem Sie die [Type](type-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-117">Abrufen von Informationen zur\*\*\*\* Ebene des\*\*\*\* Elements, indem Sie die Eigenschaften [LevelDepth](leveldepth-property-ado-md.md) und [LevelName](levelname-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="353fb-118">Abrufen verwandter\*\*\*\* Elemente in einer [Hierarchie](hierarchy-object-ado-md.md), indem Sie die Eigenschaften [Parent](parent-property-ado-md.md) und [Children](children-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="353fb-119">Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-120">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="353fb-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="353fb-121">Die Auflistungen und Eigenschaften des **Member**-Objekts einer\*\*\*\* Position an der [Achse](axis-object-ado-md.md) ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="353fb-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="353fb-122">Identifizieren des\*\*\*\* Elements, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="353fb-123">Zurückgeben einer Zeichenfolge, die zum Anzeigen des\*\*\*\* Elements verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-124">Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-125">Abrufen von Informationen zur\*\*\*\* Ebene des\*\*\*\* Elements, indem Sie die Eigenschaften [LevelDepth](leveldepth-property-ado-md.md) und [LevelName](levelname-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="353fb-126">Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="353fb-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="353fb-127">Verwenden der [DrilledDown](drilleddown-property-ado-md.md)-Eigenschaft, um zu bestimmen, ob sich mindestens ein untergeordnetes Element in direkter Folge des aktuellen\*\*\*\* Elements auf der\*\*\*\* Achse befindet.</span><span class="sxs-lookup"><span data-stu-id="353fb-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="353fb-128">Verwenden der [ParentSameAsPrev](parentsameasprev-property-ado-md.md)-Eigenschaft, um zu ermitteln, ob das übergeordnete Element dieses **Member** -Objekts mit dem übergeordneten Element des unmittelbar vorhergehenden **Member** -Objekts identisch ist.</span><span class="sxs-lookup"><span data-stu-id="353fb-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="353fb-129">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="353fb-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="353fb-p103">Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="353fb-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="353fb-134">Name</span><span class="sxs-lookup"><span data-stu-id="353fb-134">Name</span></span></p></th>
<th><p><span data-ttu-id="353fb-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="353fb-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="353fb-136">Katalogname</span><span class="sxs-lookup"><span data-stu-id="353fb-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="353fb-137">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="353fb-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="353fb-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="353fb-139">Die Anzahl der untergeordneten Elemente des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-140">CubeName</span><span class="sxs-lookup"><span data-stu-id="353fb-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="353fb-141">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="353fb-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-142">Description</span><span class="sxs-lookup"><span data-stu-id="353fb-142">Description</span></span></p></td>
<td><p><span data-ttu-id="353fb-143">Eine sinnvolle Beschreibung des Member-Objekts (Elements).</span><span class="sxs-lookup"><span data-stu-id="353fb-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="353fb-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="353fb-145">Der eindeutige Name der <a href="dimension-object-ado-md.md">Dimension</a>.</span><span class="sxs-lookup"><span data-stu-id="353fb-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="353fb-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="353fb-147">Der eindeutige Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="353fb-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="353fb-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="353fb-149">Der Abstand zwischen der Ebene und dem Stamm der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="353fb-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="353fb-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="353fb-151">Der eindeutige Name der Ebene.</span><span class="sxs-lookup"><span data-stu-id="353fb-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="353fb-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="353fb-153">Eine dem Element zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="353fb-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="353fb-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="353fb-155">Die GUID des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-156">MemberName</span><span class="sxs-lookup"><span data-stu-id="353fb-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="353fb-157">Der Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="353fb-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="353fb-159">Die Ordnungszahl des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="353fb-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="353fb-161">Der Typ des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="353fb-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="353fb-163">Der eindeutige Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="353fb-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="353fb-165">Die Anzahl der übergeordneten Elemente des Elements.</span><span class="sxs-lookup"><span data-stu-id="353fb-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="353fb-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="353fb-167">Die Ebenennummer des Elements, das dem Element übergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="353fb-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="353fb-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="353fb-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="353fb-169">Der eindeutige Name des Elements, das dem Element übergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="353fb-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="353fb-170">SchemaName</span><span class="sxs-lookup"><span data-stu-id="353fb-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="353fb-171">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="353fb-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

