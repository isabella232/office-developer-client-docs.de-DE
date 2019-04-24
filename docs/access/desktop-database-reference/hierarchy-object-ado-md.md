---
title: Hierarchy-Objekt (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291929"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="1a6fa-102">Hierarchy-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="1a6fa-102">Hierarchy object (ADO MD)</span></span>


<span data-ttu-id="1a6fa-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a6fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a6fa-p101">Stellt eine Möglichkeit dar, die Elemente einer [Dimension](dimension-object-ado-md.md) zu aggregieren (Rollup). Eine Dimension kann entlang einer oder mehrerer Hierarchien aggregiert werden.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a6fa-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a6fa-106">Remarks</span></span>

<span data-ttu-id="1a6fa-107">Die Auflistungen und Eigenschaften eines **Hierarchy**-Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1a6fa-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="1a6fa-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="1a6fa-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="1a6fa-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="1a6fa-111">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Hierarchy** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="1a6fa-p102">Die **Properties**-Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1a6fa-116">Name</span><span class="sxs-lookup"><span data-stu-id="1a6fa-116">Name</span></span></p></th>
<th><p><span data-ttu-id="1a6fa-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a6fa-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="1a6fa-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-119">Das Element auf der höchsten Rollupebene in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-120">CatalogName</span><span class="sxs-lookup"><span data-stu-id="1a6fa-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-121">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-122">CubeName</span><span class="sxs-lookup"><span data-stu-id="1a6fa-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-123">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-124">DefaultMember</span><span class="sxs-lookup"><span data-stu-id="1a6fa-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-125">Der eindeutige Name des Standardelements für diese Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a6fa-126">Description</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-127">Eine sinnvolle Beschreibung der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="1a6fa-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-129">Der Typ der Dimension, zu der diese Hierarchie gehört.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="1a6fa-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-131">Der eindeutige Name der Dimension.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="1a6fa-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-133">Eine der Hierarchie zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="1a6fa-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-135">Die Anzahl der Elemente in der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="1a6fa-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-137">Die GUID der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-138">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="1a6fa-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-139">Der Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1a6fa-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="1a6fa-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-141">Der eindeutige Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1a6fa-142">Instanzschema</span><span class="sxs-lookup"><span data-stu-id="1a6fa-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="1a6fa-143">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="1a6fa-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

