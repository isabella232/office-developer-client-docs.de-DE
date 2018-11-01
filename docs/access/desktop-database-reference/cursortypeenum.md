---
title: CursorTypeEnum (Access PC-Datenbank-Referenz)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 67b7dcd52214c23c45b48de40b46fc4782f1629d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880831"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Betrifft**: Access 2013, Office 2013

Gibt den in einem [Recordset](recordset-object-ado.md)-Objekt verwendeten Cursortyp an.

<br/>

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Verwendet einen dynamischen Cursor. Hinzufügen, ändern und Löschen von anderen Benutzern angezeigt werden, und alle Arten von Bewegung durch das <strong>Recordset-Objekt</strong> sind zulässig, mit Ausnahme von Lesezeichen, wenn der Anbieter sie nicht unterstützt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Standard. Ein Vorwärtscursor verwendet. Identisch mit einer statischen Cursor, außer dass Sie nur vorwärts durch die Datensätze blättern können. Dies verbessert die Leistung, wenn Sie nur eine Pass-through-ein <strong>Recordset</strong>treffen müssen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Verwendet einen Keysetcursor. Wie Sie einen dynamischen Cursor mit der Ausnahme, dass Sie keine Datensätze, die andere Benutzer anzeigen hinzufügen, obwohl Datensätze, die andere Benutzer löschen aus dem <strong>Recordset-Objekt</strong>zugegriffen werden kann. Datenänderungen durch andere Benutzer werden weiterhin angezeigt.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Verwendet einen statischen Cursor. Eine statische Kopie einer Datensatzgruppe, die Sie zum Suchen von Daten oder Erstellen von Berichten verwenden können. Hinzufügungen, Änderungen oder Löschvorgänge durch andere Benutzer sind nicht sichtbar.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Gibt keinen Cursortyp an.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC-Entsprechung

Paket: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Konstante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

