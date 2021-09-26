---
title: CubeDef-Objekt (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f01aa6bbc694cfc798351c9711a38e567c9d3f66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597548"
---
# <a name="cubedef-object-ado-md"></a>CubeDef-Objekt (ADO MD)


**Gilt für**: Access 2013, Office 2013

Stellt einen Cube aus einem multidimensionalen Schema dar, das eine Reihe verknüpfter Dimensionen enthält.

## <a name="remarks"></a>HinwBemerkungeneise

Die Auflistungen und Eigenschaften eines **CubeDef**-Objekts ermöglichen Folgendes:

  - Identifizieren eines **CubeDef** -Objekts, indem Sie die [Name](name-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben einer Zeichenfolge, die den Cube beschreibt, indem Sie die [Description](description-property-ado-md.md)-Eigenschaft verwenden.

  - Zurückgeben der Dimensionen, die den Cube bilden, indem Sie die [Dimensions](dimensions-collection-ado-md.md)-Auflistung verwenden.

  - Abrufen zusätzlicher Informationen zum **CubeDef** -Objekt, indem Sie die [Properties](properties-collection-ado.md)-ADO-Standardauflistung verwenden.

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
<td><p>CreatedOn</p></td>
<td><p>Datum und Uhrzeit der Cubeerstellung.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>Die GUID des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Der Name des Cubes.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>Der Typ des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>Benutzer-ID der Person, die die letzte Datenaktualisierung ausgeführt hat.</p></td>
</tr>
<tr class="odd">
<td><p>Beschreibung</p></td>
<td><p>Eine sinnvolle Beschreibung des Cubes.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Datum und Uhrzeit der letzten Schemaaktualisierung.</p></td>
</tr>
<tr class="odd">
<td><p>Schemaname</p></td>
<td><p>Der Name des Schemas, zu dem dieser Cube gehört.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>Benutzer-ID der Person, die die letzte Schemaaktualisierung ausgeführt hat.</p></td>
</tr>
</tbody>
</table>

