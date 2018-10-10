---
title: Level-Objekt (ADO MD)
TOCTitle: Level Object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13fce901860768064d450a64c44545f3c3244453
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473004"
---
# <a name="level-object-ado-md"></a>Level-Objekt (ADO MD)


**Betrifft**: Access 2013 | Office 2013

Enthält eine Gruppe von Elementen, von denen jedes denselben Rang innerhalb einer Hierarchie hat.

## <a name="remarks"></a>Hinweise

Die Auflistungen und Eigenschaften eines **Level** -Objekts ermöglichen Folgendes:

  - Identifizieren der**** Ebene, indem Sie die Eigenschaften [Name](name-property-ado-md.md) und [UniqueName](uniquename-property-ado-md.md) verwenden.

  - Zurückgeben einer Zeichenfolge, die zum Anzeigen der**** Ebene verwendet wird, indem Sie die [Caption](caption-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben einer sinnvollen Zeichenfolge, die die**** Ebene beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben der [Member](member-object-ado-md.md)-Objekte, die die**** Ebene bilden, indem Sie die [Members](members-collection-ado-md.md)-Auflistung verwenden.

  - Zurückgeben der Anzahl von Ebenen ab dem**** Ebenenstamm, indem Sie die [Depth](depth-property-ado-md.md)-Eigenschaft verwenden.

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
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="odd">
<td><p>Beschreibung</p></td>
<td><p>Eine sinnvolle Beschreibung der Ebene.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Der eindeutige Name der <a href="dimension-object-ado-md.md">Dimension</a>.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>Der eindeutige Name der Hierarchie.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Eine der Ebene zugeordnete Beschriftung.</p></td>
</tr>
<tr class="odd">
<td><p>LevelCardinality</p></td>
<td><p>Die Anzahl der Elemente in der Ebene.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>Die GUID der Ebene.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Der Name der Ebene.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>Der Abstand zwischen der Ebene und dem Stamm der Hierarchie.</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>Der Ebenentyp.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Der eindeutige Name der Ebene.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
</tbody>
</table>

