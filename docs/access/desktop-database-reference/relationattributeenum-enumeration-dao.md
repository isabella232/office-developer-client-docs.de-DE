---
title: RelationAttributeEnum (Aufzählung) (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711119"
---
# <a name="relationattributeenum-enumeration-dao"></a>RelationAttributeEnum (Aufzählung) (DAO)


**Betrifft**: Access 2013, Office 2013

Hiermit bestimmen Sie zusammen mit der **Attributes**-Eigenschaft die Attribute eines **Relation**-Objekts.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dbRelationDeleteCascade</p></td>
<td><p>4096</p></td>
<td><p>Löschungen werden weitergegeben.</p></td>
</tr>
<tr class="even">
<td><p>dbRelationDontEnforce</p></td>
<td><p>2</p></td>
<td><p>Die Beziehung wird nicht erzwungen (keine referentielle Integrität).</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationInherited</p></td>
<td><p>4</p></td>
<td><p>Die Beziehung ist in der Datenbank vorhanden, die die beiden verknüpften Tabellen enthält.</p></td>
</tr>
<tr class="even">
<td><p>dbRelationLeft</p></td>
<td><p>16777216</p></td>
<td><p>Nur Microsoft Access. In der Entwurfsansicht wird eine LEFT JOIN-Operation als Standardverknüpfungstyp angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationRight</p></td>
<td><p>33554432</p></td>
<td><p>Nur Microsoft Access. In der Entwurfsansicht wird eine RIGHT JOIN-Operation als Standardverknüpfungstyp angezeigt.</p></td>
</tr>
<tr class="even">
<td><p>dbRelationUnique</p></td>
<td><p>1</p></td>
<td><p>1:1-Beziehung.</p></td>
</tr>
<tr class="odd">
<td><p>dbRelationUpdateCascade</p></td>
<td><p>256</p></td>
<td><p>Aktualisierungen werden weitergegeben.</p></td>
</tr>
</tbody>
</table>

