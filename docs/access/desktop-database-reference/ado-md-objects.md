---
title: ADO MD-Objekte (Access Desktop Database Reference)
TOCTitle: ADO MD objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2d3acf1b236e23522da0143d577bbcbeacbb4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283296"
---
# <a name="ado-md-objects"></a>ADO MD-Objekte

**Gilt für**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Objekt</th>
<th>Beschreibung</th>
</tr>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Axis</a></p></td>
<td><p>Stellt eine Positions- oder Filterachse einer Zellmenge dar, die ausgewählte Elemente einer oder mehrerer Dimensionen enthält.</p></td>
</tr>
<tr class="even">
<td><p><a href="catalog-object-ado-md.md">Katalog</a></p></td>
<td><p>Enthält multidimensionale Schemainformationen (Cubes und zugrunde liegende Dimensionen, Hierarchien, Ebenen und Elemente), die für einen multidimensionalen Datenanbieter (Datenprovider, MDP) spezifisch sind.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cell-object-ado-md.md">Cell</a></p></td>
<td><p>Stellt die Daten am Kreuzungspunkt von Achsenkoordinaten dar, die in einer Zellmenge enthalten sind.</p></td>
</tr>
<tr class="even">
<td><p><a href="cellset-object-ado-md.md">Cellset</a></p></td>
<td><p>Stellt die Ergebnisse einer multidimensionalen Abfrage dar. Es ist eine Auflistung von Zellen, die aus Cubes oder anderen Zellmengen ausgewählt wurden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cubedef-object-ado-md.md">CubeDef</a></p></td>
<td><p>Stellt einen Cube aus einem multidimensionalen Schema dar, das eine Reihe verknüpfter Dimensionen enthält.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Stellt eine der Dimensionen eines multidimensionalen Cubes dar, der eine oder mehrere Elementhierarchien enthält.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchie</a></p></td>
<td><p>Stellt eine Möglichkeit dar, in der die Elemente einer Dimension aggregiert oder &quot;rollupd werden können. &quot; Eine Dimension kann entlang einer oder mehrerer Hierarchien aggregiert werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Grad</a></p></td>
<td><p>Umfasst eine Gruppe von Elementen, von denen jedes denselben Rang innerhalb einer Hierarchie besitzt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Member</a></p></td>
<td><p>Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Stellt eine Gruppe von einem oder mehreren Elementen unterschiedlicher Dimensionen dar, die einen Punkt auf einer Achse definiert.</p></td>
</tr>
</tbody>
</table>

<br/>

Das **Catalog**-Objekt ist außerdem mit einem ADO-**Connection**-Objekt verbunden, das in der Standard-ADO-Bibliothek enthalten ist:

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objekt</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p>Stellt eine offene Verbindung zu einer Datenquelle dar.</p></td>
</tr>
</tbody>
</table>

<br/>

Es können viele ADO MD-Objekte in einer entsprechenden Auflistung enthalten sein. Ein [CubeDef](cubedef-object-ado-md.md)-Objekt kann beispielsweise in einer [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung eines **Catalog**-Objekts enthalten sein. Weitere Informationen hierzu finden Sie unter [ADO MD-Auflistungen](ado-md-collections.md).

