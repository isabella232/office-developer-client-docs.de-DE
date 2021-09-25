---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4852562fcc755ae0edc8376d0e59d67a1e0affe0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558198"
---
# <a name="moverecordoptionsenum"></a>MoveRecordOptionsEnum


**Gilt für**: Access 2013, Office 2013

Gibt das Verhalten der [MoveRecord](moverecord-method-ado.md)-Methode des [Record](record-object-ado.md)-Objekts an.

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
<td><p><strong>adMoveOverWrite</strong></p></td>
<td><p>1</p></td>
<td><p>Überschreibt die Zieldatei oder das Verzeichnis, selbst wenn es bereits vorhanden ist.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMoveDontUpdateLinks</strong></p></td>
<td><p>2</p></td>
<td><p>Ändert das Standardverhalten der <strong>MoveRecord</strong> -Methode, indem die Hypertextlinks des <strong>Quelldatensatzes</strong>nicht aktualisiert werden. Das Standardverhalten hängt von den Funktionen des Anbieters ab. Der Verschiebungsvorgang aktualisiert Links, wenn der Anbieter in der Lage ist. Wenn der Anbieter Verknüpfungen nicht beheben kann oder dieser Wert nicht angegeben ist, ist die Verschiebung auch dann erfolgreich, wenn Verknüpfungen nicht behoben wurden.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMoveAllowEmulation</strong></p></td>
<td><p>4 </p></td>
<td><p>Fordert an, dass der Anbieter das Verschieben (mit Download-, Upload- und Löschvorgängen) simuliert. Wenn das Verschieben des Datensatzes fehlschlägt, weil sich die Ziel-URL auf einem anderen Server befindet oder von einem anderen Anbieter als die Quelle bedient wird, kann dies aufgrund verschiedener Anbieterfunktionen beim Verschieben von Ressourcen zwischen den Anbietern zu einer erhöhten Latenz oder zu Datenverlust führen.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Diese Konstanten haben keine ADO/WFC-Entsprechungen.

