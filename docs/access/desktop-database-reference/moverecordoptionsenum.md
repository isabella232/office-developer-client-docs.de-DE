---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41ec6eaf39545bf8a71f443a8e3b90052a74f1de
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475579"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Betrifft**: Access 2013 | Office 2013

Gibt das Verhalten der [MoveRecord](record-object-ado.md)-Methode des [Record](moverecord-method-ado.md)-Objekts an.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
<th><p>Wert</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adMoveUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Standardwert. Führt den Standardverschiebevorgang aus: Der Vorgang schlägt fehl, wenn die Zieldatei oder das Zielverzeichnis bereits vorhanden ist und der Vorgang Hypertextverknüpfungen aktualisiert.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveOverWrite an</strong></p></td>
<td><p>1</p></td>
<td><p>Überschreibt die Zieldatei oder das Verzeichnis, selbst wenn es bereits vorhanden ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Ändert das Standardverhalten des <strong>MoveRecord</strong> -Methode durch die Hyperlinks der Quelle <strong>Datensatz</strong>nicht aktualisieren. Das Standardverhalten, hängt von der Funktionalität des Anbieters ab. Verschiebevorgangs aktualisiert Verknüpfungen, wenn der Anbieter kann. Wenn der Anbieter nicht Links beheben kann, oder wenn dieser Wert nicht angegeben wird, erfolgreich verschieben, selbst wenn Links nicht behoben wurden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4</p></td>
<td><p>Fordert an, dass der Anbieter das Verschieben (mit Download, hochladen und Löschvorgänge) simuliert. Wenn der Versuch, den <strong>Datensatz</strong> zu verschieben, schlägt fehl, da das Ziel-URL auf einem anderen Server ist oder von einem anderen Anbieter als die Quelle bedient, kann dies eine erhöhte Wartezeit oder Datenverlust aufgrund von anderen Anbieterfunktionen beim Verschieben von Ressourcen führen. zwischen Anbietern.</p></td>
</tr>
</tbody>
</table>


**ADO/WFC-Entsprechung**

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

