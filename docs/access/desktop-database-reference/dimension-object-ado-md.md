---
title: Dimension-Objekt (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293896"
---
# <a name="dimension-object-ado-md"></a>Dimension-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt eine der Dimensionen eines multidimensionalen Cubes dar, der eine oder mehrere Elementhierarchien enthält.

## <a name="remarks"></a>Bemerkungen

Die Auflistungen und Eigenschaften eines **Dimension**-Objekts ermöglichen Folgendes:

  - Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.

  - Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.

  - Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Dimension** -Objekt abzurufen.

Die **Properties**-Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CatalogName</p></td>
<td><p>Der Name des Katalogs, zu dem dieser Cube gehört.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="odd">
<td><p>DefaultHierarchy</p></td>
<td><p>Der eindeutige Name der Standardhierarchie.</p></td>
</tr>
<tr class="even">
<td><p>Beschreibung</p></td>
<td><p>Eine sinnvolle Beschreibung des Cubes.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Eine der Dimension zugeordnete Beschriftung.</p></td>
</tr>
<tr class="even">
<td><p>DimensionCardinality</p></td>
<td><p>Die Anzahl der Elemente in der Dimension.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>Die GUID der Dimension.</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>Der Name der Dimension.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>Die Ordnungszahl der Dimension in Bezug auf die Gruppe von Dimensionen, die den Cube bilden.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Der Dimensionstyp.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Der eindeutige Name der Dimension.</p></td>
</tr>
<tr class="even">
<td><p>Instanzschema</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

