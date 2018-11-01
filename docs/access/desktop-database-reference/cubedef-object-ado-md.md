---
title: CubeDef-Objekt (ADO MD)
TOCTitle: CubeDef Object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7dc244483c3111e6e354496f1ffbbd12f463800
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878296"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="38e6c-102">CubeDef-Objekt (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="38e6c-102">CubeDef Object (ADO MD)</span></span>


<span data-ttu-id="38e6c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38e6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38e6c-104">Stellt einen Cube aus einem multidimensionalen Schema dar, das eine Reihe verknüpfter Dimensionen enthält.</span><span class="sxs-lookup"><span data-stu-id="38e6c-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="38e6c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="38e6c-105">Remarks</span></span>

<span data-ttu-id="38e6c-106">Die Auflistungen und Eigenschaften eines **CubeDef** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="38e6c-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="38e6c-107">Identifizieren eines **CubeDef** -Objekts, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e6c-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="38e6c-108">Zurückgeben einer Zeichenfolge, die den Cube beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e6c-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="38e6c-109">Zurückgeben der Dimensionen, die den Cube bilden, indem Sie die [Dimensions](dimensions-collection-ado-md.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e6c-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="38e6c-110">Abrufen zusätzlicher Informationen zum **CubeDef** -Objekt, indem Sie die [Properties](properties-collection-ado.md)-ADO-Standardauflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="38e6c-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="38e6c-p101">Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="38e6c-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38e6c-115">Name</span><span class="sxs-lookup"><span data-stu-id="38e6c-115">Name</span></span></p></th>
<th><p><span data-ttu-id="38e6c-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38e6c-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38e6c-117">Katalogname</span><span class="sxs-lookup"><span data-stu-id="38e6c-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="38e6c-118">Der Name des Katalogs, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="38e6c-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38e6c-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="38e6c-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="38e6c-120">Datum und Uhrzeit der Cubeerstellung.</span><span class="sxs-lookup"><span data-stu-id="38e6c-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38e6c-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="38e6c-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="38e6c-122">Die GUID des Cubes.</span><span class="sxs-lookup"><span data-stu-id="38e6c-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38e6c-123">CubeName</span><span class="sxs-lookup"><span data-stu-id="38e6c-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="38e6c-124">Der Name des Cubes.</span><span class="sxs-lookup"><span data-stu-id="38e6c-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38e6c-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="38e6c-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="38e6c-126">Der Typ des Cubes.</span><span class="sxs-lookup"><span data-stu-id="38e6c-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38e6c-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="38e6c-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="38e6c-128">Benutzer-ID der Person, die die letzte Datenaktualisierung ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="38e6c-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38e6c-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="38e6c-129">Description</span></span></p></td>
<td><p><span data-ttu-id="38e6c-130">Eine sinnvolle Beschreibung des Cubes.</span><span class="sxs-lookup"><span data-stu-id="38e6c-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38e6c-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="38e6c-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="38e6c-132">Datum und Uhrzeit der letzten Schemaaktualisierung.</span><span class="sxs-lookup"><span data-stu-id="38e6c-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38e6c-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="38e6c-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="38e6c-134">Der Name des Schemas, zu dem dieser Cube gehört.</span><span class="sxs-lookup"><span data-stu-id="38e6c-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38e6c-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="38e6c-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="38e6c-136">Benutzer-ID der Person, die die letzte Schemaaktualisierung ausgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="38e6c-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

