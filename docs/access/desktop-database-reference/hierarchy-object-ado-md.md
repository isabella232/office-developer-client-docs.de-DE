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
# <a name="hierarchy-object-ado-md"></a>Hierarchy-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt eine Möglichkeit dar, die Elemente einer [Dimension](dimension-object-ado-md.md) zu aggregieren (Rollup). Eine Dimension kann entlang einer oder mehrerer Hierarchien aggregiert werden.

## <a name="remarks"></a>Bemerkungen

Die Auflistungen und Eigenschaften eines **Hierarchy**-Objekts ermöglichen Folgendes:

  - Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.

  - Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.

  - Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Hierarchy** -Objekt abzurufen.

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
<td><p>AllMember</p></td>
<td><p>Das Element auf der höchsten Rollupebene in der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>CatalogName</p></td>
<td><p>Der Name des Katalogs, zu dem dieser Cube gehört.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Der eindeutige Name des Standardelements für diese Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>Beschreibung</p></td>
<td><p>Eine sinnvolle Beschreibung der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Der Typ der Dimension, zu der diese Hierarchie gehört.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Der eindeutige Name der Dimension.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Eine der Hierarchie zugeordnete Beschriftung.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>Die Anzahl der Elemente in der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>Die GUID der Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>Hierarchie</p></td>
<td><p>Der Name der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Der eindeutige Name der Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>Instanzschema</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

