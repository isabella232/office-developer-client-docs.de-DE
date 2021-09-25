---
title: Cursor- und Sperrenmerkmale
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e7793aa5beca79b8027abde8f3434a1b4d321417
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585998"
---
# <a name="cursor-and-lock-characteristics"></a>Cursor- und Sperrenmerkmale

**Gilt für**: Access 2013, Office 2013

Die Merkmale eines Cursors hängen zwar von der Funktionalität des Anbieters ab, aber die folgenden Vor- und Nachteile gelten im Allgemeinen für die verschiedenen Typen von Cursorn und Sperren.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Cursor- oder Sperrtyp</p></th>
<th><p>Vorteile</p></th>
<th><p>Nachteile</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Niedrige Ressourcenanforderungen</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Bildlauf rückwärts ist nicht möglich</p></li>
<li><p>Keine Datenparallelität</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p></p>
<ul>
<li><p>Bildlauffähigen</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Keine Datenparallelität</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p></p>
<ul>
<li><p>Gewisse Datenparallelität</p></li>
<li><p>Bildlauffähigen</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Höhere Ressourcenanforderungen</p></li>
<li><p>In getrenntem Szenario nicht verfügbar</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p></p>
<ul>
<li><p>Hohe Datenparallelität</p></li>
<li><p>Bildlauffähigen</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Höchste Ressourcenanforderungen</p></li>
<li><p>In getrenntem Szenario nicht verfügbar</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockReadOnly</strong></p></td>
<td><p></p>
<ul>
<li><p>Niedrige Ressourcenanforderungen</p></li>
<li><p>Extrem skalierbar</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Daten sind über Cursor nicht aktualisierbar</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockBatchOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Batchaktualisierungen</p></li>
<li><p>Ermöglicht getrennte Szenarien</p></li>
<li><p>Andere Benutzer haben Zugriff auf Daten</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Daten können von mehreren Benutzern gleichzeitig geändert werden</p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>adLockPessimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Daten können von anderen Benutzern nicht geändert werden, wenn sie gesperrt sind.</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Andere Benutzer haben keinen Zugriff auf Daten, wenn sie gesperrt sind.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>adLockOptimistic</strong></p></td>
<td><p></p>
<ul>
<li><p>Andere Benutzer haben Zugriff auf Daten</p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p>Daten können von mehreren Benutzern gleichzeitig geändert werden</p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

