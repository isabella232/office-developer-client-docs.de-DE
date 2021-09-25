---
title: Member-Objekt (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 88884141e90faca4eb83168d4f2378df5a6e399a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602227"
---
# <a name="member-object-ado-md"></a>Member-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.

## <a name="remarks"></a>HinwBemerkungeneise

The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.

A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.

With the collections and properties of a **Member** object of a **Level**, you can do the following:

  - Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.

  - Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.

  - Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.

  - Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.

  - Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.

  - Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level**-Objekt abzurufen.

With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:

  - Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.

  - Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.

  - Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.

  - Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.

  - Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.

  - Verwenden der [ParentSameAsPrev](parentsameasprev-property-ado-md.md)-Eigenschaft, um zu ermitteln, ob das übergeordnete Element dieses **Member** -Objekts mit dem übergeordneten Element des unmittelbar vorhergehenden **Member** -Objekts identisch ist.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level**-Objekt abzurufen.

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
<td><p>Catalogname</p></td>
<td><p>Der Name des Katalogs, zu dem dieser Cube gehört.</p></td>
</tr>
<tr class="even">
<td><p>ChildrenCardinality</p></td>
<td><p>Die Anzahl der untergeordneten Elemente des Elements.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>Beschreibung</p></td>
<td><p>Eine sinnvolle Beschreibung des Member-Objekts (Elements).</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Der eindeutige Name der <a href="dimension-object-ado-md.md">Dimension</a>.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Der eindeutige Name der Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>Der Abstand zwischen der Ebene und dem Stamm der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Der eindeutige Name der Ebene.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Eine dem Element zugeordnete Beschriftung.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>Die GUID des Elements.</p></td>
</tr>
<tr class="odd">
<td><p>Membername</p></td>
<td><p>Der Name des Elements.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>Die Ordnungszahl des Elements.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>Der Typ des Elements.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>Der eindeutige Name des Elements.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>Die Anzahl der übergeordneten Elemente des Elements.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>Die Ebenennummer des Elements, das dem Element übergeordnet ist.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>Der eindeutige Name des Elements, das dem Element übergeordnet ist.</p></td>
</tr>
<tr class="even">
<td><p>Schemaname</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

