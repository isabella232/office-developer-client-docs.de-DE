---
title: Level-Objekt (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290114"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="e9074-102">Level-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e9074-102">Level object (ADO MD)</span></span>


<span data-ttu-id="e9074-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9074-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9074-104">Enthält eine Gruppe von Elementen, von denen jedes denselben Rang innerhalb einer Hierarchie hat.</span><span class="sxs-lookup"><span data-stu-id="e9074-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9074-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9074-105">Remarks</span></span>

<span data-ttu-id="e9074-106">Die Auflistungen und Eigenschaften eines **Level**-Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e9074-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="e9074-107">Identifizieren der\*\*\*\* Ebene, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9074-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="e9074-108">Zurückgeben einer Zeichenfolge, die zum Anzeigen der\*\*\*\* Ebene verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9074-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e9074-109">Zurückgeben einer sinnvollen Zeichenfolge, die die\*\*\*\* Ebene beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9074-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e9074-110">Zurückgeben der [Member](member-object-ado-md.md)-Objekte, die die\*\*\*\* Ebene bilden, indem Sie die [Members](members-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9074-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="e9074-111">Zurückgeben der Anzahl von Ebenen ab dem\*\*\*\* Ebenenstamm, indem Sie die [Depth](depth-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9074-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="e9074-112">Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level**-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9074-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="e9074-p101">Die **Properties**-Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="e9074-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e9074-117">Name</span><span class="sxs-lookup"><span data-stu-id="e9074-117">Name</span></span></p></th>
<th><p><span data-ttu-id="e9074-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9074-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9074-119">CatalogName</span><span class="sxs-lookup"><span data-stu-id="e9074-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="e9074-120">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="e9074-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-121">CubeName</span><span class="sxs-lookup"><span data-stu-id="e9074-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="e9074-122">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="e9074-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9074-123">Description</span></span></p></td>
<td><p><span data-ttu-id="e9074-124">Eine sinnvolle Beschreibung der Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9074-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="e9074-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e9074-126">Der eindeutige Name der <a href="dimension-object-ado-md.md">Dimension</a>.</span><span class="sxs-lookup"><span data-stu-id="e9074-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="e9074-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e9074-128">Der eindeutige Name der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e9074-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-129">LevelCaption</span><span class="sxs-lookup"><span data-stu-id="e9074-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="e9074-130">Eine der Ebene zugeordnete Beschriftung.</span><span class="sxs-lookup"><span data-stu-id="e9074-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-131">LevelCardinality</span><span class="sxs-lookup"><span data-stu-id="e9074-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="e9074-132">Die Anzahl der Elemente in der Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9074-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-133">LevelGUID</span><span class="sxs-lookup"><span data-stu-id="e9074-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="e9074-134">Die GUID der Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9074-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="e9074-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="e9074-136">Der Name der Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9074-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-137">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="e9074-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="e9074-138">Der Abstand zwischen der Ebene und dem Stamm der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e9074-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-139">Leveltype</span><span class="sxs-lookup"><span data-stu-id="e9074-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="e9074-140">Der Ebenentyp.</span><span class="sxs-lookup"><span data-stu-id="e9074-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9074-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="e9074-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="e9074-142">Der eindeutige Name der Ebene.</span><span class="sxs-lookup"><span data-stu-id="e9074-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9074-143">Instanzschema</span><span class="sxs-lookup"><span data-stu-id="e9074-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="e9074-144">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="e9074-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

