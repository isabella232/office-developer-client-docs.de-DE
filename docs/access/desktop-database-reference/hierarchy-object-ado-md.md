---
title: Hierarchy-Objekt (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad6eb40873d0cd88b441adaa5568ad57dced83c6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869785"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="4a777-102">Hierarchy-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4a777-102">Hierarchy Object (ADO MD)</span></span>


<span data-ttu-id="4a777-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a777-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a777-p101">Stellt eine Möglichkeit dar, die Elemente einer [Dimension](dimension-object-ado-md.md) zu aggregieren (Rollup). Eine Dimension kann entlang einer oder mehrerer Hierarchien aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a777-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a777-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4a777-106">Remarks</span></span>

<span data-ttu-id="4a777-107">Die Auflistungen und Eigenschaften eines **Hierarchy** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4a777-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="4a777-108">Identifizieren der\*\*\*\* Hierarchie, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a777-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="4a777-109">Zurückgeben einer sinnvollen Zeichenfolge, die die\*\*\*\* Hierarchie beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a777-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4a777-110">Zurückgeben der [Level](level-object-ado-md.md)-Objekte, die die\*\*\*\* Hierarchie bilden, indem Sie die [Levels](levels-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a777-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="4a777-111">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Hierarchy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4a777-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="4a777-p102">Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="4a777-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4a777-116">Name</span><span class="sxs-lookup"><span data-stu-id="4a777-116">Name</span></span></p></th>
<th><p><span data-ttu-id="4a777-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a777-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a777-118">Member</span><span class="sxs-lookup"><span data-stu-id="4a777-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="4a777-119">Das Element auf der höchsten Rollupebene in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-120">Katalogname</span><span class="sxs-lookup"><span data-stu-id="4a777-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="4a777-121">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="4a777-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-122">CubeName</span><span class="sxs-lookup"><span data-stu-id="4a777-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="4a777-123">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="4a777-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="4a777-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="4a777-125">Der eindeutige Name des Standardelements für diese Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4a777-126">Description</span></span></p></td>
<td><p><span data-ttu-id="4a777-127">Eine sinnvolle Beschreibung der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="4a777-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="4a777-129">Der Typ der Dimension, zu der diese Hierarchie gehört.</span><span class="sxs-lookup"><span data-stu-id="4a777-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="4a777-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="4a777-131">Der eindeutige Name der Dimension.</span><span class="sxs-lookup"><span data-stu-id="4a777-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="4a777-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="4a777-133">Eine der Hierarchie zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="4a777-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="4a777-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="4a777-135">Die Anzahl der Elemente in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="4a777-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="4a777-137">Die GUID der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="4a777-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="4a777-139">Der Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a777-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="4a777-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="4a777-141">Der eindeutige Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="4a777-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4a777-142">SchemaName</span><span class="sxs-lookup"><span data-stu-id="4a777-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="4a777-143">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="4a777-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

