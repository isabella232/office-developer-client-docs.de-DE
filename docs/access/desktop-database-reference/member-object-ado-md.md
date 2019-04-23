---
title: Member-Objekt (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289422"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="fa712-102">Member-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fa712-102">Member object (ADO MD)</span></span>


<span data-ttu-id="fa712-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa712-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa712-104">Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.</span><span class="sxs-lookup"><span data-stu-id="fa712-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa712-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa712-105">Remarks</span></span>

<span data-ttu-id="fa712-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span><span class="sxs-lookup"><span data-stu-id="fa712-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="fa712-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span><span class="sxs-lookup"><span data-stu-id="fa712-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="fa712-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span><span class="sxs-lookup"><span data-stu-id="fa712-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="fa712-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="fa712-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fa712-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="fa712-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-115">Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa712-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="fa712-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="fa712-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fa712-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="fa712-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fa712-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="fa712-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-120">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fa712-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="fa712-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span><span class="sxs-lookup"><span data-stu-id="fa712-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="fa712-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="fa712-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fa712-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="fa712-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-124">Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa712-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="fa712-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="fa712-126">Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="fa712-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="fa712-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span><span class="sxs-lookup"><span data-stu-id="fa712-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="fa712-128">Verwenden der [ParentSameAsPrev](parentsameasprev-property-ado-md.md)-Eigenschaft, um zu ermitteln, ob das übergeordnete Element dieses **Member** -Objekts mit dem übergeordneten Element des unmittelbar vorhergehenden **Member** -Objekts identisch ist.</span><span class="sxs-lookup"><span data-stu-id="fa712-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="fa712-129">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level**-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fa712-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="fa712-p103">Die **Properties**-Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="fa712-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fa712-134">Name</span><span class="sxs-lookup"><span data-stu-id="fa712-134">Name</span></span></p></th>
<th><p><span data-ttu-id="fa712-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa712-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fa712-136">CatalogName</span><span class="sxs-lookup"><span data-stu-id="fa712-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="fa712-137">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="fa712-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="fa712-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="fa712-139">Die Anzahl der untergeordneten Elemente des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-140">CubeName</span><span class="sxs-lookup"><span data-stu-id="fa712-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="fa712-141">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="fa712-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa712-142">Description</span></span></p></td>
<td><p><span data-ttu-id="fa712-143">Eine sinnvolle Beschreibung des Member-Objekts (Elements).</span><span class="sxs-lookup"><span data-stu-id="fa712-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="fa712-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fa712-145">Der eindeutige Name der <a href="dimension-object-ado-md.md">Dimension</a>.</span><span class="sxs-lookup"><span data-stu-id="fa712-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="fa712-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fa712-147">Der eindeutige Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="fa712-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="fa712-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="fa712-149">Der Abstand zwischen der Ebene und dem Stamm der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="fa712-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="fa712-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fa712-151">Der eindeutige Name der Ebene.</span><span class="sxs-lookup"><span data-stu-id="fa712-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="fa712-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="fa712-153">Eine dem Element zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="fa712-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="fa712-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="fa712-155">Die GUID des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-156">MemberName</span><span class="sxs-lookup"><span data-stu-id="fa712-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="fa712-157">Der Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="fa712-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="fa712-159">Die Ordnungszahl des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="fa712-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="fa712-161">Der Typ des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="fa712-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fa712-163">Der eindeutige Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="fa712-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="fa712-165">Die Anzahl der übergeordneten Elemente des Elements.</span><span class="sxs-lookup"><span data-stu-id="fa712-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="fa712-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="fa712-167">Die Ebenennummer des Elements, das dem Element übergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa712-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fa712-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="fa712-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="fa712-169">Der eindeutige Name des Elements, das dem Element übergeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa712-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fa712-170">Instanzschema</span><span class="sxs-lookup"><span data-stu-id="fa712-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="fa712-171">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="fa712-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

