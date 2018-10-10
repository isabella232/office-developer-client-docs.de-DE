---
title: Dimension-Objekt (ADO MD)
TOCTitle: Dimension Object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15ae89905c9ca82c4c41701c4ed713c02722e322
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472693"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="5e001-102">Dimension-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5e001-102">Dimension Object (ADO MD)</span></span>


<span data-ttu-id="5e001-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="5e001-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5e001-104">Stellt eine der Dimensionen eines multidimensionalen Cubes dar, der eine oder mehrere Elementhierarchien enthält.</span><span class="sxs-lookup"><span data-stu-id="5e001-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e001-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e001-105">Remarks</span></span>

<span data-ttu-id="5e001-106">Die Auflistungen und Eigenschaften eines **Dimension** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5e001-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="5e001-107">Identifizieren der\*\*\*\* Dimension, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e001-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5e001-108">Zurückgeben einer sinnvollen Zeichenfolge, die die\*\*\*\* Dimension beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e001-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5e001-109">Zurückgeben der [Hierarchy](hierarchy-object-ado-md.md)-Objekte, die die\*\*\*\* Dimension bilden, indem Sie die [Hierarchies](hierarchies-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5e001-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="5e001-110">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Dimension** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5e001-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="5e001-p101">Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5e001-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e001-115">Name</span><span class="sxs-lookup"><span data-stu-id="5e001-115">Name</span></span></p></th>
<th><p><span data-ttu-id="5e001-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e001-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e001-117">Katalogname</span><span class="sxs-lookup"><span data-stu-id="5e001-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="5e001-118">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="5e001-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-119">CubeName</span><span class="sxs-lookup"><span data-stu-id="5e001-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="5e001-120">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="5e001-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e001-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="5e001-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="5e001-122">Der eindeutige Name der Standardhierarchie.</span><span class="sxs-lookup"><span data-stu-id="5e001-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e001-123">Description</span></span></p></td>
<td><p><span data-ttu-id="5e001-124">Eine sinnvolle Beschreibung des Cubes.</span><span class="sxs-lookup"><span data-stu-id="5e001-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e001-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="5e001-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="5e001-126">Eine der Dimension zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="5e001-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="5e001-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="5e001-128">Die Anzahl der Elemente in der Dimension.</span><span class="sxs-lookup"><span data-stu-id="5e001-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e001-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="5e001-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="5e001-130">Die GUID der Dimension.</span><span class="sxs-lookup"><span data-stu-id="5e001-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-131">DimensionName</span><span class="sxs-lookup"><span data-stu-id="5e001-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="5e001-132">Der Name der Dimension.</span><span class="sxs-lookup"><span data-stu-id="5e001-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e001-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="5e001-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="5e001-134">Die Ordnungszahl der Dimension in Bezug auf die Gruppe von Dimensionen, die den Cube bilden.</span><span class="sxs-lookup"><span data-stu-id="5e001-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="5e001-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="5e001-136">Der Dimensionstyp.</span><span class="sxs-lookup"><span data-stu-id="5e001-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e001-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="5e001-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5e001-138">Der eindeutige Name der Dimension.</span><span class="sxs-lookup"><span data-stu-id="5e001-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e001-139">SchemaName</span><span class="sxs-lookup"><span data-stu-id="5e001-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="5e001-140">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="5e001-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

