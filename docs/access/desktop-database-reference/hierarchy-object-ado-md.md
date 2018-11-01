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
# <a name="hierarchy-object-ado-md"></a>Hierarchy-Objekt (ADO MD)


**Betrifft**: Access 2013, Office 2013

Stellt eine Möglichkeit dar, die Elemente einer [Dimension](dimension-object-ado-md.md) zu aggregieren (Rollup). Eine Dimension kann entlang einer oder mehrerer Hierarchien aggregiert werden.

## <a name="remarks"></a>Hinweise

Die Auflistungen und Eigenschaften eines **Hierarchy** -Objekts ermöglichen Folgendes:

  - Identifizieren der**** Hierarchie, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.

  - Zurückgeben einer sinnvollen Zeichenfolge, die die**** Hierarchie beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben der [Level](level-object-ado-md.md)-Objekte, die die**** Hierarchie bilden, indem Sie die [Levels](levels-collection-ado-md.md)-Auflistung verwenden.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Hierarchy** -Objekt abzurufen.

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
<td><p>Member</p></td>
<td><p>Das Element auf der höchsten Rollupebene in der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>Katalogname</p></td>
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
<td><p>HierarchyName</p></td>
<td><p>Der Name der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Der eindeutige Name der Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

