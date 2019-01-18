---
title: Member-Objekt (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709579"
---
# <a name="member-object-ado-md"></a>Member-Objekt (ADO MD)


**Betrifft**: Access 2013, Office 2013

Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.

## <a name="remarks"></a>Hinweise

Die Eigenschaften eines**** Elements unterscheiden sich je nach Kontext. Ein**** Element einer [Ebene](level-object-ado-md.md) in einem [CubeDef](cubedef-object-ado-md.md)-Objekt besitzt eine [Children](children-property-ado-md.md)-Eigenschaft, die die**** Elemente der nächstniedrigeren Ebene in der Hierarchie in Bezug auf das aktuelle **Member**-Objekt zurückgibt. Die **Children**-Auflistung für das**** Element einer [Position](position-object-ado-md.md) ist immer leer. Die [Type](type-property-ado-md.md)-Eigenschaft gilt nur für**** Elemente einer**** Ebene.

Das **Member**-Objekt einer**** Position hat zwei Eigenschaften ([DrilledDown](drilleddown-property-ado-md.md) und [ParentSameAsPrev](parentsameasprev-property-ado-md.md)), die zum Anzeigen der [Zellmenge](cellset-object-ado-md.md) verwendet werden. Wenn auf diese Eigenschaften für das **Member**-Objekt einer**** Ebene zugegriffen wird, tritt ein Fehler auf.

Die Auflistungen und Eigenschaften des **Member**-Objekts einer Ebene**** ermöglichen Folgendes:

  - Identifizieren des**** Elements, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.

  - Zurückgeben einer Zeichenfolge, die zum Anzeigen des**** Elements verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Bestimmen der Art des**** Elements, indem Sie die [Type](type-property-ado-md.md)-Eigenschaft verwenden.

  - Abrufen von Informationen zur**** Ebene des**** Elements, indem Sie die Eigenschaften [LevelDepth](leveldepth-property-ado-md.md) und [LevelName](levelname-property-ado-md.md) verwenden.

  - Abrufen verwandter**** Elemente in einer [Hierarchie](hierarchy-object-ado-md.md), indem Sie die Eigenschaften [Parent](parent-property-ado-md.md) und [Children](children-property-ado-md.md) verwenden.

  - Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level** -Objekt abzurufen.

Die Auflistungen und Eigenschaften des **Member**-Objekts einer**** Position an der [Achse](axis-object-ado-md.md) ermöglichen Folgendes:

  - Identifizieren des**** Elements, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.

  - Zurückgeben einer Zeichenfolge, die zum Anzeigen des**** Elements verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben einer sinnvollen Zeichenfolge, die ein Measure- oder Formula- **Member** beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Abrufen von Informationen zur**** Ebene des**** Elements, indem Sie die Eigenschaften [LevelDepth](leveldepth-property-ado-md.md) und [LevelName](levelname-property-ado-md.md) verwenden.

  - Zählen der untergeordneten Elemente eines **Member** -Objekts, indem Sie die [ChildCount](childcount-property-ado-md.md)-Eigenschaft verwenden.

  - Verwenden der [DrilledDown](drilleddown-property-ado-md.md)-Eigenschaft, um zu bestimmen, ob sich mindestens ein untergeordnetes Element in direkter Folge des aktuellen**** Elements auf der**** Achse befindet.

  - Verwenden der [ParentSameAsPrev](parentsameasprev-property-ado-md.md)-Eigenschaft, um zu ermitteln, ob das übergeordnete Element dieses **Member** -Objekts mit dem übergeordneten Element des unmittelbar vorhergehenden **Member** -Objekts identisch ist.

  - Verwenden der [Properties](properties-collection-ado.md)-ADO-Standardauflistung, um zusätzliche Informationen zum **Level** -Objekt abzurufen.

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
<td><p>ChildrenCardinality</p></td>
<td><p>Die Anzahl der untergeordneten Elemente des Elements.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>Description</p></td>
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
<td><p>MemberName</p></td>
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
<td><p>SchemaName</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

