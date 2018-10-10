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
# <a name="dimension-object-ado-md"></a>Dimension-Objekt (ADO MD)


**Betrifft**: Access 2013 | Office 2013

Stellt eine der Dimensionen eines multidimensionalen Cubes dar, der eine oder mehrere Elementhierarchien enthält.

## <a name="remarks"></a>Hinweise

Die Auflistungen und Eigenschaften eines **Dimension** -Objekts ermöglichen Folgendes:

  - Identifizieren der**** Dimension, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.

  - Zurückgeben einer sinnvollen Zeichenfolge, die die**** Dimension beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben der [Hierarchy](hierarchy-object-ado-md.md)-Objekte, die die**** Dimension bilden, indem Sie die [Hierarchies](hierarchies-collection-ado-md.md)-Auflistung verwenden.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Dimension** -Objekt abzurufen.

Die **Properties** -Auflistung enthält Eigenschaften, die vom Anbieter bereitgestellt werden. In der folgenden Tabelle sind Eigenschaften aufgeführt, die möglicherweise verfügbar sind. Die tatsächliche Eigenschaftenliste kann je nach Anbieterimplementierung davon abweichen. Eine ausführlichere Liste mit verfügbaren Eigenschaften finden Sie in Ihrer Anbieterdokumentation.

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
<td><p>Katalogname</p></td>
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
<td><p>SchemaName</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>
