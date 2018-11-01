---
title: ADO MD-Objekte (Access PC-Datenbank-Referenz)
TOCTitle: ADO MD Objects
ms:assetid: 13501e44-70b6-1036-a8b7-c276f187e4f4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248907(v=office.15)
ms:contentKeyID: 48543366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e09676b222e7199b7f2f9f7520ebf3d5436f9a3c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875133"
---
# <a name="ado-md-objects"></a>ADO MD-Objekte


**Betrifft**: Access 2013, Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="axis-object-ado-md.md">Achse</a></p></td>
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
<td><p><a href="cubedef-object-ado-md.md">CubeDef-Objekts</a></p></td>
<td><p>Stellt einen Cube aus einem multidimensionalen Schema dar, das eine Reihe verknüpfter Dimensionen enthält.</p></td>
</tr>
<tr class="even">
<td><p><a href="dimension-object-ado-md.md">Dimension</a></p></td>
<td><p>Stellt eine der Dimensionen eines multidimensionalen Cubes dar, der eine oder mehrere Elementhierarchien enthält.</p></td>
</tr>
<tr class="odd">
<td><p><a href="hierarchy-object-ado-md.md">Hierarchie</a></p></td>
<td><p>Stellt ein Verfahren, die die Elemente einer Dimension aggregiert werden können oder &quot;zusammengefasst. &quot; Eine Dimension entlang einer oder mehrerer Hierarchien aggregiert werden kann.</p></td>
</tr>
<tr class="even">
<td><p><a href="level-object-ado-md.md">Level</a></p></td>
<td><p>Enthält eine Gruppe von Elementen, von denen jedes denselben Rang innerhalb einer Hierarchie hat.</p></td>
</tr>
<tr class="odd">
<td><p><a href="member-object-ado-md.md">Element</a></p></td>
<td><p>Stellt ein Element einer Ebene in einem Cube, die untergeordneten Elemente eines Elements einer Ebene oder ein Element einer Position auf der Achse einer Zellmenge dar.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-object-ado-md.md">Position</a></p></td>
<td><p>Stellt eine Gruppe von einem oder mehreren Elementen unterschiedlicher Dimensionen dar, die einen Punkt auf einer Achse definiert.</p></td>
</tr>
</tbody>
</table>


Das **Catalog** -Objekt ist außerdem mit einem ADO- **Connection** -Objekt verbunden, das in der Standard-ADO-Bibliothek enthalten ist:

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


Es können viele ADO MD-Objekte in einer entsprechenden Auflistung enthalten sein. Ein [CubeDef](cubedef-object-ado-md.md)-Objekt kann beispielsweise in einer [CubeDefs](cubedefs-collection-ado-md.md)-Auflistung eines **Catalog** -Objekts enthalten sein. Weitere Informationen hierzu finden Sie unter [ADO MD-Auflistungen](ado-md-collections.md).

